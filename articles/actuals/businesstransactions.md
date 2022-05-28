---
title: Zakelijke transacties in Project Operations
description: Dit onderwerp biedt een overzicht van het concept van zakelijke transacties in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582198"
---
# <a name="business-transactions-in-project-operations"></a>Zakelijke transacties in Project Operations

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

In Microsoft Dynamics 365 Project Operations is *zakelijke transactie* een abstract concept dat niet wordt vertegenwoordigd door een entiteit. Sommige algemene entiteitsvelden en -processen zijn echter ontworpen om het concept van bedrijfstransacties te gebruiken. De volgende entiteiten gebruiken deze abstractie:

- Prijsopgaveregeldetails
- Contractregeldetails
- Schattingsregels
- Journaalregels
- Werkelijke waarden

Van deze entiteiten worden Prijsopgaveregeldetails, Contractregeldetails en Schattingsregels toegewezen aan de *schattingsfase* in de levenscyclus van het project. De entiteiten Journaalregels en Werkelijke waarden worden toegewezen aan de *uitvoeringsfase* in de levenscyclus van het project.

Project Operations behandelt records in al deze vijf entiteiten als zakelijke transacties. Het enige verschil is dat records in de entiteiten die zijn toegewezen aan de schattingsfase (Prijsopgaveregeldetails, Contractregeldetails en Schattingsregels) worden beschouwd als *financiële prognoses*, terwijl de records in entiteiten die zijn toegewezen aan de uitvoeringsfase (Journaalregels en Werkelijke waarden) worden beschouwd als *financiële feiten* die zich al hebben voorgedaan.

Zie voor meer informatie [Schattingen](../project-management/estimating-projects-overview.md) en [Werkelijke waarden](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Unieke concepten voor bedrijfstransacties

De volgende concepten zijn uniek voor het concept van bedrijfstransacties:

- Transactietype
- Transactieklasse
- Oorsprong van transactie
- Transactieverbinding

### <a name="transaction-type"></a>Transactietype

Transactietype staat voor de timing en context van de financiële impact op een project. Het wordt gedefinieerd door een optieset met de volgende ondersteunde waarden in Project Operations:

- Kosten
- Projectcontract
- Niet-gefactureerde verkoop
- Gefactureerde verkoop
- Interorganisatorische verkopen
- Kosten van resource-eenheid

### <a name="transaction-class"></a>Transactieklasse

Transactieklasse vertegenwoordigt de verschillende typen kosten die worden gemaakt voor projecten. Het wordt gedefinieerd door een optieset met de volgende ondersteunde waarden in Project Operations:

- Tijd
- Onkosten
- Materiaal
- Tarief
- Mijlpaal
- Belastingen

> [!NOTE]
> De waarde **Mijlpaal** wordt meestal gebruikt door de bedrijfslogica voor facturering met een vaste prijs in Project Operations.

### <a name="transaction-origin"></a>Oorsprong van transactie

Transactieoorsprong is een entiteit die de oorsprong van elke zakelijke transactie opslaat om te helpen bij rapportage en traceerbaarheid. Wanneer de uitvoering van het project begint, maakt elke zakelijke transactie een andere zakelijke transactie die op zijn beurt weer een andere zakelijke transactie zal maken enzovoort.

### <a name="transaction-connection"></a>Transactieverbinding

Transactieverbinding is een entiteit die de relatie tussen twee soortgelijke bedrijfstransacties opslaat, zoals kosten en gerelateerde verkoopwaarden, of omkeringen van transacties die worden geactiveerd door factureringsactiviteiten zoals factuurbevestigingen of factuurcorrecties.

Samen helpen de entiteiten Oorsprong van transactie en Transactieverbinding u relaties tussen zakelijke transacties en acties die hebben geleid tot het maken van een specifieke zakelijke transactie bij te houden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
