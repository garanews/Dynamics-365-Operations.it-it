---
title: Home page della gestione costi
description: "La gestione dei costi consente di gestire la valutazione e la contabilità di materie prime, prodotti semilavorati, prodotti finiti e WIP."
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cab2f165a70e5ce8f09f0391282e055e51afb225
ms.openlocfilehash: b1513e5a7cb3a19fd3743a5aac8efd211aa02ce8
ms.contentlocale: it-it
ms.lasthandoff: 02/21/2018

---

# <a name="cost-management-home-page"></a>Home page della gestione costi

[!include [banner](../includes/banner.md)]

La [gestione dei costi (video)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) consente di utilizzare la valutazione e la contabilità per materie prime, prodotti semilavorati, prodotti finiti e cespiti semilavorati. Si tratta del processo di definizione, gestione e creazione report di [contabilità inventario](cost-object.md) e [contabilità di produzione](bom-calculations.md).

È possibile definire i criteri dei costi nelle seguenti aree: 
-  [Costo predeterminato](costing-versions.md)
-  [Contabilità inventario](cost-object.md)
-  [Contabilità produzione](bom-calculations.md)
-  [Contabilità costi indiretti](costing-sheets.md)
-  [Integrazione contabile](production-order-cost-analysis.md)

Ad esempio, è possibile definire i metodi di valutazione per le scorte, come [FIFO](fifo-physical-value-marking.md), [Media ponderata](weighted-average-physical-value-marking.md), [Costo standard](prerequisites-standard-costs.md) o [Media mobile](moving-average.md) da applicare ai prodotti del [Gruppo di modelli di articoli](../inventory/reserve-inventory-quantities.md) in Contabilità inventario.

È possibile accedere alla contabilità inventario e alla contabilità inventario tramite le aree di lavoro **Amministrazione costi** e **Analisi costo**. Queste aree di lavoro forniscono una panoramica completa dello stato corrente, degli indicatori chiave di prestazione (KPI) e del rilevamento di deviazione. 

La contabilità di produzione consente di gestire la [determinazione costi per commessa](production-order-cost-analysis.md) negli ordini di produzione e negli ordini batch, nonché la [determinazione costi di tipo backflush](backflush-costing.md) in lean manufacturing.

Il [contenuto Power BI per la gestione dei costi](../../dev-itpro/analytics/cost-management-content-pack.md) fornisce analisi manageriali dell'inventario e delle scorte WIP e di come il costo procede attraverso questi per categoria nel tempo. Le informazioni possono essere utilizzate anche come supplemento dettagliato al rendiconto finanziario.

### <a name="additional-resources"></a>Risorse aggiuntive

#### <a name="whats-new-and-in-development"></a>Novità rilasciate e in via di sviluppo

Passare alla [roadmap di Microsoft Dynamics 365](https://roadmap.dynamics.com/) per un elenco delle nuove funzionalità rilasciate e di quelle che sono in via di sviluppo. 

#### <a name="white-paper"></a>White paper
Nel white paper [Calcolo DBA tramite uno schema di determinazione dei costi](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) viene descritto come impostare una scheda di determinazione costi contenente il materiale e la produzione e come l'impostazione influisce sui risultati del calcolo DBA. Per spiegare meglio gli argomenti, vengono forniti scenari concreti e dati che dimostrano l'effetto delle varie impostazioni e configurazioni. Non è previsto che vengano seguiti tutti gli scenari, perché questo documento non fornisce dettagli sufficienti per configurarli. Tuttavia, se si dispone delle conoscenze di base, è possibile provare a riprodurre le guide delle attività elencate di seguito nell'ordine in cui vengono visualizzate. Utilizzare la conoscenza acquisita tramite la lettura del documento per eseguire l'analisi di calcolo DBA. 

-  [Creare un prodotto finito](tasks/create-finished-product-2016-02.md)
-  [Creare un prodotto semilavorato](tasks/create-semi-finished-product-2016-02.md)
-  [Creare materie prime](tasks/create-raw-materials-2016-02.md)
-  [Creare DBA](tasks/create-boms-2016-02.md)
-  [Crea cicli di lavorazione](tasks/create-routes-2016-02.md)
-  [Calcolare una DBA utilizzando una struttura a livello singolo](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [Calcolare una DBA utilizzando una struttura a più livelli](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>Blog
Opinioni, notizie e altre informazioni sulla gestione costi sono disponibili nel [blog del team di ricerca e sviluppo per Dynamics AX - Produzione](https://blogs.msdn.microsoft.com/axmfg) e nel [blog del team di ricerca e sviluppo per Dynamics AX - Gestione della supply chain](https://blogs.msdn.microsoft.com/dynamicsaxscm). Sebbene alcuni di questi post siano stati scritti per la versione precedente della gestione costi, gli stessi concetti si applicano ancora e le procedure sono simili nella versione corrente.

#### <a name="task-guides"></a>Guide attività
Informazioni aggiuntive sono disponibili come guide attività in Finance and Operations. Per accedere alle guide attività, fare clic sul pulsante ? su qualsiasi pagina.


