---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 12, v3
description: Dit onderwerp bevat informatie over wat er nieuw en gewijzigd is in Project Service Automation updaterelease 12, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281067"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="3d7c4-103">Project Service Automation, updaterelease 12, v3</span><span class="sxs-lookup"><span data-stu-id="3d7c4-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3d7c4-104">Met genoegen kondigen we de nieuwste update voor de toepassing Dynamics 365 Project Service Automation (PSA) aan.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3d7c4-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3d7c4-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3d7c4-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365. Hierin gaat u naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3d7c4-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3d7c4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3d7c4-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 12.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="3d7c4-110">Deze versie heeft het buildnummer V3.10.2.34 en is algemeen beschikbaar via een zelf-update vanaf oktober 2019.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="3d7c4-111">Updaterelease 12</span><span class="sxs-lookup"><span data-stu-id="3d7c4-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3d7c4-112">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="3d7c4-112">Bug fixes</span></span>

- <span data-ttu-id="3d7c4-113">Tijd en onkosten</span><span class="sxs-lookup"><span data-stu-id="3d7c4-113">Time and Expense</span></span>

    - <span data-ttu-id="3d7c4-114">Opgelost: foutberichten bij tijdinvoer zijn voorzien van een meer relevante context.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="3d7c4-115">Opgelost: raster en planning voor tijdinvoer geven waar nodig de verticale schuifbalk correct weer.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="3d7c4-116">Opgelost: ingediende vermeldingen voor kosten en tijd kunnen worden goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="3d7c4-117">Opgelost: het dialoogvenster Goedkeuring annuleren is gecorrigeerd en geeft nu de status van de goedkeuring weer wanneer deze wijzigt van **Goedgekeurd** naar **Ingediend**.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="3d7c4-118">Opgelost: de velden **Prijs**, **Eenheid** en **Aantal** worden nu vergrendeld in de onkostenrecord nadat deze is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="3d7c4-119">Projectbeheer</span><span class="sxs-lookup"><span data-stu-id="3d7c4-119">Project Management</span></span>

    - <span data-ttu-id="3d7c4-120">Opgelost: de actie **Nieuw** op het hoofdformulier **Teamlid** is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="3d7c4-121">Opgelost: resourcetoewijzingen zijn bijgewerkt en houden nu rekening met onnauwkeurige afrondingsfouten, die leiden tot het verschuiven van de einddatum van een taak.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="3d7c4-122">Opgelost: in het taakraster worden relevante serverfouten zichtbaar gemaakt voor de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="3d7c4-123">Opgelost: de naam van het teamlid wordt nu weergegeven in de taakkiezer in plaats van de positienaam.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="3d7c4-124">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="3d7c4-124">Resource Management</span></span>

    - <span data-ttu-id="3d7c4-125">Opgelost: details van de resourcevereisten voor projecten die met een sjabloon zijn gemaakt, maken nu gebruik van de projectagenda.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="3d7c4-126">Opgelost: vaardigheden en competenties gaan nu standaard van rolstamgegevens naar de resourcevereiste die voor die rol is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="3d7c4-127">Sales</span><span class="sxs-lookup"><span data-stu-id="3d7c4-127">Sales</span></span>

    - <span data-ttu-id="3d7c4-128">Opgelost: dubbele object-id's werden aangetroffen op het hoofdformulier **Contract**.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="3d7c4-129">Opgelost: logica is bijgewerkt en maakt nu het tabblad **Analyse prijsopgave** zichtbaar, zodat het de metadata-instellingen van het tabblad weergeeft.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="3d7c4-130">Opgelost: de datum in financiële administratie in de werkelijke record komt nu van de datum van de tijd/kosteninvoerdatum en niet de datum van de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="3d7c4-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]