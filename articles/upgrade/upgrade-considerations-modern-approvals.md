---
title: Overwegingen bij upgrades voor moderne goedkeuringen
description: In dit artikel worden de punten behandeld waarmee beheerders rekening moeten houden wanneer ze de functionaliteit Moderne goedkeuringen inschakelen.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931738"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Overwegingen bij upgrades voor moderne goedkeuringen 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Als onderdeel van de Wave 1-release van april 2022 wordt de functionaliteit Moderne goedkeuringen standaard ingeschakeld. Deze functionaliteit verbetert de betrouwbaarheid van de goedkeuringslogica en zorgt ervoor dat u de reden kunt bepalen als de goedkeuringslogica faalt.

Als onderdeel van deze wijziging worden statuswijzigingen voor projectgoedkeuringen bijgewerkt. De status gaat nu rechtstreeks van **Ingediend** naar **Goedgekeurd**. **In behandeling** is niet langer een status voor goedkeuringen. Om te bepalen of een goedkeuring in behandeling is, controleert u of de goedkeuring deel uitmaakt van een goedkeuringsset en controleert u de status van de bijgevoegde goedkeuringsset.

## <a name="before-you-upgrade"></a>Voordat u een upgrade uitvoert

Voordat u een upgrade naar Moderne goedkeuringen uitvoert, moet u ervoor zorgen dat er geen goedkeuringen in behandeling zijn. Moderne goedkeuringen maakt geen gebruik van de status **In behandeling**. Daarom worden alle goedkeuringen die na een upgrade nog als **In behandeling** zijn gemarkeerd niet verwerkt.

## <a name="after-you-upgrade"></a>Nadat u een upgrade uitvoert

Nadat u een upgrade naar Moderne goedkeuringen hebt uitgevoerd, moet een beheerder valideren dat de cloudstroom die goedkeuringen verwerkt, is ingeschakeld.

1. Meld u aan bij [flow.microsoft.com](https://flow.microsoft.com)
2. Schakel in de rechterbovenhoek van de pagina uw omgeving over naar de omgeving waarvoor u een upgrade hebt uitgevoerd.
3. Selecteer **Oplossingen** om een lijst weer te geven van de oplossingen die zijn geïnstalleerd in de omgeving.
4. Selecteer in de lijst met oplossingen de optie **Project Operations** of **Project Service**.
5. Verander het filter van **Alle** in **Cloudstromen**.
6. Controleer of de optie **Project Service – Projectgoedkeuringssets terugkerend plannen** is ingesteld op **Aan**. Als dit niet het geval is, selecteert u de stroom en selecteert u vervolgens **Inschakelen**.
7. Controleer of de verwerking elke vijf minuten plaatsvindt door de lijst **Systeemtaken** lijst in het gebied **Instellingen** te raadplegen.

## <a name="short-term-rollback"></a>Terugdraaiactie op korte termijn

Als u de wijzigingen niet kunt overnemen of als u een ernstig probleem ondervindt met deze functie, kunt u tijdelijk terugkeren naar de oorspronkelijke goedkeuringsstroom door de volgende stappen uit te voeren:
1. Meld u aan bij uw omgeving en controleer of er geen goedkeuringen in behandeling zijn.
2. Ga naar **Instellingen** > **Projectparameters**.
3. Selecteer **Besturingselement voor functie** en selecteer vervolgens **Moderne goedkeuringen** om de functie uit te schakelen.

## <a name="removing-the-feature-flag"></a>De functievlag verwijderen

In de Wave 2-update van oktober 2022 wordt de mogelijkheid om deze functie uit te schakelen verwijderd.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
