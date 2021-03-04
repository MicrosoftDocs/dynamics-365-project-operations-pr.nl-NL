---
title: Projectsjablonen
description: Dit onderwerp bevat informatie over het gebruik van projectsjablonen om snel projectinstellingen te kunnen configureren.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148052"
---
# <a name="project-templates"></a>Projectsjablonen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Een projectsjabloon is een vooraf gedefinieerd kader dat u in staat stelt snel en eenvoudig een project te starten. U kunt een vooraf gedefinieerde sjabloon gebruiken om met één klik een nieuw project te maken. Voor projecten moet u de vereisten voor projectsjablonen definiëren. U moet een projectagenda definiëren voor elke projectsjabloon en rollen en prijslijsten moeten vooraf worden gedefinieerd in de organisatie, zodat de onderdelen van de sjabloon nuttige gegevens bevatten.

Een projectsjabloon bestaat uit drie onderdelen: een planning, projectschattingen en projectteamleden.

## <a name="schedule"></a>Planning

Een planning in een projectsjabloon heeft dezelfde set elementen als een planning in een project. U kunt een taakhiërarchie maken, rollen aan taken koppelen, planningskenmerken definiëren en afhankelijkheden instellen. Een planning in een projectsjabloon ondersteunt ook de taakmodi voor elke taak. Daarom wordt ook de planningsengine ondersteund. U moet een projectagenda koppelen aan het project. Wanneer u een werkplanning maakt, is er geen verschil tussen een projectsjabloon en een project.

## <a name="project-estimates"></a>Projectschattingen

Projectschattingen in een projectsjabloon werken op dezelfde manier als projectschattingen in een project. De kosten en verkoopprijzen worden echter opgehaald uit de standaardlijsten met kosten en verkoopprijzen die in de parameters zijn gedefinieerd.

## <a name="creating-a-project-from-a-template"></a>Een project maken op basis van een sjabloon
 
Er zijn verschillende manieren om een project te maken op basis van een projectsjabloon:

- Wanneer u een project maakt op basis van een prijsopgave, kunt u een projectsjabloon selecteren in het dialoogvenster **Snelle invoer: Project**.

> ![Het dialoogvenster Snelle invoer: Project](media/project-11.png)

- Wanneer u een project maakt door **Nieuw project** te selecteren, wordt de pagina **Project** weergegeven voordat de record wordt opgeslagen. Selecteer in het veld **Een sjabloon kiezen** een van de vooraf gedefinieerde projectsjablonen in de organisatie.
- Gebruik **Een project maken op basis van een sjabloon** op de pagina **Sjabloonentiteit**.

## <a name="copying-components-of-template-to-project"></a>Onderdelen van een sjabloon kopiëren naar een project

Wanneer u de onderdelen van een projectsjabloon naar een project kopieert, kunnen er enkele overschrijvingen plaatsvinden, afhankelijk van de instellingen in het project.

### <a name="copying-the-schedule"></a>De planning kopiëren

Wanneer u de planning van een projectsjabloon kopieert, maar het project een andere projectagenda heeft dan de sjabloon, worden de werkuren van de agenda van het project toegepast op de taakplanning. Op deze manier wordt de planning aangepast, zodat deze overeenkomt met de achterliggende projectagenda. Zo wordt door de eerste taak in de planning ook de begindatum van het project overgenomen en wordt de planning van het resterende deel van de hiërarchie bijgewerkt op basis van de duur en de afhankelijkheden die in de sjabloon zijn opgegeven. 

### <a name="copying-project-estimates"></a>Projectschattingen kopiëren 

Wanneer u meerdere projectschattingsregels kopieert, worden de prijslijsten bijgewerkt. Voor de kostprijslijst zijn deze updates gebaseerd op de eenheid die eigenaar is van het project. Voor de verkoopprijslijst zijn deze updates gebaseerd op de klant. Bij projecten die zijn gekoppeld aan een verkoopentiteit, worden de kosten per eenheid en de verkoopprijzen bepaald aan de hand van deze prijslijsten.

### <a name="copying-a-project-team"></a>Een projectteam kopiëren

Wanneer een projectteam van een projectsjabloon naar een project wordt gekopieerd, worden de algemene resources gekopieerd, samen met de vaardigheden en deskundigheden die in de sjabloon zijn gedefinieerd. Algemene resourcetoewijzingen worden ook onderhouden, net zoals in de projectsjabloon. Benoemde resources worden niet ondersteund in projectsjablonen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]