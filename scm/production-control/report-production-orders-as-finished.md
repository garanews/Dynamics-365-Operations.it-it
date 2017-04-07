---
title: Dichiarare finiti gli ordini di produzione
description: "Il report finita è una fase di produzione. In questa fase, un prodotto finito viene dichiarata e spostato nell&quot;ordine di produzione al magazzino."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19a777a8e58e3c8b848e878956b457a4a730f6e2
ms.lasthandoff: 03/31/2017


---

# <a name="report-production-orders-as-finished"></a>Dichiarare finiti gli ordini di produzione

Il report finita è una fase di produzione. In questa fase, un prodotto finito viene dichiarata e spostato nell'ordine di produzione al magazzino.

Quando una quantità di prodotti finiti viene dichiarata finita in un ordine di produzione, viene impostata su disponibile nel magazzino. Quantità parziali della quantità dell'ordine originariamente pianificata possono essere dichiarate finite. Quando si dichiarano finite delle quantità, è inoltre possibile dichiarare quantità di errore con una causale dell'errore associata. Quando l'ordine di produzione raggiunge la fase Dichiarato come finito significa che non vi sono più quantità da dichiarare nell'ordine di produzione.
Anche le seguenti caratteristiche vengono associate al processo **Dichiara finito**:
-   È possibile impostare il consumo di materie prime e di tempo che sono proporzionali alla quantità dichiarata (backflush)
-   Il lavoro di stoccaggio può essere generato per articoli che sono abilitati per i processi di magazzino.
-   Il valore di costo standard o pianificato dei prodotti finiti può essere configurato in modo da essere dichiarato nei conti CoGe.
-   Un ordine di controllo qualità può essere creato per la quantità dichiarata in base all'impostazione di un'associazione di controllo qualità.

La quantità viene dichiarata nell'ubicazione di uscita. Il lavoro magazzino viene quindi generato per spostare la quantità dall'ubicazione di output alla destinazione finale definita dalla direttiva di ubicazione per il lavoro di stoccaggio.

-   Un ordine di controllo qualità può essere creato quando un ordine di produzione viene dichiarato finito se è stata impostata un'associazione di controllo qualità.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Impostare un ordine di produzione su Dichiarato finito
È possibile impostare un ordine di produzione su **Dichiara finito** attraverso la funzione di aggiornamento degli ordini di produzione standard o tramite i giornali di registrazione delle schede processo o delle schede cicli di lavorazione oppure attraverso il giornale **Dichiara finito**. È inoltre possibile aggiornare la fase a **Dichiara finito** tramite le pagine Termina schede processi e Dispositivo schede processo, quando si dichiara l'ultimo processo dell'ordine di produzione. Infine, è possibile abilitare l'opzione **Dichiara finito** come processo per la soluzione del dispositivo di magazzino palmare.  

