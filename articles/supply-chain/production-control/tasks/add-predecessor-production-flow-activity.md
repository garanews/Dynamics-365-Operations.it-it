--- 
title: "Aggiungere un'attività precedente a un'attività del flusso di produzione"
description: "In una versione del flusso di produzione, tutte le attività devono essere in sequenza."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Aggiungere un'attività precedente a un'attività del flusso di produzione

[!include [task guide banner](../../includes/task-guide-banner.md)]

In una versione del flusso di produzione, tutte le attività devono essere in sequenza. Un'attività può avere una o più attività precedenti o successive. 

In questa procedura viene illustrato come associare un'attività precedente a un'attività. 

Per eseguire questa attività, è necessario disporre di un flusso di produzione con la versione bozza con almeno due attività che possono essere connesse. 

Per ulteriori informazioni, leggere il white paper sui flussi di produzione e le attività nel lean manufacturing.


## <a name="find-the-production-flow-and-version"></a>Trovare il flusso e la versione del flusso di produzione
1. Andare a Controllo produzione > Impostazioni > Flusso di produzione snella > Flussi di produzione.
2. Nell'elenco trovare e selezionare il record desiderato.
3. Nell'elenco fare clic sul collegamento nella riga selezionata.
4. Nell'elenco trovare e selezionare il record desiderato.
5. Fare clic su Attività.

## <a name="select-an-activity-and-add-a-predecessor"></a>Selezionare un'attività e aggiungere un'attività precedente
1. Nell'elenco trovare e selezionare il record desiderato.
2. Fare clic su Aggiungi attività precedente.
3. Nel campo Attività immettere o selezionare un valore.
4. Nel campo Rapporto durata ciclo immettere un numero.
    * Il rapporto di durata ciclo predefinito di una relazione tra attività è 1. Ciò presuppone che entrambe le attività vengano eseguite allo stesso ritmo o tempo di produzione di un'unità. Se l'attività precedente viene eseguita a ritmo più alto (tempo inferiore di produzione di un'unità), il rapporto deve essere inferiore a 1, se l'attività precedente viene eseguita a ritmo più lento (tempo superiore di produzione di un'unità) il rapporto durata ciclo è maggiore di 1.  
5. Fare clic su OK.


