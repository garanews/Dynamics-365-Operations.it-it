---
title: Impostare i parametri di Risorse umane per le persone giuridiche
description: "È necessario impostare parametri condivisi per i record condivisi tra società, ad esempio Record posizione. In questo articolo viene spiegato come impostare i parametri delle risorse umane tra persone giuridiche."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.contentlocale: it-it
ms.lasthandoff: 08/09/2018

---

# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a>Impostare i parametri di Risorse umane per le persone giuridiche

[!include [banner](includes/banner.md)]

È necessario impostare parametri condivisi per i record condivisi tra società, ad esempio Record posizione. In questo articolo viene spiegato come impostare i parametri delle risorse umane tra persone giuridiche.

Alcuni tipi di record, ad esempio i record Posizione, sono condivisi tra le società. Per questi record, è necessario configurare dei parametri condivisi. Ad esempio, è possibile utilizzare la pagina **Parametri condivisi Risorse umane** per configurare i parametri HR in tutte le persone giuridiche. 

Nella pagina **Parametri condivisi Risorse umane** i parametri sono raggruppati in aree a seconda della relativa funzionalità. 

### <a name="previously-released-functionality"></a>Funzionalità già rilasciata
Nella scheda **Identificazione** è necessario selezionare i tipi di identificazione che rappresentano i numeri di identificazione che sono elencati nella pagina. È necessario impostare i tipi di identificazione prima di immettere le informazioni di identificazione per i lavoratori. Le informazioni sul Social Security Number, il numero del documento di identità, il numero di identificativo straniero e il codice ID personale vengono gestite nella pagina **Tipo di identificazione**. Per definire un nuovo tipo di identificazione o rivedere l'elenco dei tipi esistenti, fare clic su **Gestione dipendente** &gt; **scheda Collegamenti** &gt; **Impostazioni** &gt; **Tipi di identificazione**. È possibile immettere un codice e una descrizione semplici. 

### <a name="if-youre-using-dynamics-365-for-talent"></a>Se si utilizza Dynamics 365 for Talent
Nella scheda **Identificazione** è necessario selezionare i tipi di identificazione che rappresentano i numeri di identificazione che sono elencati nella pagina. È necessario impostare i tipi di identificazione prima di immettere le informazioni di identificazione per i lavoratori. Le informazioni sul Social Security Number, il numero del documento di identità, il numero di identificativo straniero e il codice ID personale vengono gestite nella pagina **Tipo di identificazione**. Per definire un nuovo tipo di identificazione o rivedere l'elenco dei tipi esistenti, fare clic su su **Risorse umane** &gt; **Impostazione** &gt; **Tipi di identificazione**. È possibile immettere un codice e una descrizione semplici. 

Nella scheda **Sequenze numeriche** è possibile selezionare le sequenze numeriche che sono utilizzate per i seguenti record: Numero dipendente, Posizione, ID richiesta utente, Documento I-9, Candidato, Discussione, ID benefit e Azione dipendente (se questo tipo di record è attivato). Per gestire i codici e i riferimenti delle sequenze numeriche, utilizzare la pagina elenco **Sequenze numeriche**. Per trovare questa pagina, utilizzare la funzionalità di ricerca della pagina. 

Nella scheda **Posizioni** indicare se per impostazione predefinita sono disponibili nuove posizioni da assegnare:

-   **Sempre**: è possibile assegnare lavoratori a nuove posizioni quando si creano posizioni. Quando vengono create posizioni, la data e l'ora **Disponibile per l'assegnazione** nella scheda **Generale** della pagina **Posizione** vengono impostate automaticamente sulla data e ora di creazione.
-   **Mai**: non è possibile assegnare lavoratori a nuove posizioni quando si creano posizioni. Se si seleziona questa opzione, è necessario aprire la pagina **Posizione** per ciascuna nuova posizione nel momento in cui diventa disponibile e, successivamente, nella scheda **Generale**, immettere la data di **Disponibile per l'assegnazione** per consentire l'assegnazione ai lavoratori.


<a name="additional-resources"></a>Risorse aggiuntive
--------

[Impostare parametri HR specifici della società](set-up-company-specific-hr-parameters.md)




