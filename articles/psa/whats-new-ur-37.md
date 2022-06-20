---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 37, v3
description: Dit artikel biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Microsoft Dynamics 365 Project Service Automation-updateversie 37, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922492"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 37, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 37, V3. Deze versie heeft als buildnummer V3.10.58.120 en is algemeen beschikbaar via een zelfupdate in november 2021.

## <a name="update-release-37"></a>Updateversie 37

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
