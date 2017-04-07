---
title: Panoramica di Impostazione budget
description: "Anche se è possibile importare quasi ciascuna società che utilizza la funzionalità dei dati finanziari in Microsoft Dynamics 365 per le operazioni dovranno essere possibile creare i report di budget con numeri reali. In questo articolo viene descritto la configurazione minima richiesta per creare budget in Dynamics 365 per le operazioni o caricarle da un programma di terzi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Panoramica di Impostazione budget

Anche se è possibile importare quasi ciascuna società che utilizza la funzionalità dei dati finanziari in Microsoft Dynamics 365 per le operazioni dovranno essere possibile creare i report di budget con numeri reali. In questo articolo viene descritto la configurazione minima richiesta per creare budget in Dynamics 365 per le operazioni o caricarle da un programma di terzi.

<a name="overview"></a>Panoramica
--------

Il budget approvato per una persona giuridica viene gestito in un documento noto come *voce del registro di budget*. Le righe di un documento della voce del registro di budget sono noti come voci del account* di *budget e contengono le informazioni sulle dimensioni finanziarie, le date e gli importi di budget approvati. Il documento della voce del registro di budget è integrato con i report finanziari e le pagine di richiesta di informazioni in cui gli importi effettivi di contabilità generale vengono confrontati gli importi del budget. 

Sono disponibili metodi per creare le voci del registro di budget in Dynamics 365 per le operazioni:

-   Immettere manualmente le informazioni del documento nella pagina **Voci del registro di budget**.
-   Utilizzare il modello di Microsoft Excel che è possibile aprire facendo clic sul pulsante **Apri in Excel** nella pagina **Voci del registro di budget**.
-   Utilizzare l'entità di dati **Voci contabili del budget** in Gestione dati per importate le voci del registro di budget. È opportuno considerare la possibilità di utilizzare questo metodo e di passare ** insieme di elaborazione ** ** ** parametro se è necessario includere più voci contabili del budget nel sistema.
-   Se la società utilizza la funzionalità di pianificazione del budget per preparare i dati del budget, è possibile utilizzare il processo periodico **Genera voce del registro di budget**.

La voce del registro di budget viene considerata completata quando i saldi budget sono stati aggiornati. ** Voci del registro ** nella pagina, fare clic su ** saldi budget di aggiornamento ** per l'immissione in un registro di budget o su più voci. Dopo aver aggiornato i saldi budget, lo stato della voce del registro di budget viene impostato su **Completata**. La voce del registro di budget completata non può essere aperta nuovamente per eventuali modifiche. Di conseguenza, se i dati del budget devono essere rettificati, è necessario creare una nuova voce del registro di budget invece di correggere i dati della voce del registro di budget completata.

## <a name="configuration"></a>Configurazione
Per configurare l'impostazione del budget, iniziare dalla pagina **Parametri impostazione budget**. In questa pagina, è necessario definire il giornale di registrazione budget, la sequenza numerica per le voci del registro di budget e il comportamento predefinito nelle aree di lavoro.

Successivamente, se esistono criteri che regolano l'approvazione delle voci del registro di budget, in base al tipo di budget (ad esempio, trasferimenti o revisioni), è necessario creare flussi di lavoro delle voci del registro di budget nella pagina **Flussi di lavoro impostazione budget**. Se sono presenti scenari in cui i trasferimenti possono essere consentiti senza l'approvazione del flusso di lavoro, è possibile definire le regole di trasferimento budget per supportare tali scenari. 

Nella pagina **Dimensioni impostazione budget** è necessario selezionare le dimensioni finanziarie che vengono utilizzate per l'impostazione del budget, in base alle dimensioni che vengono utilizzate nel piano dei conti. Per l'impostazione del budget è possibile selezionare tutte le dimensioni finanziarie o un sottoinsieme di esse.

Definire un *that del modello di *budget corrisponde a tutti i o a qualsiasi budget. È possibile utilizzare un unico modello di budget per tutte le voci del registro di budget. In alternativa, è possibile creare modelli separati basati sul tipo di budget, la posizione geografica o un altro modo in cui un budget può essere classificato. 

> [!NOTE] 
> Se il controllo del budget viene utilizzato, sarà possibile associare un solo modello di budget con una durata ciclo di budget specifica. 

Creare *codici budget *che identificano il tipo di transazioni budget da registrare e i flussi di lavoro correlati. I codici budget possono supportare i seguenti tipi di budget:

-   Budget originale
-   Trasferito
-   Revisione
-   Impegno di spesa
-   Impegno preliminare di spesa
-   Budget riportabile in avanti

I codici budget consentono di avere una audit trail di modifiche di budget approvate nel corso del ciclo del budget. Se un flusso di lavoro è associato a un codice budget, il flusso di lavoro verrà attivata per tutte le voci del registro di budget che utilizzano tale codice budget e i passaggi del flusso di lavoro è necessario completare prima che la voce del registro di budget possa ottenere ** completato ** la fase.  

È inoltre possibile impostare il rules* di trasferimento del *budget. Per utilizzare le regole di trasferimento budget, si seleziona ** regole di utilizzo dei trasferimenti di budget ** ** parametri budget ** nella pagina. Quando si utilizzano le regole per trasferimenti di budget, se un utente crea un documento utilizzando un codice budget del tipo **Trasferimento**, i saldi budget non verranno aggiornati se tali regole vengono violate. Ad esempio, è possibile consentire documenti di trasferimento budget dove il budget di spesa viene trasferito tra i conti principali del reparto Vendite e marketing, ma è possibile impedire il trasferimento del budget da o verso quel reparto a meno che non sia stata concessa l'approvazione del flusso di lavoro per quel tipo di voce contabile del budget.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Utilizzo delle aree di lavoro e delle pagine di richiesta per tenere traccia del budget rispetto valori effettivi
Il responsabile budget può verificare lo stato corrente di un budget nell'area di lavoro **Budget contabili e previsioni**. Le schede relative alle **spese sul budget** e ai **ricavi da budget** offrono una rapida panoramica delle combinazioni delle dimensioni finanziarie dove gli obiettivi del budget non sono stati rispettati o sono vicini alla soglia. È possibile personalizzare la percentuale della soglia del budget e i set di dimensioni finanziarie che sono utilizzati in queste schede facendo clic su **Configura area di lavoro personale**. È possibile fare clic su **Responsabili unità** per vedere i lavoratori che sono responsabili di specifiche combinazioni dimensioni finanziarie che sono selezionate in tali schede. Ad esempio, se si nota che il budget di spesa del reparto Operazioni sta per superare la soglia del budget, è possibile trovare e contattare il responsabile del reparto per discutere del problema. 

> [!NOTE] 
> ** Gestore reparto ** il campo ** unità organizzative ** nella pagina determina i responsabili supporto combinazioni di dimensioni finanziarie specifiche. Fare clic su **Ulteriori informazioni** nella parte inferiore della scheda per aprire la pagina di richiesta **Confronto tra budget e valori effettivi** per visualizzare altri dettagli sugli importi di budget rispetto agli importi effettivi. 

La pagina di richiesta **Effettivi rispetto al budget** consente di esaminare a fondo i dettagli del budget rispetto agli importi effettivi. Selezionare una riga nella pagina di richiesta e quindi fare clic su **Saldi del periodo** per visualizzare come il budget e gli importi effettivi si estendono su più periodi fiscali. La pagina **Voci contabili budget** fornisce informazioni dettagliate sull'importo del budget nelle voci del registro di budget. La pagina **Inserimenti nel giornale di registrazione generale **apre le transazioni contabili che sono incluse nell'importo **Effettivi** calcolato. 

Una società che utilizza la funzionalità di pianificazione del budget può creare e utilizzare le *previsioni di budget* nell'area di lavoro **Budget contabili e previsioni**.

