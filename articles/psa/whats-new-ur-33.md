---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 33, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 33, v3.
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
ms.openlocfilehash: a72202905fc0464577bb126aa5890a8f952dc3a8aff505416e535b42b53df7db
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006510"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 33, v3

[!include [banner](../includes/psa-now-project-operations.md)]

We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app. Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid. Deze app is compatibel met Dynamics 365 9.x. Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update. Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).

In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 33. Deze versie heeft een buildnummer van V3.10.54.98 en is algemeen beschikbaar via een zelfupdate in juli 2021.

## <a name="update-release-33"></a>Updaterelease 33

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
