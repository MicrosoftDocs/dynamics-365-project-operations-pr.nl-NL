---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 30, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 30, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: f99d2df3f9f6c0752109c39132c2401e0130d5df
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723534"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 30, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 30. Deze versie heeft een buildnummer van V3.10.51.61 en is algemeen beschikbaar via een zelfupdate in april 2021.

## <a name="update-release-30"></a>Updaterelease 30

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Er treedt een fout op wanneer u een tijdsvermelding maakt en opslaat op de pagina **Snelle invoer** als het veld **Rol** is verwijderd.
- Het filter Tijdsvermelding past de verkeerde filteroperator toe.
- Gekopieerde urenstaten worden niet automatisch weergegeven wanneer u **Week kopiëren** selecteert in het besturingselement voor tijdsinvoer.

**Resourcebeheer**

De volgende problemen zijn opgelost:

- Wanneer u een boeking verlengt, is de boekingsstatus die aan de harde boeking is toegewezen onjuist. Bij het verlengen van een boeking wordt de boekingsstatus gedefinieerd als **Toegezegd** in de metagegevens van de boekingsinstellingen gerespecteerd.
- Als er geen geldige boekingsstatus is opgegeven, wordt het foutbericht niet correct gelokaliseerd.

**Projectbeheer**

De volgende problemen zijn opgelost:

- Projecten kunnen niet in de ene valuta worden gemaakt en gerelateerde taken in een andere valuta bevatten.

**Verkoop**

De volgende problemen zijn opgelost:

- Wanneer een prijslijst wordt gekopieerd, worden prijzen niet bijgewerkt.
- Het sluiten van een prijsopgave als gewonnen mislukt als de kostendetails een waarde voor de oorsprong hebben.
- Voor de entiteit **Projecttaak** is de naam **Geschatte kosten** gewijzigd in **Geplande kosten (basis)** ​.
- Een null-referentie-uitzondering wordt gegenereerd wanneer er facturen worden gemaakt of verwijderd.
