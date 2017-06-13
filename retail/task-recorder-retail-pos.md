---
title: "Registrazione attività e Guida per il POS"
description: "In questo argomento viene descritto come usare la registrazione attività in Retail Modern POS e Cloud POS."
author: mugunthanm
manager: AnnBe
ms.date: 2017-05-15
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.reviewer: 41
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3ca86a3353d3f613057dd77754266fc69975229f
ms.contentlocale: it-it
ms.lasthandoff: 05/25/2017

---

# <a name="task-recorder-and-help-for-pos"></a>Registrazione attività e Guida per il POS

In questo argomento viene descritto come usare la registrazione attività in Retail Modern POS e Cloud POS.

<a name="overview"></a>Panoramica
--------

Registrazione attività di Retail Modern POS o Cloud POS è una soluzione nuova generata con lo stato attivo sull'alta reattività. Fornisce un'API flessibile per l'estensibilità e l'integrazione semplificata con i consumatori delle registrazioni di processi aziendali. Inoltre, l'integrazione di Registrazione attività con lo strumento Modellatore di processi aziendali in Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) è stata spostata in avanti. Di conseguenza, gli utenti possono continuare a produrre diagrammi complessi di processi aziendali dalle registrazioni per analizzare e progettare le applicazioni.

## <a name="architecture"></a>Architettura
Registrazione attività può registrare le azioni dell'utente del client con fedeltà esatta. Ogni controllo è strumentato per informare la Registrazione attività sull'esecuzione di un'azione dell'utente. Il controllo notifica alla Registrazione attività che si è verificato un evento e passa tutte le informazioni rilevanti sull'azione dell'utente corrispondente in tempo reale. In queste informazioni, la funzione Registrazione attività può acquisire il tipo di azione dell'utente (ad esempio il clic su un pulsante, l'immissione di un valore o un percorso) e tutti i dati correlati all'azione dell'utente (ad esempio il valore e il tipo di dati di input, il contesto del modulo o del record). Registrazione attività memorizza le informazioni con sufficienti dettagli per garantire che una riproduzione della registrazione può eseguire le azioni registrate esattamente come eseguite dall'utente. La funzionalità di riproduzione non è ancora stata implementata in Retail Modern POS o Cloud POS.

## <a name="basic-configuration"></a>Configurazione di base
Per attivare la registrazione attività nel POS, effettuare le operazioni seguenti.

1.  Fare clic su **Vendita al dettaglio e commercio** &gt; **Impostazione canale** &gt; **Impostazioni POS** &gt; **Registratori di cassa**.
2.  Fare clic sul registro per abilitare la registrazione attività.
3.  Nella scheda **Registra**, nella scheda dettaglio **Generale**, impostare l'opzione **Abilita registrazione attività** su **Sì**.
4.  Fare clic su **Salva**.
5.  Passare a **Vendita al dettaglio e commercio** &gt; **IT vendita al dettaglio** &gt; **Programmazione della distribuzione**.
6.  Selezionare il processo **Registri (1090)**, quindi fare clic su **Esegui ora**.

## <a name="create-a-recording"></a>Creare una registrazione
Attenersi alla procedura seguente per creare una nuova registrazione utilizzando la funzione Registrazione attività.

1.  Avviare Retail Modern POS o Cloud POS e accedere.
2.  Nella pagina **Impostazioni**, nella sezione **Registrazione attività**, scegliere **Apri registrazione attività**. Il riquadro **Registrazione attività** viene visualizzato. È possibile fare clic sul pulsante **Chiudi** (**X**) nell'angolo superiore destro per chiudere il riquadro **Registrazione attività** prima di avviare una nuova registrazione. Per riaprire il riquadro, ripetere il passaggio 2.
[![Riquadro Registrazione attività](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3.  Immettere un nome e una descrizione per la registrazione, quindi fare clic su **Avvia**. La sessione di registrazione inizia non appena si fa clic su **Avvia**. **Nota:** se si fa clic sul pulsante **Chiudi** (**X**) nell'angolo superiore destro mentre la registrazione è in corso, il riquadro **Registrazione attività** viene chiuso, ma la sessione di registrazione non viene terminata. Per riaprire il riquadro Registrazione attività, fare clic sul pulsante Guida (punto interrogativo) nella parte superiore dello schermo. 

[![Punto interrogativo](./media/help.jpg)](./media/help.jpg)

4.  Dopo aver fatto clic su **Avvia**, la funzione Registrazione attività attiva la modalità di registrazione. Nel riquadro **Registrazione attività** vengono visualizzate le informazioni e i controlli relativi al processo di registrazione.
5.  Eseguire le azioni desiderate nell'interfaccia utente di Retail Modern POS o Cloud POS.
6.  Per chiudere la sessione di registrazione fare clic su **Interrompi**.

## <a name="download-options"></a>Opzioni di download
Dopo aver chiuso la sessione di registrazione, vengono visualizzate diverse opzioni in modo da poter scaricare la registrazione. 
[![Opzioni di download](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Salva nel PC

È possibile utilizzare il pacchetto di registrazione per riprodurre una guida attività, gestire la registrazione o modificare le annotazioni della registrazione. La funzionalità non è ancora stata implementata in Retail Modern POS o Cloud POS.

### <a name="export-as-word-document"></a>Esporta come documento Word

È possibile salvare la registrazione come documento di Microsoft Word. Il documento contiene i passaggi registrati e le schermate acquisite.

### <a name="save-as-developer-recording"></a>Salva come registrazione sviluppatore

Il file di registrazione non elaborato è utile per gli scenari di sviluppo, ad esempio la generazione di codice di testing. Questa funzionalità non è stata ancora implementata.

## <a name="recording-controls"></a>Comandi di registrazione
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a>[![Comandi di registrazione](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Fine

Per chiudere la sessione di registrazione fare clic su **Interrompi**. Tenere presente che non sarà possibile riavviare la sessione dopo che è stata chiusa. Di conseguenza, verificare che la registrazione sia stata completata prima di chiuderla.

### <a name="pause"></a>Interruzione

Fare clic su **Pausa** per interrompere temporaneamente (sospendere) la sessione di registrazione e continuare l'operazione. I passaggi che vengono eseguiti dopo aver fatto clic su **Pausa** non sono registrati.

### <a name="continue"></a>Continua

Per riprendere la sessione di registrazione una volta sospesa, fare clic su **Continua**.

### <a name="capture-screenshots"></a>Acquisisci schermate

Registrazione attività può acquisire schermate dell'interfaccia utente di Retail Modern POS durante la registrazione di un processo aziendale. Registrazione attività utilizza le schermate se si scarica la registrazione come documento Word. Per attivare la funzionalità di acquisizione schermata, impostare l'opzione **Acquisisci schermate** su **Sì**. Nota: la funzionalità di acquisizione schermata non è supportata in Cloud POS.

### <a name="start-task-and-end-task"></a>Avvia attività e Termina attività

È possibile specificare l'inizio e la fine di un set di passaggi raggruppati utilizzando i pulsanti **Avvia attività** e **Termina** **attività**. Fare clic su **Avvia attività** per aggiungere un passaggio "Avvia attività" ed effettuare le operazioni che devono essere incluse nel gruppo. Una volta eseguiti i passaggi per il gruppo, fare clic su **Termina attività**. Le attività consentono di organizzare le procedure. Le attività possono essere nidificate in altre attività. In questo modo, è possibile organizzare meglio i processi aziendali lunghi e complessi.

## <a name="adding-annotations"></a>Aggiunta di annotazioni
Un'annotazione è un testo aggiuntivo che viene aggiunto a un passaggio in una registrazione. Ad esempio, è possibile utilizzare le annotazioni per fornire all'utente più contesto o istruzioni. È possibile aggiungere le annotazioni prima o dopo un passaggio. È possibile aggiungere un'annotazione a qualsiasi passaggio facendo clic sul pulsante **Modifica** (simbolo della matita) a destra del passaggio. 

[![Pulsante Modifica per un passaggio](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Testi e note

È possibile utilizzare i campi **Note** e **Testi** per aggiungere il testo che deve essere associato a un passaggio di una guida attività.
[![Campi Testo e Note](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Testo

Il testo che viene immesso nel campo **Testo** viene riportato *sopra* il testo del passaggio della guida attività. Questa posizione è appropriata per il testo che l'utente deve leggere prima di completare il passaggio.

#### <a name="notes"></a>Note

Il testo che viene immesso nel campo **Note** viene riportato *sotto* il testo del passaggio della guida attività. Per leggere il testo della nota, l'utente deve espandere il testo del passaggio nella finestra popup. Questa posizione è appropriata per il materiale facoltativo o altre informazioni che possono risultare utili all'utente, ma non necessarie per completare l'azione.

## <a name="help-at-retail-modern-pos-and-cloud-pos"></a>Guida per Retail Modern POS e Cloud POS
Per visualizzare i file di Registrazione attività personalizzati nel riquadro della Guida di Retail Modern POS e Cloud POS in modo che possano essere visualizzati come testo, è necessario salvare i file di Registrazione attività nella libreria BPM, quindi aggiornare i parametri di sistema della Guida in modo che puntino alla libreria BPM. Per ulteriori informazioni vedere [Connessione alla Guida](https://ax.help.dynamics.com/en/wiki/working-with-help/#connecting-the-help-system). La Guida di Retail Modern POS e Cloud POS esegue le ricerche in LCS in tempo reale. Cerca in tutte le raccolte BPM selezionate nei parametri di sistema della Guida di Microsoft Dynamics AX e visualizza i risultati rilevanti. Per accedere al menu **Guida**, fare clic sul pulsante **Guida** nella parte superiore della schermata, quindi digitare nella casella di ricerca il nome del processo e selezionare il pulsante di ricerca. 

[![Pulsante ?](./media/help.jpg)](./media/help.jpg) 

Quando si fa clic su una Guida attività nei risultati della ricerca, è possibile visualizzare i passaggi come argomento della Guida o esportare i passaggi in un documento Word. Nota: la Guida in Retail Modern POS e Cloud POS non porterà le guide attività automaticamente in base al modulo o alle operazioni, è necessario immettere il nome del processo nella casella di ricerca e selezionare il pulsante di ricerca per ottenere risultati.

