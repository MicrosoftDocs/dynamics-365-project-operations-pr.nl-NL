---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 16, v3
description: In dit artikel worden de functies en oplossingen vermeld die beschikbaar zijn in Project Service Automation-updateversie 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e4429ace3d8206369b91917cf87f6968fbb12277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926494"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, updateversie 16, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.  Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren en bijwerken](/dynamics365/project-service/upgrade-psa-home-page).
In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor PSA V3, updateversie 16. Deze versie heeft het buildnummer V3.10.6.34 en is algemeen beschikbaar via een zelf-update vanaf januari 2020.


## <a name="update-release-16"></a>Updateversie 16

### <a name="bug-fixes"></a>Bugfixes

-   Tijd en onkosten

    -   Opgelost: gebruikers die proberen verwijderde tijds- en onkostenvermeldingen voor goedkeuring in te dienen, ontvangen nu relevante foutmeldingen.

-   Projectbeheer

    -   Opgelost: er wordt rekening gehouden met de resources die voor teamleden in sjablonen zijn gedefinieerd, terwijl de sjablonen worden toegepast op een nieuw project.

    -   Opgelost: verbeterde afhandeling van het opnieuw toewijzen van het eigendom van records.

    -   Opgelost: projecten die worden gekopieerd, mogen pas worden gekopieerd als alle kopieerbewerkingen zijn voltooid.

-   Resourcebeheer

    -   Opgelost: Boekingen uitbreiden verwerkt korte duur nu correct en creëert niet langer nul uur voor uitgebreide boekingen.

    -   Opgelost: de afstemmingsweergave wordt nu weergegeven wanneer de projecttijdzone +5:30 GMT is en alleen de tijd van de gebruiker anders is.

-   Sales

    -   Opgelost: wanneer een project dat aan een contractregel is toegewezen, wordt verwijderd en een nieuw project wordt toegewezen, werden de werkelijke records van het nieuwe project niet opnieuw geëvalueerd op basis van de facturerings- en prijsregels die op de contractregel waren gedefinieerd. Dit is opgelost in deze release. De prijzen en werkelijke records van het nieuw toegewezen project worden teruggedraaid en correct opnieuw gemaakt op basis van de prijs- en factureringsregels van de contractregel. De werkelijke records van het niet-toegewezen project zullen als gevolg daarvan ook opnieuw worden geëvalueerd en opnieuw worden gemaakt.

    -   Opgelost: er is extra validatie toegevoegd aan het veld **Bedrag** van de schattingsregel om ervoor te zorgen dat null-waarden niet worden behouden.

    -   Opgelost: wanneer werkelijke waarden zijn bijgewerkt in een project, is er een vernieuwingsknop toegevoegd aan het hoofdformulier van het project, zodat gebruikers de werkelijke waarden opnieuw kunnen synchroniseren.

    -   Opgelost: wanneer gebruikers upgraden van 2.X naar 3.X, zijn projecten met de waarde NULL voor de projectnaam toegestaan.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
