---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 25, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 25, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183537"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="89319-103">Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 25, v3</span><span class="sxs-lookup"><span data-stu-id="89319-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="89319-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="89319-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="89319-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="89319-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="89319-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="89319-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="89319-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="89319-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="89319-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="89319-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="89319-109">Dit onderwerp geeft een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation V3, Update versie 25. Deze versie heeft buildnummer V 3.10.43.76 en is algemeen beschikbaar via een zelfupdate in oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="89319-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="89319-110">Updaterelease 25</span><span class="sxs-lookup"><span data-stu-id="89319-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="89319-111">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="89319-111">Bug fixes</span></span>

<span data-ttu-id="89319-112">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="89319-112">**Time and Expense**</span></span>

<span data-ttu-id="89319-113">Het volgende probleem is opgelost:</span><span class="sxs-lookup"><span data-stu-id="89319-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="89319-114">Tijdinvoergrafiek met aanvullende gegevens op basis van een te groot interval dat wordt opgehaald.</span><span class="sxs-lookup"><span data-stu-id="89319-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="89319-115">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="89319-115">**Resource Management**</span></span>

<span data-ttu-id="89319-116">Het volgende probleem is opgelost:</span><span class="sxs-lookup"><span data-stu-id="89319-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="89319-117">Package Deployer-code toegevoegd om het importeren van Universal Resource Scheduling-patch over te slaan als er al een patch uit een hogere versie bestaat.</span><span class="sxs-lookup"><span data-stu-id="89319-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="89319-118">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="89319-118">**Project Management**</span></span>

<span data-ttu-id="89319-119">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="89319-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="89319-120">Afrondings- en wisselkoersverschillen gecorrigeerd die resulteren in onjuiste geplande kosten in het projectvolgraster.</span><span class="sxs-lookup"><span data-stu-id="89319-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="89319-121">Ondersteuning van de mogelijkheid om twee of meer reactierasters weer te geven op het formulier **Project**.</span><span class="sxs-lookup"><span data-stu-id="89319-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="89319-122">Validatie voor de mogelijkheid om een taak toe te wijzen na de einddatum van de kalender, wat resulteert in een mislukte toewijzing van resources.</span><span class="sxs-lookup"><span data-stu-id="89319-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="89319-123">Verbeterde foutafhandeling om een uitzondering met een null-verwijzing te verwerken die is gegenereerd op basis van het volgende:</span><span class="sxs-lookup"><span data-stu-id="89319-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="89319-124">Invoegtoepassing **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="89319-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="89319-125">**PreValidateprojectTaskCreate** wanneer een projecttaak wordt gemaakt zonder een bijbehorend project</span><span class="sxs-lookup"><span data-stu-id="89319-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="89319-126">Invoegtoepassing **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="89319-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="89319-127">Invoegtoepassing **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="89319-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="89319-128">invoegtoepassing **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="89319-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="89319-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="89319-129">**Sales**</span></span>

<span data-ttu-id="89319-130">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="89319-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="89319-131">Verbeterde foutafhandeling om uitzonderingen met null-verwijzingen te verwerken die zijn gegenereerd op basis van **Project kopiëren: schattingen van HelperResource Management**.</span><span class="sxs-lookup"><span data-stu-id="89319-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="89319-132">Bij **Niet gereed voor facturering** voor **Achterstallige facturering van tijd en materiaal** wordt de factureringsstatus niet gewist.</span><span class="sxs-lookup"><span data-stu-id="89319-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="89319-133">Gecorrigeerd verkeerd label voor knoppen **Prijzen** op het tabblad **Rolprijs** en **Catalogusartikelen**.</span><span class="sxs-lookup"><span data-stu-id="89319-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
