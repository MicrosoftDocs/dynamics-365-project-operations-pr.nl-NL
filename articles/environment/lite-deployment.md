---
title: Project Operations Lite implementeren
description: Dit artikel bevat informatie over het installeren van Project Operations Lite-implementatie - van deal tot pro-formafacturering.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810972"
---
# <a name="deploy-project-operations-lite"></a>Project Operations Lite implementeren

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_



Project Operations ondersteunt meerdere implementatiemodellen. Zie voor het bepalen van het beste implementatiemodel [Implementatietypen](determine-deployment-type.md).


> [!IMPORTANT]
> De Lite-implementatie - van deal tot proforma-facturering resulteert in een **Implementatie van Project Operations met alleen Dataverse**.

- [Project Operations installeren in een nieuwe Dataverse-omgeving](#new)
- [Installeren in een bestaande Dataverse-omgeving](#existing)
- [Installeren in een bestaande Dataverse-omgeving met twee keer wegschrijven-componenten](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations Lite in een nieuwe Dataverse-omgeving installeren

1. Als [algemene of Power Platform-beheerder](/power-platform/admin/global-service-administrators-can-administer-without-license) met een Project Operations-licentie maakt u een nieuwe Dataverse-omgeving in het [Power Platform-beheercentrum](https://admin.powerplatform.com). Zorg ervoor dat **Een database voor deze omgeving maken** en **Dynamics 365-apps** zijn ingeschakeld. Zie [Omgevingen maken en beheren in het Power Platform-beheercentrum](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) voor meer informatie.
1. Selecteer **Microsoft Dynamics 365 Project Operations** uit de implementatielijst met Dynamics 365-apps.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations Lite in een bestaande Dataverse-omgeving installeren 
1. Als [algemene of Power Platform-beheerder](/power-platform/admin/global-service-administrators-can-administer-without-license) met een Project Operations-licentie zoekt u de omgeving in het [PowerPlatform-beheercentrum](https://admin.powerplatform.com) waar u Project Operations wilt installeren.
1. Installeer **Microsoft Dynamics 365 Project Operations** uit de implementatielijst met Dynamics 365-apps. Zie [Dynamics 365-apps beheren](/power-platform/admin/manage-apps) voor meer informatie.

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Project Operations Lite in een bestaande Dataverse-omgeving installeren waar al oplossingen voor twee keer wegschrijven aanwezig zijn

Als u Project Operations wilt blijven uitvoeren in de Lite-implementatiemodus, volgt u deze stappen:

1. Als [algemene of Power Platform-beheerder](/power-platform/admin/global-service-administrators-can-administer-without-license) met een Project Operations-licentie zoekt u de omgeving in het [PowerPlatform-beheercentrum](https://admin.powerplatform.com) waar u Project Operations wilt installeren.
1. Installeer **Microsoft Dynamics 365 Project Operations** uit de implementatielijst met Dynamics 365-apps. Zie [Dynamics 365-apps beheren](/power-platform/admin/manage-apps) voor meer informatie.
1. Omdat uw omgeving twee keer wegschrijven-componenten heeft die helpen bij de integratie met geïnstalleerde financiële en operationele apps, worden bij de installatie van Project Operations ook de mogelijkheden en uitbreidingen geïnstalleerd die nodig zijn om projectgerelateerde gegevens te integreren in financiële en operationele apps. Aangezien u Project Operations in Lite-implementatie wilt uitvoeren, moeten deze integratiecomponenten worden verwijderd omdat ze beperkingen en overhead creëren voor Lite-implementatiescenario's. Verwijder handmatig de oplossingen **Dynamics 365 Project Operations voor twee keer wegschrijven** en **Dynamics 365 Project Operations-entiteitstoewijzingen voor twee keer wegschrijven** om deze componenten te verwijderen.
1. Ga naar **Project Operations -> Instellingen -> Parameters**. Open de detailpagina **Projectparameter** en stel het veld **Gedrag van oplossingsupgrade** in op **Alleen Lite**. Dit zorgt ervoor dat eventuele volgende Project Operations-upgrades de integratiecomponenten niet terugbrengen naar Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
