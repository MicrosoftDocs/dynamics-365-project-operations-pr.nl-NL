---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 25, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 25, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2d24403b1bf6a06cc138de3f0158f675f6d3b6ec
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581508"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 25, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

Dit onderwerp geeft een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation V3, Update versie 25. Deze versie heeft buildnummer V 3.10.43.76 en is algemeen beschikbaar via een zelfupdate in oktober 2020.

## <a name="update-release-25"></a>Updaterelease 25

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

Het volgende probleem is opgelost:

- Tijdinvoergrafiek met aanvullende gegevens op basis van een te groot interval dat wordt opgehaald.

**Resourcebeheer**

Het volgende probleem is opgelost:

- Package Deployer-code toegevoegd om het importeren van Universal Resource Scheduling-patch over te slaan als er al een patch uit een hogere versie bestaat.

**Projectbeheer**

De volgende problemen zijn opgelost:

- Afrondings- en wisselkoersverschillen gecorrigeerd die resulteren in onjuiste geplande kosten in het projectvolgraster.
- Ondersteuning van de mogelijkheid om twee of meer reactierasters weer te geven op het formulier **Project**.
- Validatie voor de mogelijkheid om een taak toe te wijzen na de einddatum van de kalender, wat resulteert in een mislukte toewijzing van resources.
- Verbeterde foutafhandeling om een uitzondering met een null-verwijzing te verwerken die is gegenereerd op basis van het volgende:

    - Invoegtoepassing **PreValidateProjectTeamMemberCreate**
    - **PreValidateprojectTaskCreate** wanneer een projecttaak wordt gemaakt zonder een bijbehorend project
    - Invoegtoepassing **PreProjectTeamMemberCreate**
    - Invoegtoepassing **PostProjectTeamMemberDelete**
    - invoegtoepassing **PreValidateProjectTaskDelete**

**Sales**

De volgende problemen zijn opgelost:

- Verbeterde foutafhandeling om uitzonderingen met null-verwijzingen te verwerken die zijn gegenereerd op basis van **Project kopiëren: schattingen van HelperResource Management**.
- Bij **Niet gereed voor facturering** voor **Achterstallige facturering van tijd en materiaal** wordt de factureringsstatus niet gewist.
- Gecorrigeerd verkeerd label voor knoppen **Prijzen** op het tabblad **Rolprijs** en **Catalogusartikelen**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
