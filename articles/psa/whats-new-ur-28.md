---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 28, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 28, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150617"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 28, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dit onderwerp geeft een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation V3, Updateversie 28. Deze versie heeft buildnummer V3.10.46.32 en is algemeen beschikbaar via een zelfupdate in januari 2021.

## <a name="update-release-28"></a>Updaterelease 28

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Gebruikers kunnen **Bulkbewerking** gebruiken om tijdsvermeldingen die zijn goedgekeurd en ingediend bij te werken.

**Projectbeheer**

De volgende problemen zijn opgelost:

- In gevallen waarin de taak-GUID wordt geïnterpreteerd als een getal, kunnen taken niet worden geopend voor bewerking met **Taak bewerken** in het lint op de pagina **Structuur voor werkspecificatie**.

**Sales**

De volgende problemen zijn opgelost:

- Er wordt een null-referentie-uitzondering gegenereerd wanneer de invoegtoepassing **GetEstimatesForproject** wordt aangeroepen.
- **Markeren als klaar voor facturering** op het mijlpaalraster werkt kenmerken slechts gedeeltelijk bij, behalve voor het kenmerk **InvoiceStatus**, dat wel wordt bijgewerkt.
