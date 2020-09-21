---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 12, v3
description: Dit onderwerp bevat informatie over wat er nieuw en gewijzigd is in Project Service Automation updaterelease 12, v3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750755"
---
# <a name="project-service-automation-v3-update-release-12"></a>Wat is er nieuw of gewijzigd in Project Service Automation v3, updaterelease 12
Met genoegen kondigen we de nieuwste update voor de toepassing Dynamics 365 Project Service Automation (PSA) aan. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365. Hierin gaat u naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 12. Deze versie heeft het buildnummer V3.10.2.34 en is algemeen beschikbaar via een zelf-update vanaf oktober 2019.

## <a name="update-release-12"></a>Updaterelease 12

### <a name="bug-fixes"></a>Bugfixes

- Tijd en onkosten

    - Opgelost: foutberichten bij tijdinvoer zijn voorzien van een meer relevante context.
    - Opgelost: raster en planning voor tijdinvoer geven waar nodig de verticale schuifbalk correct weer.
    - Opgelost: ingediende vermeldingen voor kosten en tijd kunnen worden goedgekeurd.
    - Opgelost: het dialoogvenster Goedkeuring annuleren is gecorrigeerd en geeft nu de status van de goedkeuring weer wanneer deze wijzigt van **Goedgekeurd** naar **Ingediend**.
    - Opgelost: de velden **Prijs**, **Eenheid** en **Aantal** worden nu vergrendeld in de onkostenrecord nadat deze is goedgekeurd.

- Projectbeheer

    - Opgelost: de actie **Nieuw** op het hoofdformulier **Teamlid** is verwijderd.
    - Opgelost: resourcetoewijzingen zijn bijgewerkt en houden nu rekening met onnauwkeurige afrondingsfouten, die leiden tot het verschuiven van de einddatum van een taak.
    - Opgelost: in het taakraster worden relevante serverfouten zichtbaar gemaakt voor de gebruiker.
    - Opgelost: de naam van het teamlid wordt nu weergegeven in de taakkiezer in plaats van de positienaam.

- Resourcebeheer

    - Opgelost: details van de resourcevereisten voor projecten die met een sjabloon zijn gemaakt, maken nu gebruik van de projectagenda.
    - Opgelost: vaardigheden en competenties gaan nu standaard van rolstamgegevens naar de resourcevereiste die voor die rol is gemaakt.

- Sales

    - Opgelost: dubbele object-id's werden aangetroffen op het hoofdformulier **Contract**.
    - Opgelost: logica is bijgewerkt en maakt nu het tabblad **Analyse prijsopgave** zichtbaar, zodat het de metadata-instellingen van het tabblad weergeeft.
    - Opgelost: de datum in financiële administratie in de werkelijke record komt nu van de datum van de tijd/kosteninvoerdatum en niet de datum van de goedkeuring.
