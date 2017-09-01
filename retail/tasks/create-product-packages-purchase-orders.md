--- 
title: " Creare i colli prodotto per gli ordini fornitore"
description: In questa procedura vengono descritti i passaggi per creare un collo di prodotti e utilizzarlo in un ordine fornitore.
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 695460415f81d65ec35eeee60209358b722c9244
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="create-product-packages-for-purchase-orders"></a> Creare i colli prodotto per gli ordini fornitore

[!include[task guide banner](../includes/task-guide-banner.md)]

In questa procedura vengono descritti i passaggi per creare un collo di prodotti e utilizzarlo in un ordine fornitore. L'ordine fornitore verrà utilizzato per creare un ordine per un set predefinito di prodotti. Questa procedura utilizza la società di dati dimostrativi USRT.


## <a name="create-a-product-package"></a>Creare un collo di prodotti
1. Passare a Vendita al dettaglio e commercio > Gestione inventario > Rifornimento > Colli prodotti.
2. Fare clic su Nuovo.
3. Nel campo Numero collo, digitare un valore.
4. Nel campo Descrizione digitare un valore.
5. Nel campo Conto fornitore fare clic sul pulsante a discesa per aprire la ricerca.
6. Nell'elenco fare clic sul collegamento nella riga selezionata.
7. Scegliere Aggiungi.
8. Nel campo Numero articolo digitare '0160'.
9. Nel campo Dimensione fare clic sul pulsante a discesa per aprire la ricerca.
10. Nell'elenco fare clic sul collegamento nella riga selezionata.
11. Nel campo Quantità immettere un numero.
12. Scegliere Aggiungi.
13. Nel campo Numero articolo digitare '0160'.
14. Nel campo Numero variante fare clic sul pulsante a discesa per aprire la ricerca.
15. Nell'elenco fare clic sul collegamento nella riga selezionata.
16. Nel campo Quantità immettere un numero.
17. Scegliere Aggiungi.
18. Nel campo Numero articolo digitare '0175'.
19. Nel campo Quantità immettere un numero.
20. Fare clic su Salva.
21. Chiudere la pagina.

## <a name="add-package-to-puchase-order"></a>Aggiungere il collo all'ordine fornitore
1. Fare clic su Contabilità fornitori > Ordini fornitore > Tutti gli ordini fornitore.
2. Fare clic su Nuovo.
3. Nel campo Conto fornitore fare clic sul pulsante a discesa per aprire la ricerca.
4. Nell'elenco, selezionare lo stesso fornitore per cui è stato creato il collo di prodotti in precedenza, se un fornitore è stato selezionato.
5. Attivare/disattivare l'espansione della sezione Generale.
6. Nel campo Sito fare clic sul pulsante a discesa per aprire la ricerca.
7. Nell'elenco fare clic sul collegamento nella riga selezionata.
8. Nel campo Magazzino fare clic sul pulsante a discesa per aprire la ricerca.
9. Nell'elenco fare clic sul collegamento nella riga selezionata.
10. Fare clic su OK.
11. Attivare/disattivare l'espansione della sezione Dettagli riga.
12. Fare clic sulla scheda Colli prodotti.
13. Fare clic su Riga ordine fornitore.
14. Fare clic su Crea righe da collo.
15. Nell'elenco, individuare e selezionare il collo di prodotti creato nel passaggio precedente.
16. Nel campo Quantità immettere un numero.
17. Fare clic su Crea.
18. Fare clic su Salva.

