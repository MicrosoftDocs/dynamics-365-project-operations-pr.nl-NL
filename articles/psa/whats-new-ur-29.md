---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 29, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 29, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948619"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="a4fe5-103">Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 29, v3</span><span class="sxs-lookup"><span data-stu-id="a4fe5-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a4fe5-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a4fe5-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a4fe5-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a4fe5-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a4fe5-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a4fe5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a4fe5-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 29.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="a4fe5-110">Deze versie heeft buildnummer V3.10.47.7 en is algemeen beschikbaar via een zelfupdate in februari 2021.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="a4fe5-111">Updaterelease 29</span><span class="sxs-lookup"><span data-stu-id="a4fe5-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a4fe5-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="a4fe5-112">Bug fixes</span></span>

<span data-ttu-id="a4fe5-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="a4fe5-113">**Time and Expense**</span></span>

<span data-ttu-id="a4fe5-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="a4fe5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a4fe5-115">Gebruikers kunnen de geregistreerde werkuren op niet-werkdagen niet zien in het raster voor tijdsvermelding.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="a4fe5-116">Goedgekeurde onkostenposten kunnen in het raster worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="a4fe5-117">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="a4fe5-117">**Project Management**</span></span>

<span data-ttu-id="a4fe5-118">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="a4fe5-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a4fe5-119">Ontbrekende validatielogica om ervoor te zorgen dat inspanningsuren voor resourcetoewijzing niet negatief kunnen zijn.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="a4fe5-120">De aangepaste actie, **AssignResourcesForTask** werkt alle velden bij in plaats van alleen gewijzigde velden.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="a4fe5-121">Bij het kopiëren van een project in een omgeving met invoegtoepassingen of werkstromen die zijn geregistreerd voor de gebeurtenis **Createproject**, wordt het kenmerk **msdyn_bulkgenerationstatus** niet bijgewerkt als het **CopyWBSToProject** mislukt.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="a4fe5-122">Wanneer u de projectkalender uitvouwt, worden de werkdagen niet in oplopende volgorde gesorteerd, waardoor sommige updates van projecttaken mislukken.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="a4fe5-123">Als de projectmanager wordt gewijzigd voor een bestaand project wordt de standaardlogica van de organisatie-eenheid geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="a4fe5-124">**Verkoop**</span><span class="sxs-lookup"><span data-stu-id="a4fe5-124">**Sales**</span></span>

<span data-ttu-id="a4fe5-125">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="a4fe5-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="a4fe5-126">Het tabblad **Contractprestaties** op de pagina **Contract** mislukt zonder melding tijdens de initialisatie als er geen contractregels aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="a4fe5-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>