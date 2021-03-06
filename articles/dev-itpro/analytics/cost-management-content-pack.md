---
title: Contenuto Power BI per la gestione dei costi
description: "In questo argomento viene descritto cosa è incluso nel contenuto Power BI per la gestione dei costi."
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: caf1c13d48d1f8af5c88927ccb23118e99cb38e0
ms.contentlocale: it-it
ms.lasthandoff: 08/13/2018

---

# <a name="cost-management-power-bi-content"></a>Contenuto Power BI per la gestione dei costi

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Panoramica

I contenuto Microsoft Power BI per la **Gestione costi** è destinato ai contabili di inventario o agli utenti nell'organizzazione responsabili o interessati allo stato dell'inventario o WIP o ai responsabili o interessati all'analisi degli scostamenti dei costi standard.

> [!NOTE]
> Il contenuto Power BI per la **Gestione costi** descritto in questo argomento si applica a Dynamics 365 for Finance and Operations 8.0.
> 
> Il pacchetto di contenuti Power BI per la **Gestione costi**, disponibile sul sito AppSource, è stato deprecato. Per ulteriori informazioni sulle funzionalità deprecate, vedere [Pacchetti di contenuti Power BI disponibili in AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Il contenuto Power BI si presenta in un formato strutturato in categorie che aiuta a monitorare le prestazioni degli inventari e a visualizzare il flusso dei costi. È possibile estrapolare informazioni approfondite manageriali, ad esempio l'indice di rotazione, il numero di giorni in cui l'inventario è a disposizione, la precisione e la "classificazione ABC" al livello di aggregazione preferito (società, articolo, gruppo di articoli o sito). Le informazioni disponibili possono essere utilizzate anche come supplemento dettagliato al rendiconto finanziario.

Il contenuto Power BI si basa sulla misura di aggregazione **CostObjectStatementCacheMonthly**, che ha la tabella **CostObjectStatementCache** impostata come origine dati primaria. Questa tabella viene gestita dal framework della cache del set di dati. Per impostazione predefinita, la tabella viene aggiornata ogni 24 ore, ma è possibile modificare la frequenza di aggiornamento o abilitare gli aggiornamenti manuali nella configurazione della cache dei set di dati. Gli aggiornamenti manuali possono essere eseguiti nell'area di lavoro **Amministrazione costi** è nell'area di lavoro **Analisi costo**.

Dopo ogni aggiornamento della tabella **CostObjectStatementCache**, è necessario aggiornare la misura di aggregazione **CostObjectStatementCacheMonthly** prima che vengano aggiornati i dati nelle visualizzazioni di Power BI.

## <a name="accessing-the-power-bi-content"></a>Accesso al contenuto Power BI

Il contenuto Power BI per la **Gestione costi** viene mostrato nelle aree di lavoro **Amministrazione costi** e **Analisi costo**.

L'area di lavoro **Amministrazione costi** contiene le schede seguenti:

- **Panoramica** - Questa scheda visualizza i dati dell'applicazione.
- **Stato contabilità inventario** - Questa scheda visualizza il contenuto di Power BI.
- **Stato contabilità produzione** - Questa scheda visualizza il contenuto di Power BI.

L'area di lavoro **Analisi costo** contiene le schede seguenti:

- **Panoramica** - Questa scheda visualizza i dati dell'applicazione.
- **Analisi contabilità inventario** - Questa scheda visualizza il contenuto di Power BI.
- **Analisi contabilità produzione** - Questa scheda visualizza il contenuto di Power BI.
- **Analisi scostamento costo standard** - Questa scheda visualizza il contenuto di Power BI.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Pagine di report incluse nel contenuto Power BI

Il contenuto Power BI per la **Gestione costi** include un set di pagine di report che consistono in un set di metriche. Queste metriche vengono visualizzate come grafici, riquadri e tabelle. 

Nelle seguenti tabelle viene fornita una panoramica delle visualizzazioni nel contenuto Power BI per la **Gestione costi**.

### <a name="inventory-accounting-status"></a>Stato contabilità inventario

| Pagina di report                               | Visualizzazione                                   |
|-------------------------------------------|-------------------------------------------------|
| Panoramica di Gestione articoli                        | Saldo iniziale                               |
|                                           | Modifica netto                                      |
|                                           | % modifica netto                                    |
|                                           | Saldo finale                                  |
|                                           | Precisione inventario                              |
|                                           | Indice di rotazione scorte                        |
|                                           | Scorte disponibili giornaliere                          |
|                                           | Prodotto attivo nel periodo                        |
|                                           | Oggetti di costo attivi nel periodo                   |
|                                           | Saldo per gruppo di articoli                           |
|                                           | Saldo per sito                                 |
|                                           | Rendiconto per categoria                           |
|                                           | Variazione netta per trimestre                           |
| Panoramica di magazzino per sito e per gruppo di articoli | Precisione inventario per sito                      |
|                                           | Indice di rotazione scorte per sito                |
|                                           | Saldo finale inventario per sito                |
|                                           | Precisione inventario per gruppo di articoli                |
|                                           | Indice di rotazione scorte per gruppo di articoli          |
|                                           | Saldo finale inventario per nome sito e gruppo di articoli |
| Rendiconto inventario                       | Rendiconto inventario                             |
| Rendiconto inventario per sito               | Rendiconto inventario per sito                     |
| Rendiconto inventario per categoria di prodotti  | Rendiconto inventario                             |
| Rendiconto inventario per categoria di prodotti  | Rendiconto inventario per sito                     |

### <a name="manufacturing-accounting-status"></a>Stato contabilità produzione

| Pagina di report                | Visualizzazione                       |
|----------------------------|-------------------------------------|
| Panoramica WIP da inizio anno           | Saldo iniziale                   |
|                            | Modifica netto                          |
|                            | % modifica netto                        |
|                            | Saldo finale                      |
|                            | Indice di rotazione WIP                  |
|                            | WIP giornaliero disponibile                    |
|                            | Oggetto di costo attivo nel periodo        |
|                            | Modifica netto per gruppo di risorse        |
|                            | Saldo per sito                     |
|                            | Rendiconto per categoria               |
|                            | Variazione netta per trimestre               |
| rendiconto WIP              | Saldo iniziale                   |
|                            | Saldo finale                      |
|                            | Rendiconto WIP per categoria           |
| Rendiconto WIP per sito      | Saldo iniziale                   |
|                            | Saldo finale                      |
|                            | Rendiconto WIP per categoria e sito  |
| Rendiconto WIP per gerarchia | Saldo iniziale                   |
|                            | Saldo finale                      |
|                            | Rendiconto WIP per gerarchia di categorie |

### <a name="inventory-accounting-analysis"></a>Analisi contabilità inventario

| Pagina di report        | Visualizzazione                                                                |
|--------------------|------------------------------------------------------------------------------|
| Dettagli delle scorte  | Prime 10 risorse per saldo finale                                           |
|                    | Prime 10 risorse per aumento modifica netto                                      |
|                    | Prime 10 risorse per decremento modifica netto                                      |
|                    | Prime 10 risorse per indice di rotazione scorte                                 |
|                    | Risorse per indice di rotazione scorte basso e saldo finale sopra soglia |
|                    | Prime 10 risorse per precisione bassa                                             |
| Classificazione ABC | Saldo finale inventario                                                     |
|                    | Materiale consumato                                                            |
|                    | Venduto (COGS)                                                                  |
| Tendenze scorte   | Saldo finale inventario                                                     |
|                    | Modifica netto inventario                                                         |
|                    | Indice di rotazione scorte                                                     |
|                    | Precisione inventario                                                           |

### <a name="manufacturing-accounting-analysis"></a>Analisi contabilità produzione

| Pagina di report | Visualizzazione      |
|-------------|--------------------|
| Tendenze WIP  | Saldo finale WIP |
|             | Modifica netto WIP     |
|             | Indice di rotazione WIP |

### <a name="std-cost-variance-analysis"></a>Analisi scostamento costo standard

| Pagina di report                             | Visualizzazione                                        |
|-----------------------------------------|------------------------------------------------------|
| Scostamento prezzi di acquisto (costo standard) da inizio anno | Saldo approvvigionato                                     |
|                                         | Scostamento prezzi di acquisto                              |
|                                         | Indice di scostamento prezzi di acquisto                        |
|                                         | Scostamento per gruppo di articoli                               |
|                                         | Scostamento per sito                                     |
|                                         | Prezzo di acquisto per trimestre                            |
|                                         | Prezzo di acquisto per trimestre e gruppo di articoli             |
|                                         | Prime 10 risorse per indice di prezzo di acquisto sfavorevole |
|                                         | Prime 10 risorse per indice di prezzo di acquisto favorevole   |
| Scostamento produzione (costo standard) da inizio anno     | Costo di produzione                                    |
|                                         | Scostamento produzione                                  |
|                                         | Indice di scostamento produzione                            |
|                                         | Scostamento per gruppo di articoli                               |
|                                         | Scostamento per sito                                     |
|                                         | Scostamento di produzione per trimestre                       |
|                                         | Scostamento di produzione per trimestre e tipo di scostamento     |
|                                         | Prime 10 risorse per scostamento di produzione sfavorevole  |
|                                         | Prime 10 risorse per scostamento di produzione favorevole    |

## <a name="understanding-the-data-model-and-entities"></a>Informazioni su modelli ed entità di dati

I dati di Microsoft Dynamics 365 for Finance and Operations vengono utilizzati per compilare le pagine del report nel contenuto Power BI per la **Gestione costi**. Questi dati sono rappresentati come misure di aggregazione che vengono collocate nell'archivio entità, ovvero un database di Microsoft SQL Server ottimizzato per l'analisi. Per ulteriori informazioni, vedere [Integrazione di Power BI con l'archivio entità](power-bi-integration-entity-store.md).

Le misure di aggregazione chiave degli oggetti seguenti vengono utilizzate come base del contenuto Power BI.

| Oggetto                          | Misure di aggregazione chiave | Origine dati per Finance and Operations | Campo               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Periodo                     | CostObjectStatementCache               | Periodo              |
| CostObjectStatementCacheMonthly | Quantità                   | CostObjectStatementCache               | Qtà                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Nella tabella seguente vengono illustrate le misure chiave calcolate nel contenuto Power BI.

| Unità di misura                            | Calcolo |
|------------------------------------|-------------|
| Saldo iniziale                  | Saldo iniziale = \[Saldo finale\]-\[Modifica netto\] |
| Qtà saldo iniziale             | Qtà saldo iniziale = \[Qtà saldo finale\]-\[Qtà modifica netto\] |
| Saldo finale                     | Saldo finale = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Qtà saldo finale                | Qtà saldo finale = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Modifica netto                         | Modifica netto = SUM(\[AMOUNT\]) |
| Qtà modifica netto                    | Qtà modifica netto = SUM(\[QTY\]) |
| Indice di rotazione scorte per importo | Indice di rotazione scorte per importo = if(OR(\[Saldo medio inventario\] \<= 0, \[Inventario venduto o uscite consumate\] \>= 0), 0, ABS(\[Inventario venduto o uscite consumate\])/\[Saldo medio inventario\]) |
| Saldo medio inventario          | Saldo medio inventario = ((\[Saldo finale\] + \[Saldo iniziale\]) / 2) |
| Scorte disponibili giornaliere             | Scorte disponibili giornaliere = 365 / CostObjectStatementEntries\[Indice di rotazione scorte per importo\] |
| Precisione inventario                 | Precisione inventario per importo = IF(\[Saldo finale\] \<= 0, IF(OR(\[Importo conteggiato inventario\] \<\> 0, \[Saldo finale\] \< 0), 0, 1), MAX(0, (\[Saldo finale\] - ABS(\[Importo conteggiato inventario\]))/\[Saldo finale\])) |

La seguenti dimensioni chiave vengono utilizzate come filtri per dividere le misure di aggregazione in modo da poter ottenere una maggiore granularità e informazioni analitiche più approfondite.


| Entità                                                  | Esempi di attributi                          |
|---------------------------------------------------------|-------------------------------------------------|
| Prodotti                                                | Numero prodotto, nome prodotto, unità, gruppi di articoli |
| Gerarchie di categorie (assegnate al ruolo Gestione costi) | Gerarchia di categorie, livello di categoria              |
| Persone giuridiche                                          | Nomi di persone giuridiche                              |
| Calendari fiscali                                        | Calendario fiscale, anno, trimestre, periodo, mese   |
| Sito                                                    | ID, nome, indirizzo, Stato/regione, paese               |

