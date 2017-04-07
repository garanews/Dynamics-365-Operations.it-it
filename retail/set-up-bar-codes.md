---
title: Impostare codici a barre
description: In questo articolo viene descritto come utilizzare i codici a barre in Microsoft Dynamics 365 per le operazioni al dettaglio.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 7734a08756f5b737744f9c8ce1d358be020b859f
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-codes"></a>Impostare codici a barre

In questo articolo viene descritto come utilizzare i codici a barre in Microsoft Dynamics 365 per le operazioni al dettaglio.

È possibile utilizzare i codici a barre per acquistare o vendere prodotti, tenere traccia delle varianti prodotto e impostare clienti e dipendenti. È inoltre possibile utilizzare i codici a barre per emettere e approvare buoni sconto, gift card e note di credito. È possibile impostare prodotti al dettaglio in modo che abbiano codici a barre standard o interni personalizzati. I prodotti possono avere più di un codice a barre. Ad esempio, un prodotto può avere più codici a barre se il prodotto proviene da diversi produttori o se dispone di varianti in base a dimensioni, stile o colore. I codici a barre possono includere il peso o il prezzo del prodotto. Le maschere codice a barre sono modelli utilizzati per creare codici a barre. **Nota:** l'assegnazione di un codice a barre univoco a ogni combinazione di varianti consente di eseguire la scansione del codice a barre nel registratore di cassa e individuare automaticamente la variante del prodotto venduta. È anche possibile raccogliere e visualizzare statistiche delle vendite a livello di varianti. A ogni gruppo di dimensioni, colori e stili può essere assegnato un numero univoco che lo identifica nel codice a barre. Dynamics 365 per le operazioni maschera codice a barre viene utilizzata per generare automaticamente i codici a barre a ogni combinazione di varianti. Tale funzionalità può essere utile in presenza di un gran numero di dimensioni, colori e stili poiché le combinazioni aumentano in modo significativo con ogni codice di variante aggiunto. Se non si utilizza questa funzionalità, è necessario assegnare manualmente i codici a barre a ogni combinazione che rappresenta una variante di prodotto. È possibile creare i codici a barre manualmente o automaticamente. Per creare i codici a barre, completare le seguenti attività nell'ordine in cui sono elencate.

1.  [] Caratteri maschera codice a barre di attrezzaggio setup-bar-code-masks.md).
2.  [] Maschere dei codici a barre Impostazioni (setup-bar-code-masks.md).
3.  Configurare le impostazioni dei codici a barre.
4.  Creare codici a barre per prodotti.


<a name="see-also"></a>Vedere anche
--------

[Impostare le maschere codice a barre](set-up-bar-code-masks.md)

