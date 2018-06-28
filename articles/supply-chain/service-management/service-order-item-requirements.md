---
title: Richieste articoli degli ordini di assistenza
description: "Se è necessario prenotare articoli specifici per un ordine di assistenza, è possibile creare le richieste articolo di magazzino."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjSalesItemReq
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
ms.openlocfilehash: 880d41a5b3d8c9200a0a1f4b13af2d6d24d30766
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-item-requirements"></a><span data-ttu-id="2527d-103">Richieste articoli degli ordini di assistenza</span><span class="sxs-lookup"><span data-stu-id="2527d-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2527d-104">È possibile creare un ordine di assistenza per tenere traccia dei e gestire i servizi forniti ai clienti.</span><span class="sxs-lookup"><span data-stu-id="2527d-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="2527d-105">Se è necessario prenotare articoli specifici per un ordine di assistenza, è possibile creare le richieste articolo di magazzino.</span><span class="sxs-lookup"><span data-stu-id="2527d-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="2527d-106">Una richiesta articolo può essere immediatamente utilizzata dal magazzino oppure può avviare un ordine di produzione per l'articolo.</span><span class="sxs-lookup"><span data-stu-id="2527d-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="2527d-107">Le richieste articoli consentono, rispetto alle transazioni articolo, di pianificare la consegna per il momento immediatamente precedente l'utilizzo effettivo dell'articolo, di creare un ordine fornitore, di includere l'articolo all'interno di un accordo commerciale e di includere la richiesta articolo nella pianificazione della produzione.</span><span class="sxs-lookup"><span data-stu-id="2527d-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="2527d-108">Le richieste articoli per gli ordini di assistenza vengono elaborati nel corso di un progetto.</span><span class="sxs-lookup"><span data-stu-id="2527d-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="2527d-109">Per creare una richiesta articolo in un ordine di assistenza, è necessario che l'ordine di assistenza sia collegato a un progetto.</span><span class="sxs-lookup"><span data-stu-id="2527d-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="2527d-110">Una richiesta articolo creata per un ordine di assistenza è immediatamente visibile da **Gestione progetti** nell'ordine di assistenza specifico o mediante il modulo **Ordine cliente**.</span><span class="sxs-lookup"><span data-stu-id="2527d-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="2527d-111">Visualizzare una richiesta articolo da un ordine di assistenza</span><span class="sxs-lookup"><span data-stu-id="2527d-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="2527d-112">Fare clic su **Gestione assistenza** \> **Comune** \> **Ordini di assistenza** \> **Ordini di assistenza**.</span><span class="sxs-lookup"><span data-stu-id="2527d-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="2527d-113">Fare clic su **Spedisci** quindi su **Richiesta articolo** per aprire il modulo **Richieste articoli**.</span><span class="sxs-lookup"><span data-stu-id="2527d-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="2527d-114">Fare clic su **Progetto** e selezionare il campo **Ordine di assistenza** per visualizzare gli ordini di assistenza della richiesta articolo.</span><span class="sxs-lookup"><span data-stu-id="2527d-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="2527d-115">Eliminare ordini di assistenza con richieste articoli</span><span class="sxs-lookup"><span data-stu-id="2527d-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="2527d-116">Se si crea una richiesta articolo per un ordine di assistenza, non è possibile eliminare l'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="2527d-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="2527d-117">È necessario eliminare la richiesta articolo prima di poter eliminare l'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="2527d-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="2527d-118">Fare clic su **Gestione assistenza** \> **Comune** \> **Ordini di assistenza** \> **Ordini di assistenza**.</span><span class="sxs-lookup"><span data-stu-id="2527d-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="2527d-119">Fare clic su **Spedisci** quindi su **Richiesta articolo** per aprire il modulo **Richieste articoli**.</span><span class="sxs-lookup"><span data-stu-id="2527d-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="2527d-120">In questo modulo verrà visualizzato l'elenco di tutte le richieste articoli create nell'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="2527d-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="2527d-121">Selezionare la richiesta articolo da eliminare, quindi fare clic su **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="2527d-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="2527d-122">oppure</span><span class="sxs-lookup"><span data-stu-id="2527d-122">–or–</span></span>

1.  <span data-ttu-id="2527d-123">Fare clic su **Gestione progetti e contabilità** \> **Comune** \> **Progetti** \> **Tutti i progetti**.</span><span class="sxs-lookup"><span data-stu-id="2527d-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="2527d-124">Aprire il progetto che include l'ordine di assistenza in cui è stata creata una richiesta articolo.</span><span class="sxs-lookup"><span data-stu-id="2527d-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="2527d-125">Nel modulo **Progetti**, nel riquadro destro, fare clic su **Richieste articoli**.</span><span class="sxs-lookup"><span data-stu-id="2527d-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="2527d-126">Verrà aperto il modulo **Richieste articoli** con l'elenco delle richieste articolo associate al progetto selezionato.</span><span class="sxs-lookup"><span data-stu-id="2527d-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="2527d-127">Selezionare la richiesta articolo da eliminare, quindi fare clic su **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="2527d-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2527d-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2527d-128">See also</span></span>

<span data-ttu-id="2527d-129">[Richieste articoli (modulo)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="2527d-129">[Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span></span>

