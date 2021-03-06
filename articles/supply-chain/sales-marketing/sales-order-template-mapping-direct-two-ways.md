---
title: Sincronizzazione di ordini cliente direttamente tra Sales e Finance and Operations
description: "L'argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare gli ordini cliente direttamente tra Microsoft Dynamics 365 for Sales e Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: it-it
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Sincronizzazione di ordini cliente direttamente tra Sales e Finance and Operations

[!include [banner](../includes/banner.md)]

L'argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare gli ordini cliente direttamente tra Microsoft Dynamics 365 for Sales e Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Modelli e attività

Per accedere ai modelli disponibili, aprire l'[Interfaccia di amministrazione di PowerApps](https://preview.admin.powerapps.com/dataintegration). Selezionare **Progetti**, quindi nell'angolo superiore destro, selezionare **Nuovo progetto** per selezionare i modelli pubblici.

I modelli e le attività sottostanti seguenti vengono utilizzati per sincronizzare le gli ordini cliente direttamente tra Sales e Finance and Operations:

- **Nomi dei modelli in Integrazione dati:** 

    - Ordini cliente (da Sales in Fin and Ops) - Diretto
    - Ordini cliente (da Fin and Ops in Sales) - Diretto

- **Nomi delle attività nel progetto di Integrazione dati:**

    - OrderHeader
    - OrderLine

Le attività di sincronizzazione seguenti sono necessarie prima di eseguire la sincronizzazione delle intestazioni e delle righe di fatture di vendita:

- Prodotti (da Fin and Ops in Sales) - Diretto
- Conti (da Sales in Fin and Ops) - Diretto (se utilizzata)
- Da Contatti a Clienti (da Sales in Fin and Ops) - Diretto (se utilizzata)

## <a name="entity-set"></a>Insieme di entità

| Finance and Operations  | Vendite             |
|-------------------------|-------------------|
| Intestazioni ordine cliente CDS | SalesOrders       |
| Righe ordine cliente CDS   | SalesOrderDetails |

## <a name="entity-flow"></a>Flusso di entità

Gli ordini cliente vengono creati in Sales e sincronizzati in Finance and Operations quando **Esegui progetto** viene attivato per un progetto basato sul modello **Ordini cliente (da Sales in Fin and Ops) - Diretto**. È possibile attivare e sincronizzare gli ordini da Sales se tutti i **prodotti dell'ordine** sono prodotti gestiti esternamente. Di conseguenza, non possono includere prodotti fuori catalogo. Dopo l'attivazione dell'ordine, l'ordine cliente diventa di sola lettura nell'interfaccia utente (UI). A quel punto, gli aggiornamenti vengono effettuati in Finance and Operations. Dopo che lo stato dell'ordine cliente diventa **Confermato**, un progetto basato sul modello **Ordini cliente (da Fin and Ops in Sales) - Diretto** può essere utilizzato per sincronizzare gli aggiornamenti o lo stato dell'evasione da Finance and Operations in Sales.

Non è necessario creare ordini in Sales. È invece possibile creare nuovi ordini cliente in Finance and Operations. Dopo che lo stato di un ordine cliente diventa **Confermato**, viene sincronizzato in Sales come descritto nel paragrafo precedente.

In Finance and Operations, i filtri nel modello garantiscono che solo gli ordini cliente pertinenti siano inclusi nella sincronizzazione:

- Nell'ordine cliente, il cliente che richiede l'ordine e quello che emette la fattura devono essere originati in Sales per essere inclusi nella sincronizzazione. In Finance and Operations, i campi **OrderingCustomerIsExternallyMaintained** e **InvoiceCustomerIsExternallyMaintained** sono utilizzati per filtrare ordini cliente dalle entità di dati.
- L'ordine cliente in Finance and Operations deve essere confermato. Solo gli ordini cliente confermati o gli ordini cliente con stato di elaborazione più elevato, ad esempio **Inviato** o **Fatturato** vengono sincronizzati in Sales.
- Dopo la creazione o la modifica di un ordine cliente, è necessario eseguire il processo batch **Calcola totali vendite** in Finance and Operations. Solo gli ordini cliente in cui vengono calcolati i totali delle vendite saranno sincronizzati in Sales.

## <a name="freight-tax"></a>Imposta di trasporto

Sales non supporta le imposte a livello di intestazione in quanto sono registrate a livello di riga. Per supportare le imposte a livello di intestazione da Finance and Operations, ad esempio l'imposta di trasporto, il sistema sincronizza l'imposta in Sales come prodotto fuori catalogo denominato **Imposta di trasporto** e con l'importo imposta in Finance and Operations. In questo modo, il calcolo del prezzo standard in Sales può essere utilizzato per i totali, anche quando vi sono imposte a livello di intestazione in Finance and Operations.

## <a name="discount-calculation-and-rounding"></a>Calcolo e arrotondamento dello sconto

Il modello di calcolo dello sconto in Sales differisce da quello in Finance and Operations. In Finance and Operations, l'importo di sconto finale in una riga di vendita può derivare da una combinazione di importi e percentuali di sconto. Se questo importo di sconto finale viene diviso per la quantità nella riga, è possibile che venga applicato l'arrotondamento. Tuttavia, questo arrotondamento non viene considerato se un importo di sconto per unità arrotondato viene sincronizzato in Sales. Per garantire la corretta sincronizzazione in Sales dell'intero importo di sconto da una riga di vendita in Finance and Operations, l'intero importo deve essere sincronizzato senza essere diviso per la quantità della riga. Di conseguenza, è necessario definire il **metodo di calcolo sconto** come **Voce** in Sales.

Quando una riga dell'ordine cliente viene sincronizzata da Sales in Finance and Operations, viene utilizzato l'intero importo di sconto riga. Poiché Finance and Operations non include un campo in cui registrare l'intero importo di sconto per una riga, l'importo viene diviso per la quantità e registrato nel campo **Sconto riga**. Qualsiasi arrotondamento in questa divisione viene registrato nel campo **Addebiti vendite** nella riga di vendita.

### <a name="example"></a>Esempio

**Sincronizzazione da Sales in Finance and Operations**

- **Sales:** Quantità = 3, sconto per riga = $ 10,00
- **Finance and Operations:** Quantità = 3, importo di sconto riga = $ 3,33, addebito vendita = -$ 0,01 

**Sincronizzazione da Finance and Operations in Sales**

- **Finance and Operations:** Quantità = 3, importo di sconto riga = $ 3,33, addebito vendita = -$ 0,01
- **Sales:** Quantità = 3, sconto per riga = (3 × $ 3,33) + $ 0,01 = $ 10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Soluzione Prospect to cash per Sales

Nuovi campi sono stati aggiunti all'entità **Ordine** e visualizzati nella pagina:

- **Gestito esternamente** - Impostare questa opzione su **Sì** se l'ordine proviene da Finance and Operations.
- **Stato elaborazione** - Questo campo mostra lo stato di elaborazione dell'ordine in Finance and Operations. Sono disponibili i valori seguenti:

    - **Bozza** - Lo stato iniziale quando un ordine viene creato in Sales. In Sales, solo gli ordini con questo stato di elaborazione possono essere modificati.
    - **Attivo** - Lo stato dopo che l'ordine viene attivato in Sales utilizzando il pulsante **Attiva**.
    - **Confermato**
    - **Documento di trasporto**
    - **Fatturato**
    - **Prelevato**
    - **Prelevato in parte**
    - **Parzialmente imballato**
    - **Spedito**
    - **Parzialmente spedito**
    - **Parzialmente fatturato**
    - **Operazione annullata**

L'impostazione **Solo prodotti gestiti esternamente** viene utilizzata durante l'attivazione dell'ordine per rilevare in modo coerente se un ordine cliente consiste interamente di prodotti gestiti esternamente. Se un ordine cliente include solo prodotti gestiti esternamente, i prodotti vengono gestiti in Finance and Operations. Questa impostazione impedisce l'attivazione e il tentativo di sincronizzare righe dell'ordine cliente che hanno prodotti sconosciuti in Finance and Operations.

I pulsanti **Crea fattura**, **Annulla ordine**, **Ricalcola**, **Ottieni prodotti** e **Cerca indirizzo** della pagina **Ordine cliente** sono nascosti per gli ordini gestiti esternamente poiché le fatture verranno create in Finance and Operations e sincronizzate in Sales. Questi ordini non sono modificabili poiché le relative informazioni verranno sincronizzate da Finance and Operations dopo l'attivazione.

Lo stato dell'ordine cliente rimarrà **attivo** per garantire che le modifiche da Finance and Operations possano essere applicate all'ordine cliente in Sales. Per controllare questo comportamento, impostare il valore **Codice stato \[Stato\]** su **Attivo** nel progetto di Integrazione dati.

## <a name="preconditions-and-mapping-setup"></a>Prerequisiti e impostazioni di mapping

Prima di sincronizzare gli ordini cliente, è importante aggiornare le impostazioni seguenti nei sistemi.

### <a name="setup-in-sales"></a>Impostazione in Sales

- Assicurarsi che le autorizzazioni siano impostate per il team a cui l'utente dal set di connessione in Sales viene assegnato. Se si utilizzano dati dimostrativi, in genere l'utente ha privilegi di amministratore, ma non il team. Se il team non dispone di privilegi di amministratore quando si esegue il progetto da Integrazione dati, verrà visualizzato un messaggio di errore in cui viene indicato che il team principale è mancante.

    Andare a **Impostazioni** &gt; **Sicurezza** &gt; **Team**, selezionare il team pertinente, selezionare **Gestisci ruoli** e selezionare un ruolo con le autorizzazioni desiderate, ad esempio **Amministratore di sistema**.

- Per garantire il calcolo corretto degli sconti in Sales e in Finance and Operations, il campo **Metodo di calcolo sconto** deve essere impostato su **Voce**.
- Andare a **Impostazioni** &gt; **Amministrazione** &gt; **Impostazioni di sistema** &gt; **Vendite** e assicurarsi che:

    - L'opzione **Usa sistema di calcolo prezzi sistema** sia impostata su **Sì**.
    - Il campo **Metodo di calcolo sconto** sia impostato su **Voce**.

### <a name="setup-in-finance-and-operations"></a>Impostazione in Finance and Operations

- Andare a **Vendite e marketing** &gt; **Attività periodiche** &gt; **Calcola totali vendite** e impostare il processo da eseguire come processo batch. Impostare l'opzione **Calcola totali per ordini cliente** su **Sì**. Questo passaggio è importante perché solo gli ordini cliente con totali vendite calcolati verranno sincronizzati in Sales. La frequenza del processo batch deve essere in linea con la frequenza della sincronizzazione dell'ordine cliente.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Impostazione nel progetto di Integrazione dati Ordini cliente (da Sales in Fin and Ops) - Diretto

- Assicurarsi che il mapping necessario esista per **Shipto\_country** a **DeliveryAddressCountryRegionISOCode**. È possibile impostare come vuoto un valore predefinito nella mappa di valori per evitare di immettere il paese per gli ordini nazionali. Impostare la parte sinistra su Vuoto e la parte destra sul paese desiderato.

    Il valore di modello è una mappa di valori dove vari paesi vengono mappati e dove Vuoto = Stati Uniti.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Impostazione nel progetto di Integrazione dati Ordini cliente (da Fin and Ops in Sales) - Diretto

#### <a name="salesheader-task"></a>Attività SalesHeader

- Un listino prezzi è necessario per creare ordini in Sales. Aggiornare la mappa di valori per **pricelevelid.name \[nome listino prezzi\]** al listino prezzi utilizzato in Sales per la valuta. È possibile utilizzare il listino prezzi predefinito per una singola valuta. In alternativa, se si hanno listini prezzi in più valute, è possibile utilizzare una mappa di valori.

    Il valore di modello predefinito per **pricelevelid.name \[nome listino prezzi\]** è **Servizio CRM USA (esempio)**.

#### <a name="salesline-task"></a>Attività SalesLine

- Assicurarsi che la mappa di valori richiesta esista per **SalesUnitSymbol** in Finance and Operations.
- Assicurarsi che le unità richieste siano definite in Sales.

    Un valore di modello con una mappa di valori viene definito per **SalesUnitSymbol** a **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Mapping dei modelli in Integrazione dati

> [!NOTE]
> I campi **Termini di pagamento**, **Termini di trasporto**, **Termini di consegna**, **Metodo di spedizione** e **Modalità di consegna** non sono inclusi nei mapping predefiniti. Per mappare questi campi, è necessario impostare un mapping di valori che sia specifico ai dati delle organizzazioni tra cui l'entità viene sincronizzata.

Nelle figure seguenti viene illustrato un esempio di mapping di modelli in Integrazione dati.

> [!NOTE]
> Il mapping mostra quali informazioni dei campi verranno sincronizzate da Sales in Finance and Operations o da Finance and Operations in Sales.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Ordini cliente (da Fin and Ops in Sales) - Diretto: OrderHeader

[![Mapping dei modelli in Integrazione dati](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Ordini cliente (da Fin and Ops in Sales) - Diretto: OrderLine

[![Mapping dei modelli in Integrazione dati](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Ordini cliente (da Sales in Fin and Ops) - Diretto: OrderHeader

[![Mapping dei modelli in Integrazione dati](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Ordini cliente (da Sales in Fin and Ops) - Diretto: OrderLine

[![Mapping dei modelli in Integrazione dati](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Argomenti correlati

[Prospect to cash](prospect-to-cash.md)

