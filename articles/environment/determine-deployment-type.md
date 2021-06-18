---
title: Het type implementatie bepalen
description: Dit onderwerp biedt informatie waarmee u het juiste implementatietype van projectactiviteiten voor uw bedrijf kunt bepalen.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997100"
---
# <a name="determine-your-deployment-type"></a>Het type implementatie bepalen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

> [!IMPORTANT]
> Nadat u de licentie hebt aangeschaft, begint u hier om het beste implementatiemodel van Dynamics 365 Project Operations te bepalen met de [Begeleide installatiestroom](https://aka.ms/provisionprojectoperations).
> Nadat u de begeleide installatiestroom hebt voltooid, wordt u naar de juiste beheerportal geleid om uw installatie te voltooien. Zie de implementatiedetails om de installatie te voltooien.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Bestaande klanten van Dynamics die Dynamics 365 Project Service Automation gebruiken
Project Operations omvat de mogelijkheden die bij Project Service Automation worden geleverd. In releasewave 1 van 2021 wordt voor deze klanten een upgradepad vrijgegeven.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Bestaande klanten van Dynamics 365 Finance die Projectmanagement en financiële administratie gebruiken 

Bestaande klanten van Finance die de functionaliteit Projectbeheer en financiële administratie gebruiken, kunnen deze gewoon blijven gebruiken. Zie [Project Operations voor scenario's op basis van voorradige artikelen/productieorders](#pma).


## <a name="deployment-regions"></a>Implementatieregio's
Zie [Geografische beschikbaarheid voor Dynamics 365 en Power Platform-rapport](https://dynamics.microsoft.com/en-us/geographic-availability/) om te bepalen welke regio's de implementatie van Project Operations ondersteunen. Selecteer **Rapport weergeven** en vouw **Dynamics 365> Operations-apps > Dynamics 365 Project Operations** uit om de ondersteunde regio's te bekijken.

## <a name="deployment-types"></a>Implementatietypen
Project Operations ondersteunt meerdere implementatieopties om aan uw vereisten te voldoen. Of u nu een nieuwe of bestaande Dynamics 365-klant bent, Project Operations kan uw behoeften ondersteunen.

Onze [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations) helpt u de juiste implementatie te kiezen. De resultaten leiden u naar een van de volgende implementatietypen:

- [Lite-implementatie – van deal tot pro-formafacturering](#lite)
- [Project Operations voor scenario's op basis van resources/niet-voorradige artikelen](#integrated)
- [Project Operations voor scenario's op basis van voorradige artikelen/productieorders](#pma)

Project Operations ondersteunt scenario's op basis van voorradige artikelen/productieorders en scenario's op basis van niet-voorradige artikelen/resources in dezelfde omgeving via configuraties op rechtspersoonsniveau. Contoso kan bijvoorbeeld gebruikmaken van de mogelijkheden voor voorraad/productieorders in hun Amerikaanse productiefaciliteit (Rechtspersoon = Contoso Manufacturing United States). Contoso kan de mogelijkheden op basis van niet-voorradige artikelen/resources in hun servicefaciliteit Contoso Robotics Arms in het VK (rechtspersoon = Contoso Robotics United Kingdom) gebruiken.

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lite-implementatie - van deal tot pro-formafacturering

De Lite-implementatie omvat de volgende mogelijkheden:

- Verkoopproces voor projecten waarbij de voorzieningen van Dynamics 365 Sales-toepassingen worden uitgebreid
- Projectplanning met Microsoft Project voor het web
- Multidimensionale prijzen
- Geïntegreerd resourcebeheer
- Tijden bijhouden
- Basisonkosten
- Pro-formafacturering voor beoordeling en bewerkingen van de projectmanager 

#### <a name="deployment-steps"></a>Installatiestappen
Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).

Zie voor deze implementatie [Aanmelden voor preview-abonnementen](lite-preview-subscription-sign-up.md) en [Nieuwe omgeving inrichten](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
Project Operations biedt voor scenario's voor resources/niet-voorradige artikelen de volgende mogelijkheden:
 
- Verkoopproces voor projecten waarbij de Dynamics 365 Sales-toepassing wordt uitgebreid
- Projectplanning met Microsoft Project voor het web
- Multidimensionale prijzen
- Geïntegreerd resourcebeheer
- Tijden bijhouden
- Basisonkosten
- Volledige onkosten
- OCR ontvangst
- Pro-forma- en klantgerichte facturering 
- Opbrengstverantwoording voor projecten

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
- Ondersteuning voor voorradig materiaal met inventaris

#### <a name="deployment-steps"></a>Installatiestappen
Bepaal het beste implementatiemodel van Project Operations met behulp van de [vragenlijst voor implementaties](https://aka.ms/provisionprojectoperations).

Zie voor deze implementatie [Aanmelden voor preview-abonnementen](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) en [Nieuwe omgeving inrichten](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]