---
title: "Configurare la contabilità fornitori"
description: "Questo articolo descrive le pagine utilizzate per impostare le funzionalità di base e facoltative per la contabilità fornitori in Microsoft Dynamics AX. Vengono descritti i passaggi di configurazione da completare prima di iniziare a impostare la contabilità fornitori."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: b06623a0eb754654f41c50b92af67dc94a069663
ms.lasthandoff: 03/31/2017


---

# <a name="configure-accounts-payable"></a>Configurare la contabilità fornitori

Questo articolo descrive le pagine utilizzate per impostare le funzionalità di base e facoltative per la contabilità fornitori in Microsoft Dynamics AX. Vengono descritti i passaggi di configurazione da completare prima di iniziare a impostare la contabilità fornitori.

<a name="prerequisites-for-accounts-payable-setup"></a>Prerequisiti per l'impostazione della contabilità fornitori
----------------------------------------

Prima di poter impostare la contabilità fornitori, occorre completare la seguente configurazione:

-   In contabilità generale:
    -   Se si prevede di utilizzare i giornali di registrazione pagamenti, è necessario prima configurarli.
    -   Se si prevede di eseguire le rettifiche tasso di cambio, impostare i codici valuta nella pagina Valute, i tipi di tasso di cambio nella pagina Tipi di tasso di cambio e i tassi di cambio valutario di impostazione nella pagina Tassi di cambio valutario.
-   In Gestione cassa e banche impostare i conti bancari da utilizzare con i metodi di pagamento.

## <a name="setup-pages-for-accounts-payable"></a>Pagine di impostazione per la contabilità fornitori

Utilizzare le pagina descritte di seguito per impostare le funzionalità di base della contabilità fornitori per ogni persona giuridica. Le pagine sono elencate nell'ordine di impostazione consigliato. Per semplificare il processo di impostazione, è possibile creare modelli in base ai primi record creati. In un modello i valori sono in genere immessi in base alle funzionalità che l'organizzazione desidera implementare per un particolare tipo di fornitore.
1.  Nella pagina Termini di pagamento definire i termini di pagamento che si assegnano a ordini cliente, ordini fornitore, clienti e fornitori e che determinano le date di scadenza delle fatture.
2.  Nella pagina Metodi di pagamento - Fornitori creare e gestire le informazioni sui metodi utilizzati dall'organizzazione per il pagamento dei fornitori.
3.  Nella pagina Gruppi di fornitori creare e gestire i gruppi di fornitori che condividono parametri importanti per la registrazione, la liquidazione, il pagamento, il reporting e le previsioni.
4.  Nella pagina Profili registrazione fornitori definire come registrare le transazioni fornitore nella contabilità generale.
5.  Nella pagina Parametri contabilità fornitori configurare le impostazioni predefinite che verranno applicate se non è definita un'impostazione più specifica, i parametri per vari tipi di funzionalità e varie sequenze numeriche per la contabilità fornitori.
6.  Nella pagina Impostazione moduli definire il formato di vari documenti correlati ai fornitori e utilizzati all'interno dell'organizzazione per tenere traccia dei ricevimenti dai fornitori e per specificare i motivi del flusso di pagamenti a favore dei fornitori.
7.  Nella pagina Fornitori creare e gestire i conti fornitore e gli uffici tributari a cui devono essere inviati i report IVA dell'organizzazione.

## <a name="optional-setup-pages-for-accounts-payable"></a>Pagine di impostazione facoltativi per la contabilità fornitori
Oltre alla funzionalità di base, la contabilità fornitori ha altre funzionalità da impostare.

Le pagine di impostazione aggiuntive sono organizzate per funzionalità.

**Policies**
-   Nella pagina Criteri fattura fornitore, impostare i criteri fatture fornitore.

**Invoice matching**

-   Nella pagina Tolleranze totali fatture, impostare le tolleranze per i totali fattura.
-   Nella pagina Criteri di abbinamento, impostare i criteri di abbinamento a due elementi di verifica e a tre elementi di verifica.
-   Nella pagina Tolleranze prezzi, impostare le tolleranze per i prezzi unitari.
-   Nella pagina Gruppi di controllo tolleranza prezzi articolo impostare i gruppi di controllo tolleranza per prezzi articolo.
-   Nella pagina Gruppi di controllo tolleranza prezzi fornitore impostare i gruppi di controllo tolleranza per prezzi fornitore.
-   Nella pagina Tolleranze spese, impostare le tolleranze per le spese.

**Workflow**

-   Nella pagina Flussi di lavoro contabilità fornitori impostare configurazioni di flusso di lavoro per l'approvazione dei giornali di registrazione e per le richieste di acquisto.

**Reasons**

-   Nella pagina Motivi fornitore, impostare i codici motivo.

**Charges**

-   Nella pagina Codice spese, impostare i codici per le spese utilizzate negli ordini fornitore.
-   Nel fornitore che le spese parte della pagina, che creare e gestire gruppi di spese per i fornitori.
-   Nella pagina Gruppi di addebito articoli  creare e gestire i gruppi di spese per gli articoli.
-   Nella pagina Spese automatiche , definire le spese assegnate automaticamente agli ordini.

**Supplementary items**

-   Nella pagina Gruppi di articoli supplementari - Fornitore , creare e gestire gruppi di articoli supplementari per i fornitori.
-   Nella pagina Gruppi di articoli supplementari - Magazzino creare e gestire gruppi di articoli supplementari per gli articoli.

**Distribution**

-   Nella pagina Termini di consegna, creare e gestire le condizioni per il trasferimento di un articolo dal venditore all'acquirente.
-   Nella pagina Modi di consegna, creare e gestire il mezzo di trasporto utilizzato per la consegna di un ordine dal venditore all'acquirente.
-   Nella pagina Codici di destinazione, creare e gestire gli ID e le descrizioni per le destinazioni di consegna.

**Forms**

-   Nella pagine Note moduli, creare il testo standard visualizzato su diverse pagine.
-   Nella pagina Parametri di ordinamento moduli, impostare i criteri di ordinamento per le richieste di approvvigionamento, gli elenchi entrate, i documenti di trasporto e le fatture.
-   Nella pagina Impostazione Gestione stampa impostare informazioni di gestione stampa per gli originali e le copie delle pagine.

**Payments**

-   Nella pagina Sconti di cassa, impostare e gestire le condizioni per ottenere sconti di cassa. I codici sconto di cassa vengono collegati ai fornitori e applicati ai rispettivi ordini.
-   Nella pagina Scadenzari pagamenti, impostare gli scadenzari pagamenti utilizzati per gestire i pagamenti rateali ai fornitori.
-   Nella pagina Giorni di pagamento, definire i giorni di pagamento utilizzati per il calcolo delle date di scadenza e impostare un giorno specifico della settimana e del mese.
-   Nella pagina Commissione pagamento creare e gestire le commissioni di pagamento associate ai fornitori.
-   Nella pagina Istruzione di pagamento, creare e gestire le istruzioni di pagamento.

**Statistics**

-   Nella pagina Definizioni periodo di aging, impostare intervalli definiti dall'utente utilizzati per analizzare la distribuzione delle scadenze dei conti fornitore.
-   Nella pagina Linea di business creare i codici della linea di business (LOB) assegnati ai fornitori.

**Imposta 1099**

-   ** Campi 1099 ** nella pagina, verificare e aggiornare gli importi minimi che devono essere dichiarati all'IRS (Internal Revenue Service (IRS), in base ai più recenti requisiti IRS.

## <a name="optional-setup-for-other-modules"></a>** Impostazioni facoltative per altri moduli **
**Organization administration**

-   Nella pagina Sequenze numeriche, impostare i gruppi di sequenze numeriche per i numeri di fattura.
-   Nelle seguenti pagine impostare le informazioni relative all'indirizzo:
    -   Impostazione indirizzo
    -   Codici NAF
    -   Importa codici postali (CAP)

**General ledger**

-   Nella pagina Dimensioni finanziarie impostare le dimensioni finanziarie.
-   Nelle seguenti pagine impostare le informazioni sulle imposte:
    -   Codici IVA
    -   Fasce IVA
    -   Fasce IVA articoli
    -   Gruppo di conti
    -   Codici di esenzione IVA
    -   Uffici IVA competenti
    -   Uffici IVA
    -   Periodi liquidazione IVA

**Cash and bank management**

-   Nella pagina Codici scopo pagamento impostare il codice di scopo pagamento della banca centrale.



