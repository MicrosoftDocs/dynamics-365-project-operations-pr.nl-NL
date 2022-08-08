---
title: Een projectsjabloon maken
description: Informatie over een projectsjabloon maken in Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
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
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177419"
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

## <a name="create-a-project-template-from-an-existing-project"></a>Een projectsjabloon maken van een bestaand project
U kunt op de volgende manieren een projectsjabloon maken op basis van een project:

- **Structuur voor werkspecificatie**: een structuur voor werkspecificatie in een sjabloon die is afgeleid van een project kopieert alle taken en afhankelijkheden. De toewijzingen die worden gemaakt, zijn gebaseerd op de generieke teamleden die aan het projectteam worden toegevoegd tijdens het maken van de projectsjabloon.
- **Projectschattingen**: wanneer een projectsjabloon wordt gemaakt op basis van een bestaand project, worden de schattingen van het bronproject gekopieerd naar de projectsjabloon.
- **Projectteamleden**: wanneer een sjabloon wordt gemaakt op basis van een bestaand project, worden alle benoemde teamleden vervangen door de algemene resource van de organisatie. Alle functienamen en rollen blijven behouden.

## <a name="create-a-project-from-a-template"></a>Een project maken op basis van een sjabloon  
 U kunt op de volgende manieren een project maken op basis van een sjabloon:  
  
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
