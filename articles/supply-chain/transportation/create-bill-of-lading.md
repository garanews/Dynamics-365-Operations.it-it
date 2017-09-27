---
title: Creare una polizza di carico
description: In questo argomento viene descritto come creare una polizza di carico quando si utilizzano i processi di gestione magazzino.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f3010daa41f54cf026d46b1b7648a277651173da
ms.contentlocale: it-it
ms.lasthandoff: 05/25/2017

---

# <a name="create-a-bill-of-lading"></a>Creare una polizza di carico

[!include[banner](../includes/banner.md)]


In questo argomento viene descritto come creare una polizza di carico quando si utilizzano i processi di gestione magazzino.  

La polizza di carico costituisce un documento legale tra la società che spedisce articoli e il vettore. Il documento accompagna gli articoli spediti e serve come ricevuta di spedizione quando gli articoli vengono consegnati a destinazione. Se si utilizza la gestione magazzino, sono presenti due modi per generare una polizza di carico:

  -   Creare manualmente il report, utilizzando la pagina **Polizza di carico**.
  -   Generare il report da **Workbench pianificazione carico**.

Se si genera la polizza di carico da **Workbench pianificazione carico**, lo stato del carico deve essere **Spedito**. Se sono presenti più di una spedizione nel carico, una polizza di carico viene creata per ogni spedizione. Dopo che una polizza di carico è stata creata è possibile apportarvi modifiche nella pagina **Polizza di carico**.

## <a name="master-bill-of-lading"></a>Polizza di carico generale
Se nel carico è presente più di una spedizione, è possibile generare una polizza di carico generale che ha lo stesso layout e le stesse informazioni di una polizza di carico, ma è presente il contenuto di riepilogo per tutte le spedizioni. Se l'opzione **Creare una polizza di carico generale se è presente più di una spedizione in un carico** è impostata su **Sì** nella pagina **Parametri di gestione trasporto**, una polizza di carico generale viene generata automaticamente se si crea una polizza di carico in **Workbench pianificazione carico** ed è presente più di una spedizione. È inoltre possibile ottenere un elenco delle polizze di carico facendo clic su **Informazioni correlate** &gt; **Polizza di carico**. Se si creano manualmente le polizze di carico, è possibile creare una polizza di carico generale nella pagina **Polizza di carico**.



