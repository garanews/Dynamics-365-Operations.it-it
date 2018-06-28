---
title: Origini dati interaziendali nella creazione di report elettronici
description: In questo argomento viene descritto come utilizzare le origini dati interaziendali nella creazione di report elettronici (ER).
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 7f0f78d15e99397d61c3abace197cf1281d3769f
ms.contentlocale: it-it
ms.lasthandoff: 05/25/2018

---

# <a name="cross-company-data-sources-in-electronic-reporting"></a><span data-ttu-id="266b9-103">Origini dati interaziendali nella creazione di report elettronici</span><span class="sxs-lookup"><span data-stu-id="266b9-103">Cross-company data sources in Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="266b9-104">È possibile progettare formati di report elettronici (ER) per generare documenti in uscita in vari formati.</span><span class="sxs-lookup"><span data-stu-id="266b9-104">You can design Electronic reporting (ER) formats to generate outgoing documents in various formats.</span></span> <span data-ttu-id="266b9-105">Quando viene generato un documento, un formato di ER chiama le origini dati che sono state configurate in un mapping di modelli di ER corrispondente.</span><span class="sxs-lookup"><span data-stu-id="266b9-105">When a document is generated, an ER format calls data sources that were configured in a corresponding ER model mapping.</span></span> <span data-ttu-id="266b9-106">Per configurare l'accesso alle tabelle dell'applicazione per il recupero di record, è possibile utilizzare le origini dati di ER di tipo **Record di tabella**.</span><span class="sxs-lookup"><span data-stu-id="266b9-106">To configure access to application tables for record retrieval, you can use ER data sources of the **Table records** type.</span></span> <span data-ttu-id="266b9-107">Quando la tabella cui di deve accedere è condivisa (vale a dire una tabella in cui i dati sono salvati senza un identificatore della società), questa origine dati restituisce tutti i record.</span><span class="sxs-lookup"><span data-stu-id="266b9-107">When the accessing table is a shared table (that is, a table where data is saved without a company identifier), this data source returns all records.</span></span> <span data-ttu-id="266b9-108">Quando la tabella di accesso è una tabella dipendente dalla società (vale a dire una tabella in cui i dati vengono salvati per società), l'origine dati restituisce solo i record che sono stati salvati per la società corrente (vale a dire il contesto aziendale in cui viene eseguito il formato di ER).</span><span class="sxs-lookup"><span data-stu-id="266b9-108">When the accessing table is a company-dependent table (that is, a table where data is saved per company), this data source returns only the records that have been saved for the current company (that is, the company context that the ER format is running under).</span></span>

<span data-ttu-id="266b9-109">Ogni origine dati di tipo **Record di tabella** in un mapping di modello può a questo punto essere contrassegnata come origine dati interaziendale.</span><span class="sxs-lookup"><span data-stu-id="266b9-109">Every data source of the **Table records** type in a model mapping can be now marked as a cross-company data source.</span></span> <span data-ttu-id="266b9-110">Si può quindi utilizzare le origini dati di tipo **Record di tabella** per accedere ai dati interaziendali nelle tabelle dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="266b9-110">Therefore, you can use data sources of the **Table records** type to access cross-company data in application tables.</span></span> 

<span data-ttu-id="266b9-111">Se si contrassegna un'origine dati come interaziendale, si verifica il comportamento seguente:</span><span class="sxs-lookup"><span data-stu-id="266b9-111">If you mark a data source as cross-company, the following behavior occurs:</span></span>

- <span data-ttu-id="266b9-112">Per un'origine dati che fa riferimento a una qualsiasi tabella condivisa eccetto CompanyInfo, l'origine dati restituisce tutti i record presenti nella tabella di riferimento.</span><span class="sxs-lookup"><span data-stu-id="266b9-112">For a data source that refers to any shared table except CompanyInfo, the data source returns all records that exist in the referenced table.</span></span> 
- <span data-ttu-id="266b9-113">Per un'origine dati che fa riferimento alla tabella CompanyInfo, anche se CompanyInfo è una tabella condivisa, l'origine dati restituisce i record contenenti l'identificatore di una società dall'ambito definito.</span><span class="sxs-lookup"><span data-stu-id="266b9-113">For a data source that refers to the CompanyInfo table, even though CompanyInfo is a shared table, the data source returns the records that contain the identifier of a company from the defined scope.</span></span>
- <span data-ttu-id="266b9-114">Per qualsiasi tabella dipendente dalla società, l'origine dati restituisce i record della tabella di riferimento che contengono l'identificatore di una società dall'ambito definito.</span><span class="sxs-lookup"><span data-stu-id="266b9-114">For any company-dependent table, the data source returns the records of the referenced table that contain the identifier of a company from the defined scope.</span></span>

<span data-ttu-id="266b9-115">Nella finestra di dialogo delle query di sistema, quando l'opzione **Chiedi query** è attivata per una qualsiasi origine dati che è contrassegnata come interaziendale, è possibile selezionare manualmente una o più società da includere nella scheda **Intervallo società**.</span><span class="sxs-lookup"><span data-stu-id="266b9-115">In the system query dialog box, when the **Ask for query** option is turned on for any data source that is marked as cross-company, you can manually select one or more companies to include on the **Company range** tab.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="266b9-116">Come altri filtri, il filtro dalla società è persistente come valore utilizzato per ultimo per le query quando si esegue un formato di ER.</span><span class="sxs-lookup"><span data-stu-id="266b9-116">Like other filters, the company filter is persisted as a last-used value for queries when you run an ER format.</span></span> <span data-ttu-id="266b9-117">Il filtro non cambia automaticamente se si modifica il valore interaziendale per un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="266b9-117">The filter isn't automatically changed if you change the cross-company value for a data source.</span></span> <span data-ttu-id="266b9-118">Per utilizzare un valore interaziendale diverso per un'altra origine dati, eliminare la selezione specifica dell'utente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="266b9-118">To use a different cross-company value for another data source, delete the corresponding user-specific selection.</span></span>

<span data-ttu-id="266b9-119">Per ogni origine dati contrassegnata come interaziendale, è possibile selezionare i record desiderati utilizzando le funzioni **FILTER** e **WHERE** nelle espressioni di ER.</span><span class="sxs-lookup"><span data-stu-id="266b9-119">For every data source that is marked as cross-company, you can select the records that you want by using the **FILTER** and **WHERE** functions in ER expressions.</span></span> <span data-ttu-id="266b9-120">Anche il campo **dataAreaID** viene utilizzato come identificatore di società.</span><span class="sxs-lookup"><span data-stu-id="266b9-120">The **dataAreaID** field can also be used as a company identifier.</span></span> <span data-ttu-id="266b9-121">Attualmente, il campo **dataAreaID** è limitato ai seguenti tipi di condizioni quando viene utilizzata la funzione **FILTER**:</span><span class="sxs-lookup"><span data-stu-id="266b9-121">Currently, the **dataAreaID** field is limited to the following types of conditions when the **FILTER** function is used:</span></span> 

- <span data-ttu-id="266b9-122">Sono supportate solo le condizioni che hanno un singolo confronto del campo **dataAreaID**.</span><span class="sxs-lookup"><span data-stu-id="266b9-122">Only conditions that have a single **dataAreaID** field comparison are supported.</span></span>
- <span data-ttu-id="266b9-123">Sono consentiti solo i confronti con espressioni che non dipendono da elementi dell'elenco di record.</span><span class="sxs-lookup"><span data-stu-id="266b9-123">Only comparisons that have expressions that don't depend on records list items are allowed.</span></span>

<span data-ttu-id="266b9-124">L'espressione seguente è pertanto valida.</span><span class="sxs-lookup"><span data-stu-id="266b9-124">Therefore, the following expression is valid.</span></span>

    FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
    While shown below expressions will not pass the validation:
    FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
    FILTER (MyTable, 
        OR(
            MyTable.dataAreaID = $StringUserInputParameter1,
            MyTable.dataAreaID = $StringUserInputParameter2
        )
    )

<span data-ttu-id="266b9-125">Per impostazione predefinita, l'ambito include tutte le società dell'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="266b9-125">By default, the scope includes all companies of the current application.</span></span> <span data-ttu-id="266b9-126">Tuttavia, è possibile limitarlo.</span><span class="sxs-lookup"><span data-stu-id="266b9-126">However, it can be restricted.</span></span> <span data-ttu-id="266b9-127">Per limitare l'ambito di accesso ai dati interaziendali per un formato di ER, assegnare una gerarchia organizzativa specifica al formato.</span><span class="sxs-lookup"><span data-stu-id="266b9-127">To restrict the scope of cross-company data access for a single ER format, assign a specific organization hierarchy to the format.</span></span> <span data-ttu-id="266b9-128">Quando una gerarchia viene definita per un formato di ER, vengono restituiti solo i record per le persone giuridiche presentate nella gerarchia assegnata, anche se il formato chiama origini dati interaziendali.</span><span class="sxs-lookup"><span data-stu-id="266b9-128">When a hierarchy is defined for an ER format, only records for legal entities that are presented in the assigned hierarchy are returned, even though the format calls cross-company data sources.</span></span> <span data-ttu-id="266b9-129">Quando si definisce un riferimento a una gerarchia non più disponibile per un formato di ER, viene applicato l'ambito predefinito e il formato chiama origini dati interaziendali.</span><span class="sxs-lookup"><span data-stu-id="266b9-129">When a reference to a hierarchy that no longer exists is defined for an ER format, the default scope is applied, and the format calls cross-company data sources.</span></span> <span data-ttu-id="266b9-130">In questo caso, vengono restituiti i record di tutte le società dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="266b9-130">In this situation, records for all application companies are returned.</span></span> 

<span data-ttu-id="266b9-131">Quando l'opzione **Usa bozza** viene attivata per una gerarchia organizzativa assegnata a un singolo formato di ER, le persone giuridiche dalla versione bozza di questa gerarchia verranno utilizzate per identificare l'ambito per le origini dati interaziendali.</span><span class="sxs-lookup"><span data-stu-id="266b9-131">Note that when the **Use draft** option is turned on for the assigned to a single ER format organization hierarchy, the legal entities from the draft version of this hierarchy will be used to identify the scope for cross-company data sources.</span></span> <span data-ttu-id="266b9-132">Se la versione bozza non è disponibile, verranno utilizzate le persone giuridiche dell'ultima versione pubblicata della gerarchia organizzativa.</span><span class="sxs-lookup"><span data-stu-id="266b9-132">If the draft version does not exist, the legal entities from the last published version of this organization hierarchy will be used for this.</span></span>

<span data-ttu-id="266b9-133">Quando l'opzione **Usa bozza** viene disattivata per una gerarchia organizzativa assegnata a un singolo formato di ER, le persone giuridiche dall'ultima versione pubblicata di questa gerarchia organizzativa verranno utilizzate per identificare l'ambito per le origini dati interaziendali.</span><span class="sxs-lookup"><span data-stu-id="266b9-133">Note that when the **Use draft** option is turned off for the assigned to a single ER format organization hierarchy, the legal entities from the last published version of this organization hierarchy will be used to identify the scope for cross-company data sources.</span></span> <span data-ttu-id="266b9-134">La validità delle date per le gerarchie organizzative non è ancora supportata nel framework di ER.</span><span class="sxs-lookup"><span data-stu-id="266b9-134">Date effectiveness of organization hierarchies is not supported yet in the ER framework.</span></span>

<span data-ttu-id="266b9-135">La gerarchia può essere assegnata a un formato in una pagina specifica a cui è possibile accedere dall'area di lavoro di ER o scegliendo **Amministrazione organizzazione -> Creazione di report elettronici -> Filtro persona giuridica per i formati**.</span><span class="sxs-lookup"><span data-stu-id="266b9-135">The hierarchy can be assigned to a format in a specific page that can be accessed from the ER workspace or by using the **Organization administration -> Electronic reporting -> Legal entity filter for formats** menu item.</span></span> <span data-ttu-id="266b9-136">Per accedere alla pagina, all'utente deve essere concesso il privilegio **Mantieni filtri persona giuridica per i formati** (ERMaintainFormatMappingLegalEntityFilters).</span><span class="sxs-lookup"><span data-stu-id="266b9-136">To access the page, the **Maintain legal entity filters for format** privilege (ERMaintainFormatMappingLegalEntityFilters) must be granted to a user.</span></span> <span data-ttu-id="266b9-137">La restrizione dell'ambito delle persone giuridiche basate sulla gerarchia per il formato viene applicata insieme alla restrizione che l'utente può specificare manualmente nella finestra di dialogo di query del sistema.</span><span class="sxs-lookup"><span data-stu-id="266b9-137">The scope restriction of hierarchy-based legal entities for the format is applied in addition to the restriction that the user can manually specify in the system query dialog box.</span></span> <span data-ttu-id="266b9-138">L'intersezione di queste restrizioni viene utilizzata quando il formato viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="266b9-138">The intersection of these restrictions is used when the format is run.</span></span>

<span data-ttu-id="266b9-139">Per ulteriori informazioni su questa funzionalità, riprodurre la guida attività **ER Accedere ai record di tabelle dipendenti dalla società nella modalità interaziendale**, che fa parte del processo aziendale 7.5.4.3 Acquisire/sviluppare componenti di soluzioni/servizi IT (10677) e che può essere scaricata dall'[Area download Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="266b9-139">To learn more about this feature, play the task guide, **ER Access records of company dependent tables in cross-company mode**, which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process, and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="266b9-140">Questa guida attività illustra in dettaglio il processo di configurazione di un mapping di modello di ER e il formato ER per accedere alle tabelle dell'applicazione nella modalità interaziendale.</span><span class="sxs-lookup"><span data-stu-id="266b9-140">This task guide walks you through the process of configuring an ER model mapping and ER format to access application tables in cross-company mode.</span></span>

<span data-ttu-id="266b9-141">Scaricare i seguenti file per completare la guida attività:</span><span class="sxs-lookup"><span data-stu-id="266b9-141">Download the following files to complete the task guide:</span></span>

- [<span data-ttu-id="266b9-142">Configurazione del modello di ER - CrossCompanyDataAccessModel.xml</span><span class="sxs-lookup"><span data-stu-id="266b9-142">ER model configuration - CrossCompanyDataAccessModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="266b9-143">Configurazione del formato di ER - CrossCompanyDataAccessFormat.xml</span><span class="sxs-lookup"><span data-stu-id="266b9-143">ER format configuration - CrossCompanyDataAccessFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
