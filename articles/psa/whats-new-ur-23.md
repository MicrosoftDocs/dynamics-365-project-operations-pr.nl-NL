---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 23, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 23, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 379379ff643baa10417333b4be5e56d56eb5bc26
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280527"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="d51eb-103">Project Service Automation, updaterelease 23, v3</span><span class="sxs-lookup"><span data-stu-id="d51eb-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d51eb-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d51eb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d51eb-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="d51eb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d51eb-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d51eb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d51eb-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="d51eb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d51eb-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d51eb-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d51eb-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 23.</span><span class="sxs-lookup"><span data-stu-id="d51eb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="d51eb-110">Deze versie heeft het buildnummer V 3.10.34.30 en is algemeen beschikbaar via een zelf-update vanaf augustus 2020.</span><span class="sxs-lookup"><span data-stu-id="d51eb-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="d51eb-111">Updaterelease 23</span><span class="sxs-lookup"><span data-stu-id="d51eb-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d51eb-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="d51eb-112">Bug fixes</span></span>

<span data-ttu-id="d51eb-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="d51eb-113">**Time and Expense**</span></span>

<span data-ttu-id="d51eb-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="d51eb-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="d51eb-115">Afhandeling van randgeval in **Project-teamlid verwijderen** om een zinvolle uitzondering te bieden.</span><span class="sxs-lookup"><span data-stu-id="d51eb-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="d51eb-116">Import van toewijzingen resulteert in een leeg verwijderscherm.</span><span class="sxs-lookup"><span data-stu-id="d51eb-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="d51eb-117">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="d51eb-117">**Resource Management**</span></span>

<span data-ttu-id="d51eb-118">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="d51eb-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="d51eb-119">De resourcekaart voor het raster **Bestede uren van resource** bevat onjuiste gegevens als de tijdschaal meer dan vijf dagen is.</span><span class="sxs-lookup"><span data-stu-id="d51eb-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="d51eb-120">Wanneer klanten een boekbare resource maken, kan de invoegtoepassing de resource af en toe niet automatisch toevoegen aan een Microsoft Office 365-groep.</span><span class="sxs-lookup"><span data-stu-id="d51eb-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="d51eb-121">In de weergave **Vereffening** worden handmatige contouren onjuist weergegeven in de weergave **Week** of **Maand**.</span><span class="sxs-lookup"><span data-stu-id="d51eb-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="d51eb-122">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="d51eb-122">**Project Management**</span></span>

<span data-ttu-id="d51eb-123">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="d51eb-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="d51eb-124">Een te groot aantal entiteiten voor **RetrieveMultiple for usersettings** leidt tot mindere prestaties voor projectgoedkeuringen en andere bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="d51eb-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="d51eb-125">In de opzoekfunctie voor resources in het raster **Taakplanning** kunnen maximaal vijf teamleden van het projectteam worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d51eb-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="d51eb-126">In de opzoekfunctie voor resources in het raster **Taakplanning** worden inactieve resources niet gefilterd.</span><span class="sxs-lookup"><span data-stu-id="d51eb-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="d51eb-127">De handmatige modus werkt niet zoals verwacht in de projectplanningsstructuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="d51eb-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="d51eb-128">In het raster **Taakplanning** wordt **Inactieve transactiecategorieën** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d51eb-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="d51eb-129">Het raster **Resourcetoewijzing** rondt onjuist af wanneer een taak meerdere toewijzingen heeft.</span><span class="sxs-lookup"><span data-stu-id="d51eb-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="d51eb-130">Afrondingswaarden verschillen tussen geplande en werkelijke kosten voor een enkele taak.</span><span class="sxs-lookup"><span data-stu-id="d51eb-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="d51eb-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d51eb-131">**Sales**</span></span>

<span data-ttu-id="d51eb-132">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="d51eb-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="d51eb-133">Wanneer in **Alle transactiecategorieën ophalen** wordt gedubbelklikt, worden er meerdere regels gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d51eb-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]