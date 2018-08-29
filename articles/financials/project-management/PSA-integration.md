---
title: Project Service Automation
description: "In questo argomento vengono fornite informazioni sulla soluzione di integrazione di Project Service Automation con Finance and Operations. Questa soluzione di integrazione utilizza la funzionalità Integrazione dati per sincronizzare i dati tra istanze di Microsoft Dynamics 365 for Finance and Operations e Microsoft Dynamics 365 for Project Service Automation tramite Common Data Service."
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.contentlocale: it-it
ms.lasthandoff: 08/09/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="11028-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11028-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11028-105">La soluzione di integrazione di Project Service Automation con Finance and Operations utilizza la funzionalità Integrazione dati per sincronizzare i dati tra istanze di Microsoft Dynamics 365 for Finance and Operations e Microsoft Dynamics 365 for Project Service Automation tramite Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="11028-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="11028-106">I modelli di integrazione disponibili con la funzionalità Integrazione dati abilita il flusso di progetti, contratti di progetto, righe di contratto di progetto, punti cardine delle righe di contratto di progetto, attività di progetto, categorie di transazione di spesa, stime orarie e delle spese da Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="11028-107">Se si utilizza Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, dopo avere installato gli aggiornamenti KB 4132657 e KB 4132660, sarà possibile utilizzare i modelli per integrare le attività di progetto, le categorie di transazione delle spese, le stime orarie, le stime di spesa e i valori effettivi, nonché di configurare il blocco delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="11028-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="11028-108">Se è necessario reimpostare le distribuzioni contabili, si consiglia di installare anche KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="11028-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="11028-109">Se si utilizza Finance and Operations 7.3.0, è necessario installare KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="11028-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="11028-110">In questo modo sarà possibile integrare i progetti a prezzo fisso.</span><span class="sxs-lookup"><span data-stu-id="11028-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="11028-111">Se si utilizza Finance and Operations 7.3.0 e si eseguono transazioni di tipo commissione da Project Service Automation, è necessario installare KB 4345320 per includere tali commissioni nella fattura di progetto.</span><span class="sxs-lookup"><span data-stu-id="11028-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="11028-112">Se si utilizza Microsoft Dynamics 365 for Finance and Operations versione 8.0, sarà possibile utilizzare l'integrazione delle attività di progetto, le categorie di transazione spese, le stime orarie, le stime di spesa e il blocco delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="11028-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="11028-113">Se si utilizza Microsoft Dynamics 365 for Finance and Operations 8.0.1 o versioni successive, sarà possibile sincronizzare i valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="11028-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="11028-114">Prima di poter integrare Project Service Automation con Finance and Operations, è necessario configurare i parametri di integrazione Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11028-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="11028-115">Per ulteriori informazioni, vedere [Parametri di integrazione di Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="11028-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="11028-116">Questa soluzione di integrazione consente la sincronizzazione diretta negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="11028-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="11028-117">Gestire i contratti di progetto in Project Service Automation e sincronizzarli direttamente da Project Service Automation in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="11028-118">Creare progetti in Project Service Automation e sincronizzarli direttamente da Project Service Automation in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="11028-119">Gestire righe di contratti di progetto in Project Service Automation e sincronizzarle direttamente da Project Service Automation in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="11028-120">Gestire attività cardine di righe di contratti di progetto in Project Service Automation e sincronizzarle direttamente da Project Service Automation in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="11028-121">Gestire attività di progetto in Project Service Automation e sincronizzarle direttamente da Project Service Automation in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="11028-122">Gestire le categorie di transazione delle spese in Finance and Operations e sincronizzarle direttamente da Finance and Operations in Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11028-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="11028-123">Creare stime di ore di progetto in Project Service Automation e sincronizzarle direttamente da Project Service Automation in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="11028-124">Creare stime di spese di progetto in Project Service Automation e sincronizzarle direttamente da Project Service Automation in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="11028-125">Creare tempi di progetto, spese di progetto e valori effettivi di commissione in Project Service Automation e creare transazioni di progetto nel giornale di registrazione di integrazione di Project Service Automation in modo da poterli registrare in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="11028-126">Sincronizzazione dati</span><span class="sxs-lookup"><span data-stu-id="11028-126">Data synchronization</span></span>

<span data-ttu-id="11028-127">La figura seguente mostra il modo in cui i dati vengono sincronizzati nell'ambito dell'integrazione tra Project Service Automation e Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11028-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="11028-128">Non tutti i modelli sono disponibili al momento.</span><span class="sxs-lookup"><span data-stu-id="11028-128">Not all templates are currently available.</span></span> <span data-ttu-id="11028-129">I modelli verranno rilasciati man mano che vengono completati.</span><span class="sxs-lookup"><span data-stu-id="11028-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="11028-130">[![Integrazione di Project Service Automation con Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="11028-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="11028-131">Requisiti di sistema di Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11028-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="11028-132">Per utilizzare la soluzione di integrazione di Project Service Automation con Finance and Operations, è necessario installare Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 con aggiornamento 12 della piattaforma o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="11028-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="11028-133">Requisiti di sistema per Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11028-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="11028-134">Per utilizzare la soluzione di integrazione di Project Service Automation con Finance and Operations, è necessario installare i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="11028-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="11028-135">Microsoft Dynamics 365 for Project Service Automation versione 9.0.0.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="11028-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="11028-136">Soluzione Prospect to cash per Microsoft Dynamics 365 for Sales versione 1.14.0.0 (v14) o versione successiva</span><span class="sxs-lookup"><span data-stu-id="11028-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="11028-137">Soluzione Project Service Automation con Finance and Operations per Microsoft Dynamics 365 for Project Service Automation versione 1.0.0.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="11028-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="11028-138">Installare la soluzione di integrazione Project Service Automation in Finance and Operations nell'istanza di Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11028-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="11028-139">Scaricare la soluzione di integrazione di Project Service Automation con Finance and Operations dall'[Area download Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=57016) e seguire le istruzioni incluse con la soluzione.</span><span class="sxs-lookup"><span data-stu-id="11028-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
