---
title: "Capacità risorsa"
description: "Questo articolo fornisce informazioni sulle capacità delle risorse. Si definisce capacità l&quot;idoneità di una risorsa operativa di eseguire un&quot;attività specifica. L&quot;articolo illustra come le capacità e i concetti correlati, ad esempio il livello di competenza e priorità, vengono utilizzati per selezionare le risorse appropriate per un&quot;attività."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4463ca8e11115eb83323716faa4ed6b38937a3e4
ms.lasthandoff: 03/31/2017


---

# <a name="resource-capabilities"></a>Capacità risorsa

Questo articolo fornisce informazioni sulle capacità delle risorse. Si definisce capacità l'idoneità di una risorsa operativa di eseguire un'attività specifica. L'articolo illustra come le capacità e i concetti correlati, ad esempio il livello di competenza e priorità, vengono utilizzati per selezionare le risorse appropriate per un'attività.

Si definisce capacità l'idoneità di una risorsa operativa di eseguire un'attività specifica. È possibile assegnare più funzioni a una risorsa operativa e più risorse a una funzione. È inoltre possibile assegnare capacità a risorse in modo temporaneo, definendo una data di inizio e una di scadenza durante l'assegnazione delle capacità. Una volta che le capacità di una risorsa sono scadute, non è possibile pianificare la risorsa per un progetto o una produzione che richiede quelle capacità. È possibile rinnovare una capacità scaduta. È possibile eliminare capacità a condizione che non si trovino in una relazione ciclo di lavorazione o che non facciano parte di un ciclo di lavorazione produzione per un ordine di produzione attivo. In generale, effettuare le operazioni di eliminazione delle capacità con molta cautela. Si consiglia piuttosto di rettificare la data di scadenza delle risorse che possiedono la capacità. È possibile assegnare capacità a tutti i tipi di risorse: strumento, fornitore, computer, ubicazione, struttura o risorsa umana.

## <a name="level"></a>Livello
Più risorse spesso hanno la stessa capacità funzionale ma con livello di competenza differenti (ad esempio, forza, velocità di elaborazione o precisione). Di conseguenza, quando si assegna una capacità a una risorsa, è necessario specificare un valore per **Livello**. Il livello è un valore numerico semplice. Se si specifica che una capacità è un requisito di risorsa per un ciclo di lavorazione produzione, è possibile specificare un valore in **Livello minimo necessario** per la capacità. Il motore di programmazione quindi seleziona solo le risorse con la capacità richiesta a un livello uguale o superiore al livello minimo che è specificato nei requisiti delle risorse.

## <a name="priority"></a>Priorità
Alle risorse operative che hanno le stesse capacità è possibile assegnare una priorità. Quindi, se più risorse hanno capacità che soddisfano i requisiti di programmazione a livello richiesto e presentano capacità aperte, il motore di programmazione può scegliere tra le risorse. ** Se priorità ** è selezionato in ** selezione della risorsa primaria ** sistemi ** parametri di programmazione ** nella pagina, la risorsa con la priorità più alta (il valore numerico più basso ** priorità ** nel campo) è selezionata per prima durante la programmazione.

## <a name="resource-requirements"></a>Requisiti risorsa
Quando si definiscono i requisiti risorsa per un ciclo di lavorazione produzione, è possibile specificare una o più capacità come requisiti. Durante la programmazione della produzione, le capacità definite nei requisiti risorsa per l'operazione del ciclo di lavorazione vengono associate alle capacità definite per le risorse. Vengono quindi selezionate le risorse le cui capacità soddisfano i requisiti. Se più risorse hanno la stessa capacità funzionale ma competenze differenti (ad esempio forza, velocità di elaborazione o precisione), è possibile definire più funzionalità o utilizzare il livello di capacità per qualificare la capacità della risorsa. Ecco un esempio:

-   In un ciclo di lavorazione, il tempo di elaborazione per le perforazioni è impostato su 10 unità per ora e il requisito è definito come "Perforazione".
-   Sono presenti due perforatrici, M1 e M2.
-   La capacità "Perforazione" è assegnata a entrambe le risorse: M1 e M2.
-   La macchina M1 è in grado di perforare due unità all'ora, mentre la macchina M2 può perforarne 11 in un'ora.

In questo esempio, entrambe le macchine possono essere selezionate dal motore di programmazione in quanto entrambe soddisfano il requisito di capacità di base, "Perforazione". Tuttavia, la macchina M1 può perforare solo due unità all'ora. Poiché il tasso è molto inferiore alle 10 unità all'ora specificate nel ciclo di lavorazione, la macchina M1 causerà problemi di produzione se viene selezionata. Sono disponibili due metodi per risolvere il problema e assicurarsi che venga selezionata la macchina M2:

-   Creare due capacità separate: perforazione lenta e perforazione rapida. Definire "Perforazione lenta" con un tempo di elaborazione di perforazione compreso tra una e nove unità all'ora. Definire la capacità "Perforazione rapida" con un tempo di elaborazione di perforazione compreso tra 10 e 19 unità all'ora. Quindi assegnare alla macchina M1 la capacità lenta per le perforazioni e assegnare alla macchina M2 della capacità molto velocità di perforazione. Infine, modificare il fabbisogno di capacità della risorsa ciclo di lavorazione dalla Perforazione rapida. Il motore di programmazione selezionerà quindi la macchina corretta (in questo caso M2).
-   Utilizzare il livello di capacità per qualificare la capacità di perforazione assegnata alle perforatrici. Specifica che la macchina M1 è disponibile la capacità per le perforazioni a un livello pari a 2.0 e che la macchina M2 ha della capacità per le perforazioni a un livello pari a 11.0. Specificare quindi di 10.0 è il livello minimo necessario per il fabbisogno di capacità per le perforazioni del ciclo di lavorazione. Il motore di programmazione determinerà quindi che solo la macchina M2 soddisfa i requisiti di risorsa.

## <a name="competencies-for-human-resources"></a>Competenze per le risorse umane
Quando si dispone di risorse operative del tipo **Risorse umane** che sono collegate ai lavoratori in Risorse umane, è possibile usufruire anche delle competenze dei lavoratori quando si definiscono i requisiti delle risorse per un ciclo di lavorazione produzione. In altre parole, è possibile specificare i requisiti per specifiche competenze, corsi, certificati o titoli. Il motore di programmazione può quindi selezionare le risorse che sono collegate ai lavoratori e la selezione si basa sulle competenze dei lavoratori. Le competenze vengono impostate in Risorse umane, non nella pagina **Capacità risorsa**. Quando si definiscono le competenze, corsi, certificati, o titoli come requisiti risorsa, è necessario utilizzare la funzionalità Risorse umane e collegare ciascuna risorsa ** di Risorse umane ** digitare un lavoratore corrispondente. Se non si utilizza la funzionalità Risorse umane, è possibile definire le capacità dei ** capacità della risorsa ** impaginate che somigliano o eliminati alle competenze risorse umane. Tuttavia, la pagina **Capacità risorsa** non contiene la funzionalità richiesta per gestire le competenze, i corsi, le certificazioni o i titoli.

