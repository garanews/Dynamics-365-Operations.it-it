---
title: Convenzioni per l'ammortamento dei cespiti
description: In questo argomento viene fornita una panoramica delle convenzioni per l'ammortamento dei cespiti.
author: saraschi2
manager: AnnBe
ms.date: 03/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 730da7caaa4caae0cc47d392798ceec02bbcd743
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---

# <a name="fixed-asset-depreciation-conventions"></a><span data-ttu-id="0a30a-103">Convenzioni per l'ammortamento dei cespiti</span><span class="sxs-lookup"><span data-stu-id="0a30a-103">Fixed asset depreciation conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a30a-104">Le convenzioni di ammortamento vengono utilizzate per determinare se e come l'ammortamento viene calcolato sia per l'anno in cui il cespite viene acquisito che per l'anno in cui il cespite viene scartato.</span><span class="sxs-lookup"><span data-stu-id="0a30a-104">Depreciation conventions are used to determine when and how depreciation is calculated for both the year when the fixed asset is acquired and the year when the fixed asset is disposed of.</span></span>

<span data-ttu-id="0a30a-105">Le convenzioni di ammortamento possono essere assegnate all'impostazione di un libro gruppo cespiti.</span><span class="sxs-lookup"><span data-stu-id="0a30a-105">Depreciation conventions can be assigned to the setup for a fixed asset group book.</span></span> <span data-ttu-id="0a30a-106">In questo caso, le convenzioni di ammortamento assegnate vengono utilizzate come valori predefiniti quando i libri gruppo cespiti vengono creati.</span><span class="sxs-lookup"><span data-stu-id="0a30a-106">In this case, the depreciation conventions that are assigned are used as default values when fixed asset books are created.</span></span> <span data-ttu-id="0a30a-107">Le convenzioni di ammortamento possono inoltre essere impostate in un singolo libro cespiti.</span><span class="sxs-lookup"><span data-stu-id="0a30a-107">Depreciation conventions can also be set on an individual fixed asset book.</span></span>


|  <span data-ttu-id="0a30a-108">Convenzione di ammortamento</span><span class="sxs-lookup"><span data-stu-id="0a30a-108">Depreciation convention</span></span>  |                                                                                                                                                                                                                                                                                                                                                                                                     <span data-ttu-id="0a30a-109">descrizione</span><span class="sxs-lookup"><span data-stu-id="0a30a-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           <span data-ttu-id="0a30a-110">Nessuna</span><span class="sxs-lookup"><span data-stu-id="0a30a-110">None</span></span>            |                                                                                                                                                                                                                                                                                                                                                                     <span data-ttu-id="0a30a-111">L'ammortamento dei cespiti inizia nella data di <strong>Messa a servizio</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a30a-111">Assets start to depreciate on the <strong>Placed in service</strong> date.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|         <span data-ttu-id="0a30a-112">Semestre</span><span class="sxs-lookup"><span data-stu-id="0a30a-112">Half year</span></span>         |                                                                                                                                                                                                                                                                                                     <span data-ttu-id="0a30a-113">Si deduce mezzo anno di ammortamento sia per il primo anno che per l'ultimo che si ammortizza la proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a30a-113">You deduct a half-year of depreciation for both the first year and the last year that you depreciate the property.</span></span> <span data-ttu-id="0a30a-114">Si deduce un intero anno di ammortamento per ogni due anni durante il periodo di recupero.</span><span class="sxs-lookup"><span data-stu-id="0a30a-114">You deduct a full year of depreciation for every other year during the recovery period.</span></span>                                                                                                                                                                                                                                                                                                      |
|        <span data-ttu-id="0a30a-115">Mese intero</span><span class="sxs-lookup"><span data-stu-id="0a30a-115">Full month</span></span>         |                                                                                                                                                                                                                                                        <span data-ttu-id="0a30a-116">I cespiti con una data di <strong>Messa a servizio</strong> che si verifica in qualsiasi momento durante il mese iniziano l'ammortamento i primo giorno di quel mese.</span><span class="sxs-lookup"><span data-stu-id="0a30a-116">Assets that have a <strong>Placed in service</strong> date that occurs at any time during the month start to depreciate on the first day of that month.</span></span> <span data-ttu-id="0a30a-117">I cespiti che sono stati ritirati in qualsiasi momento durante il mese vengono considerati ritirati per scopi di ammortamento l'ultimo giorno del mese precedente.</span><span class="sxs-lookup"><span data-stu-id="0a30a-117">Assets that are retired at any time during the month are considered retired for depreciation purposes on the last day of the previous month.</span></span>                                                                                                                                                                                                                                                         |
|        <span data-ttu-id="0a30a-118">Metà trimestre</span><span class="sxs-lookup"><span data-stu-id="0a30a-118">Mid quarter</span></span>        |                                                                                                           <span data-ttu-id="0a30a-119">Per calcolare la detrazione dell'ammortamento per l'anno quando si mette la proprietà a servizio, moltiplicare l'ammortamento per un intero anno per la percentuale per il trimestre in cui la proprietà viene messa a servizio, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0a30a-119">To calculate your depreciation deduction for the year when you put the property in service, multiply the depreciation for a full year by the percentage for the quarter when the property is put in service, as shown in the following table.</span></span><table><thead><tr><th><span data-ttu-id="0a30a-120">Trimestre</span><span class="sxs-lookup"><span data-stu-id="0a30a-120">Quarter</span></span></th><th><span data-ttu-id="0a30a-121">Percentuale</span><span class="sxs-lookup"><span data-stu-id="0a30a-121">Percentage</span></span></th></tr></thead><tbody><tr><td><span data-ttu-id="0a30a-122">Nome</span><span class="sxs-lookup"><span data-stu-id="0a30a-122">First</span></span></td><td><span data-ttu-id="0a30a-123">87.5</span><span class="sxs-lookup"><span data-stu-id="0a30a-123">87.5</span></span></td></tr><tr><td><span data-ttu-id="0a30a-124">Seconda</span><span class="sxs-lookup"><span data-stu-id="0a30a-124">Second</span></span></td><td><span data-ttu-id="0a30a-125">62.5</span><span class="sxs-lookup"><span data-stu-id="0a30a-125">62.5</span></span></td></tr><tr><td><span data-ttu-id="0a30a-126">Terza</span><span class="sxs-lookup"><span data-stu-id="0a30a-126">Third</span></span></td><td><span data-ttu-id="0a30a-127">37.5</span><span class="sxs-lookup"><span data-stu-id="0a30a-127">37.5</span></span></td></tr><tr><td><span data-ttu-id="0a30a-128">Quarta</span><span class="sxs-lookup"><span data-stu-id="0a30a-128">Fourth</span></span></td><td><span data-ttu-id="0a30a-129">12.5</span><span class="sxs-lookup"><span data-stu-id="0a30a-129">12.5</span></span></td></tr></tbody></table><span data-ttu-id="0a30a-130">Metà trimestre di ammortamento viene preso nel trimestre di dismissione (o il trimestre completamente ammortizzato).</span><span class="sxs-lookup"><span data-stu-id="0a30a-130">A half-quarter of depreciation is taken in the quarter of disposal (or the fully depreciated quarter).</span></span>                                                                                                            |
| <span data-ttu-id="0a30a-131">Metà mese (giorno 1 del mese)</span><span class="sxs-lookup"><span data-stu-id="0a30a-131">Mid month (1st of month)</span></span>  | <span data-ttu-id="0a30a-132">I cespiti con una data di <strong>Messa a servizio</strong> nella prima metà del mese (giorni da 1 a 15) iniziano l'ammortamento il primo giorno del mese in cui cade la data di <strong>Messa a servizio</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a30a-132">Assets that have a <strong>Placed in service</strong> date in the first half of the month (days 1 through 15) start to depreciate on the first day of the month of the <strong>Placed in service</strong> date.</span></span> <span data-ttu-id="0a30a-133">I cespiti con una data di <strong>Messa a servizio</strong> nella seconda metà del mese (giorni da 16 fino alla fine del mese) iniziano l'ammortamento il primo giorno del mese successivo a quello in cui cade la data di <strong>Messa a servizio</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a30a-133">Assets that have a <strong>Placed in service</strong> date in the second half of the month (day 16 through the end of the month) start to depreciate on the first day of the month after the <strong>Placed in service</strong> date.</span></span> <span data-ttu-id="0a30a-134">I cespiti che sono stati ritirati nella prima metà del mese (giorni da 1 a 15) vengono considerati ritirati per scopi di ammortamento l'ultimo giorno del mese precedente.</span><span class="sxs-lookup"><span data-stu-id="0a30a-134">Assets that are retired in the first half of the month (days 1 through 15) are considered retired for depreciation purposes on the last day of the previous month.</span></span> <span data-ttu-id="0a30a-135">I cespiti che sono stati ritirati nella seconda metà del mese (giorni da 16 fino alla fine del mese) vengono considerati ritirati per scopi di ammortamento l'ultimo giorno del mese di ritiro.</span><span class="sxs-lookup"><span data-stu-id="0a30a-135">Assets that are retired in the second half of the month (day 16 through the end of the month) are considered retired for depreciation purposes on the last day of the month of retirement.</span></span> |
| <span data-ttu-id="0a30a-136">Metà mese (giorno 15 del mese)</span><span class="sxs-lookup"><span data-stu-id="0a30a-136">Mid month (15th of month)</span></span> |                                                                                                                                                        <span data-ttu-id="0a30a-137">Per calcolare la detrazione dell'ammortamento per l'anno quando si mette la proprietà a servizio, moltiplicare l'ammortamento per un intero anno per una frazione.</span><span class="sxs-lookup"><span data-stu-id="0a30a-137">To calculate your depreciation deduction for the year when you put the property in service, multiply the depreciation for a full year by a fraction.</span></span> <span data-ttu-id="0a30a-138">Il numeratore (numero superiore) della frazione è il numero di mesi completi dell'anno in cui la proprietà è a servizio, più 1/2 o (0,5).</span><span class="sxs-lookup"><span data-stu-id="0a30a-138">The numerator (top number) of this fraction is the number of full months in the year that the property is in service, plus 1/2 or (0.5).</span></span> <span data-ttu-id="0a30a-139">Il denominatore (numero inferiore) è 12.</span><span class="sxs-lookup"><span data-stu-id="0a30a-139">The denominator (bottom number) is 12.</span></span> <span data-ttu-id="0a30a-140">Se si smaltisce la proprietà prima della fine del periodo di recupero, utilizzare lo stesso metodo per calcolare la detrazione di ammortamento per l'anno di smaltimento.</span><span class="sxs-lookup"><span data-stu-id="0a30a-140">If you dispose of the property before the end of your recovery period, use the same method to calculate your depreciation deduction for the year of disposition.</span></span>                                                                                                                                                        |
| <span data-ttu-id="0a30a-141">Semestre (inizio anno)</span><span class="sxs-lookup"><span data-stu-id="0a30a-141">Half year (start of year)</span></span> |                                                                                                                                                                                                                                                          <span data-ttu-id="0a30a-142">I cespiti con una data di <strong>Messa a servizio</strong> che cade nella prima metà dell'anno iniziano l'ammortamento il primo giorno dell'anno (intero anno).</span><span class="sxs-lookup"><span data-stu-id="0a30a-142">Assets that have a <strong>Placed in service</strong> date in the first half of the year start to depreciate on the first day of the year (full year).</span></span> <span data-ttu-id="0a30a-143">I cespiti con una data di <strong>Messa a servizio</strong> che cade nella seconda metà dell'anno iniziano l'ammortamento a metà anno.</span><span class="sxs-lookup"><span data-stu-id="0a30a-143">Assets that have a <strong>Placed in service</strong> date in the second half of the year start to depreciate at the midpoint of the year.</span></span>                                                                                                                                                                                                                                                          |
|   <span data-ttu-id="0a30a-144">Semestre (prossimo anno)</span><span class="sxs-lookup"><span data-stu-id="0a30a-144">Half year (next year)</span></span>   |                                                            <span data-ttu-id="0a30a-145">I cespiti con una data di <strong>Messa a servizio</strong> che cade nella prima metà dell'anno iniziano l'ammortamento il primo giorno dell'anno (intero anno).</span><span class="sxs-lookup"><span data-stu-id="0a30a-145">Assets that have a <strong>Placed in service</strong> date in the first half of the year start to depreciate on the first day of the year (full year).</span></span> <span data-ttu-id="0a30a-146">I cespiti con una data di <strong>Messa a servizio</strong> che cade nella seconda metà dell'anno iniziano l'ammortamento il primo giorno dell'anno successivo.</span><span class="sxs-lookup"><span data-stu-id="0a30a-146">Assets that have a <strong>Placed in service</strong> date in the second half of the year start to depreciate on the first day of the next year.</span></span> <span data-ttu-id="0a30a-147">I cespiti che sono stati ritirati nella prima metà dell'anno vengono considerati ritirati per scopi di ammortamento l'ultimo giorno dell'anno precedente.</span><span class="sxs-lookup"><span data-stu-id="0a30a-147">Assets that are retired in the first half of the year are considered retired for depreciation purposes on the last day of the previous year.</span></span> <span data-ttu-id="0a30a-148">Qualsiasi ammortamento registrato durante l'anno corrente deve essere invertito o rettificato. I cespiti che sono stati ritirati nella seconda metà dell'anno vengono considerati ritirati per scopi di ammortamento l'ultimo giorno dell'anno di ritiro.</span><span class="sxs-lookup"><span data-stu-id="0a30a-148">Any depreciation that is posted in the current year must be reversed or adjusted out. Assets that are retired in the second half of the year are considered retired for depreciation purposes on the last day of the year of retirement.</span></span>                                                            |

