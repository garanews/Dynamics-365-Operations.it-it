---
title: Sincronizzare i contratti di progetto e progetti direttamente da Project Service Automation a Finance and Operations
description: "Questo argomento descrive il modello e le attività sottostanti che vengono utilizzati per sincronizzare i contratti di progetto e i progetti direttamente da Microsoft Dynamics 365 for Project Service Automation con Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 65a274323a2d95c9c76727c9e40aa7e649e6350a
ms.contentlocale: it-it
ms.lasthandoff: 08/09/2018

---

# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="332ea-103">Sincronizzare i contratti di progetto e progetti direttamente da Project Service Automation a Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="332ea-103">Synchronize project contracts and projects directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="332ea-104">Questo argomento descrive il modello e le attività sottostanti che vengono utilizzati per sincronizzare i contratti di progetto e i progetti direttamente da Microsoft Dynamics 365 for Project Service Automation con Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="332ea-105">Se si utilizza Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, è necessario installare KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="332ea-105">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="332ea-106">Flusso di dati per Project Service Automation verso Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="332ea-106">Data flow for Project Service Automation to Finance and Operations</span></span>

> [!NOTE]
> <span data-ttu-id="332ea-107">Prima di poter utilizzare la soluzione di integrazione di Project Service Automation con Finance and Operations, è consigliabile acquisire familiarità con la funzionalità Integrazione dati di Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="332ea-107">Before you can use the Project Service Automation to Finance and Operations integration solution, you should be familiar with the Microsoft Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="332ea-108">La soluzione di integrazione di Project Service Automation in Finance and Operations utilizza la funzionalità di integrazione dei dati per sincronizzare i dati tra istanze di Project Service Automation e Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-108">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="332ea-109">Il modello di integrazione disponibile con la funzionalità Integrazione dati abilita il flusso di dati su progetti, contratti di progetto, righe di contratto di progetto e punti cardine delle righe di contratto di progetto da Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="332ea-110">La figura seguente mostra il modo in cui i dati vengono sincronizzati tra Project Service Automation e Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="332ea-111">[![Flusso di dati per l'integrazione di Project Service Automation con Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="332ea-111">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="332ea-112">Modelli e attività</span><span class="sxs-lookup"><span data-stu-id="332ea-112">Templates and tasks</span></span>

<span data-ttu-id="332ea-113">Per accedere ai modelli disponibili, nell'interfaccia di amministrazione di Microsoft PowerApps selezionare **Progetti** e quindi, nell'angolo superiore destro, selezionare **Nuovo progetto** per selezionare modelli pubblici.</span><span class="sxs-lookup"><span data-stu-id="332ea-113">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="332ea-114">Il seguente modello e le attività sottostanti vengono utilizzati per sincronizzare i contratti di progetto e i progetti da Project Service Automation a Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="332ea-114">The following template and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="332ea-115">**Nome del modello in Integrazione dati:** Progetti e contratti (da PSA a Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="332ea-115">**Name of the template in Data integration:** Projects and contracts (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="332ea-116">**Nome delle attività del progetto:**</span><span class="sxs-lookup"><span data-stu-id="332ea-116">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="332ea-117">Contratti di progetto da PSA a Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="332ea-117">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="332ea-118">Progetto da PSA a Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="332ea-118">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="332ea-119">Righe di contratto di progetto da PSA a Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="332ea-119">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="332ea-120">Punti cardine righe di contratto di progetto da PSA a Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="332ea-120">Project contract line milestones PSA to Fin and Ops</span></span>

<span data-ttu-id="332ea-121">Prima di eseguire la sincronizzazione di contratti di progetto e di progetti, è necessario sincronizzare gli account.</span><span class="sxs-lookup"><span data-stu-id="332ea-121">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="332ea-122">Insieme di entità</span><span class="sxs-lookup"><span data-stu-id="332ea-122">Entity set</span></span>

| <span data-ttu-id="332ea-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="332ea-123">Project Service Automation</span></span>       | <span data-ttu-id="332ea-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="332ea-124">Finance and Operations</span></span>                                 |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="332ea-125">Ordini</span><span class="sxs-lookup"><span data-stu-id="332ea-125">Orders</span></span>                           | <span data-ttu-id="332ea-126">Entità di integrazione per contratto di progetto</span><span class="sxs-lookup"><span data-stu-id="332ea-126">Integration entity for project contract</span></span>                |
| <span data-ttu-id="332ea-127">Progetti</span><span class="sxs-lookup"><span data-stu-id="332ea-127">Projects</span></span>                         | <span data-ttu-id="332ea-128">Entità di integrazione per progetto</span><span class="sxs-lookup"><span data-stu-id="332ea-128">Integration entity for project</span></span>                         |
| <span data-ttu-id="332ea-129">Righe ordine</span><span class="sxs-lookup"><span data-stu-id="332ea-129">Order lines</span></span>                      | <span data-ttu-id="332ea-130">Entità di integrazione per riga di contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="332ea-130">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="332ea-131">Punti cardine righe di contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="332ea-131">Project contract line milestones</span></span> | <span data-ttu-id="332ea-132">Entità di integrazione per il punto cardine della riga di contratto del progetto</span><span class="sxs-lookup"><span data-stu-id="332ea-132">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="332ea-133">Flusso di entità</span><span class="sxs-lookup"><span data-stu-id="332ea-133">Entity flow</span></span>

<span data-ttu-id="332ea-134">I contratti di progetto vengono gestiti in Project Service Automation e vengono sincronizzati con Finance and Operations come contratti di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-134">Project contracts are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contracts.</span></span> <span data-ttu-id="332ea-135">Come parte del modello di integrazione, è possibile impostare l'origine dell'integrazione in Finance and Operations per il contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-135">As part of the integration template, you can set the integration source in Finance and Operations for the project contract.</span></span>

<span data-ttu-id="332ea-136">I progetti di tempistica e materiali e a prezzo fisso vengono gestiti in Project Service Automation e vengono sincronizzati con Finance and Operations come progetti.</span><span class="sxs-lookup"><span data-stu-id="332ea-136">Time and material project and Fixed price projects are managed in Project Service Automation, and they are synchronized to Finance and Operations as projects.</span></span> <span data-ttu-id="332ea-137">Come parte dell'integrazione del modello, è possibile impostare l'origine dell'integrazione in Finance and Operations per il contratto di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-137">As part of the template integration, you can set the integration source in Finance and Operations for the project.</span></span>

<span data-ttu-id="332ea-138">Le righe di contratto di progetto vengono gestite in Project Service Automation e vengono sincronizzate con Finance and Operations come regole di fatturazione dei contratti di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-138">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contract billing rules.</span></span> <span data-ttu-id="332ea-139">Se il metodo di fatturazione differisce dal tipo di progetto predefinito, la sincronizzazione aggiorna il tipo di progetto per il progetto o il gruppo di progetti con riga di contratto.</span><span class="sxs-lookup"><span data-stu-id="332ea-139">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="332ea-140">I punti cardine delle righe di contratto di progetto vengono gestiti in Project Service Automation e vengono sincronizzati con Finance and Operations come punti cardine delle regole di fatturazione dei contratti di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-140">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a><span data-ttu-id="332ea-141">Soluzione di integrazione di Project Service Automation con Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="332ea-141">Project Service Automation to Finance and Operations integration solution</span></span>

<span data-ttu-id="332ea-142">Il campo **ID contratto di progetto** è disponibile nella pagina **Contratti di progetto**.</span><span class="sxs-lookup"><span data-stu-id="332ea-142">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="332ea-143">Questo campo è diventato una chiave naturale e univoca per supportare l'integrazione.</span><span class="sxs-lookup"><span data-stu-id="332ea-143">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="332ea-144">Quando un nuovo contratto di progetto viene creato, se un valore di **ID contratto di progetto** non è già presente, viene generato automaticamente utilizzando una sequenza numerica.</span><span class="sxs-lookup"><span data-stu-id="332ea-144">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="332ea-145">Il valore consiste di **ORD**, seguito da una sequenza numerica crescente, quindi da un suffisso di sei caratteri.</span><span class="sxs-lookup"><span data-stu-id="332ea-145">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="332ea-146">Ecco un esempio: **ORD-01022-Z4M9Q0**.</span><span class="sxs-lookup"><span data-stu-id="332ea-146">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="332ea-147">Il campo **Numero progetto** è disponibile nella pagina **Progetti**.</span><span class="sxs-lookup"><span data-stu-id="332ea-147">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="332ea-148">Questo campo è diventato una chiave naturale e univoca per supportare l'integrazione.</span><span class="sxs-lookup"><span data-stu-id="332ea-148">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="332ea-149">Quando un nuovo progetto viene creato, se un valore per **Numero progetto** non è già presente, viene generato automaticamente utilizzando una sequenza numerica.</span><span class="sxs-lookup"><span data-stu-id="332ea-149">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="332ea-150">Il valore consiste di **PRJ**, seguito da una sequenza numerica crescente, quindi da un suffisso di sei caratteri.</span><span class="sxs-lookup"><span data-stu-id="332ea-150">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="332ea-151">Ecco un esempio: **PRJ-01049-CCNID0**.</span><span class="sxs-lookup"><span data-stu-id="332ea-151">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="332ea-152">Quando viene applicata la soluzione di integrazione di Project Service Automation con Finance and Operations<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, uno script di aggiornamento imposta il campo **ID contratto di progetto** per i contratti di progetto esistenti e il campo **Numero progetto** per i progetti esistenti in Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="332ea-152">When the Project Service Automation to Finance and Operations integration solution is applied<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="332ea-153">Prerequisiti e impostazione del mapping</span><span class="sxs-lookup"><span data-stu-id="332ea-153">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="332ea-154">Prima di eseguire la sincronizzazione di contratti di progetto e di progetti, è necessario sincronizzare gli account.</span><span class="sxs-lookup"><span data-stu-id="332ea-154">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="332ea-155">Nel set di connessioni, aggiungere il mapping di un campo chiave di integrazione per **msdyn\_organizationalunits** a **msdyn\_name \[Name\]**.</span><span class="sxs-lookup"><span data-stu-id="332ea-155">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="332ea-156">È innanzitutto necessario aggiungere un progetto al set di connessioni.</span><span class="sxs-lookup"><span data-stu-id="332ea-156">You might first have to add a project to the connection set.</span></span> <span data-ttu-id="332ea-157">Per ulteriori informazioni sulle chiavi di integrazione, vedere [Integrazione dati di Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="332ea-157">For more information about integration keys, see [Dynamics 365 Data integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span>
- <span data-ttu-id="332ea-158">Nel set di connessioni, aggiungere il mapping di un campo chiave di integrazione per **msdyn\_projects** a **msdynce\_projectnumber \[Project Number\]**.</span><span class="sxs-lookup"><span data-stu-id="332ea-158">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="332ea-159">È innanzitutto necessario aggiungere un progetto al set di connessioni.</span><span class="sxs-lookup"><span data-stu-id="332ea-159">You might first have to add a project to the connection set.</span></span> <span data-ttu-id="332ea-160">Per ulteriori informazioni sulle chiavi di integrazione, vedere [Integrazione dati di Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="332ea-160">For more information about integration keys, see [Dynamics 365 Data integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span>
- <span data-ttu-id="332ea-161">L'elemento **SourceDataID** per i contratti di progetti e i progetti può essere aggiornato su un valore diverso o essere rimosso dal mapping.</span><span class="sxs-lookup"><span data-stu-id="332ea-161">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="332ea-162">Il valore del modello predefinito è **Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="332ea-162">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="332ea-163">Il mapping di **PaymentTerms** deve essere aggiornato in modo che rifletta i termini di pagamento validi in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-163">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance and Operations.</span></span> <span data-ttu-id="332ea-164">È inoltre possibile rimuovere il mapping dall'attività di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-164">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="332ea-165">La mappa dei valori predefiniti include i valori predefiniti per i dati dimostrativi.</span><span class="sxs-lookup"><span data-stu-id="332ea-165">The default value map has default values for demo data.</span></span> <span data-ttu-id="332ea-166">Nella seguente tabella sono riportati i valori in Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="332ea-166">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="332ea-167">Valore</span><span class="sxs-lookup"><span data-stu-id="332ea-167">Value</span></span> | <span data-ttu-id="332ea-168">descrizione</span><span class="sxs-lookup"><span data-stu-id="332ea-168">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="332ea-169">1</span><span class="sxs-lookup"><span data-stu-id="332ea-169">1</span></span>     | <span data-ttu-id="332ea-170">Net 30</span><span class="sxs-lookup"><span data-stu-id="332ea-170">Net 30</span></span>        |
    | <span data-ttu-id="332ea-171">2</span><span class="sxs-lookup"><span data-stu-id="332ea-171">2</span></span>     | <span data-ttu-id="332ea-172">2%10, Net 30</span><span class="sxs-lookup"><span data-stu-id="332ea-172">2% 10, Net 30</span></span> |
    | <span data-ttu-id="332ea-173">3</span><span class="sxs-lookup"><span data-stu-id="332ea-173">3</span></span>     | <span data-ttu-id="332ea-174">Net 45</span><span class="sxs-lookup"><span data-stu-id="332ea-174">Net 45</span></span>        |
    | <span data-ttu-id="332ea-175">4</span><span class="sxs-lookup"><span data-stu-id="332ea-175">4</span></span>     | <span data-ttu-id="332ea-176">Net 60</span><span class="sxs-lookup"><span data-stu-id="332ea-176">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="332ea-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="332ea-177">Power Query</span></span>

<span data-ttu-id="332ea-178">È necessario utilizzare Microsoft Power Query per Excel per filtrare i dati se si verificano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="332ea-178">You must use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="332ea-179">Si dispone di ordini cliente in Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="332ea-179">You have sales orders in Microsoft Dynamics 365 for Sales.</span></span>
- <span data-ttu-id="332ea-180">Si dispone di più unità organizzative in Project Service Automation e queste unità verranno mappate a più persone giuridiche in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-180">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance and Operations.</span></span>

<span data-ttu-id="332ea-181">Se è necessario utilizzare Power Query, seguire queste indicazioni:</span><span class="sxs-lookup"><span data-stu-id="332ea-181">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="332ea-182">Il modello di progetti e contratti (da PSA a Fin and Ops) presenta un filtro predefinito che include solo ordini cliente del tipo **Elemento di lavoro (msdyn\_ordertype = 192350001)**.</span><span class="sxs-lookup"><span data-stu-id="332ea-182">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="332ea-183">Questo filtro assicura che non vengano creati contratti di progetto per gli ordini cliente in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-183">This filter helps guarantee that project contracts aren't created for sales orders in Finance and Operations.</span></span> <span data-ttu-id="332ea-184">Se si crea un modello personale, è necessario aggiungere questo filtro.</span><span class="sxs-lookup"><span data-stu-id="332ea-184">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="332ea-185">È necessario creare un filtro di Power Query che includa solo le organizzazioni del contratto che devono essere sincronizzate con la persona giuridica del set di connessioni di integrazione.</span><span class="sxs-lookup"><span data-stu-id="332ea-185">You must create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="332ea-186">Ad esempio, i contratti di progetto di cui si dispone con l'unità organizzativa del contratto di Contoso US devono essere sincronizzati con la persona giuridica USSI, ma i contratti di progetto di cui si dispone con l'unità organizzativa di contratto di Contoso Global devono essere sincronizzati con la persona giuridica USMF.</span><span class="sxs-lookup"><span data-stu-id="332ea-186">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="332ea-187">Se non si aggiunge questo filtro al mapping delle attività, tutti i contratti di progetto verranno sincronizzati con la persona giuridica che è definita per il set di connessioni, indipendentemente dall'unità organizzativa del contratto.</span><span class="sxs-lookup"><span data-stu-id="332ea-187">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="332ea-188">Mapping dei modelli in Integrazione dati</span><span class="sxs-lookup"><span data-stu-id="332ea-188">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="332ea-189">I campi **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** e **AddressZipCode** non vengono inclusi nel mapping predefinito per i contratti di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-189">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="332ea-190">È possibile aggiungere i mapping se è necessario che questi dati siano sincronizzati per i contratti di progetto.</span><span class="sxs-lookup"><span data-stu-id="332ea-190">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="332ea-191">I campi **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** e **ProjectType** non vengono inclusi nel mapping predefinito per i progetti.</span><span class="sxs-lookup"><span data-stu-id="332ea-191">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="332ea-192">È possibile aggiungere i mapping se è necessario che questi dati siano sincronizzati per i progetti.</span><span class="sxs-lookup"><span data-stu-id="332ea-192">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="332ea-193">Nelle figure seguenti vengono mostrati esempi dei mapping delle attività di modello in Integrazione dati.</span><span class="sxs-lookup"><span data-stu-id="332ea-193">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="332ea-194">Il mapping mostra le informazioni di campo che verranno sincronizzate da Project Service Automation a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="332ea-194">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="332ea-195">[![Mapping del modello](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="332ea-195">[![Template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="332ea-196">[![Mapping del modello](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="332ea-196">[![Template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="332ea-197">[![Mapping del modello](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="332ea-197">[![Template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="332ea-198">[![Mapping del modello](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="332ea-198">[![Template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>
