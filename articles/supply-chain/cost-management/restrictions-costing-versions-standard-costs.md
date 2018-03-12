---
title: Restrizioni per le versioni di determinazione costi per i costi standard
description: In questo argomento vengono elencate le restrizioni che sia applicano a una versione di determinazione costi per i costi standard.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: it-it
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="e1a34-103">Restrizioni per le versioni di determinazione costi per i costi standard</span><span class="sxs-lookup"><span data-stu-id="e1a34-103">Restrictions on costing versions for standard costs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e1a34-104">In questo argomento vengono elencate le restrizioni che sia applicano a una versione di determinazione costi per i costi standard.</span><span class="sxs-lookup"><span data-stu-id="e1a34-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="e1a34-105">Le restrizioni seguenti aiutano a garantire la conformità ai principi di determinazione costi standard:</span><span class="sxs-lookup"><span data-stu-id="e1a34-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="e1a34-106">Le spese devono essere incluse nel costo di un articolo.</span><span class="sxs-lookup"><span data-stu-id="e1a34-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="e1a34-107">Nel caso di un articolo prodotto, rappresentano i costi costanti ammortizzati nelle informazioni sulla distinta base (DBA) e sul ciclo di lavorazione.</span><span class="sxs-lookup"><span data-stu-id="e1a34-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="e1a34-108">Pertanto, questi addebiti devono essere inclusi nel costo unitario.</span><span class="sxs-lookup"><span data-stu-id="e1a34-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="e1a34-109">Nel caso di un articolo acquistato, vengono incluse anche nel costo unitario dell'articolo.</span><span class="sxs-lookup"><span data-stu-id="e1a34-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="e1a34-110">Il calcolo dei costi standard per un articolo prodotto deve basarsi sui record dei costi in una versione di determinazione costi per costi standard.</span><span class="sxs-lookup"><span data-stu-id="e1a34-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="e1a34-111">È possibile utilizzare origini di dati di costo alternative solo con una versione di determinazione costi per costi pianificati, ad esempio accordi commerciali sui prezzi di acquisto per gli articoli acquistati.</span><span class="sxs-lookup"><span data-stu-id="e1a34-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="e1a34-112">Le origini di dati di costo alternative vengono definite dal gruppo di calcolo DBA.</span><span class="sxs-lookup"><span data-stu-id="e1a34-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="e1a34-113">I calcoli DBA devono essere eseguiti nella modalità di esplosione a livello singolo.</span><span class="sxs-lookup"><span data-stu-id="e1a34-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="e1a34-114">I dati relativi al costo dell'articolo per i costi standard possono essere copiati in un'altra versione di determinazione costi contenente costi standard o pianificati.</span><span class="sxs-lookup"><span data-stu-id="e1a34-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="e1a34-115">Tali dati per i costi pianificati tuttavia non potranno essere copiati in una versione di determinazione costi contenente costi standard, in quanto le restrizioni indicate in precedenza in questo argomento non sono applicabili ai costi pianificati.</span><span class="sxs-lookup"><span data-stu-id="e1a34-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="e1a34-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1a34-116">Related topics</span></span>
--------

[<span data-ttu-id="e1a34-117">Versioni determinazione costi</span><span class="sxs-lookup"><span data-stu-id="e1a34-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="e1a34-118">Aggiornare costi standard in un ambiente non di produzione</span><span class="sxs-lookup"><span data-stu-id="e1a34-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="e1a34-119">Eseguire le operazioni preliminari alla gestione dei costi standard per gli articoli prodotti</span><span class="sxs-lookup"><span data-stu-id="e1a34-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

