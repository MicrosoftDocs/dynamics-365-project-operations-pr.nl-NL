---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 41, v3
description: Dit onderwerp biedt een overzicht van de functies en oplossingen die beschikbaar zijn in Update-versie 41, V3 van Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580910"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 41, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 41, V3. Deze versie heeft het buildnummer V3.10.62.162 en is algemeen beschikbaar via een zelf-update vanaf maart 2022.

## <a name="update-release-41"></a>Updaterelease 41

### <a name="bug-fixes"></a>Opgeloste fouten

De volgende problemen zijn opgelost.

**Projectbeheer**
- Wanneer u probeert een project te maken op basis van een sjabloon die is gebaseerd op een project dat is gemaakt met de invoegtoepassing voor bureaublad, wordt de volgende fout weergegeven: "Validatie van het veld Gepland werk voor resourcetoewijzing: de einddatum van een tijdssegment voor resourcetoewijzing mag niet vóór de begindatum vallen.".

**Tijd en onkosten**
- Wanneer u een tijdsvermelding probeert te verwijderen, wordt het volgende foutbericht weergegeven: "Er is een onverwachte fout opgetreden door de ISV-code".

**Verkoop**
- Wanneer u een factuur maakt voor een mijlpaal met een vaste prijs, worden de velden **Beschrijving** en **Externe beschrijving** niet gevuld. 
