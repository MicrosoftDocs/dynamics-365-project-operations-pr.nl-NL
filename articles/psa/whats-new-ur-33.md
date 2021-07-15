---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 33, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 33, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334524"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="2bf41-103">Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 33, v3</span><span class="sxs-lookup"><span data-stu-id="2bf41-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2bf41-104">We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app.</span><span class="sxs-lookup"><span data-stu-id="2bf41-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="2bf41-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="2bf41-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2bf41-106">Deze app is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2bf41-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2bf41-107">Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update.</span><span class="sxs-lookup"><span data-stu-id="2bf41-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="2bf41-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2bf41-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2bf41-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 33.</span><span class="sxs-lookup"><span data-stu-id="2bf41-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="2bf41-110">Deze versie heeft een buildnummer van V3.10.54.98 en is algemeen beschikbaar via een zelfupdate in juli 2021.</span><span class="sxs-lookup"><span data-stu-id="2bf41-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="2bf41-111">Updaterelease 33</span><span class="sxs-lookup"><span data-stu-id="2bf41-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2bf41-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="2bf41-112">Bug fixes</span></span>

<span data-ttu-id="2bf41-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="2bf41-113">**Time and Expense**</span></span>

<span data-ttu-id="2bf41-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2bf41-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2bf41-115">Twee vergrendelde velden, **msdyn_description** en **msdyn_externaldescription** zijn bewerkbaar na indiening.</span><span class="sxs-lookup"><span data-stu-id="2bf41-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="2bf41-116">Er treedt een foutbericht op als er onkosten worden gemaakt die niet gerelateerd zijn aan een project.</span><span class="sxs-lookup"><span data-stu-id="2bf41-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="2bf41-117">Wanneer een tijdsvermelding wordt gemaakt, wordt de resourcerol standaard ingesteld op een inactieve rol.</span><span class="sxs-lookup"><span data-stu-id="2bf41-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="2bf41-118">Journaalregels die zijn gekoppeld aan ingetrokken en verwijderde onkosten, worden niet verwijderd.</span><span class="sxs-lookup"><span data-stu-id="2bf41-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="2bf41-119">Werk in het **Formulier voor snelle invoer van tijdsvermelding** de **Projecttakenlijst** bij om de standaard weergegeven datum te wijzigen in de begindatum van de taak.</span><span class="sxs-lookup"><span data-stu-id="2bf41-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="2bf41-120">Wanneer u een tijdsvermelding maakt via het tabblad **Gerelateerd** van de boekbare resource, is de tijdsvermelding onjuist gemaakt voor de aangemelde gebruiker in plaats van de bovenliggende boekbare resource.</span><span class="sxs-lookup"><span data-stu-id="2bf41-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="2bf41-121">Nieuwe velden worden toegevoegd aan het dialoogvenster **Bulkgoedkeuring MDD**.</span><span class="sxs-lookup"><span data-stu-id="2bf41-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="2bf41-122">**Projectplanning**</span><span class="sxs-lookup"><span data-stu-id="2bf41-122">**Project planning**</span></span>

<span data-ttu-id="2bf41-123">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2bf41-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="2bf41-124">Trage prestaties bij het maken van projecten wanneer sjablonen voor projectwerkuren worden toegepast met complexe kalenders.</span><span class="sxs-lookup"><span data-stu-id="2bf41-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="2bf41-125">Wanneer de begindatum later is dan de einddatum, wordt er een fout weergegeven in de kopieerprojectsjabloon vanwege verschillen in de tijdcomponent van elk veld.</span><span class="sxs-lookup"><span data-stu-id="2bf41-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="2bf41-126">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="2bf41-126">**Resource management**</span></span>

<span data-ttu-id="2bf41-127">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2bf41-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="2bf41-128">Er wordt een onjuiste parameter gebruikt in de query voor resourcegebruik en de XML leidt tot onjuiste filterresultaten in het raster **Resourcegebruik**.</span><span class="sxs-lookup"><span data-stu-id="2bf41-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="2bf41-129">De bevestiging **Boekingen verlengen** geeft de onjuiste einddatum voor boekingen weer.</span><span class="sxs-lookup"><span data-stu-id="2bf41-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="2bf41-130">**Verkoop**</span><span class="sxs-lookup"><span data-stu-id="2bf41-130">**Sales**</span></span>

<span data-ttu-id="2bf41-131">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2bf41-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="2bf41-132">Er treedt een foutmelding op als er een categorieprijs wordt gemaakt met ontbrekende waarden.</span><span class="sxs-lookup"><span data-stu-id="2bf41-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="2bf41-133">Er treedt een foutmelding op als een mijlpaal in de contractregel wordt gemaakt zonder een orderregel.</span><span class="sxs-lookup"><span data-stu-id="2bf41-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
