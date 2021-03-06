--- 
title: Elaborare giornale di registrazione allocazioni contabili
description: "Utilizzare la pagina Elabora richiesta di allocazione per creare un giornale di registrazione allocazione che è possibile rivedere e approvare prima della registrazione in contabilità generale o registrare direttamente in contabilità generale."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="process-ledger-allocation-journal"></a>Elaborare giornale di registrazione allocazioni contabili

[!include [task guide banner](../../includes/task-guide-banner.md)]

Utilizzare la pagina Elabora richiesta di allocazione per creare un giornale di registrazione allocazione che è possibile rivedere e approvare prima della registrazione in contabilità generale o registrare direttamente in contabilità generale. Prima di creare un giornale di registrazione allocazioni, è necessario che esista almeno una regola di allocazione contabile attiva. In questa attività viene utilizzata la società dimostrativa USMF.

1. Andare a Contabilità generale > Allocazioni > Elabora richiesta di allocazione.
2. Nel campo Regola fare clic sul pulsante a discesa per aprire la ricerca.
3. Trovare e selezionare il record desiderato nell'elenco.
4. Nell'elenco fare clic sul collegamento nella riga selezionata.
5. Immettere una data nel campo In data.
    * Il valore di In data è molto importante quando la contabilità generale è l'origine dati per la regola. Questa data determina quali saldi contabili includere per l'allocazione.     Nel campo Origine zero selezionare Interrompi. Questo interromperà il processo di allocazione e visualizzerà un messaggio indicante che è selezionato un importo di origine pari a zero.  
6. Nel campo Opzioni proposta, selezionare 'Solo proposta'.
    * Selezionare Solo proposta per esaminare e facoltativamente approvare il risultato nei giornali di registrazione allocazioni prima della registrazione dell'allocazione nella contabilità generale.  
7. Immettere una data nel campo Data registrazione CoGe.
8. Fare clic su OK.
9. Andare a Contabilità generale > Allocazioni > Giornali di registrazione allocazioni.
10. Fare clic su Righe.
11. Fare clic su Registra.
12. Fare clic su Registra.


