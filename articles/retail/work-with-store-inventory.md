---
title: Archiviare la gestione inventario
description: Questo articolo descrive i tipi di documenti utilizzabili per la gestione dell'inventario.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 72f6f5e2645240ee3ddd31657176f27cb7db404f
ms.contentlocale: it-it
ms.lasthandoff: 08/09/2018

---

# <a name="store-inventory-management"></a>Archiviare la gestione inventario

[!include [banner](includes/banner.md)]

Questo articolo descrive i tipi di documenti utilizzabili per la gestione dell'inventario.

È possibile utilizzare i seguenti tipi di documenti per la gestione dell'inventario dell'organizzazione.

## <a name="purchase-orders"></a>Ordine fornitore
Gli ordini fornitore vengono creati nella sede centrale. Se un magazzino al dettaglio viene incluso nell'intestazione dell'ordine fornitore, l'ordine può essere ricevuto presso il punto vendita utilizzando Modern POS (MPOS) o il POS cloud in Microsoft Dynamics 365 for Retail. Una volta immesse, è possibile salvare in locale le quantità ricevute all'interno del punto vendita per ulteriori modifiche. In alternativa, i quantitativi possono essere impegnati e inviati alla sede principale. Presso la sede principale i quantitativi che sono stati ricevuti nel punto vendita vengono visualizzati in Dynamics 365 for Retail, nel campo **Ricevi ora** dell'ordine fornitore.

## <a name="transfer-orders"></a>Ordini di trasferimento
Un ordine di trasferimento può specificare che un particolare punto vendita è un percorso da cui possono essere spediti gli articoli. In questo caso, l'ordine di trasferimento viene visualizzato presso il punto vendita come una richiesta di prelievo in MPSO o POS cloud. Una volta che i quantitativi richiesti sono stati prelevati, vengono impegnati e inviati alla sede principale. Presso la sede principale i quantitativi che sono stati prelevati nel punto vendita vengono visualizzati in Dynamics 365 for Retail, nel campo **Spedisci ora** dell'ordine di trasferimento. Un ordine di trasferimento può specificare che un particolare punto vendita è un percorso da cui possono essere spediti gli articoli. In questo caso, l'ordine di trasferimento viene visualizzato presso il punto vendita come una richiesta di ricezione in MPSO o POS cloud. Una volta immesse, è possibile salvare in locale le quantità ricevute all'interno del punto vendita per ulteriori modifiche. In alternativa, i quantitativi possono essere impegnati e inviati alla sede principale. Presso la sede principale i quantitativi che sono stati ricevuti nel punto vendita vengono visualizzati in Dynamics 365 for Retail, nel campo **Ricevi ora** dell'ordine di trasferimento.

## <a name="stock-counts"></a>Conteggi scorte
I conteggi scorte possono essere pianificati o non pianificati. I conteggi di scorte programmate sono avviati presso la sede principale, la quale specifica gli articoli da conteggiare. La sede principale crea un documento relativo ai conteggi che si può ricevere in punto vendita, dove le quantità delle scorte disponibili effettive vengono inserite in MPOS oppure in POS cloud. I conteggi scorte non pianificati vengono avviati in un punto vendita e le quantità delle scorte disponibili effettive vengono aggiornate in MPOS o POS cloud. A differenza dei conteggi scorte pianificati, i conteggi scorte non pianificati non dispongono di un elenco predefinito di elementi. Al termine di un conteggio scorte di entrambi i tipi, questo viene impegnato e inviato alla sede principale. Presso la sede centrale, il conteggio viene convalidato e registrato.

## <a name="inventory-lookup"></a>Ricerca in magazzino
La quantità corrente di prodotto disponibile per più catene e magazzini può essere visualizzata nella pagina Ricerca in magazzino. Oltre alla quantità corrente di scorte disponibili, le quantità available-to-promise (ATP) future possono essere visualizzate per ogni singolo punto vendita. A questo scopo, selezionare il punto vendita di cui si desidera visualizzare il valore ATP, quindi fare clic su **Mostra disponibilità punto vendita**.





