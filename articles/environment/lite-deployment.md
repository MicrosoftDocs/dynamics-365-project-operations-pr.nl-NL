---
title: Project Operations implementeren - lite
description: In dit onderwerp vindt u informatie over hoe u de implementatie met Project Operations Lite installeert, van deal tot pro-formafacturering.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580726"
---
# <a name="deploy-project-operations---lite"></a>Project Operations implementeren - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_



Project Operations ondersteunt meerdere implementatiemodellen. Zie voor het bepalen van het beste implementatiemodel [Implementatietypen](determine-deployment-type.md).


> [!IMPORTANT]
> De Lite-implementatie - van deal tot proforma-facturering resulteert in een **Implementatie van Project Operations met alleen Dataverse**.

- [Project Operations installeren in een nieuwe Dataverse-omgeving](#new)
- [Installeren in een bestaande Dataverse-omgeving](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new">Project Operations in een nieuwe Dataverse-omgeving installeren</a>

1. Als [algemene of Power Platform-beheerder](/power-platform/admin/global-service-administrators-can-administer-without-license) met een Project Operations-licentie maakt u een nieuwe Dataverse-omgeving in het [Power Platform-beheercentrum](https://admin.powerplatform.com). Zorg ervoor dat **Een database voor deze omgeving maken** en **Dynamics 365-apps** zijn ingeschakeld. Zie [Omgevingen maken en beheren in het Power Platform-beheercentrum](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) voor meer informatie.
2. Selecteer **Microsoft Dynamics 365 Project Operations** uit de implementatielijst met Dynamics 365-apps.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing">Project Operations in een bestaande Dataverse-omgeving installeren</a>
1. Zorg ervoor dat de omgeving niet is geconfigureerd met [twee keer wegschrijven](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), omdat de installatie dan de mogelijkheden voor [Project Operations voor scenario's op basis van hulpbronnen/niet-voorraad](project-operations-integrated-deployment-overview.md) zal installeren.
2. Als [algemene of Power Platform-beheerder](/power-platform/admin/global-service-administrators-can-administer-without-license) met een Project Operations-licentie zoekt u de omgeving in het [PowerPlatform-beheercentrum](https://admin.powerplatform.com) waar u Project Operations wilt installeren.
3. Installeer **Microsoft Dynamics 365 Project Operations** uit de implementatielijst met Dynamics 365-apps. Zie [Dynamics 365-apps beheren](/power-platform/admin/manage-apps) voor meer informatie.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
