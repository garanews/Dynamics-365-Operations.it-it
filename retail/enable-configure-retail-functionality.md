---
title: Inizializzare dati iniziali in un nuovo ambiente al dettaglio
description: In questo articolo viene descritto i dati creati durante il processo del sistema Microsoft Dynamics 365 per le operazioni al dettaglio.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Inizializzare dati iniziali in un nuovo ambiente al dettaglio

In questo articolo viene descritto i dati creati durante il processo del sistema Microsoft Dynamics 365 per le operazioni al dettaglio.

Dopo la distribuzione della soluzione di vendita al dettaglio tramite Microsoft Dynamics Lifecycle Services (LCS), è necessario inizializzare la configurazione della soluzione per creare i dati di configurazione di base. **Importante:** prima di inizializzare la configurazione di vendita al dettaglio, assicurarsi che sia specificata una lingua e un indirizzo postale per ogni persona giuridica per cui si desidera impostare i punti vendita al dettaglio. Questo passaggio deve essere completato per ogni persona giuridica che utilizza la funzionalità di vendita al dettaglio. Per inizializzare la configurazione della funzionalità di vendita al dettaglio, effettuare le operazioni indicate di seguito.

1.  Avviare Dynamics 365 per il client delle operazioni.
2.  ** Fare clic su Retail e il commercio ** &gt; ** sede Impostazioni ** &gt; ** parametri ** &gt; ** parametri ** al dettaglio.
3.  Fare clic su **Inizializza**.

L'inizializzazione crea i seguenti dati di configurazione predefiniti:

-   Processi e processi secondari di Retail Scheduler
-   Schema del canale di vendita al dettaglio
-   Programmazioni della distribuzione di vendita al dettaglio
-   Layout della schermata predefiniti, che includono griglie dei pulsanti, immagini e temi
-   Informazioni fuso orario
-   Operazioni POS
-   Autorizzazioni POS
-   Report canale
-   Metadati di attributi
-   Modelli di convalida entità
-   Processo batch per l'eliminazione dello storico della sessione di scambio dei dati commerciali

Inoltre, registrare che è correlata all'industria (PCI) della carta di pagamento è abilitato per Dynamics 365 per il database delle operazioni. **Nota:** è disponibile un'opzione per configurare separatamente Retail scheduler. Questa opzione consente di reimpostare la configurazione il dettaglio dell'utilità di pianificazione con le relative impostazioni predefinite. Dopo il completamento dell'inizializzazione, è necessario configurare i dati aggiuntivi per la dati vendita al dettaglio. Di seguito sono riportati alcuni esempi.

-   Parametri di vendita al dettaglio
-   Parametri Retail Scheduler
-   Canali di vendita al dettaglio
-   Registri e dispositivi
-   Assortimenti


