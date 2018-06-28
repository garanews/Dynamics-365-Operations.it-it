---
title: Ordini di assistenza
description: L'ordine di assistenza rappresenta l'intervento eseguito da un tecnico presso la sede di un cliente in una data specifica.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 647bbe9cca0167d33048ad07e092708f90b41fc3
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---

# <a name="service-orders"></a><span data-ttu-id="0af11-103">Ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="0af11-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0af11-104">L'ordine di assistenza rappresenta l'intervento eseguito da un tecnico presso la sede di un cliente in una data specifica.</span><span class="sxs-lookup"><span data-stu-id="0af11-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="0af11-105">Ogni ordine di assistenza consiste in una o più righe di ordine di assistenza,</span><span class="sxs-lookup"><span data-stu-id="0af11-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="0af11-106">che rappresentano le ore di lavoro che il tecnico dovrà effettuare, nonché gli articoli, le spese e gli addebiti.</span><span class="sxs-lookup"><span data-stu-id="0af11-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="0af11-107">È possibile collegare le attività e gli oggetti a una riga di ordine di assistenza</span><span class="sxs-lookup"><span data-stu-id="0af11-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="0af11-108">e raggruppare quindi le righe di ordine di assistenza in base a un'attività o a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="0af11-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="0af11-109">È inoltre possibile allegare articoli a magazzino alle righe dell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="0af11-110">Creare ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="0af11-110">Create service orders</span></span>

<span data-ttu-id="0af11-111">Gli ordini di assistenza vengono creati in base al contratto di assistenza e alle relative righe.</span><span class="sxs-lookup"><span data-stu-id="0af11-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="0af11-112">Tuttavia, è possibile creare ordini di assistenza associati a un contratto di assistenza solo nel periodo specificato nel contratto.</span><span class="sxs-lookup"><span data-stu-id="0af11-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="0af11-113">Ad esempio, per il contratto di assistenza valido per l'anno 2011, era possibile creare ordini di assistenza nel periodo che andava dal 1 gennaio 2011 al 31 dicembre 2011.</span><span class="sxs-lookup"><span data-stu-id="0af11-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="0af11-114">Gli ordini di assistenza possono essere anche individuali, ovvero non devono necessariamente essere associati a un contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="0af11-115">Tali ordini di assistenza possono essere utilizzati per gestire interventi singoli o non programmati.</span><span class="sxs-lookup"><span data-stu-id="0af11-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="0af11-116">Nel mese di marzo il cliente decide, ad esempio, di richiedere un intervento di assistenza su due macchine oltre a quelle specificate nel contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="0af11-117">Per questa attività, vengono creati gli ordini di assistenza, ma senza associarli a un contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0af11-118">Per creare degli ordini di assistenza non associati a un contratto di assistenza, è necessario selezionare la casella di controllo <STRONG>Consenti senza contratto di assistenza</STRONG> nel modulo <STRONG>Parametri di gestione assistenza</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0af11-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="0af11-119">**Scenario**</span><span class="sxs-lookup"><span data-stu-id="0af11-119">**Scenario**</span></span>

<span data-ttu-id="0af11-120">Nel seguente scenario viene descritta un'altra situazione in cui è utile creare un ordine di assistenza non associato a un contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="0af11-121">Il responsabile interventi della società riceve una chiamata in cui si richiede un intervento di assistenza urgente per un ascensore.</span><span class="sxs-lookup"><span data-stu-id="0af11-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="0af11-122">Non c'è tempo per impostare un contratto di assistenza e un progetto per l'assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="0af11-123">Di conseguenza, il responsabile intervento crea un ordine di assistenza direttamente nel modulo **Ordini di assistenza**, allega l'ordine di assistenza a un progetto esistente e crea le righe di ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="0af11-124">Per registrare il lavoro non correlato al contratto di assistenza, il responsabile intervento crea inoltre una relazione di attività o oggetto per un ordine di assistenza esistente.</span><span class="sxs-lookup"><span data-stu-id="0af11-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="0af11-125">Per ulteriori informazioni, vedere [Creare ordini di assistenza manualmente](create-service-orders-manually.md) e [Creare relazioni di attività di assistenza tecnica](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="0af11-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="0af11-126">Monitoraggio dello stato di avanzamento degli ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="0af11-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="0af11-127">Per monitorare lo stato di avanzamento di un ordine cliente attraverso i diversi team e processi di lavoro, è possibile impostare un sistema di fasi e di codici causale per gli ordini di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="0af11-128">Per ogni fase, è possibile specificare le azioni che sono consentite.</span><span class="sxs-lookup"><span data-stu-id="0af11-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="0af11-129">Per ulteriori informazioni sui codici motivo, vedere [Creare codici motivo](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0af11-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="0af11-130">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0af11-130">**Example**</span></span>

<span data-ttu-id="0af11-131">Un ordine di assistenza è approvato dal responsabile intervento.</span><span class="sxs-lookup"><span data-stu-id="0af11-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="0af11-132">Il responsabile aggiorna la fase dell'ordine di assistenza e specifica un codice causale che indichi che l'ordine di assistenza è stato rilasciato al tecnico.</span><span class="sxs-lookup"><span data-stu-id="0af11-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="0af11-133">Il tecnico si reca presso la sede del cliente ed effettua l'assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="0af11-134">Specificare richieste articoli per gli ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="0af11-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="0af11-135">È possibile specificare gli articoli di magazzino necessari per gli ordini di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="0af11-136">Tuttavia, l'ordine di assistenza deve essere associato a un progetto.</span><span class="sxs-lookup"><span data-stu-id="0af11-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="0af11-137">Le richieste articoli per gli ordini di assistenza vengono elaborati nel corso di un progetto.</span><span class="sxs-lookup"><span data-stu-id="0af11-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="0af11-138">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0af11-138">**Example**</span></span>

<span data-ttu-id="0af11-139">Gli ordini di assistenza creati in base al contratto di assistenza vengono quindi elaborati dal responsabile intervento.</span><span class="sxs-lookup"><span data-stu-id="0af11-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="0af11-140">Al primo ordine di assistenza, il responsabile intervento si rende conto che il tecnico ha bisogno di un pezzo di ricambio importante che non è disponibile in magazzino,</span><span class="sxs-lookup"><span data-stu-id="0af11-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="0af11-141">di conseguenza crea una richiesta per il pezzo di ricambio direttamente dall'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="0af11-142">Spostare e registrare le righe</span><span class="sxs-lookup"><span data-stu-id="0af11-142">Move and post lines</span></span>

<span data-ttu-id="0af11-143">Il tecnico torna da un intervento di assistenza e modifica e aggiorna le righe di ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="0af11-144">Durante l'assistenza, ha eseguito un lavoro di manutenzione che era programmato per l'intervento di assistenza successivo.</span><span class="sxs-lookup"><span data-stu-id="0af11-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="0af11-145">Di conseguenza, il tecnico sposta le righe dall'intervento di assistenza successivo nell'intervento di assistenza corrente.</span><span class="sxs-lookup"><span data-stu-id="0af11-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="0af11-146">Il tecnico quindi registra l'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-146">The technician then posts the service order.</span></span> <span data-ttu-id="0af11-147">Per ulteriori informazioni, vedere [Spostare righe ordine di assistenza](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="0af11-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="0af11-148">Annulla ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="0af11-148">Cancel service orders</span></span>

<span data-ttu-id="0af11-149">Uno degli altri ordini di assistenza generati per il mese di gennaio è diventato obsoleto, perché l'intervento è stato annullato.</span><span class="sxs-lookup"><span data-stu-id="0af11-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="0af11-150">Il responsabile intervento annulla pertanto l'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="0af11-151">Per ulteriori informazioni, vedere [Annullare ordini di assistenza](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="0af11-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="0af11-152">Effettuare una registrazione da progetti</span><span class="sxs-lookup"><span data-stu-id="0af11-152">Post from projects</span></span>

<span data-ttu-id="0af11-153">Al termine di ciascuna settimana, il responsabile intervento desidera registrare tutti gli ordini di assistenza collegati a un progetto specifico.</span><span class="sxs-lookup"><span data-stu-id="0af11-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="0af11-154">Di conseguenza, individua il progetto pertinente nel modulo **Progetti** e registra gli ordini di assistenza che sono stati completati.</span><span class="sxs-lookup"><span data-stu-id="0af11-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="0af11-155">Per ulteriori informazioni, vedere [Registra ordini di assistenza (modulo di classe)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="0af11-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="0af11-156">Elimina ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="0af11-156">Delete service orders</span></span>

<span data-ttu-id="0af11-157">Durante il secondo semestre il cliente decide che gli interventi di assistenza non sono sufficientemente frequenti.</span><span class="sxs-lookup"><span data-stu-id="0af11-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="0af11-158">È necessario creare una nuova serie di interventi più frequenti per la durata rimanente del contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="0af11-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="0af11-159">Gli ordini di assistenza già creati devono quindi essere eliminati ed è necessario crearne di nuovi.</span><span class="sxs-lookup"><span data-stu-id="0af11-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="0af11-160">Per ulteriori informazioni, vedere [Eliminare ordini di assistenza](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="0af11-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0af11-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0af11-161">See also</span></span>

<span data-ttu-id="0af11-162">[Ordini di assistenza (modulo)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="0af11-162">[Service orders (form)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span></span>

  


