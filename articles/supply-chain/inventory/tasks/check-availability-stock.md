--- 
title: "Controllare la disponibilità scorte"
description: Nella procedura viene illustrato come controllare le scorte disponibili e fisiche disponibili per un numero articolo specifico.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: 
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Controllare la disponibilità scorte

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nella procedura viene illustrato come controllare le scorte disponibili e fisiche disponibili per un numero articolo specifico. Viene inoltre illustrato come ottenere informazioni sulla fornitura correlate a un articolo. Le scorte fisiche disponibili sono le scorte disponibili, ovvero che sono state acquistate, ricevute e registrate. Le scorte disponibili includono le scorte disponibili, ma anche le scorte ordinate e previste, ma non ancora ricevute o registrate. È possibile eseguire questa procedura nella società di dati dimostrativi USMF oppure utilizzando i propri dati. Se si utilizza USMF è possibile utilizzare i valori di esempio visualizzati. Queste attività in genere verranno svolte da un addetto al magazzino.


## <a name="check-on-hand-inventory-for-an-item"></a>Selezionare le scorte disponibili di un articolo
1. Passare a Gestione articoli > Richieste di informazioni e report > Scorte disponibili.
2. Selezionare la riga numero articolo.
    * Per eseguire query sulle scorte disponibili per numero articolo, selezionare la riga in cui la Tabella è impostata su Scorte disponibili e il campo è impostato su Numero articolo.  
3. Nel campo Criteri selezionare l'articolo su cui si desidera eseguire una query.
    * Se si utilizza la società di dati dimostrativi USMF, è possibile selezionare 'M9201'.  
4. Fare clic su OK.
5. Fare clic su Dimensioni.
    * La scheda Dimensioni consente di selezionare la quantità di dettagli che si desidera visualizzare sulle scorte disponibili. Se sono necessari dei dati relativi alla prenotazione, è necessario visualizzare tutte le dimensioni inventariali per gli articoli che utilizzano i processi avanzati di magazzino (WHS).  
6. Fare clic su OK.
7. Nel riquadro azioni, fare clic su Informazioni correlate.
    * Se non si vedono, può essere necessario fare clic sul pulsante con i puntini di sospensione (…) per visualizzare le opzioni aggiuntive del riquadro azioni.  
8. Fare clic su Panoramica fornitura.
    * La scheda Panoramica della fornitura fornisce informazioni sulla fornitura di un articolo specifico, ad esempio la quantità disponibile, il lead time e informazioni sul fornitore.  
9. Espandere la sezione Disponibilità.
10. Espandere la sezione Fornitori.
11. Chiudere la pagina.
12. Chiudere la pagina.

## <a name="check-physical-on-hand-inventory"></a>Selezionare le scorte fisiche disponibili
1. Andare a Gestione magazzino > Richieste di informazioni e report > Scorte fisiche disponibili.
2. Nel campo Numero articolo, digitare un valore.
    * È possibile utilizzare i campi Sito e Magazzino per filtrare l'elenco di articoli.  
3. Aggiorna la pagina.
4. Fare clic su Visualizza dimensioni.
    * La scheda Visualizzazione consente di selezionare la quantità di dettagli che si desidera visualizzare sulle scorte disponibili.  
5. Fare clic su OK.
6. Chiudere la pagina.

## <a name="check-on-hand-inventory-by-location"></a>Selezionare le scorte disponibili in base all'ubicazione
1. Andare a Gestione magazzino > Richieste di informazioni e report > Disponibili per ubicazione.
2. Digitare un valore nel campo Magazzino.
    * Se si utilizza la società di dati dimostrativi USMF, è possibile utilizzare "51".  
3. Aggiorna la pagina.
4. Fare clic su Visualizza dimensioni.
5. Fare clic su OK.
6. Chiudere la pagina.


