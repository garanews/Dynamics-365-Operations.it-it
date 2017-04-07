---
title: Ammortamento basato su coefficiente
description: Questo articolo fornisce una panoramica del metodo di ammortamento basato su coefficiente.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: d57c1811bfed466b7707214b85bc1fcecabbce2b
ms.lasthandoff: 03/31/2017


---

# <a name="factor-depreciation"></a>Ammortamento basato su coefficiente

Questo articolo fornisce una panoramica del metodo di ammortamento basato su coefficiente.

I fattori sono percentuali utilizzate per l'ammortamento dei cespiti. Quando si imposta un profilo di ammortamento cespiti e si seleziona **Fattore** nel campo **Metodo** della pagna **Profili di ammortamento**, è possibile impostare un ammortamento progressivo, digressivo o a quote costanti.

-   Nell'ammortamento progressivo, l'importo di ammortamento aumenta con ogni periodo di ammortamento.
-   Nell'ammortamento digressivo, l'importo di ammortamento per periodo diminuisce nel tempo.
-   Nell'ammortamento a quote costanti, l'ammortamento è lo stesso per ogni periodo.

Nelle regole e negli esempi illustrati di seguito viene descritto come impostare i fattori per ogni tipo di ammortamento. 

> [!NOTE] 
> Quando si seleziona ** fattore ** in ** metodo ** sistemi, ** fattore ** il campo e ** intervallo ** il campo visualizzare.

## <a name="progressive-depreciation"></a>Ammortamento progressivo
Il valore del campo **Fattore** è maggiore di **50**

### <a name="example"></a>Esempio

Si supponga che il prezzo di acquisizione sia 100.000, il fattore sia 70, la vita utile sia 10 anni e l'ammortamento inizi il 1° gennaio. Gli importi di ammortamento e valore contabile netto vengono mostrati solo per i primi sei anni di vita utile.

| Anno | Periodo      | Importo di ammortamento | Importo valore contabile netto |
|------|-------------|---------------------|-----------------------|
| 1    | 31 dicembre | 307,69              | 99.692,31             |
| 2    | 31 dicembre | 1.447,21            | 98.245,10             |
| 3    | 31 dicembre | 3.104,50            | 95.140,60             |
| 4    | 31 dicembre | 5.150,21            | 89.990,39             |
| 5    | 31 dicembre | 7.522,95            | 82.467,44             |
| 6    | 31 dicembre | 10.184,06           | 72.283,38             |

## <a name="digressive-depreciation"></a>Ammortamento digressivo
Il valore del campo **Fattore** è minore di **50**.

### <a name="example"></a>Esempio

Si supponga che il prezzo di acquisizione sia 100.000, il fattore sia 20, la vita utile sia 10 anni e l'ammortamento inizi il 1° gennaio. Gli importi di ammortamento e valore contabile netto vengono mostrati solo per i primi sei anni di vita utile.

| Anno | Periodo      | Importo di ammortamento | Importo valore contabile netto |
|------|-------------|---------------------|-----------------------|
| 1    | 31 dicembre | 56.080,43           | 43.919,57             |
| 2    | 31 dicembre | 10.665,70           | 33.253,87             |
| 3    | 31 dicembre | 7.156,22            | 26.097,65             |
| 4    | 31 dicembre | 5.538,06            | 20.559,59             |
| 5    | 31 dicembre | 4.579,89            | 15.979,70             |
| 6    | 31 dicembre | 3.937,36            | 12.042,34             |

## <a name="straight-line-depreciation"></a>Ammortamento a quote costanti
Il valore del campo **Fattore** è uguale a **50**. In questo caso, l'ammortamento è lo stesso in ogni periodo ed è consigliabile prendere in considerazione le implicazioni delle scelte effettuate in altri campi, come descritto in [Ammortamento a quote costanti basato sulla vita utile](straight-line-service-life-depreciation.md).

