---
title: Configurare i parametri HR nelle persone giuridiche
description: "È necessario impostare parametri condivisi per i record condivisi tra società, ad esempio Record posizione. In questo articolo viene spiegato come impostare i parametri delle risorse umane tra persone giuridiche."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: 5df6079605d2d8d320c38d302e8e5e2cba51a3f1
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>Configurare i parametri HR nelle persone giuridiche

È necessario impostare parametri condivisi per i record condivisi tra società, ad esempio Record posizione. In questo articolo viene spiegato come impostare i parametri delle risorse umane tra persone giuridiche.

Alcuni tipi di record, ad esempio i record Posizione, sono condivisi tra le società. Per questi record, è necessario configurare dei parametri condivisi. Ad esempio, è possibile utilizzare la pagina **Parametri condivisi Risorse umane** per configurare i parametri HR in tutte le persone giuridiche. 

Nella pagina **Parametri condivisi Risorse umane** i parametri sono raggruppati in aree a seconda della relativa funzionalità. 

Nella scheda **Identificazione** è necessario selezionare i tipi di identificazione che rappresentano i numeri di identificazione che sono elencati nella pagina. È necessario impostare i tipi di identificazione prima di immettere le informazioni di identificazione per i lavoratori. Le informazioni sul Social Security Number, il numero del documento di identità, il numero di identificativo straniero e il codice ID personale vengono gestite nella pagina **Tipo di identificazione**. Per definire un nuovo ID digitare o esaminare l'elenco dei tipi esistenti, fare clic su ** Risorse umane ** &gt; ** impostazione ** &gt; ** tipi di identificazione **. È possibile immettere un codice e una descrizione semplici. 

Nella scheda **Sequenze numeriche** è possibile selezionare le sequenze numeriche che sono utilizzate per i seguenti record: Numero dipendente, Posizione, ID richiesta utente, Documento I-9, Candidato, Discussione, ID benefit e Azione dipendente (se questo tipo di record è attivato). Per gestire i codici e i riferimenti delle sequenze numeriche, utilizzare la pagina elenco **Sequenze numeriche**. Per trovare questa pagina, utilizzare la funzionalità di ricerca della pagina. 

Nella scheda **Posizioni** indicare se per impostazione predefinita sono disponibili nuove posizioni da assegnare:

-   ** ** - È possibile assegnare sempre i lavoratori alle nuove ubicazioni quando vengono create posizioni. Quando vengono create posizioni, ** disponibile per l'assegnazione ** la data e l'ora ** dettagli relativi all'identificazione ** nella scheda ** ** posizione della pagina vengono impostate automaticamente alla data e all'ora di creazione.
-   **Mai**: non è possibile assegnare lavoratori a nuove posizioni quando si creano posizioni. Se si seleziona questa opzione, è necessario aprire la pagina **Posizione** per ciascuna nuova posizione nel momento in cui diventa disponibile e, successivamente, nella scheda **Generale**, immettere la data di **Disponibile per l'assegnazione **per consentire l'assegnazione ai lavoratori.


<a name="see-also"></a>Vedere anche
--------

[] Parametri specifici di HR Società di attrezzaggio setup-company-specific-hr-parameters.md)

