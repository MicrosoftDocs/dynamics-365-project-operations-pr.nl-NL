---
title: Valutaconversie instellen om verkoopprijzen te berekenen op basis van kostprijstarieven
description: In dit artikel wordt uitgelegd hoe u het valutaconversiegedrag configureert dat wordt gebruikt in Microsoft Dynamics 365 Project Operations wanneer verkooptransacties worden gegenereerd op basis van kostentransacties.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816663"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Valutaconversie instellen om verkoopprijzen te berekenen op basis van kostprijstarieven

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In Microsoft Dynamics 365 Project Operations kunnen verkoopprijzen voor onkostencategorieën worden ingesteld als numerieke waarden, of ze kunnen zo worden ingesteld dat ze worden berekend op basis van de gemaakte kosten.

Wanneer ze zijn ingesteld om te worden berekend op basis van de gemaakte kosten, zijn de volgende opties beschikbaar:

- Tegen kosten
- Percentage boven de kosten markeren

In scenario's waarin de onkosten worden gemaakt in een valuta die verschilt van de verkoopvaluta voor het projectcontract, is valutaconversie vereist om de verkoopprijs te berekenen op basis van de kosten.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Valutaconversiegedrag dat native Dataverse wisselkoersen gebruikt

Project Operations gebruikt standaard de wisselkoersen die zijn opgeslagen in de valutatabel in Dataverse. Volg deze stappen om Project Operations te configureren voor het gebruik van native wisselkoersen voor het berekenen van verkoopprijzen op kostprijsbasis.

1. Ga naar **Project Operations \> Instellingen \> Parameters**.
1. Open de detailpagina van **projectparameter**.
1. Stel het veld **Valutaconversielogica** in op een lege waarde.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Valutaconversiegedrag waarbij wisselkoersen van financiële en operationele apps worden gebruikt

De wisselkoersen in de valutatabel die standaard beschikbaar zijn in Dataverse zijn niet geldig vanaf de datum. Daarom zijn ze mogelijk niet altijd geschaald naar uw vereisten voor het berekenen van verkoopprijzen op basis van kostprijstarieven.

U kunt wisselkoersen uit de financiële en operationele omgeving gebruiken om de verkoopprijs in de verkoopvaluta te berekenen op basis van een kostprijstarief in de kostprijsvaluta. Volg deze stappen om dit valutaconversiegedrag te configureren.

1. Voeg op de pagina **Projectparameters** het veld **Valutaconversielogica** toe. Sla vervolgens de aanpassingen op en publiceer deze.
1. Ga naar **Project Operations \> Instellingen \> Parameters**.
1. Open de detailpagina van **projectparameter**. 
1. Stel het veld **Valutaconversiegedrag** in op **Uitgebreid met terugval naar standaard**.
1. Geef de **Twee keer wegschrijven app-gebruiker** beveiligingsrol **Algemeen lezen** toestemming voor de volgende tabellen:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Voer in uw financiële en operationele omgeving de volgende toewijzingen twee keer wegschrijven uit met initiële synchronisatie:

    - Wisselkoerstype (msdyn\_exchangeratetypes)
    - Valutapaar wisselkoers (msdyn\_currencyexchangeratepairs)
    - CDS-wisselkoersen (msdyn\_currencyexchangerates)

Nadat deze wijzigingen zijn voltooid, maakt twee keer wegschrijven de wisselkoersen van de financiële en operationele omgeving beschikbaar in Dataverse. Project Operations gebruikt die wisselkoersen vervolgens om kostentarieven om te rekenen naar de verkoopvaluta van het contract.

> [!NOTE]
> Dit valutaconversiegedrag is alleen van toepassing op de berekening van verkoopprijzen op basis van kostprijstarieven. Het wordt niet gebruikt om algemene basisvalutawaarden te berekenen. Basisvalutawaarden gebruiken altijd oorspronkelijke Dataverse-wisselkoersen, ongeacht of u deze procedure voltooit.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
