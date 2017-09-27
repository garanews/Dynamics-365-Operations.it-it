---
title: 'Assegni fornitore di esempio per la creazione di report elettronici '
description: In questo argomento sono riportate le informazioni generali sull'utilizzo dei formati di assegni di esempio per la creazione di report elettronici.
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a8ba439ff643fce4811be9224a3edf96b2b9025c
ms.contentlocale: it-it
ms.lasthandoff: 07/27/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>Formati di assegni di esempio per la creazione di report elettronici 

È possibile utilizzare la creazione report elettronici per formattare gli assegni fornitore. Molti formati di assegni specifici della banca e del fornitore sono disponibili sul mercato. I formati di assegni di esempio sono stati inclusi nel modello di assegno di pagamento nell'archivio degli strumenti della creazione di report elettronici. Questi assegni di esempio sono denominati **Assegno in mezzo (US)** e **Assegno nella prima matrice sotto (US)**.

## <a name="what-check-formats-are-currently-supported"></a>Quali formati di assegni sono attualmente supportati?

È necessario passare alla libreria Risorsa condivisa in Microsoft Dynamics Lifecycle Services (LCS) e visualizzare l'elenco corrente di file disponibili con tipo di risorsa **Configurazione GER**. La sezione successiva, "Cosa devo impostare?", fornisce un collegamento all'argomento che illustra come creare un archivio LCS per esaminare le configurazioni disponibili e importare quelle selezionate.

Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition include un formato di esempio in cui l'assegno è in alto, seguito da due sezioni di rimessa. Include anche un formato di esempio in cui l'assegno è in mezzo, tra due sezioni di rimessa. Questi formati di esempio corrispondono ai formati di assegni aziendali di tipo deluxe.

## <a name="what-do-i-have-to-set-up"></a>Cosa devo impostare?

- Prima di poter stampare assegni tramite la creazione di report elettronici, almeno una configurazione dell'assegno attiva deve essere importata nelle configurazioni della creazione di report elettronici. Per istruzioni, vedere [Scaricare le configurazioni per la creazione di report elettronici da Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
- Quando si configurano gli assegni in Gestione cassa e banche per il conto bancario, selezionare la casella di controllo **Formato esportazione elettronica generica** e selezionare il formato dell'assegno appropriato come configurazione del formato esportazione.
- È inoltre necessario specificare il numero di righe divise che verranno stampate sulla rimessa. Assicurarsi di includere le righe di intestazione quando si calcola questo numero. Per i due formati di assegni di esempio, il numero di righe divise consigliato è 17. Tuttavia, questo numero varia in base alle scorte dell'assegno e ai driver della stampante.
- Si consiglia di stampare una assegno di test per convalidare il layout degli assegni. Per stampare un assegno di test, selezionare l'opzione **Stampa di prova**. I formati di assegni di esempio funzionano meglio se **Margini** è impostato su **Nessuno** nelle proprietà avanzate della stampante per Microsoft Excel. Dopo che l'assegno di test è stato generato, attivare la modifica dell'output di Excel e configurare il layout di pagina in modo da impostare tutti margini su **0** (zero). Confrontare la copia di test degli assegni con le scorte degli assegni e modificare le impostazioni fino a soddisfare le necessità di allineamento.
- Quando vengono generati i pagamenti per il conto bancario configurato nel giornale di registrazione pagamenti, gli assegni verranno stampati utilizzando il formato specificato.

Per ulteriori informazioni, vedere [Modificare un formato per la creazione di report elettronici](/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template).
