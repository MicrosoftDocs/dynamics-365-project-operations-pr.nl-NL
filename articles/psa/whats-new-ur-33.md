---
title: Wat is er nieuw of gewijzigd in Project Service Automation updateversie 33, v3
description: In dit artikel worden de functies en oplossingen vermeld die beschikbaar zijn in Project Service Automation-updateversie 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915410"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updateversie 33, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit artikel worden de functies en oplossingen vermeld die nieuw of gewijzigd zijn voor Project Service Automation-updateversie 33, V3. Deze versie heeft een buildnummer van V3.10.54.98 en is algemeen beschikbaar via een zelfupdate in juli 2021.

## <a name="update-release-33"></a>Updateversie 33

### <a name="bug-fixes"></a>Opgeloste fouten

**Tijd en onkosten**

De volgende problemen zijn opgelost:

- Twee vergrendelde velden, **msdyn_description** en **msdyn_externaldescription** zijn bewerkbaar na indiening.
- Er treedt een foutbericht op als er onkosten worden gemaakt die niet gerelateerd zijn aan een project.
- Wanneer een tijdsvermelding wordt gemaakt, wordt de resourcerol standaard ingesteld op een inactieve rol.
- Journaalregels die zijn gekoppeld aan ingetrokken en verwijderde onkosten, worden niet verwijderd.
- Werk in het **Formulier voor snelle invoer van tijdsvermelding** de **Projecttakenlijst** bij om de standaard weergegeven datum te wijzigen in de begindatum van de taak.
- Wanneer u een tijdsvermelding maakt via het tabblad **Gerelateerd** van de boekbare resource, is de tijdsvermelding onjuist gemaakt voor de aangemelde gebruiker in plaats van de bovenliggende boekbare resource.
- Nieuwe velden worden toegevoegd aan het dialoogvenster **Bulkgoedkeuring MDD**.

**Projectplanning**

De volgende problemen zijn opgelost:
- Trage prestaties bij het maken van projecten wanneer sjablonen voor projectwerkuren worden toegepast met complexe kalenders.
- Wanneer de begindatum later is dan de einddatum, wordt er een fout weergegeven in de kopieerprojectsjabloon vanwege verschillen in de tijdcomponent van elk veld.

**Resourcebeheer**

De volgende problemen zijn opgelost:
- Er wordt een onjuiste parameter gebruikt in de query voor resourcegebruik en de XML leidt tot onjuiste filterresultaten in het raster **Resourcegebruik**.
- De bevestiging **Boekingen verlengen** geeft de onjuiste einddatum voor boekingen weer.

**Verkoop**

De volgende problemen zijn opgelost:
- Er treedt een foutmelding op als er een categorieprijs wordt gemaakt met ontbrekende waarden.
- Er treedt een foutmelding op als een mijlpaal in de contractregel wordt gemaakt zonder een orderregel.
