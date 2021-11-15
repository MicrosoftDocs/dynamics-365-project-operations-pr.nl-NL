---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 37, v3
description: Dit onderwerp biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Update-versie 37, V3 van Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727599"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 37, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 37, V3. Deze versie heeft als buildnummer V3.10.58.120 en is algemeen beschikbaar via een zelfupdate in november 2021.

## <a name="update-release-37"></a>Updaterelease 37

### <a name="bug-fixes"></a>Bugfixes

De volgende problemen zijn opgelost.

**Tijd en onkosten**
- Gebruikers kunnen een tijdsvermelding niet verwijderen door de cel te wissen.
- De weergave **Mijn mislukte goedkeuring** bevat alleen projectgoedkeuringen met de status **Ingediend**.

**Projectbeheer**
- Voor gebruikers wordt een null-referentie-uitzonderingsfout gegenereerd wanneer ze een project in de Microsoft Desktop-invoegtoepassing openen als de positienaam van het projectteamlid leeg is.
- Er is geen knop **Opslaan** op de pagina **Projecttaak**, zodat gebruikers geen wijzigingen in taakrecords kunnen opslaan.
- Gebruikers kunnen geen project verwijderen waarin een taak is opgenomen die is gekoppeld aan een prijsopgave met de status **Binnengehaald**.

**Verkoop**
- Het veld **Valuta** op de pagina **Project** wordt bijgewerkt zodat dit overeenkomt met de valuta van de toegepaste sjabloon.
- De kosten worden onjuist berekend voor taken met meerdere valuta's.
