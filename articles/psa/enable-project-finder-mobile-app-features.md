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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074571"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="59302-103">Functies van de app Project Finder Mobile inschakelen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="59302-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="59302-104">Uw resources kunnen de app Project Finder Mobile op hun telefoon met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gebruiken om nieuwe projecten te zoeken waaraan kan worden gewerkt en om hun vaardighedensets bij te werken.</span><span class="sxs-lookup"><span data-stu-id="59302-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="59302-105">De toepassing is beschikbaar voor [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoons en [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="59302-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="59302-106">U moet een aantal opties instellen in de parameterinstelling voor uw organisatie-eenheid zodat gebruikers de resourcevereisten van projecten kunnen weergeven en hun vaardigheden kunnen bijwerken.</span><span class="sxs-lookup"><span data-stu-id="59302-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="59302-107">De app Project Finder Mobile werkt alleen met [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], niet met lokale installaties.</span><span class="sxs-lookup"><span data-stu-id="59302-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="59302-108">Ga naar **Project Service > Parameters**.</span><span class="sxs-lookup"><span data-stu-id="59302-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="59302-109">Klik op de parameterinstelling die u wilt gebruiken om de functies van de toepassing Project Finder Mobile toe te staan.</span><span class="sxs-lookup"><span data-stu-id="59302-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="59302-110">Stel in het gebied **Algemeen** **Resourcevereisten zichtbaar voor resources** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="59302-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="59302-111">Stel **Vaardigheidsupdate door resource toestaan** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="59302-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="59302-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="59302-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="59302-113">Dit is een algemene instelling.</span><span class="sxs-lookup"><span data-stu-id="59302-113">This is a global setting.</span></span> <span data-ttu-id="59302-114">Projectmanagers kunnen instellen of een afzonderlijk project zichtbaar is op de pagina **Projectteam** van dat project.</span><span class="sxs-lookup"><span data-stu-id="59302-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="59302-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="59302-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="59302-116">E-mailmeldingen</span><span class="sxs-lookup"><span data-stu-id="59302-116">Email notifications</span></span>  
 <span data-ttu-id="59302-117">Met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] worden e-mailberichten over resourceaanvragen verzonden naar de volgende geadresseerden op de volgende tijdstippen:</span><span class="sxs-lookup"><span data-stu-id="59302-117">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="59302-118">Geadresseerde</span><span class="sxs-lookup"><span data-stu-id="59302-118">Recipient</span></span>|<span data-ttu-id="59302-119">Gebeurtenis</span><span class="sxs-lookup"><span data-stu-id="59302-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="59302-120">Projectmanager</span><span class="sxs-lookup"><span data-stu-id="59302-120">Project manager</span></span>|<span data-ttu-id="59302-121">-   Als een resource zich aanmeldt voor een project met de toepassing Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="59302-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="59302-122">Resource</span><span class="sxs-lookup"><span data-stu-id="59302-122">Resource</span></span>|<span data-ttu-id="59302-123">-   Als het projectwerk waarvoor de resource zich heeft aangemeld, al door een andere resource is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="59302-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="59302-124">-   Als hun vaardigheidsgoedkeuringsaanvraag is goedgekeurd of geweigerd.</span><span class="sxs-lookup"><span data-stu-id="59302-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="59302-125">-   Als hun projectaanmeldingsaanvraag is goedgekeurd of geweigerd.</span><span class="sxs-lookup"><span data-stu-id="59302-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="59302-126">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="59302-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="59302-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="59302-127">See Also</span></span>  
 [<span data-ttu-id="59302-128">Resources configureren</span><span class="sxs-lookup"><span data-stu-id="59302-128">Set up resources</span></span>](../psa/set-up-resources.md)
