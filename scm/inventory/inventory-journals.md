---
title: Giornali di registrazione magazzino
description: In questo articolo viene descritto come utilizzare i giornali di registrazione magazzino per registrare i diversi tipi di transazioni dell&quot;inventario fisico.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: c64ba9e081ab4224556af86ec855ebf508853454
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-journals"></a>Giornali di registrazione magazzino

In questo articolo viene descritto come utilizzare i giornali di registrazione magazzino per registrare i diversi tipi di transazioni dell'inventario fisico. 

I giornali di registrazione magazzino in Microsoft Dynamics 365 for Operations vengono utilizzati per registrare le transazioni di inventario fisico di diversi tipi, ad esempio la registrazione delle uscite e delle entrate, i movimenti inventario, la creazione delle distinte base (DBA) e la riconciliazione dell'inventario fisico. Tutti i giornali di registrazione magazzino vengono utilizzati in una modalità simile, ma vengono suddivisi in diversi tipi.

## <a name="types-of-inventory-journals"></a>Tipi di giornali di registrazione magazzino
Sono disponibili i seguenti tipi di giornali di registrazione magazzino:

-   Spostamento
-   Rettifica magazzino
-   Trasferito
-   DBA
-   Arrivo articoli
-   Entrata produzione
-   Conteggio
-   Conteggio tag

### <a name="movement"></a>Spostamento

Quando si utilizza un giornale di registrazione movimenti scorte, è possibile aggiungere il costo di un articolo quando si aggiungono scorte, ma è necessario manualmente allocare il costo aggiuntivo in un Conto CoGe specifico specificando un conto di contropartita della contabilità generale quando si crea il giornale di registrazione. Questo tipo di giornale di registrazione magazzino è utile se si desidera registrare la spesa per un articolo in un reparto diverso o per rimuovere articoli dal magazzino per scopi di spesa.

### <a name="inventory-adjustment"></a>Rettifica magazzino

Quando si utilizza un giornale di registrazione di rettifica magazzino, è possibile aggiungere il costo di un articolo quando si aggiungono scorte. Il costo aggiuntivo verrà registrato automaticamente in un Conto CoGe specifico, in base all'impostazione del profilo registrazione del gruppo di articoli. Utilizzare questo tipo di giornale di registrazione magazzino per aggiornare profitti e perdite nelle quantità di scorte quando per l'articolo deve essere presente il conto di contropartita predefinito della contabilità generale. Durante la registrazione di un giornale di registrazione di rettifica magazzino viene registrata un'entrata o un'uscita dal magazzino, vengono modificati i valori di magazzino scorte e vengono create le transazioni contabili.

### <a name="transfer"></a>Trasferito

È possibile utilizzare i giornali di registrazione trasferimento per trasferire articoli tra le ubicazioni di stoccaggio, batch o varianti prodotto senza associare implicazioni di costo. Ad esempio, è possibile trasferire gli articoli da un magazzino a un altro magazzino all'interno della stessa società. Quando si utilizza un giornale di registrazione trasferimenti, è necessario specificare dimensioni inventariali "da" e "a" (ad esempio, per Sito e Magazzino). Le scorte disponibili per le dimensioni inventariali definite vengono modificate di conseguenza. I trasferimenti scorte riflettono il movimento immediato di materiale. Le scorte in transito non sono tracciate. Se le scorte in transito devono essere tracciate, utilizzare un ordine di trasferimento. Quando si registra un giornale di registrazione trasferimenti, vengono create due operazioni di magazzino per ogni una riga del giornale di registrazione:

-   Un'uscita da magazzino nell'ubicazione "da"
-   Un'entrata in magazzino nell'ubicazione "a"

### <a name="bom"></a>DBA

Quando si dichiara una DBA come finita, è possibile creare un giornale di registrazione DBA. Utilizzando un giornale di registrazione DBA, è possibile registrare direttamente la DBA. Questa registrazione genera un'entrata in magazzino del prodotto, insieme a una DBA associata, e un'entrata in magazzino dei prodotti inclusi nella DBA. Questo tipo di giornale di registrazione magazzino è utile negli scenari di produzione semplici o con volumi elevati in cui i cicli di lavorazione non sono obbligatori.

### <a name="item-arrival"></a>Arrivo articoli

È possibile utilizzare il giornale di registrazione arrivi articoli per registrare l'entrata di articoli (ad esempio, ordini fornitore). Un giornale di registrazione arrivi articoli può essere creato come parte della gestione degli arrivi dalla pagina **Panoramica arrivi** oppure è possibile creare manualmente un inserimento nel giornale di registrazione dalla pagina **Arrivo articoli **. Se si consente al nome del giornale di registrazione arrivi articoli di controllare le ubicazioni di prelievo, Dynamics 365 for Operations cerca una ubicazione per gli articoli ricevuti e, se c'è spazio disponibile, genera le destinazioni di ubicazione per gli articoli in arrivo.

### <a name="production-input"></a>Entrata produzione

I giornali di registrazione entrata produzione funzionano in modo analogo ai giornali di registrazione arrivi articoli ma vengono utilizzati per gli ordini di produzione.

### <a name="counting"></a>Conteggio

Giornali di registrazione di conteggio consentono di correggere le scorte attualmente disponibili registrate per gli articoli o i gruppi di articoli e registrare l'effettivo conteggio fisico, in modo che è possibile apportare rettifiche necessarie per riconciliare le differenze. È possibile associare i criteri di conteggio ai gruppi di conteggio per agevolare gli articoli del gruppo con varie caratteristiche, in modo che gli articoli possano essere inclusi in un giornale di registrazione di conteggio. Ad esempio, è possibile impostare i gruppi di conteggio per conteggiare gli articoli che hanno una frequenza specifica o per conteggiare gli articoli quando le scorte rientrano in un livello specifico. Per informazioni sulla definizione dei gruppi, vedere [definire i processi di conteggio scorte (Guida di attività)](http://ax.help.dynamics.com/en/wiki/define-inventory-counting-processes/).

### <a name="tag-counting"></a>Conteggio tag

I giornali di registrazione di conteggio tag vengono usati per assegnare un tag numerato a un lotto di conteggio. Il tag deve contenere un numero di tag, un numero di articolo e una quantità dell'articolo. Per garantire che un tag venga utilizzato solo una volta e che tutti i tag vengano utilizzati, ogni numero di articolo deve essere un set univoco di tag con la sequenza numerica specifica. Tre valori di stato possono essere impostati per ogni tag:

-   **Utilizzato** – Il numero di articolo viene conteggiato per il tag.
-   **Annullato** – Il numero di articolo viene annullato per il tag.
-   **Mancante** – Il numero di articolo è mancante per il tag.

Quando si registra il giornale di registrazione di conteggio tag, viene creato un nuovo giornale di registrazione di conteggio in base alle righe del giornale di conteggio tag. Per ulteriori informazioni sul conteggio tag, vedere [Conteggio tag scorte](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Utilizzo di giornali di registrazione
A un giornale di registrazione può accedere solo un utente per volta. Se più utenti devono accedere ai giornali di registrazione contemporaneamente per creare righe del giornale di registrazione, devono selezionare i giornali di registrazione che attualmente non vengono utilizzati per impedire la sovrascrittura delle informazioni. In situazioni in cui più reparti utilizzano lo stesso tipo di giornale di registrazione, è utile creare più nomi di giornale di registrazione, ad esempio uno per reparto. Può inoltre essere utile dividere i giornali affinché ogni routine di registrazione venga immessa nel relativo giornale di registrazione magazzino univoco. Per le routine di registrazione associate alle operazioni di magazzino, creare un giornale per le rettifiche periodiche dell'inventario e uno per il conteggio delle scorte.

## <a name="posting-journal-lines"></a>Registrazione delle righe del giornale di registrazione
È possibile registrare le righe del giornale di registrazione create in qualsiasi momento fino a bloccare un articolo da ulteriori transazioni. I dati immessi in un giornale di registrazione vengono mantenuti nel giornale anche se questo viene chiuso senza registrare le righe.

