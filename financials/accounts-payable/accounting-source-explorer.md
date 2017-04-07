---
title: "Esplora origine contabilità"
description: "Questo articolo fornisce informazioni su Esplora origine contabilità, che è possibile utilizzare per analisi dettagliate delle informazioni di origine relative alle voci della contabilità generale."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 8913e61285d5d180883471991b659ddcb260afe3
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-source-explorer"></a>Esplora origine contabilità

Questo articolo fornisce informazioni su Esplora origine contabilità, che è possibile utilizzare per analisi dettagliate delle informazioni di origine relative alle voci della contabilità generale.

Esplora origine contabilità è una nuova pagina contenente le informazioni relative all'origine. È possibile utilizzare tali Esplora di origine della contabilità come strumento autonomo oppure analizzare i dettagli relativi alle voci contabili di contabilità generale. Ad esempio, è possibile eseguire tale Esplora di origine di registrazione per ottenere informazioni più dettagliate sull'origine per un saldo in bilancio di verifica o per una transazione giustificativo. È quindi possibile utilizzare la funzionalità Esporta in MS Excel per visualizzare le informazioni in modo ancora più dettagliato in Microsoft Excel (ad esempio, in una tabella Pivot o in un report di tabella pivot).

Esplora origine contabilità mostra sempre lo stesso importo totale per conto CoGe in base a quanto indicato in Contabilità generale (ad esempio, in Bilancio di verifica). Come in Bilancio di verifica, è possibile visualizzare segmenti in colonne separate. È sufficiente selezionare il set di dimensioni finanziarie appropriato. 

È possibile utilizzare i parametri per definire un intervallo di date per l'analisi. Anche questa funzionalità è simile a quella presente in Bilancio di verifica.

Per tutti i documenti che utilizzano il framework del documento di origine, altre informazioni di stima relativi di Esplora di origine, in base alle distribuzioni contabili e, se applicabile, le distribuzioni contabili di progetto. Queste informazioni includono l'importo monetario di tipo, progetto, attività, categoria e proprietà riga. Di seguito sono riportati alcuni esempi dell'analisi che è possibile effettuare:

-   Scostamenti tra ordini di acquisto e fatture fornitore, poiché ogni scostamento viene rappresentato da un tipo di importo monetario, ad esempio lo scostamento addebiti
-   Ore e spese fatturabili rispetto a quelle non fatturabili per progetto, Business Unit e conto principale

Per i documenti di origine che utilizzano il concetto di identità di riferimento del documento di origine, Esplora origine contabilità mostra un numero maggiore di dettagli, ad esempio il cliente, il fornitore, il lavoratore, il prodotto, la quantità, il testo unità e le descrizioni. Di seguito sono riportati alcuni esempi dell'analisi che è possibile effettuare:

-   Spese di albergo per Business Unit e catena alberghiera per un periodo fiscale, in base alle note spese
-   Sconti per fornitore, prodotto, reparto

Per questi documenti, è possibile inoltre passare al documento di origine effettivo da Esplora origine contabilità.

