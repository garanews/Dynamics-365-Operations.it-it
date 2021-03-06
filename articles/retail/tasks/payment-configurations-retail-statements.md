--- 
title: " Configurazioni dei pagamenti per rendiconti di vendita al dettaglio"
description: "In questa procedura sono illustrate le configurazioni per i metodi di pagamento di punto vendita al dettaglio che interessano la modalità di creazione e registrazione dei rendiconti di vendita al dettaglio."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f12d8ac9be11b92eaef4acce094ae183906278d4
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="payment-configurations-for-retail-statements"></a> Configurazioni dei pagamenti per rendiconti di vendita al dettaglio

[!include[task guide banner](../includes/task-guide-banner.md)]

In questa procedura sono illustrate le configurazioni per i metodi di pagamento di punto vendita al dettaglio che interessano la modalità di creazione e registrazione dei rendiconti di vendita al dettaglio.

Questa registrazione utilizza la società dimostrativa USRT.

1. Passare a Vendita al dettaglio e commercio > Canali > Punti vendita al dettaglio > Tutti i punti vendita al dettaglio.
2. Nell'elenco trovare e selezionare il record desiderato.
3. Nell'elenco fare clic sul collegamento nella riga selezionata.
4. Nel riquadro azioni, fare clic su Imposta.
5. Fare clic su Metodi di pagamento.
6. Espandere o comprimere la sezione Registrazione.
7. Fare clic su Modifica.
    * Selezionare se gli importi ricevuti per il metodo di pagamento devono essere registrati in un conto CoGe o in un conto bancario.  
    * Selezionare il conto in cui dovranno essere registrati gli importi ricevuti per il metodo di pagamento.  
    * Selezionare un conto per registrare le possibili differenze tra l'importo totale della transazione ricevuto e l'importo conteggiato per il metodo di pagamento.  
    * In questo campo è possibile immettere un importo per verificare se l'importo della differenza deve essere registrato in un altro conto di differenza. È possibile utilizzare questa opzione per tenere traccia delle grandi differenze.  
    * Selezionare un conto per registrare le possibili differenze tra l'importo totale della transazione ricevuto e l'importo conteggiato, quando supera il valore specificato nel campo "Importo massimo di differenza".  
    * Selezionare "Sì" per registrare gli importi di deposito bancario in un conto separato.  
    * In questo campo è possibile selezionare se gli importi di deposito bancario devono essere registrati in un conto CoGe o in un conto bancario.  
    * Selezionare il conto in cui registrare gli importi di deposito bancario.  
    * Selezionare il tipo di transazione bancaria da utilizzare per la registrazione degli importi di deposito bancario nel conto bancario.  
    * Selezionare "Sì" per registrare gli importi di deposito in cassaforte in un conto separato.  
    * Selezionare se gli importi di deposito in cassaforte devono essere registrati nel conto CoGe o nel conto bancario.  
    * Selezionare il conto in cui registrare gli importi di deposito in cassaforte.  
8. Fare clic su Salva.


