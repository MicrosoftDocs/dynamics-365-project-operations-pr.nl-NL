---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 29, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 29, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499665"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 29, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 29. Deze versie heeft buildnummer V3.10.45.98 en is algemeen beschikbaar via een zelfupdate in februari 2021.

## <a name="update-release-29"></a>Updaterelease 29

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Gebruikers kunnen de geregistreerde werkuren op niet-werkdagen niet zien in het raster voor tijdsvermelding.
- Goedgekeurde onkostenposten kunnen in het raster worden bewerkt.

**Projectbeheer**

De volgende problemen zijn opgelost:

- Ontbrekende validatielogica om ervoor te zorgen dat inspanningsuren voor resourcetoewijzing niet negatief kunnen zijn.
- De aangepaste actie, **AssignResourcesForTask** werkt alle velden bij in plaats van alleen gewijzigde velden.
- Bij het kopiëren van een project in een omgeving met invoegtoepassingen of werkstromen die zijn geregistreerd voor de gebeurtenis **Createproject**, wordt het kenmerk **msdyn_bulkgenerationstatus** niet bijgewerkt als het **CopyWBSToProject** mislukt.
- Wanneer u de projectkalender uitvouwt, worden de werkdagen niet in oplopende volgorde gesorteerd, waardoor sommige updates van projecttaken mislukken.
- Als de projectmanager wordt gewijzigd voor een bestaand project wordt de standaardlogica van de organisatie-eenheid geactiveerd.

**Verkoop**

De volgende problemen zijn opgelost:

- Het tabblad **Contractprestaties** op de pagina **Contract** mislukt zonder melding tijdens de initialisatie als er geen contractregels aanwezig zijn.
