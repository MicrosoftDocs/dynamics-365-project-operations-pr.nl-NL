---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 29, v3
description: In dit artikel worden de functies en oplossingen vermeld die beschikbaar zijn in Project Service Automation-updateversie 29, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 733bbad53933b2de62222e78e3c5c919543c59e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915363"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 29, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 29, V3. Deze versie heeft buildnummer V3.10.47.7 en is algemeen beschikbaar via een zelfupdate in februari 2021.

## <a name="update-release-29"></a>Updateversie 29

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
