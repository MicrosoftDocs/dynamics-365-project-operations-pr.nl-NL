---
title: Toeleveringscontractopties voor projectteamleden
description: In dit artikel worden de toeleveringscontractopties voor projectteamleden in Microsoft Dynamics 365 Project Operations uitgelegd.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522272"
---
# <a name="subcontracting-options-for-project-team-members"></a>Toeleveringscontractopties voor projectteamleden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

In Microsoft Dynamics 365 Project Operations kunt u de toeleveringscontractopties evalueren die beschikbaar zijn voor een of meer projectteamleden. Met de beschikbare toeleveringscontractopties kunt u:

- Maak een nieuw toeleveringscontract en/of maak nieuwe regels op een bestaand toeleveringscontract aan voor de geselecteerde projectteamleden. 
- Reserveer op basis van een toeleveringscontract en toeleveringscontractregel die al bestaan. 

U kunt kiezen uit de beschikbare toeleveringscontractopties voor algemene projectteamleden of kiezen uit projectteamleden die zijn zijn voorzien van personeel met een benoemde resource die contractwerknemer is. 

Er zijn geen toeleveringscontractopties beschikbaar in de volgende gevallen:

- Teamleden van een project dat is bemand met een medewerker. 
- Projectteamleden die al zijn gekoppeld aan een toeleveringscontract en toeleveringscontractregel. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Een teamlid voor een onbemand project onder contract nemen

Volg deze stappen om de beschikbare toeleveringscontractopties voor een algemeen of onbemand-projectteamlid te bekijken en te kiezen:

1. Selecteer een of meer records van projectteamleden waarbij de resource een algemene resource is.
2. Zorg ervoor dat geen van de geselecteerde records van projectteamleden al onder contract is. 
3. Selecteer **Toeleveringscontractopties** op het subraster van de projectteamleden. Het dialoogvenster **Toeleveringscontractopties** wordt geopend. 
4. Als u in stap 1 slechts één record van een projectteamlid hebt geselecteerd, zijn de volgende opties beschikbaar:
    - Maak nieuwe toeleveringscontractregels. 
    - Reserveren voor een bestaand toeleveringscontract Als u in stap 1 meerdere records van projectteamleden hebt geselecteerd, is de enig beschikbare optie het maken van nieuwe toeleveringscontractregels.
5. Met de optie om te reserveren voor een bestaande toeleveringscontractregel kunt u een toeleveringscontract en toeleveringscontractregel selecteren waarvoor u wilt reserveren. Wanneer u een toeleveringscontractregel selecteert om capaciteit te reserveren, moet u ervoor zorgen dat de geselecteerde toeleveringscontractregel voor tijd is en dat de vereiste rol voor het projectteamlid overeenkomt met de rol die op de toeleveringscontractregel is ingekocht.
6. Wanneer u ervoor kiest om nieuwe toeleveringscontractregels voor de projectteamleden aan te maken, kunt u in het systeem het toeleveringscontract selecteren dat u voor deze regels wilt maken. Het toeleveringscontract dat u selecteert om nieuwe regels in te maken moet de status **Concept** hebben. Met deze optie om nieuwe toeleveringscontractregels te maken voor de geselecteerde projectteamleden, zal het systeem één toeleveringscontractregel voor tijd maken voor elk projectteamlid. De rol, uren en datums worden gekopieerd van het projectteamlid naar elke toeleveringscontractsregel die wordt gemaakt. 
7. Wanneer een algemeen teamlid is gekoppeld aan een toeleveringscontract en toeleveringscontractregel, wordt het veld **Werknemertype** op de algemene-teamlidrij bijgewerkt naar **Contractwerknemer** en wordt de waarde van **Geldigheid toeleveringscontract** ingesteld op **Geldig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Een teamlid voor een bemand project onder contract nemen

Net als algemene of onbemand-projectteamleden, kunt u ook toeleveringscontractopties bekijken voor een bemand-projectteamlid mits dat teamlid een contractwerknemer is. Volg deze stappen om de beschikbare toeleveringscontractopties voor een bemand- of benoemd-projectteamlid te bekijken en te kiezen:

1. Selecteer een of meer records van projectteamleden waarbij de resource een benoemde contractwerknemer is.
2. Zorg ervoor dat geen van de geselecteerde records van projectteamleden al onder contract is. 
3. Selecteer **Toeleveringscontractopties** op het subraster van de projectteamleden. Het dialoogvenster **Toeleveringscontractopties** wordt geopend. 
4. Als u in stap 1 slechts één record van een projectteamlid hebt geselecteerd, zijn de volgende opties beschikbaar:
      - Maak nieuwe toeleveringscontractregels.
      - Reserveren op basis van een bestaand toeleveringscontract.
  Als u in stap 1 meerdere records van projectteamleden hebt geselecteerd, is de enig beschikbare optie het maken van nieuwe toeleveringscontractregels.
5. Met de optie om te reserveren voor een bestaande toeleveringscontractregel kunt u een toeleveringscontract en toeleveringscontractregel selecteren waarvoor u wilt reserveren. Wanneer u een toeleveringscontractregel selecteert om capaciteit te reserveren, moet u voor het volgende zorgen:
      - De geselecteerde toeleveringscontractregel is voor tijd. 
      - De vereiste rol voor het projectteamlid komt overeen met de rol die is ingekocht op de toeleveringscontractregel. 
      - De leverancier waaraan de contractmedewerker is gekoppeld, is dezelfde als de leverancier op het toeleveringscontract.
6. Wanneer u ervoor kiest om nieuwe toeleveringscontractregels voor de projectteamleden aan te maken, kunt u in het systeem het toeleveringscontract selecteren dat u voor deze regels wilt maken. Met deze optie moet u ervoor zorgen dat de leverancier waartoe de contractwerknemer behoort, dezelfde is als de leverancier op het toeleveringscontract. 
7. Het toeleveringscontract dat u selecteert om nieuwe regels in te maken moet de status **Concept** hebben. Met deze optie om nieuwe toeleveringscontractregels te maken voor de geselecteerde projectteamleden, zal het systeem één toeleveringscontractregel voor tijd maken voor elk projectteamlid. De rol, uren en datums worden gekopieerd van het projectteamlid naar elke toeleveringscontractsregel die wordt gemaakt.  
8. Wanneer een benoemd teamlid is gekoppeld aan een toeleveringscontract en toeleveringscontractregel, wordt het veld **Werknemertype** op de benoemde-teamlidrij bijgewerkt naar **Contractwerknemer** en wordt de waarde van **Geldigheid toeleveringscontract** ingesteld op **Geldig**.

## <a name="re-costing-subcontractor-assignments"></a>Kostprijs van toewijzingen voor toeleveranciers opnieuw berekenen

Wanneer een projectteamlid (algemeen of benoemd) aan toeleveringscontractregels wordt gekoppeld met behulp van het dialoogvenster **Toeleveringscontractopties**, wordt de kostprijs van eventuele toewijzingen aan taken die het teamlid heeft herberekend op basis van de inkoopprijslijst die aan het toeleveringscontract is gekoppeld. Op het tabblad **Schattingen** op de pagina **Projectgegevens** selecteert u de knop **Prijzen bijwerken** om bijgewerkte prijzen en/of kostprijsberekeningen te zien die voortvloeien uit de beslissing om uit te besteden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
