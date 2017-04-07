---
title: Impostare pagamenti centralizzati
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 815282422a6d7b8eef7d0628cf10b715449e1d1d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-centralized-payments"></a>Impostare pagamenti centralizzati



Seguire questi passaggi per preparare l'elaborazione dei pagamenti in una persona giuridica per conto di altre persone giuridiche dell'organizzazione. Prima di iniziare, la seguente impostazione deve essere completata:

-   Creazione di persone giuridiche.
-   Impostazione dei parametri di contabilità generale e dei piani dei conti.
-   Impostazione dei parametri di contabilità fornitori e di contabilità clienti (a seconda dei moduli utilizzati nei pagamenti centralizzati).
-   Impostazione della contabilità interaziendale.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Impostare una gerarchia organizzativa per i pagamenti centralizzati
Per i pagamenti centralizzati è necessario impostare una gerarchia organizzativa. Tale gerarchia organizzativa viene utilizzata per elaborare sia i pagamenti centralizzati dei fornitori che quelli dei clienti. **Nota:** la struttura della gerarchia non è rilevante ai fini dei pagamenti centralizzati. Qualsiasi persona giuridica della gerarchia potrà elaborare pagamenti per conto di qualsiasi altra persona giuridica nella gerarchia. Nella pagina **Gerarchie organizzative** è possibile creare una nuova gerarchia organizzativa.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Impostare un conto interaziendale per i pagamenti centralizzati
Quando le transazioni di pagamento nella persona giuridica corrente vengono liquidate con fatture presenti in altre persone giuridiche, vengono create le transazioni relative a importi da versare e da ricevere appropriate per ciascuna persona giuridica. È necessario specificare la persona giuridica in cui vengono registrati gli sconti di cassa applicabili e gli importi di profitti o perdite realizzati. Prima di iniziare, scegliere la persona giuridica da utilizzare per l'elaborazione dei pagamenti fornitore e cliente. Se una persona giuridica elabora i pagamenti fornitore mentre un'altra elabora i pagamenti cliente, sarà necessario passare a ciascuna persona giuridica. ** Contabilità interaziendale ** nella pagina, è possibile selezionare un record di relazione interaziendale per una persona giuridica per conto della quale verranno elaborati i pagamenti. ** Pagamenti centralizzati ** nella scheda, è possibile scegliere se registrare gli sconti di cassa per la persona giuridica di pagamento (o di un'altra transazione che riduce il saldo del conto fornitore) oppure nella persona giuridica della fattura (o di un'altra transazione che aumenta il saldo del conto fornitore). Questa selezione è correlata al campo **Applicazione sconto di cassa** nelle pagine **Parametri contabilità fornitori** e **Parametri contabilità clienti**. Per le tolleranze relative alle eccedenze di pagamento e alle differenze in centesimi viene utilizzata l'impostazione definita nella persona giuridica del pagamento. Per le tolleranze relative alle insufficienze di pagamento e alle differenze in centesimi viene utilizzata l'impostazione definita nella persona giuridica della fattura.

## <a name="map-vendor-accounts-across-legal-entities"></a>Mappare i conti fornitore tra più persone giuridiche
Se si effettuano pagamenti a un fornitore di una persona giuridica e si desidera selezionare le fatture relative a tale fornitore presenti in altre persone giuridiche, verificare che tutti i conti fornitore corrispondenti in ciascuna persona giuridica utilizzino tutti lo stesso ID Rubrica. Se si riceve un pagamento da un cliente che paga fatture in più di una persona giuridica, è necessario verificare che tutti i conti cliente corrispondenti in ciascuna persona giuridica utilizzino tutti lo stesso ID Rubrica.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Impostare i profili di registrazione per i pagamenti centralizzati
Quando si crea un pagamento in una persona giuridica che esegue la liquidazione delle fatture in altre persone giuridiche, gli ID profilo di registrazione delle persone giuridiche devono essere identici. Per assicurare che i pagamenti vengano creati correttamente, in ogni persona giuridica della fattura, impostare un profilo di registrazione corrispondente ai profili di registrazione utilizzati nella persona giuridica del pagamento. Passare alla prima persona giuridica della fattura, quindi ** profili registrazione fornitori ** nella pagina, è possibile creare un nuovo profilo registrazione o modificare un profilo esistente di registrazione. Le selezioni effettuate per il profilo di registrazione nella persona giuridica della fattura non devono corrispondere alle impostazioni del profilo di registrazione nella persona giuridica del pagamento.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Impostare i metodi di pagamento per i pagamenti centralizzati
Quando si crea un pagamento in una persona giuridica che esegue la liquidazione delle fatture in altre persone giuridiche, gli ID relativi al metodo di pagamento devono essere identici in entrambe persone giuridiche. Per assicurarsi che i pagamenti vengano creati correttamente, impostare in tutte le persone giuridiche della fattura un metodo di pagamento corrispondente ai metodi di pagamento utilizzati nella persona giuridica del pagamento. Passare alla prima persona giuridica della fattura e nella pagina **Metodi di pagamento** creare un nuovo metodo di pagamento o modificare un metodo di pagamento esistente. Le selezioni effettuate per il metodo di pagamento nella persona giuridica della fattura non devono necessariamente corrispondere all'impostazione del metodo di pagamento nella persona giuridica del pagamento.

## <a name="set-up-default-descriptions"></a>Impostare descrizioni predefinite
È possibile definire descrizioni predefinite per i giustificativi di compensazione interaziendale. La descrizione predefinita viene inclusa nelle transazioni relative a importi da versare e da ricevere durante il processo di compensazione interaziendale. Nella pagina **Descrizioni predefinite**, è possibile creare nuove descrizioni per **Compensazione interaziendale cliente** e **Compensazione interaziendale fornitore** selezionando una lingua e quindi immettendo il relativo testo.

