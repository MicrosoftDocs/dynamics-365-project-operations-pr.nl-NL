---
title: Omzetschattingen beheren
description: Dit artikel bevat informatie over het werken met omzetschattingen voor projecten.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 051535ce8dd4997a923b1511d242638361076979
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928472"
---
# <a name="manage-revenue-estimates"></a>Omzetschattingen beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

U kunt omzetschattingen maken, berekenen, boeken, terugdraaien of elimineren. U kunt dit handmatig doen of door middel van een periodiek proces. Dit artikel bevat informatie over het werken met omzetschattingen voor projecten.

### <a name="manage-revenue-estimates-manually"></a>Omzetschattingen handmatig beheren

Voor projecten met omzetschattingen met een vaste prijs of de pagina **Vragen over schattingen** (**Projectbeheer en financiële administratie** > **Rapporten en vragen** > **Vragen en rapporten voor schattingen**), selecteert u **Schattingen**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Omzetschattingen beheren met behulp van een periodiek proces

Ga naar **Projectbeheer en financiële administratie** > **Periodiek** > **Schattingen** en selecteer het bijbehorende proces.

## <a name="create-a-revenue-estimate"></a>Een omzetschatting maken

Voer de volgende stappen uit om een omzetschatting te maken. 

1. Ga naar **Projectbeheer en financiële administratie** > **Periodiek** > **Schattingen**.
2. Selecteer **Nieuw**. Selecteer op de pagina **Schatting maken** de volgende parameters:

   - **Periodecode**: met deze code bepaalt u hoe vaak schattingen worden geboekt.
   - **Schattingsdatum**: de datum waarop de schatting is verwerkt.
   - **Continu**: schakel dit selectievakje in om alleen schattingen te maken als er schattingen zijn geboekt in de vorige periode, of als dit de eerste schatting is die is gemaakt. Als dit niet is geselecteerd, worden schattingen gemaakt zelfs als er geen schattingen zijn geboekt in de vorige periode.
   - **Kosten om methoden te voltooien**: bepaal hoe u het resterende projectwerk wilt schatten. Zie voor meer informatie [Kosten om methoden te voltooien](cost-complete-methods.md).
   - **Voltooiingsmethode**: selecteer een voltooiingsmethode uit de volgende opties:
     - **Automatisch**: het voltooiingspercentage wordt automatisch berekend en gebaseerd op de kostenregels die in de berekening zijn opgenomen. De kostensjabloon definieert de kostenregels die worden opgenomen.
     - **Handmatig**: het voltooiingspercentage is gelijk aan het voltooiingspercentage van de laatste schatting. Nadat de schatting is gemaakt, kunt u de **Handmatige berekening** op de pagina **Schattingen** wijzigen.
     - **Van kostensjabloon**: een combinatie van de automatische en handmatige methoden. Deze optie wordt automatisch of handmatig ingesteld, afhankelijk van de standaardwaarde in de kostensjabloon.
   - **Prognosemodel**: selecteer een prognosemodel voor de schatting.
   - **Lijst met schattingen afdrukken**: maak een lijst met schattingen en geef deze weer. De lijst bevat de status van de huidige functie. U kunt eventuele waarschuwingen over de schatting op het rapport afdrukken. Door de volgende omstandigheden verschijnen er waarschuwingen in de schattingslijst:
     - Een voltooiingspercentage van meer dan 100 procent.
     - Een voltooiingspercentage van minder dan nul procent.
     - Een negatief bedrag in de kolom **Te voltooien**.
     - Een schatting zonder bijbehorend contractbedrag.
     - Een schatting zonder bijgevoegde kostenraming.
   - **Infolog weergeven**: selecteer deze optie om een bericht te ontvangen met informatie over de schattingsprojecten die werden verwerkt toen de taak werd uitgevoerd.


## <a name="post-wip-or-accruals"></a>OHW of toegerekende posten boeken

Nadat de schattingen zijn geëvalueerd, worden ze gehandhaafd, verlaagd of verhoogd. U kunt het OHW boeken wanneer u met het beoordelingsprincipe **Voltooid contract** werkt of de toegerekende posten wanneer u met het beoordelingsprincipe **Voltooid percentage** werkt.
  
De status van de geschatte periode verandert van **Gemaakt** in **Geboekt**.

## <a name="reverse-wip-or-accruals"></a>OHW of toegerekende posten omkeren

Gebruik de optie Omkeren om reeds geboekte OHW of toegerekende posten te crediteren en vervolgens schattingen voor de periode te maken.

> [!NOTE]
> Als u een periode tussen andere perioden wilt omkeren, draait u de benodigde schattingsperioden terug en boekt u ze opnieuw. Omdat alle volgende perioden afhankelijk zijn van de schattingen van de vorige periode, kunt u geen perioden overslaan.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Het schattingsproject elimineren en het project voltooien

De laatste stap in het schattingsproces is om het schattingsproject te elimineren en het project met een vaste prijs te beëindigen wanneer het voltooiingspercentage 100 procent bereikt.

Het volgende gebeurt wanneer u de eliminatie uitvoert:

- Voor een project met een vaste prijs met een voltooid contract worden de OHW-waarden verwijderd uit de balansrekeningen en geboekt op de winst- en verliesrekeningen.
- Voor een project met een vaste prijs en een voltooid percentage worden de toerekende bedragen uit de winst- en verliesrekening verwijderd.

De status van de schatting verandert in **Geëlimineerd**.

> [!NOTE]
> In bijzondere gevallen kan het percentage meer dan 100 procent bedragen. Als dit gebeurt, verlaagt u het voltooiingspercentage door **Kosten voor voltooiing instellen op nulmethode** om 100 procent te bereiken.

## <a name="reverse-elimination"></a>Eliminatie omkeren

1. Ga naar **Projectbeheer en financiële administratie** > **Periodiek** > **Schattingen** > **Eliminatie omkeren**. 
2. Selecteer in het actievenster op het tabblad **Verwerken** in de groep **Onderhouden** de optie **Schatting**. 
3. Selecteer **Eliminatie omkeren**.

Gebruik deze pagina om alle eliminaties terug te draaien met een gespecificeerde schattingsdatum en met een schattingsstatus van **Geëlimineerd**. De transactiestatus verandert nadat u de juiste velden hebt geselecteerd.

Hierdoor wordt ook automatisch de projectstatus gewijzigd in **Wordt uitgevoerd** als de projectfase is voltooid. De schattingsstatus van de projectperiode verandert weer naar **Geboekt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]