---
title: Functies van de app Project Finder Mobile inschakelen
description: Informatie over de app Project Finder Mobile inschakelen voor Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750689"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Functies van de app Project Finder Mobile inschakelen (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Uw resources kunnen de app Project Finder Mobile op hun telefoon met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gebruiken om nieuwe projecten te zoeken waaraan kan worden gewerkt en om hun vaardighedensets bij te werken.  
  
 De toepassing is beschikbaar voor [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoons en [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 U moet een aantal opties instellen in de parameterinstelling voor uw organisatie-eenheid zodat gebruikers de resourcevereisten van projecten kunnen weergeven en hun vaardigheden kunnen bijwerken.  
  
> [!NOTE]
>  De app Project Finder Mobile werkt alleen met [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], niet met lokale installaties.  
  
1. Ga naar **Project Service > Parameters**.  
  
2. Klik op de parameterinstelling die u wilt gebruiken om de functies van de toepassing Project Finder Mobile toe te staan.  
  
3. Stel in het gebied **Algemeen** **Resourcevereisten zichtbaar voor resources** in op **Ja**.  
  
4. Stel **Vaardigheidsupdate door resource toestaan** in op **Ja**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Dit is een algemene instelling. Projectmanagers kunnen instellen of een afzonderlijk project zichtbaar is op de pagina **Projectteam** van dat project.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-mailmeldingen  
 Met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] worden e-mailberichten over resourceaanvragen verzonden naar de volgende geadresseerden op de volgende tijdstippen:  
  
|Geadresseerde|Gebeurtenis|  
|---------------|-----------|  
|Projectmanager|-   Als een resource zich aanmeldt voor een project met de toepassing Project Finder Mobile.|  
|Resource|-   Als het projectwerk waarvoor de resource zich heeft aangemeld, al door een andere resource is uitgevoerd.<br />-   Als hun vaardigheidsgoedkeuringsaanvraag is goedgekeurd of geweigerd.<br />-   Als hun projectaanmeldingsaanvraag is goedgekeurd of geweigerd.|  
  
## <a name="privacy-notice"></a>Privacyverklaring  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Zie ook  
 [Resources configureren](../project-service/set-up-resources.md)
