---
title: Registrare con i libri derivati
description: In questo articolo viene descritta la procedura per utilizzare i libri derivati.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 94eb82936da2a51a25105b26723088fb7dee9ae5
ms.contentlocale: it-it
ms.lasthandoff: 11/03/2017

---

# <a name="post-with-derived-books"></a>Registrare con i libri derivati

[!include [banner](../includes/banner.md)]

In questo articolo viene descritta la procedura per utilizzare i libri derivati.

Quando si registrano transazioni per un libro contenente libri derivati, le transazioni relative ai libri derivati vengono registrate automaticamente in giornali di registrazione, ordini fornitore o fatture a testo libero. Se tuttavia si preparano le transazioni del libro principale nel giornale di registrazione cespiti, sarà possibile visualizzare e modificare gli importi delle transazioni derivate prima di effettuarne la registrazione.
-   Alcuni conti, ad esempio i conti IVA o i conti cliente o fornitore, vengono aggiornati una sola volta mediante la registrazione del libro principale. Le transazioni del libro derivato vengono registrate nei conti definiti per il libro derivato nella pagina Profili registrazione cespiti.
-   L'acquisizione viene spesso utilizzata come tipo di transazione per i libri derivati. È opportuno utilizzare questa impostazione quando è necessario che il libro e il libro derivato siano applicati al cespite dal momento dell'acquisizione.
-   Per il tipo di transazione è possibile applicare anche altri valori. Ad esempio, se per il libro principale e i libri derivati sono stati impostati gli stessi intervalli relativi a vendita o dismissione, per l'impostazione di un libro derivato saranno disponibili tutti i tipi di transazione cespiti.

> [!WARNING]
> L'ammortamento registrato nel libro derivato corrisponderà all'importo registrato per il libro principale. Se i metodi di ammortamento utilizzati per i libri sono diversi, evitare di generare transazioni di ammortamento utilizzando il processo derivato. |

## <a name="example"></a>Esempio 
Di seguito viene descritto come impostare le transazioni di acquisizione con la funzionalità libro derivato.

1.  Creare i libri nella pagina Libri.
    -   Il libro per la contabilità: VM 1, livello di registrazione Corrente
    -   Libro per scopi fiscali: VM 2, livello di registrazione Imposta

2.  In VM 1 fare clic sulla scheda Libri derivati. Selezionare VM 2 nel campo Libro e Acquisizione nel campo Tipo di transazione.

I libri possono quindi essere collegati ai cespiti specifici. 

Quando si registra un'acquisizione per un cespite con il libro VM 1, la registrazione viene effettuata non solo in VM 1, ma anche nel libro derivato VM 2. Lo stato di entrambi i libri cespiti viene aggiornato in Aperto.

> [!NOTE]                                                                                                         
> Se non si utilizzano libri derivati, è necessario registrare l'acquisizione del cespite sia per il libro VM 1 sia per il libro VM 2.

Per ulteriori informazioni, vedere [Libri derivati](derived-books.md).




