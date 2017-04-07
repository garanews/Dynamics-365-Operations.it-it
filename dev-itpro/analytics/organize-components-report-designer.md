---
title: Organizzare i componenti del report in Progettazione report
description: "Dopo aver progettato i blocchi predefiniti e generato i report, è utile organizzare questi oggetti in modo che gli utenti possano individuarli più facilmente. In questo articolo viene spiegato come organizzare i report, i blocchi predefiniti e gli oggetti esistenti in Progettazione report."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 19 - 06 - 25
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: c8efd57805cd89eb8cdfabe81a60704bb4390194
ms.lasthandoff: 03/29/2017


---

# <a name="organize-report-components-in-report-designer"></a>Organizzare i componenti del report in Progettazione report

Dopo aver progettato i blocchi predefiniti e generato i report, è utile organizzare questi oggetti in modo che gli utenti possano individuarli più facilmente. In questo articolo viene spiegato come organizzare i report, i blocchi predefiniti e gli oggetti esistenti in Progettazione report.

È possibile rinominare le cartelle, i report, i blocchi predefiniti e altri oggetti in Progettazione report per migliorare l'organizzazione dei file. A seconda del tipo di oggetto che rinominate, potrebbe essere necessario aggiornare le associazioni a tale oggetto.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Rinominare una cartella o un blocco predefinito in Progettazione report
In Progettazione report, è possibile rinominare le cartelle, le definizioni di report, le definizioni di riga, le definizioni di colonna e le definizioni di albero gerarchico. **Nota:** quando si rinomina un blocco predefinito, è necessario aggiornare le definizioni di report che utilizzano il blocco predefinito. In caso contrario, non è possibile generare un nuovo report.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Rinominare una cartella o un blocco predefinito in Progettazione report

1.  In Progettazione report, utilizzare il pannello di navigazione per individuare la cartella o l'oggetto da rinominare.
2.  Fare clic con il pulsante destro del mouse sulla cartella o sull'oggetto, quindi scegliere **Rinomina**. Il campo **Nome** nel pannello di navigazione diventa disponibile.
3.  Immettere un nuovo nome e premere Invio.
4.  Se il blocco predefinito è una definizione di riga, una definizione di colonna o una definizione di albero gerarchico, è necessario aggiornare altri blocchi predefiniti associati a esso. Fare clic con il pulsante destro del mouse sul blocco prefedinito rinominato al passaggio 3, selezionare **Associazioni** quindi selezionare un elemento nell'elenco per aggiornarlo.
5.  Ripetere il passaggio 4 fino a che tutti gli elementi associati sono aggiornati.

## <a name="create-and-manage-report-groups"></a>Creare e gestire gruppi di report
È possibile raggruppare le definizioni di report per generare più report contemporaneamente. Per creare, modificare, eliminare e generare gruppi di report, è necessario disporre del ruolo di designer o amministratore. Gli utenti con il ruolo di generatore possono generare gruppi di report e possono inoltre modificare l'impostazione delle definizioni di report dell'utente per i gruppi di report.

### <a name="create-a-report-group"></a>Creare un gruppo di report.

1.  In Progettazione report, nel pannello di navigazione, fare clic su **Gruppi di report**.
2.  ** File ** il menu, fare clic su ** nuovo ** &gt; ** la definizione del gruppo di report ** aprire un nuovo gruppo di report nella finestra del visualizzatore. In alternativa, fare clic su ** gruppo di report ** il pulsante! [Gruppo di report] (https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "gruppo di report") sulla barra degli strumenti.
3.  Fare clic sulla scheda **Gruppo di report**. Per ignorare le informazioni sulle singole definizioni di report per la generazione di questo report, selezionare la casella di controllo **Ignora impostazioni società, dettagli e data dalle singole definizioni di report**. Il nome della società, il livello di dettaglio, l'impostazione provvisoria e le informazioni sulla data vengono immessi automaticamente ma è comunque possibile effettuare aggiornamenti.
4.  Selezionare la casella di controllo **Includi tutte le valute di dichiarazione** per generare più report che mostrano tali valute. È quindi possibile accedere a più visualizzazioni facendo clic sul pulsante **Valuta** nel Visualizzatore Web quando si visualizza il report.
5.  Nel campo **Report nel gruppo**, fare clic su **Aggiungi** per selezionare i report da includere nel gruppo di report. Per selezionare più report nella finestra di dialogo **Aggiungi**, tenere premuto il tasto Ctrl mentre si seleziono i report. Una volta terminata la selezione dei report, fare clic su **OK**.
6.  Fare clic su ** file ** &gt; ** Salva ** salvare il nuovo gruppo di report.

### <a name="modify-a-report-group"></a>Modificare un gruppo di report

1.  In Progettazione report, nel pannello di navigazione, fare clic su **Gruppi di report**.
2.  Fare doppio clic sul gruppo di report da modificare.
3.  Nella scheda **Gruppo di report** apportare le modifiche desiderate.
4.  ** File ** il menu, fare clic su Salva ** ** per salvare il gruppo di report, modifica, fare clic su un'area ** Salva ** il pulsante! Salva [] (https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "")icona sulla barra degli strumenti.

**Nota:** Se è stata pianificata la generazione di report a intervalli stabiliti, è possibile ignorare tali impostazioni e generare un report immediatamente.

### <a name="generate-a-report-group-report"></a>Generare un gruppo di report

1.  In Progettazione report, nel pannello di navigazione, fare clic su **Gruppi di report**.
2.  Aprire il gruppo di report da generare.
3.  Fare clic su ** generare il report ** il pulsante! [Generare il report] (https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "generato il report") Generare i report.

### <a name="delete-a-report-group"></a>Eliminare un gruppo di report

1.  In Progettazione report, nel pannello di navigazione, fare clic su **Gruppi di report**.
2.  Fare clic con il pulsante destro del mouse sul gruppo di report da eliminare e selezionare **Elimina**.
3.  Quando viene visualizzato un messaggio di conferma, fare clic su **Sì**.

## <a name="report-group-tab-controls"></a>Controlli della scheda Gruppo di report
Nella tabella riportata di seguito viene fornita una descrizione dei controlli presenti nella scheda **Gruppo di report**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Controlla</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignora impostazioni società, dettagli e data dalle singole definizioni di report</td>
<td>Selezionare questa casella di controllo per ignorare le singole definizioni di report nel gruppo di report solo per la generazione di questi report.</td>
</tr>
<tr class="even">
<td>Nome società</td>
<td>Selezionare la società da utilizzare per i report.</td>
</tr>
<tr class="odd">
<td>Livello dettagli</td>
<td>Specificare il livello di dettaglio da includere nei report.
<ul>
<li><strong>Finanziario</strong>- Un report di riepilogo di alto livello. Non è possibile eseguire il drill-down nei conti e dimensioni, ad eccezione di quelli aggiunti tramite un albero gerarchico.</li>
<li><strong>Riepilogo finanziario &amp; Conto</strong> Report del tasso contenente un riepilogo generale e i dettagli dei conti.</li>
<li><strong>Riepilogo finanziario, conto, &amp; Transazione</strong> Report del tasso contenente un riepilogo generale e i dettagli delle transazioni.</li>
</ul></td>
</tr>
<tr class="even">
<td>Dati provvisori</td>
<td>Specificare i tipi di attività da includere nei report.
<ul>
<li><strong>Solo attività registrata</strong>- include solo le transazioni e i saldi registrati nei dati finanziari.</li>
<li><strong>Attività registrata e non registrata</strong>- include tutte le transazioni e i saldi immessi e registrati nei dati finanziari.</li>
<li><strong>Solo attività non registrata</strong>- include solo le transazioni e i saldi immessi ma non ancora registrati nei dati finanziari.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Includi tutte le valute di dichiarazione</td>
<td>Le valute di dichiarazione aggiuntive configurate nel sistema Microsoft Dynamics ERP vengono elencate qui. Selezionare questa casella di controllo per generare report aggiuntivi nelle valute indicate. Per visualizzare questi report nel Visualizzatore Web, fare clic sul pulsante <strong>Valuta</strong> e selezionare una valuta.</td>
</tr>
<tr class="even">
<td>Informazioni data non salvate con la definizione di report</td>
<td><ul>
<li>Periodo di base</li>
<li>Anno di base</li>
<li>Periodo coperto</li>
</ul>
Solo le impostazioni del periodo di base predefinito vengono salvate con la definizione di report.</td>
</tr>
<tr class="odd">
<td>Informazioni data salvate con la definizione di report</td>
<td><ul>
<li>Data report</li>
<li>Periodo di base predefinito</li>
</ul></td>
</tr>
<tr class="even">
<td>Report nel gruppo</td>
<td>Aggiungere, rimuovere e riordinare i report nel gruppo di report.
<ul>
<li>Per aggiungere definizioni di report al gruppo di report, fare doppio clic sul gruppo di report per aprirlo quindi fare clic su <strong>Aggiungi</strong>. Selezionare i report da includere nel gruppo di report, quindi fare clic su <strong>OK</strong>.</li>
<li>Per rimuovere un report dal gruppo di report, selezionarlo quindi fare clic su <strong>Rimuovi</strong>.</li>
<li>Per modificare l'ordine in cui i report vengono generati, selezionare un report nell'elenco e quindi fare clic su <strong>Sposta su</strong> o <strong>Sposta giù</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Vedere anche
--------

[Report finanziari per Microsoft Dynamics 365 per le operazioni financial-reporting-intro.md] ()

