---
title: Een projectsjabloon maken
description: Informatie over een projectsjabloon maken in Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149357"
---
# <a name="create-a-project-template-project-service"></a>Een projectsjabloon maken (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projectsjablonen besparen u tijd als uw bedrijf regelmatig op soortgelijke projecttypen biedt. Ze bieden een standaardset van rollen en geschatte uren voor een type project. Accountmanagers en projectmanagers kunnen projecten maken op basis van een projectsjabloon of ze kunnen de sjabloon kopiëren en een eigen project maken.  
  
## <a name="components-of-project-template"></a>Onderdelen van een projectsjabloon
 Een projectsjabloon bestaat uit drie onderdelen:  
  
- **Structuur voor werkspecificatie**: een structuur voor werkspecificatie in een projectsjabloon heeft dezelfde verzameling elementen als in het project. U kunt een taakhiërarchie maken, rollen aan de taak koppelen, planningskenmerken definiëren, afhankelijkheden instellen en alle gegevens weergeven in Gantt. De structuur voor werkspecificatie in projectsjablonen ondersteunt ook taakmodi voor elke taak. Er is geen verschil tussen een projectsjabloon en een project bij het maken van een werkplanning.  
  
- **Projectschattingen**: projectschattingen in sjablonen werken op dezelfde manier als in projecten, behalve dat de prijslijsten standaard altijd worden ingesteld op de standaardkosten en de standaardverkoopprijslijsten die in de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-parameters zijn gedefinieerd. De rest van de functionaliteit is hetzelfde als in een project.  
  
- **Projectteamvorming**: als u een projectteam vormt voor een projectsjabloon, kunt u geen benoemde resource in een sjabloon boeken. U kunt **Projectteam genereren** in de structuur voor werkspecificatie gebruiken om een set algemene resources te genereren. U kunt ook de vereiste vaardigheden en deskundigheden voor algemene resources opgeven. U kunt een algemene resource niet vervangen met een boekbare resource in projectsjablonen.  
  
## <a name="create-a-project-from-a-template"></a>Een project maken op basis van een sjabloon  
 U kunt een project op de volgende manieren op basis van een sjabloon maken:  
  
-   Bij het maken van een project op basis van de prijsopgave kunt u een projectsjabloon in het projectformulier voor snelle invoer kiezen.  
  
-   Wanneer u een project maakt door te klikken op **Nieuw project**, wordt het projectformulier weergegeven voordat u de record opslaat. Vanaf hier kunt u klikken op het veld **Een sjabloon kiezen** om een keuze te maken in de lijst met vooraf gedefinieerde projectsjablonen in uw organisatie.  
  
-   Klik op **Projecten maken van een sjabloon** op de pagina **Projectsjabloon** om een project op basis van de sjabloon te maken.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Onderdelen van een sjabloon kopiëren naar een project  
 Wanneer u onderdelen van een sjabloon naar een project kopieert, zijn er enkele dingen die u moet weten.  
  
 **Een structuur voor werkspecificatie kopiëren**: als u de structuur voor werkspecificatie van een projectsjabloon kopieert, worden als het project een andere projectkalender dan de sjabloon heeft, de werkuren van de agenda van het project toegepast op de planning van taken. Hiermee wordt de planning aangepast aan de ondersteunende projectkalender. Op dezelfde manier gebruikt de eerste taak in de structuur voor werkspecificatie de begindatum van het project, waardoor de rest van de planning van de taakhiërarchie wordt bijgewerkt op basis van de duur en de afhankelijkheden die in de structuur voor werkspecificatie van de sjabloon zijn opgegeven.  
  
 **Projectschattingen kopiëren**: als u schattingsregels van meerdere projecten kopieert, worden prijslijsten bijgewerkt op basis van de eenheid die eigenaar is van het project voor de kostprijslijst en klant voor de verkoopprijslijst. De kosten per eenheid en de verkoopprijzen worden bepaald aan de hand van deze prijslijsten in projecten die aan een verkoopentiteit zijn gekoppeld.  
  
 **Een projectteam kopiëren**: als u het projectteam op basis van een sjabloon kopieert naar een project, worden de algemene resources gekopieerd samen met de vaardigheden en de deskundigheden die in de sjabloon zijn gedefinieerd. Algemene resourcetoewijzingen worden ook onderhouden zoals in de projectsjabloon.  
  
### <a name="see-also"></a>Zie ook  
 [Projectmanager-handleiding](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]