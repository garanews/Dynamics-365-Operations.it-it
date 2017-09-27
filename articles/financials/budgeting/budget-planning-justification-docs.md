---
title: Documenti di motivazione per la pianificazione del budget
description: "I documenti di motivazione forniscono una descrizione per chi richiede un budget per spiegare perché un budget specifico è necessario."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1d23c0e1725a39d25d2be8971f541b2c31bbe859
ms.contentlocale: it-it
ms.lasthandoff: 06/13/2017

---

# <a name="budget-planning-justification-documents"></a>Documenti di motivazione per la pianificazione del budget

[!include[banner](../includes/banner.md)]


I documenti di motivazione forniscono una descrizione per chi richiede un budget per spiegare perché un budget specifico è necessario. 

Un modello di piano di budget viene creato dal responsabile budget in Microsoft Word e viene assegnato al processo di pianificazione del budget corrente. I proprietari del budget potranno quindi aprire il modello e i dati verranno inseriti automaticamente in Word in base alla relativa richiesta di budget. I proprietari possono quindi aggiungere testo o dati aggiuntivi prima di salvare e allegare il proprio documento di motivazione personale al piano di budget.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Impostare il componente aggiuntivo di Microsoft Dynamics Office per Microsoft Word

1.  Aprire un nuovo documento di Microsoft Word.
2.  Fare clic su **Inserisci** sulla barra multifunzione e fare clic su **Punto vendita**.
3.  Ricerca di un componente aggiuntivo di Microsoft Dynamics Office e fare clic su **Aggiungi**.
4.  In Word, nel riquadro destro, fare clic su **Aggiungi informazioni sul server**.
5.  Digitare o incollare l'URL del server e fare clic su **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definire il modello Motivazione in Microsoft Word

1.  Fare clic su **Progetto** nel componente aggiuntivo di Office di Microsoft Dynamics Office dopo aver effettuato l'accesso.
2.  Per informazioni sull'intestazione, utilizzare il pulsante **Aggiungi campi**.
3.  Selezionare l'origine dati dell'entità di BudgetPlanJustification, quindi fare clic su **Avanti**. **Nota:** l'entità è necessaria per qualsiasi documento di motivazione. È possibile utilizzare altre entità ma il caricamento di nuovo su Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition avrà esito negativo se questa entità non verrà inclusa.
4.  Aggiungere i valori e le etichette BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter e DocumentNumber nel documento Word. **Nota:** è possibile utilizzare le proprie etichette personalizzate anziché le etichette standard, se necessario.
5.  Fare clic su **Fine** per completare la sezione dell'intestazione.
6.  Per il dettaglio del livello di riga degli importi del piano di budget, fare clic su **Aggiungi tabella**.
7.  Di nuovo, selezionare l'origine dati dell'entità di BudgetPlanJustification, quindi fare clic su **Avanti**.
8.  Aggiungere i campi per EffectiveDate, ScenarioName, AccountDisplayValue e AccountingCurrencyExpenseAmount. **Nota:** se è possibile aggiungere commenti all'interno di singole righe del piano di budget, questi possono essere aggiunti alla tabella corrispondente.
9.  Aggiungere eventuali istruzioni aggiuntive da fornire all'utente finale ed eseguire eventuali formattazioni necessarie o modifiche allo stile del documento.
10. Salvare il documento sul computer locale e chiudere il file prima di continuare.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Configurare il processo di pianificazione del budget per utilizzare per il modello Motivazione

1.  In Finance and Operations, passare a **Impostazione budget** &gt; **Impostazioni** &gt; **Pianificazione del budget** &gt; **Modelli documento di motivazione**.
2.  Fare clic su **Nuovo** e individuare il documento di Microsoft Word appena creato.
3.  Immettere un nome di visualizzazione e una descrizione del modello. Fare clic su **OK**.
4.  Accedere a **Impostazione budget** &gt; **Impostazioni** &gt; **Pianificazione** del **budget** &gt; **Processo di pianificazione del budget**.
5.  Selezionare il processo in cui il modello di motivazione deve essere utilizzato e fare clic su **Modifica**.
6.  Nel campo **Modello documento di motivazione**, selezionare il modello appropriato e salvare.

##### <a name="edit-and-save-personalized-justification-documents"></a>Modificare e salvare documenti di motivazione personalizzati

1.  In Finance and Operations, creare un nuovo piano di budget o aprire un piano di budget esistente.
2.  Dal menu a discesa **Motivazione**, selezionare **Crea nuova motivazione**.
3.  Dopo aver inserito i dettagli, selezionare per caricare il documento personalizzato dal menu a discesa **Motivazione**.




