--- 
title: Impostare l'ID IVA
description: In questa procedura si descrivono i prerequisiti di registrazione di ID IVA, ad esempio l'impostazione di un tipo di registrazione e la sua assegnazione a una categoria di registrazione.
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 20f64385b988ff48d865d2d521a9e580dc04c4a2
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vat-id"></a>Impostare l'ID IVA

[!include [task guide banner](../../includes/task-guide-banner.md)]

In questa procedura si descrivono i prerequisiti di registrazione di ID IVA, ad esempio l'impostazione di un tipo di registrazione e la sua assegnazione a una categoria di registrazione. È possibile ottenere ulteriori informazioni sugli ID registrazione e la loro elaborazione, inclusi i prerequisiti necessari, nell'argomento della Guida sugli ID registrazione. 

Queste informazioni si applicano a tutti i paesi europei. Questa attività è stata creata utilizzando la società di dati dimostrativi DEMF con l'indirizzo principale della persona giuridica in Germania. Quest'attività è destinata agli amministratori di sistema. Questa procedura è per una funzionalità che è stata aggiunta in Dynamics 365 for Operations versione 1611.

1. Scegliere Amministrazione organizzazione > Rubrica globale > Tipi di registrazione > Tipi di registrazione.
2. Fare clic su Nuovo per aprire la finestra di dialogo a discesa.
3. Nel campo Nome digitare 'ID IVA'.
4. Nel campo Descrizione, numero di partita IVA.
5. Nel campo Paese immettere o selezionare un valore DEU
6. Selezionare Sì nel campo Univoco.
    * Selezionare questa casella di controllo per verificare se l'ID IVA è univoco.  
7. Selezionare Sì nel campo Principale per paese.
    * Selezionare questa casella di controllo se l'ID IVA deve essere valido per tutti gli indirizzi che appartengono al paese specificato.  
8. Fare clic su Crea.
9. Scegliere Aggiungi.
10. Nel campo Paese immettere o selezionare un valore ITA
11. Nel campo Formato digitare '###########'.
    * Quando si immette un ID registrazione di questo tipo per il paese selezionato, l'ID registrazione verrà verificato rispetto a questo formato.  
12. Selezionare la casella di controllo Univoco.
    * Selezionare questa casella di controllo per verificare se l'ID IVA è univoco.  
13. Selezionare la casella di controllo Principale per paese.
    * Selezionare questa casella di controllo se l'ID IVA deve essere valido per tutti gli indirizzi che appartengono al paese specificato.  
14. Fare clic su Salva.
15. Scegliere Amministrazione organizzazione > Rubrica globale > Tipi di registrazione > Categorie di registrazione.
16. Fare clic su Nuovo.
17. Nel campo Paese immettere o selezionare un valore ID IVA, DEU
18. Nel campo Categoria di registrazione selezionare 'ID IVA'
    * Assegnare il tipo di registrazione creato in precedenza a una categoria predefinita di registrazione.  
19. Fare clic su Nuovo.
20. Nel campo Paese immettere o selezionare un valore ID IVA, ITA
21. Nel campo Categoria di registrazione selezionare 'ID IVA'
    * Assegnare il tipo di registrazione creato a una categoria predefinita di registrazione.  
22. Fare clic su Salva.


