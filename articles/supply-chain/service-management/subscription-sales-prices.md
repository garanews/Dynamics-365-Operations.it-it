---
title: Prezzi di vendita sottoscrizione
description: Quando si crea una sottoscrizione, il prezzo di vendita deriva dall'impostazione del prezzo di vendita creata nel modulo Sottoscrizione prezzo di vendita.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d9d462121915ce3f800581a9540dc1ef8f6e785f
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---

# <a name="subscription-sales-prices"></a><span data-ttu-id="0a54d-103">Prezzi di vendita sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a54d-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0a54d-104">Quando si crea una sottoscrizione, il prezzo di vendita deriva dall'impostazione del prezzo di vendita creata nel modulo **Sottoscrizione prezzo di vendita**.</span><span class="sxs-lookup"><span data-stu-id="0a54d-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="0a54d-105">Nel modulo **Sottoscrizione prezzo di vendita** è possibile creare prezzi di vendita per una sottoscrizione specifica o prezzi di vendita da applicare su più larga scala.</span><span class="sxs-lookup"><span data-stu-id="0a54d-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="0a54d-106">Per applicare un prezzo di vendita a una sottoscrizione, il codice periodo e la valuta della sottoscrizione e del prezzo di vendita devono essere identici.</span><span class="sxs-lookup"><span data-stu-id="0a54d-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="0a54d-107">Se il codice periodo e la valuta sono identici per la sottoscrizione e per il prezzo di vendita, i prezzi di vendita di sottoscrizione verranno selezionati sulla base delle priorità elencate nella seguente tabella.</span><span class="sxs-lookup"><span data-stu-id="0a54d-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="0a54d-108">Una cella vuota nella tabella indica un campo vuoto e la X indica un valore uguale al valore nella sottoscrizione da cui viene generata la transazione.</span><span class="sxs-lookup"><span data-stu-id="0a54d-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a54d-109">Priorità </span><span class="sxs-lookup"><span data-stu-id="0a54d-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="0a54d-110"><strong>Categoria</strong></span><span class="sxs-lookup"><span data-stu-id="0a54d-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="0a54d-111"><strong>ID progetto</strong></span><span class="sxs-lookup"><span data-stu-id="0a54d-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="0a54d-112"><strong>Sottoscrizione</strong></span><span class="sxs-lookup"><span data-stu-id="0a54d-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="0a54d-113"><strong>Valuta di vendita</strong></span><span class="sxs-lookup"><span data-stu-id="0a54d-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="0a54d-114"><strong>Codice periodo</strong></span><span class="sxs-lookup"><span data-stu-id="0a54d-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-115">1</span><span class="sxs-lookup"><span data-stu-id="0a54d-115">1</span></span></p></td>
<td><p><span data-ttu-id="0a54d-116">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-116">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-117">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-117">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-118">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-118">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-119">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-119">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-120">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-121">2</span><span class="sxs-lookup"><span data-stu-id="0a54d-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-122">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-122">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-123">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-123">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-124">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-124">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-125">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-126">3</span><span class="sxs-lookup"><span data-stu-id="0a54d-126">3</span></span></p></td>
<td><p><span data-ttu-id="0a54d-127">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-128">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-128">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-129">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-129">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-130">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-131">4</span><span class="sxs-lookup"><span data-stu-id="0a54d-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-132">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-132">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-133">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-133">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-134">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-135">5</span><span class="sxs-lookup"><span data-stu-id="0a54d-135">5</span></span></p></td>
<td><p><span data-ttu-id="0a54d-136">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-136">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-137">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-138">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-138">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-139">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-140">6</span><span class="sxs-lookup"><span data-stu-id="0a54d-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-141">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-142">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-142">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-143">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-144">7</span><span class="sxs-lookup"><span data-stu-id="0a54d-144">7</span></span></p></td>
<td><p><span data-ttu-id="0a54d-145">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-146">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-146">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-147">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-148">8</span><span class="sxs-lookup"><span data-stu-id="0a54d-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0a54d-149">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-149">X</span></span></p></td>
<td><p><span data-ttu-id="0a54d-150">X</span><span class="sxs-lookup"><span data-stu-id="0a54d-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a54d-151">Quando viene creata una commissione di sottoscrizione, viene selezionato come prezzo di vendita di sottoscrizione il prezzo di vendita con il livello massimo di dettagli, come indicato nella tabella sopra riportata.</span><span class="sxs-lookup"><span data-stu-id="0a54d-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="0a54d-152">Aggiornare e indicizzare i prezzi di vendita di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a54d-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="0a54d-153">È possibile aggiornare il prezzo di vendita di sottoscrizione aggiornando l'indice o il prezzo di base.</span><span class="sxs-lookup"><span data-stu-id="0a54d-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="0a54d-154">L'aggiornamento può essere eseguito in base a un valore percentuale o a un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="0a54d-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="0a54d-155">Prezzi di vendita di commissioni di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a54d-155">Subscription fee sales prices</span></span>

<span data-ttu-id="0a54d-156">Quando si crea una commissione di sottoscrizione, il prezzo di vendita è basato sull'impostazione del prezzo di vendita della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0a54d-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="0a54d-157">È possibile utilizzare il prezzo di base dell'impostazione del prezzo di sottoscrizione oppure creare prezzi di vendita indicizzati.</span><span class="sxs-lookup"><span data-stu-id="0a54d-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="0a54d-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="0a54d-158">Example</span></span>

<span data-ttu-id="0a54d-159">Si desidera impostare prezzi di vendita di sottoscrizione di 500 EUR per un nuovo progetto 9030.</span><span class="sxs-lookup"><span data-stu-id="0a54d-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="0a54d-160">Nel modulo **Sottoscrizione prezzo di vendita** creare una riga del prezzo di vendita di sottoscrizione come indicato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="0a54d-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a54d-161">Valido dal</span><span class="sxs-lookup"><span data-stu-id="0a54d-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0a54d-162">Categoria</span><span class="sxs-lookup"><span data-stu-id="0a54d-162">Category</span></span></p></th>
<th><p><span data-ttu-id="0a54d-163">Progetto</span><span class="sxs-lookup"><span data-stu-id="0a54d-163">Project</span></span></p></th>
<th><p><span data-ttu-id="0a54d-164">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a54d-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0a54d-165">Codice periodo</span><span class="sxs-lookup"><span data-stu-id="0a54d-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="0a54d-166">Valuta di vendita</span><span class="sxs-lookup"><span data-stu-id="0a54d-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0a54d-167">Prezzo di vendita</span><span class="sxs-lookup"><span data-stu-id="0a54d-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-168">28/08/2006</span><span class="sxs-lookup"><span data-stu-id="0a54d-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0a54d-169">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0a54d-170">Mese</span><span class="sxs-lookup"><span data-stu-id="0a54d-170">Month</span></span></p></td>
<td><p><span data-ttu-id="0a54d-171">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-172">500</span><span class="sxs-lookup"><span data-stu-id="0a54d-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a54d-173">Si noti che i campi **Categoria** e **Sottoscrizione** sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="0a54d-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="0a54d-174">Creare a questo punto le seguenti sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="0a54d-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a54d-175">Sottoscrizione assistenza</span><span class="sxs-lookup"><span data-stu-id="0a54d-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0a54d-176">Progetto</span><span class="sxs-lookup"><span data-stu-id="0a54d-176">Project</span></span></p></th>
<th><p><span data-ttu-id="0a54d-177">Gruppo di sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="0a54d-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="0a54d-178">Categoria</span><span class="sxs-lookup"><span data-stu-id="0a54d-178">Category</span></span></p></th>
<th><p><span data-ttu-id="0a54d-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="0a54d-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="0a54d-180">Codice periodo</span><span class="sxs-lookup"><span data-stu-id="0a54d-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="0a54d-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0a54d-182">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-182">9030</span></span></p></td>
<td><p><span data-ttu-id="0a54d-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="0a54d-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0a54d-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0a54d-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0a54d-185">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-186">Mensile</span><span class="sxs-lookup"><span data-stu-id="0a54d-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="0a54d-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0a54d-188">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-188">9030</span></span></p></td>
<td><p><span data-ttu-id="0a54d-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="0a54d-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0a54d-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="0a54d-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0a54d-191">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-192">Mensile</span><span class="sxs-lookup"><span data-stu-id="0a54d-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a54d-193">Creare ora commissioni di sottoscrizione per entrambe le sottoscrizioni del gruppo di sottoscrizioni Sub1:</span><span class="sxs-lookup"><span data-stu-id="0a54d-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="0a54d-194">Fare clic su **Gestione assistenza** \> **Impostazione** \> **Sottoscrizioni assistenza** \> **Gruppo di sottoscrizioni**.</span><span class="sxs-lookup"><span data-stu-id="0a54d-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="0a54d-195">Nel modulo **Gruppi di sottoscrizioni**, fare clic su **Funzione** \> **Crea commissione sottoscrizione**.</span><span class="sxs-lookup"><span data-stu-id="0a54d-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="0a54d-196">Nel modulo **Crea commissione sottoscrizione**, immettere le informazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="0a54d-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="0a54d-197">Per ulteriori informazioni, vedere [Creare transazioni di commissione di sottoscrizione](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="0a54d-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="0a54d-198">Verranno create commissioni di sottoscrizione con prezzo di vendita di 500 EUR per entrambe le sottoscrizioni, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0a54d-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a54d-199">Data progetto</span><span class="sxs-lookup"><span data-stu-id="0a54d-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="0a54d-200">Sottoscrizione assistenza</span><span class="sxs-lookup"><span data-stu-id="0a54d-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0a54d-201">Progetto</span><span class="sxs-lookup"><span data-stu-id="0a54d-201">Project</span></span></p></th>
<th><p><span data-ttu-id="0a54d-202">Categoria</span><span class="sxs-lookup"><span data-stu-id="0a54d-202">Category</span></span></p></th>
<th><p><span data-ttu-id="0a54d-203">Data di inizio</span><span class="sxs-lookup"><span data-stu-id="0a54d-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="0a54d-204">Data di fine</span><span class="sxs-lookup"><span data-stu-id="0a54d-204">End date</span></span></p></th>
<th><p><span data-ttu-id="0a54d-205">Valuta di vendita</span><span class="sxs-lookup"><span data-stu-id="0a54d-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0a54d-206">Prezzo di vendita</span><span class="sxs-lookup"><span data-stu-id="0a54d-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-207">28/08/2006</span><span class="sxs-lookup"><span data-stu-id="0a54d-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0a54d-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="0a54d-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0a54d-209">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-209">9030</span></span></p></td>
<td><p><span data-ttu-id="0a54d-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0a54d-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0a54d-211">01/01/2007</span><span class="sxs-lookup"><span data-stu-id="0a54d-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0a54d-212">31/03/2007</span><span class="sxs-lookup"><span data-stu-id="0a54d-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0a54d-213">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-214">500</span><span class="sxs-lookup"><span data-stu-id="0a54d-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-215">28/08/2006</span><span class="sxs-lookup"><span data-stu-id="0a54d-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0a54d-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="0a54d-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0a54d-217">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-217">9030</span></span></p></td>
<td><p><span data-ttu-id="0a54d-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="0a54d-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0a54d-219">01/01/2007</span><span class="sxs-lookup"><span data-stu-id="0a54d-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0a54d-220">31/03/2007</span><span class="sxs-lookup"><span data-stu-id="0a54d-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0a54d-221">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-222">500</span><span class="sxs-lookup"><span data-stu-id="0a54d-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a54d-223">Si decide successivamente che si desidera specificare i prezzi di vendita per la categoria SubCat1 del progetto 9030.</span><span class="sxs-lookup"><span data-stu-id="0a54d-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="0a54d-224">Viene creata pertanto una nuova riga con prezzo di vendita di 550 EUR per la combinazione del progetto 9030 e della categoria di commissione SubCat1.</span><span class="sxs-lookup"><span data-stu-id="0a54d-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="0a54d-225">Per il progetto 9030 ora sono presenti due righe di prezzo di vendita di sottoscrizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0a54d-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a54d-226">Valido dal</span><span class="sxs-lookup"><span data-stu-id="0a54d-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0a54d-227">Categoria</span><span class="sxs-lookup"><span data-stu-id="0a54d-227">Category</span></span></p></th>
<th><p><span data-ttu-id="0a54d-228">Progetto</span><span class="sxs-lookup"><span data-stu-id="0a54d-228">Project</span></span></p></th>
<th><p><span data-ttu-id="0a54d-229">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a54d-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0a54d-230">Codice periodo</span><span class="sxs-lookup"><span data-stu-id="0a54d-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="0a54d-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="0a54d-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="0a54d-232">Prezzo di vendita</span><span class="sxs-lookup"><span data-stu-id="0a54d-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-233">28/08/2007</span><span class="sxs-lookup"><span data-stu-id="0a54d-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0a54d-234">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0a54d-235">Mese</span><span class="sxs-lookup"><span data-stu-id="0a54d-235">Month</span></span></p></td>
<td><p><span data-ttu-id="0a54d-236">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-237">500</span><span class="sxs-lookup"><span data-stu-id="0a54d-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-238">28/08/2007</span><span class="sxs-lookup"><span data-stu-id="0a54d-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="0a54d-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0a54d-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0a54d-240">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0a54d-241">Mese</span><span class="sxs-lookup"><span data-stu-id="0a54d-241">Month</span></span></p></td>
<td><p><span data-ttu-id="0a54d-242">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-243">550</span><span class="sxs-lookup"><span data-stu-id="0a54d-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a54d-244">Ripetere la procedura sopra descritta per creare commissioni di sottoscrizione per entrambe le sottoscrizioni del gruppo di sottoscrizioni Sub1.</span><span class="sxs-lookup"><span data-stu-id="0a54d-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="0a54d-245">Nella tabella seguente vengono illustrate le transazioni create per ogni sottoscrizione collegata al gruppo di sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="0a54d-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a54d-246">Data progetto</span><span class="sxs-lookup"><span data-stu-id="0a54d-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="0a54d-247">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a54d-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0a54d-248">Progetto</span><span class="sxs-lookup"><span data-stu-id="0a54d-248">Project</span></span></p></th>
<th><p><span data-ttu-id="0a54d-249">Categoria</span><span class="sxs-lookup"><span data-stu-id="0a54d-249">Category</span></span></p></th>
<th><p><span data-ttu-id="0a54d-250">Data di inizio</span><span class="sxs-lookup"><span data-stu-id="0a54d-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="0a54d-251">Data di fine</span><span class="sxs-lookup"><span data-stu-id="0a54d-251">End date</span></span></p></th>
<th><p><span data-ttu-id="0a54d-252">Valuta di vendita</span><span class="sxs-lookup"><span data-stu-id="0a54d-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0a54d-253">Prezzo di vendita</span><span class="sxs-lookup"><span data-stu-id="0a54d-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a54d-254">28/07/2007</span><span class="sxs-lookup"><span data-stu-id="0a54d-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="0a54d-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="0a54d-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0a54d-256">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-256">9030</span></span></p></td>
<td><p><span data-ttu-id="0a54d-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="0a54d-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0a54d-258">01/01/2008</span><span class="sxs-lookup"><span data-stu-id="0a54d-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0a54d-259">31/03/2008</span><span class="sxs-lookup"><span data-stu-id="0a54d-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0a54d-260">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-261">550</span><span class="sxs-lookup"><span data-stu-id="0a54d-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a54d-262">28/07/2008</span><span class="sxs-lookup"><span data-stu-id="0a54d-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="0a54d-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="0a54d-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0a54d-264">9030</span><span class="sxs-lookup"><span data-stu-id="0a54d-264">9030</span></span></p></td>
<td><p><span data-ttu-id="0a54d-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="0a54d-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0a54d-266">01/01/2008</span><span class="sxs-lookup"><span data-stu-id="0a54d-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0a54d-267">31/03/2008</span><span class="sxs-lookup"><span data-stu-id="0a54d-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0a54d-268">EUR</span><span class="sxs-lookup"><span data-stu-id="0a54d-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="0a54d-269">500</span><span class="sxs-lookup"><span data-stu-id="0a54d-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a54d-270">Nella prima transazione della sottoscrizione 00020\_135 il prezzo di vendita di 550 EUR deriva dal prezzo di vendita di sottoscrizione impostato per la combinazione di progetto e categoria specifici.</span><span class="sxs-lookup"><span data-stu-id="0a54d-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="0a54d-271">Nella seconda transazione della sottoscrizione 00021\_135 il prezzo di vendita di 500 EUR viene utilizzato come prezzo di vendita di sottoscrizione del progetto, poiché per la combinazione del progetto 9030 e della categoria SubCat2 non è impostato alcun prezzo.</span><span class="sxs-lookup"><span data-stu-id="0a54d-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a54d-272">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0a54d-272">See also</span></span>

[<span data-ttu-id="0a54d-273">Aggiornare e indicizzare i prezzi di vendita di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a54d-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


