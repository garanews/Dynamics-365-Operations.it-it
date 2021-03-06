--- 
title: Configurare l'elaborazione di ondate
description: In questo guida viene descritto come impostare i criteri che determinano quale lavoro viene generato per un magazzino quando viene elaborata un'ondata e se le ondate vengono elaborate manualmente o automaticamente.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="configure-wave-processing"></a>Configurare l'elaborazione di ondate

[!include [task guide banner](../../includes/task-guide-banner.md)]

In questo guida viene descritto come impostare i criteri che determinano quale lavoro viene generato per un magazzino quando viene elaborata un'ondata e se le ondate vengono elaborate manualmente o automaticamente. I criteri vengono specificati impostando i modelli ondata e le query che corrispondono a un'ondata con le righe rilasciate negli ordini cliente, negli ordini di produzione o negli ordini kanban. L'elaborazione ondata viene utilizzata in magazzini che utilizzano la funzionalità del modulo Gestione magazzino e non in quelli che utilizzano la funzionalità nel modulo Gestione inventario. È possibile eseguire questa procedura nella società di dati dimostrativi USMF.

1. Andare a Gestione magazzino > Impostazioni > Ondate > Modelli ondata.
2. Fare clic su Nuovo.
3. Digitare un valore nel campo Nome modello ondata.
    * Quando si imposta un modello di ondata, si specifica la sequenza in cui i modelli verranno associati alle righe rilasciate negli ordini cliente, negli ordini di produzione o sui kanban. Quando una riga viene rilasciata al magazzino o alla produzione, viene utilizzato il primo modello di ondata che soddisfa i criteri. Si consiglia di inserire i modelli con i criteri più specifici in cima all'elenco. Più ampi sono i criteri, maggiore è la possibilità che una riga soddisfi i criteri e ciò potrebbe comportare che le righe vengano assegnate a un'ondata errata.  
4. Nel campo Descrizione modello ondata immettere un valore.
5. Nel campo Sito immettere o selezionare un valore.
    * Se si utilizza USMF, è possibile selezionare il sito 2.  
6. Nel campo Magazzino immettere o selezionare un valore.
    * Se si utilizza USMF, è possibile selezionare il magazzino 24.  
7. Impostare il campo Automatizza creazione ondata su Sì.
    * Selezionare questa opzione per creare un'ondata quando viene rilasciato un ordine cliente, un ordine di produzione, un kanban al magazzino.  
8. Impostare l'opzione Elabora ondata al rilascio in magazzino su Sì. 
    * Selezionare questa opzione per elaborare automaticamente l'ondata e creare il lavoro quando una riga viene rilasciata nel magazzino.  
9. Impostare l'opzione Automatizza rilascio ondata su Sì. 
    * Selezionare questa opzione per rilasciare automaticamente l'ondata. Il lavoro di prelievo viene creato e reso disponibile sui dispositivi mobili.  
10. Impostare l'opzione Assegna a ondate aperte su Sì. 
    * Le righe vengono assegnate a ondate sul filtro di query per il modello ondata.  
11. Impostare l'opzione Elabora ondata automaticamente alla soglia su Sì. 
    * Selezionare questa opzione per elaborare automaticamente l'ondata quando i relativi valori raggiungono le soglie di peso, la spedizione e le righe specificate nel gruppo di campi Soglie ondata. Questa opzione è disponibile solo se nel campo Tipo di modello ondata è selezionata l'opzione Spedizione.  
12. Impostare l'opzione Automatizza rilascio lavoro di rifornimento su Sì. 
    * Selezionare questa opzione per creare lavoro di rifornimento basato sulla domanda e per rilasciarlo automaticamente. È necessario aggiungere il metodo ondata di rifornimento al modello di ondata e creare un modello rifornimento di tipo Domanda ondata.  
13. Espandere la sezione Metodi.
    * I metodi del modello di ondata consentono di controllare la sequenza di attività cui ogni ondata viene sottoposta quando è elaborata. Ad esempio, potrebbe essere disponibile un metodo per il rifornimento per ondata. Quando si aggiunge un metodo, viene automaticamente elencato nella posizione appropriata nella sequenza delle fasi. Se è stata impostata l'opzione Automatizza rilascio lavoro di rifornimento su Sì, è necessario aggiungere qui il metodo di rifornimento.  
    * Gli attributi di ondata fungono da filtri per limitare il tipo di articoli che possono utilizzare l'ondata. Ad esempio, è possibile specificare un gruppo di articoli.  
14. Fare clic su Salva.
15. Chiudere la pagina.
16. Andare a Gestione magazzino > Impostazioni > Parametri di gestione magazzino.
17. Espandere la sezione Elaborazione ondata.
18. Nel campo Gruppo batch elaborazione ondata immettere o selezionare un valore.
19. Impostare l'opzione Elabora ondate in batch su Sì.
20. Nel campo Attesa blocco (ms) immettere un numero.
    * Immettere il tempo, espresso in millisecondi, in cui un passaggio di allocazione aspetterà una risorsa di sistema bloccata da un altro passaggio di allocazione. Quando il tempo viene superato, l'ondata non viene elaborata e viene visualizzato un messaggio di errore.  
21. Fare clic su Salva.
22. Chiudere la pagina.
23. Andare a Controllo produzione > Impostazioni > Parametri di controllo produzione.
24. Nel campo Rilascia in magazzino selezionare un'opzione.
    * Per gli ordini cliente e gli ordini di kanban, l'inventario deve essere prenotato prima che l'ordine venga rilasciato al magazzino. In caso contrario, gli articoli o le righe di allocazione non possono essere elaborati in un'ondata. Per gli ordini di produzione, è anche possibile scegliere Consenti prenotazione parziale. Ad esempio, questo è utile se si dispone dei materiali necessari per avviare una produzione ed è quindi possibile attendere fino a quando i materiali aggiuntivi diventano disponibili per terminare il processo. Se si seleziona questa opzione, è necessario ripetere manualmente il rilascio al processo di magazzino quando i materiali aggiuntivi diventano disponibili.  
25. Chiudere la pagina.


