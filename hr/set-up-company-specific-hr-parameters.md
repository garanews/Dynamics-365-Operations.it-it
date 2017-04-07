---
title: "Impostare parametri HR specifici della società"
description: "Le impostazioni di alcuni parametri delle Risorse umane sono condivise tra società, mentre le impostazioni di altri parametri sono specifiche. In questo articolo viene illustrato come impostare parametri risorse umane specifici della società."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: aaf5c93a1ac71de27338c13218407616808ee001
ms.openlocfilehash: 39f2904a6b722ad0048ba1d94651098ee642079b
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Impostare parametri HR specifici della società

Le impostazioni di alcuni parametri delle Risorse umane sono condivise tra società, mentre le impostazioni di altri parametri sono specifiche. In questo articolo viene illustrato come impostare parametri risorse umane specifici della società.

Per l'impostazione dei parametri HR vengono utilizzate due pagine. Per i parametri che vengono condivisi tra le società, si utilizza la pagina **Parametri condivisi Risorse umane**. Per i parametri che sono specifici della società (vale a dire le impostazioni che si applicano a una singola società), si utilizza la pagina **Parametri Risorse umane**. Nella pagina **Parametri Risorse umane** le impostazioni sono suddivise in sei schede:

-   Generale
-   Selezione del personale
-   Retribuzione
-   Sequenze numeriche
-   Normativa per il congedo per motivi medici e familiari (FMLA)
-   Dipendente self-service

Ogni scheda contiene informazioni che si riferiscono a una singola società. Le impostazioni nella scheda **Generale** definiscono l'aspetto delle informazioni sull'assenza, gli infortuni, la malattia e le nuove assunzioni. Le impostazioni di questa scheda definiscono inoltre alcuni valori predefiniti che vengono visualizzati quando si lavora. Nello specifico, questa scheda consente di selezionare un colore da applicare alle transazioni assenze aperte, specificare il foglio di stile da utilizzare per i report, indicare se attivare l'integrazione tra corsi di formazione e registrazione delle assenze e selezionare il codice assenza utilizzato per controllare questa integrazione. È inoltre possibile indicare per quanto tempo mantenere i casi su eventi di infortunio e malattia e specificare il numero di identificazione predefinito che viene visualizzato quando viene assunto un nuovo lavoratore. 

Le impostazioni nella scheda **Selezione del personale** definiscono i tipi di documenti che vengono utilizzati per la corrispondenza che viene automaticamente inviata ai candidati e il progetto di selezione del personale che viene utilizzato per le domande di lavoro non sollecitate (le domande che non appartengono a un progetto specifico di selezione del personale). Il periodo che viene definito per l'aging del progetto di selezione determina i progetti di selezione che sono inclusi nel riquadro **Progetti di aging** nell'area di lavoro **Gestione della selezione del personale**. Il periodo che viene definito per l'avviso di scadenza della domanda di lavoro viene utilizzato per visualizzare i progetti di selezione che si avvicinano alla scadenza della domanda nel riquadro **Scadenza domanda di lavoro imminente** nell'area di lavoro **Selezione del personale**. 

Le impostazioni ** retribuzione ** della scheda definiscono se gli utenti devono confermare che desidera salvare le informazioni relative a un piano di retribuzione fissa o variabile. Se si seleziona ** attivare la convalida Salva ** la casella di controllo, qualsiasi momento che gli utenti chiudere una pagina compensazione- correlata, ricevere un messaggio in cui viene chiesto se si desidera salvare il record. In alcune finestre della gestione delle retribuzioni non permettono agli utenti di eliminare le informazioni. Di conseguenza, la richiesta agli utenti per verificare se desiderano salvare le informazioni può limitare la quantità di informazioni che vengono salvate, ma che non possono essere successivamente eliminate. Se la casella di controllo **Attivare la convalida del salvataggio** è deselezionata, i record vengono sempre salvati immediatamente, possibilmente prima che l'utente sia pronto. Se si utilizza la gestione delle prestazioni, nella scheda **Retribuzione** è possibile selezionare un modello di valutazione da utilizzare al posto di quello assegnato ai piani di retribuzione durante la valutazione delle prestazioni. 

Le impostazioni nella scheda **Sequenza numerica** determinano le sequenze che vengono utilizzate per assegnare automaticamente gli ID agli elementi in Risorse umane, ad esempio le domande di lavoro, le registrazioni delle assenze, i risultati del processo retributivo, i numeri dei casi, i corsi e le agende dei corsi. Per gestire i riferimenti e i codici delle sequenze numeriche, utilizzare ** sequenze numeriche ** la pagina elenco (** clic su Amministrazione organizzazione ** &gt; ** sequenze numeriche ** &gt; ** sequenze numeriche **). 

Le impostazioni nella scheda **FMLA** definiscono la quantità di ore che un dipendente deve svolgere per ottenere l'idoneità ai vantaggi FMLA, la durata dell'impiego che è richiesta per l'idoneità e la data di inizio dell'impiego che viene utilizzata per determinare la durata dell'impiego. Le impostazioni definiscono inoltre il numero di ore FMLA a cui i dipendenti sono autorizzati e il calendario di congedo FMLA che viene utilizzato per calcolare il numero di ore FMLA utilizzato dai dipendenti. La scheda **FMLA** è disponibile solo per le società negli Stati Uniti. 

**Nota:** il numero di ore lavorate non può superare le 1.250 ore e la durata dell'impiego non può superare i 12 mesi. Questi valori massimi sono definiti in osservanza delle normative federali negli Stati Uniti. Infine, le impostazioni nella scheda **Dipendente self-service** determinano le informazioni che un responsabile può immettere per conto dei propri dipendenti.

<a name="see-also"></a>Vedere anche
--------

[Configurare i parametri HR nelle persone giuridiche](set-up-hr-parameters-across-legal-entities.md)

