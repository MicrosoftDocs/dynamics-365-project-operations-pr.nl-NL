---
title: Projectsjablonen ontwikkelen met Project kopiëren
description: Dit onderwerp bevat informatie over het maken van projectsjablonen met de aangepaste actie Project kopiëren.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074504"
---
# <a name="develop-project-templates-with-copy-project"></a>Projectsjablonen ontwikkelen met Project kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations ondersteunt de mogelijkheid om een project te kopiëren en eventuele toewijzingen terug te zetten naar de algemene bronnen die de rol vertegenwoordigen. Klanten kunnen deze functionaliteit gebruiken om eenvoudige projectsjablonen te maken.

Als u **Project kopiëren** selecteert, wordt de status van het doelproject bijgewerkt. Gebruik **Reden van status** om te bepalen wanneer de kopieeractie is voltooid. Door **Project kopiëren** te selecteren, wordt ook de begindatum van het project bijgewerkt naar de huidige begindatum als er geen streefdatum wordt gedetecteerd in de doelprojectentiteit.

## <a name="copy-project-custom-action"></a>Aangepaste actie Project kopiëren 

### <a name="name"></a>Meetcriterium 

**msdyn_CopyprojectV2**

### <a name="input-parameters"></a>Invoerparameters
Er zijn drie invoerparameters:

| Parameter          | Type   | Waarden                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** of **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entiteitverwijzing | Bronproject |
| Doel             | Entiteitverwijzing | Doelproject |


- **{"clearTeamsAndAssignments":true}** : het standaardgedrag voor Project for the Web; hiermee worden alle toewijzingen en teamleden verwijderd.
- **{"removeNamedResources":true}** : het standaardgedrag voor Project Operations; hiermee worden toewijzingen teruggezet naar algemene resources.

Zie [Web-API -acties gebruiken](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions) voor meer standaardwaarden voor acties.

## <a name="specify-fields-to-copy"></a>Te kopiëren velden opgeven 
Wanneer de actie wordt aangeroepen, wordt met **Project kopiëren** de projectweergave **Projectkolommen kopiëren** gecontroleerd om te bepalen welke velden moeten worden gekopieerd wanneer het project wordt gekopieerd.
