---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 17, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 17, v3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074520"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, updaterelease 17, v3

Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.  Deze versie is compatibel met Dynamics 365 9.x. Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 17. Deze versie heeft het buildnummer V3.10.6.34 en is algemeen beschikbaar via een zelf-update vanaf maart 2020.


## <a name="update-release-17"></a>Updaterelease 17

### <a name="bug-fixes"></a>Bugfixes

**Algemeen**

- Opgelost: Project Service Automation bijwerken om Team Member-licenties af te dwingen (Hub voor projectresource bevat metagegevens voor Serviceplan voor teamlid 3.x)
 
**Tijd en onkosten**

- Opgelost: het is niet mogelijk om een kostenraming te wijzigen van een prijs die niet nul is naar nul (0). De wijziging wordt genegeerd.

**Projectbeheer**

- Opgelost: er is een controle op null-waarden toegevoegd aan de positienaam van een teamlid.
- Opgelost: het veld **msdyn_userresourceid** in de entiteit **msdyn_resourceassignment** is afgeschaft.
- Opgelost: door upgrade van 2.x naar 3.x worden nu lege inspanningscontouren verwerkt bij taakopdrachten.

**Sales**

- Opgelost: door **Invoice.PreValidateInvoiceUpdate** wordt nu het scenario van het toewijzen van recordeigenaren op de juiste manier verwerkt.
- Opgelost: wanneer de transactieklasse is **Tijd** , is **UnitGroup** niet bewerkbaar voor alle entiteiten, waaronder **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** en **ContractLineDetails**. **Eenheid** is echter niet bewerkbaar voor **JournalLine** en **InvoiceLineDetails**.


