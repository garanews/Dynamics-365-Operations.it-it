---
title: Data di competenza per le transazioni
description: "In questo argomento vengono fornite informazioni sulla data di competenza e illustra come attivare la funzionalità per le transazioni in Italia."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264534
ms.search.region: Italy
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 07d09512ef612b41bf527b74496fa440f23851fc
ms.openlocfilehash: feb88b88ad9cb65b8404ad68a25993bea9f41cdf
ms.contentlocale: it-it
ms.lasthandoff: 02/14/2018

---

# <a name="competence-date-for-transactions"></a>Data di competenza per le transazioni

[!include [banner](../includes/banner.md)]

In questo argomento vengono fornite informazioni sulla data di competenza e illustra come attivare la funzionalità per le transazioni in Italia.

In Italia, le società devono utilizzare una data di registrazione per registrare le transazioni. La data di registrazione è la data in cui la società conferma la transazione. Le transazioni di chiusura e rettifica possono essere effettuate diversi mesi dopo l'ultimo giorno dell'anno fiscale. In genere, queste transazioni vengono effettuate alla data in cui lo stato patrimoniale viene approvato dal Consiglio di Amministrazione. Queste transazioni devono essere dichiarate nel giornale di registrazione fiscale italiano alla data in cui vengono registrate, ma devono disporre di un riferimento alla data di competenza. Due sono pertanto le date richieste:

-   La data di competenza, che rappresenta la data in cui la transazione influisce sull'importo del saldo
-   La data di registrazione, che è la data in cui l'utente registra la transazione

**Esempio:** l'anno fiscale della società inizia l'1 gennaio e termina il 31 dicembre. Lo stato patrimoniale viene approvato il 15 aprile. Di conseguenza, le transazioni di chiusura e rettifica vengono dichiarate nel giornale di registrazione fiscale italiano ad aprile, ma influiscono sul saldo al 31 dicembre.

## <a name="enable-the-competence-date"></a>Attivare la data di competenza
Per attivare questa funzionalità per le transazioni, nella pagina **Parametri di contabilità generale**, nella scheda **Contabilità generale**, impostare l'opzione **Riferimento alla data competenza nella data della transazione** su **Sì**. Dopo aver attivato la data di competenza, è possibile specificare le date di competenza e delle transazioni per ogni giornale di registrazione utilizzato per registrare le transazioni di rettifica e di chiusura/apertura per l'anno fiscale:

-   Giornale di registrazione generale
-   Giornale di registrazione cespiti
-   Riconciliazione estratti conto
-   Bilancio di chiusura
-   Transazione di apertura
-   Progetto - Registra costi
-   Progetto - Volume d'affari accumulato
-   Progetto - Stima registrata
-   Progetto - Storna stima





