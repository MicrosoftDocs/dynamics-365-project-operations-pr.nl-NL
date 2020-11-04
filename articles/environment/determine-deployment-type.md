---
title: Het type implementatie bepalen
description: Dit onderwerp biedt informatie waarmee u het juiste implementatietype van projectactiviteiten voor uw bedrijf kunt bepalen.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074568"
---
# <a name="determine-your-deployment-type"></a>Het type implementatie bepalen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

> [!IMPORTANT]
> Nadat u de licentie hebt aangeschaft, begint u hier om het beste implementatiemodel van Dynamics 365 Project Operations te bepalen met behulp van de [begeleide installatiestroom](https://aka.ms/provisionprojectoperations).
> Nadat u de begeleide installatiestroom hebt voltooid, wordt u naar de juiste beheerportal geleid om uw installatie te voltooien. Zie de implementatiedetails om de installatie te voltooien.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Bestaande klanten van Dynamics die Dynamics 365 Project Service Automation gebruiken
Project Operations omvat de mogelijkheden die bij Project Service Automation worden geleverd. Voor deze klanten wordt in de toekomst een upgradepad vrijgegeven.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Bestaande klanten van Dynamics 365 Finance die Projectmanagement en financiële administratie gebruiken 

Bestaande klanten van Finance die gebruikmaken van de functionaliteit Projectmanagement en financiële administratie, kunnen dit zo blijven doen. Zie [Project Operations voor scenario's op basis van voorradige artikelen/productieorders](#pma).


## <a name="deployment-types"></a>Implementatietypen
Project Operations ondersteunt meerdere implementatieopties om aan uw vereisten te voldoen. Of u nu een nieuwe of bestaande Dynamics 365-klant bent, Project Operations kan uw behoeften ondersteunen.

Onze [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations) helpt u de juiste implementatie te kiezen. De resultaten leiden u naar een van de volgende implementatietypen:

- [Lite-implementatie – van deal tot pro-formafacturering](#lite)
- [Project Operations voor scenario's op basis van resources/niet-voorradige artikelen](#integrated)
- [Project Operations voor scenario's op basis van voorradige artikelen/productieorders](#pma)

Project Operations ondersteunt scenario's op basis van voorradige artikelen/productieorders en scenario's op basis van niet-voorradige artikelen/resources in dezelfde omgeving via configuraties op rechtspersoonsniveau. Contoso kan bijvoorbeeld de mogelijkheden voor voorradige artikelen/productieorder gebruiken in de productiefaciliteit in de VS (rechtspersoon = Contoso Manufacturing, Verenigde Staten). Contoso kan de mogelijkheden voor niet-voorradige artikelen/resource gebruiken in hun servicefaciliteit voor Contoso Robotics Arms in het VK (rechtspersoon = Contoso Robotics Verenigd Koninkrijk).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Vereenvoudigde implementatie - van deal tot pro-formafacturering

De Lite-implementatie omvat de volgende mogelijkheden:

- Projectplanning met Microsoft Project voor het web
- Multidimensionale prijzen
- Geïntegreerd resourcebeheer
- Tijden bijhouden
- Basisonkosten
- Factuurvoorstel

#### <a name="deployment-steps"></a>Installatiestappen
Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).

Zie voor deze implementatie [Aanmelden voor preview-abonnementen](lite-preview-subscription-sign-up.md) en [Nieuwe omgeving inrichten](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
Project Operations biedt voor scenario's voor resources/niet-voorradige artikelen de volgende mogelijkheden:
  
- Projectplanning met Microsoft Project voor het web
- Multidimensionale prijzen
- Geïntegreerd resourcebeheer
- Tijden bijhouden
- Basisonkosten
- Volledige onkosten
- OCR ontvangst
- Volledige facturering
- Omzetverantwoording

#### <a name="deployment-steps"></a>Installatiestappen
Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).

Zie voor deze implementatie [Aanmelden voor preview-abonnementen](resource-sign-up-preview-subscription.md) en [Nieuwe omgeving inrichten](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations voor scenario's op basis van voorradige artikelen/productieorders

- Projectplanning met structuur voor werkspecificatie
- Resourcebeheer
- Tijden bijhouden
- Volledige onkosten
- OCR ontvangst
- Volledige facturering
- Omzetverantwoording
- Productieorders
- Ondersteuning voor materiaal

#### <a name="deployment-steps"></a>Installatiestappen
Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).

Zie voor deze implementatie [Aanmelden voor preview-abonnementen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) en [Nieuwe omgeving inrichten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

