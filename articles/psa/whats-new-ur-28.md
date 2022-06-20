---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 28, v3
description: In dit artikel worden de functies en oplossingen vermeld die beschikbaar zijn in Project Service Automation-updateversie 28, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930588"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 28, v3

[!include [banner](../includes/psa-now-project-operations.md)]

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation V3, updateversie 28.5. Deze versie heeft buildnummer V3.10.46.32 en is algemeen beschikbaar via een zelfupdate in januari 2021.

## <a name="update-release-28"></a>Updateversie 28

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
