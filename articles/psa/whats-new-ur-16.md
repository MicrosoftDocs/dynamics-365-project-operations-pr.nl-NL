---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 16, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 16, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 33a711816e8cca34c4595aa0929de9a808a48b0f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949370"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="24370-103">Project Service Automation, updaterelease 16, v3</span><span class="sxs-lookup"><span data-stu-id="24370-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="24370-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="24370-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="24370-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="24370-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="24370-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="24370-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="24370-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="24370-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="24370-108">Meer informatie vindt u in [Een voorkeursoplossing installeren en bijwerken](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="24370-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="24370-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 16.</span><span class="sxs-lookup"><span data-stu-id="24370-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="24370-110">Deze versie heeft het buildnummer V3.10.6.34 en is algemeen beschikbaar via een zelf-update vanaf januari 2020.</span><span class="sxs-lookup"><span data-stu-id="24370-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="24370-111">Updaterelease 16</span><span class="sxs-lookup"><span data-stu-id="24370-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="24370-112">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="24370-112">Bug fixes</span></span>

-   <span data-ttu-id="24370-113">Tijd en onkosten</span><span class="sxs-lookup"><span data-stu-id="24370-113">Time and Expense</span></span>

    -   <span data-ttu-id="24370-114">Opgelost: gebruikers die proberen verwijderde tijds- en onkostenvermeldingen voor goedkeuring in te dienen, ontvangen nu relevante foutmeldingen.</span><span class="sxs-lookup"><span data-stu-id="24370-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="24370-115">Projectbeheer</span><span class="sxs-lookup"><span data-stu-id="24370-115">Project Management</span></span>

    -   <span data-ttu-id="24370-116">Opgelost: er wordt rekening gehouden met de resources die voor teamleden in sjablonen zijn gedefinieerd, terwijl de sjablonen worden toegepast op een nieuw project.</span><span class="sxs-lookup"><span data-stu-id="24370-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="24370-117">Opgelost: verbeterde afhandeling van het opnieuw toewijzen van het eigendom van records.</span><span class="sxs-lookup"><span data-stu-id="24370-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="24370-118">Opgelost: projecten die worden gekopieerd, mogen pas worden gekopieerd als alle kopieerbewerkingen zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="24370-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="24370-119">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="24370-119">Resource Management</span></span>

    -   <span data-ttu-id="24370-120">Opgelost: Boekingen uitbreiden verwerkt korte duur nu correct en creëert niet langer nul uur voor uitgebreide boekingen.</span><span class="sxs-lookup"><span data-stu-id="24370-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="24370-121">Opgelost: de afstemmingsweergave wordt nu weergegeven wanneer de projecttijdzone +5:30 GMT is en alleen de tijd van de gebruiker anders is.</span><span class="sxs-lookup"><span data-stu-id="24370-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="24370-122">Sales</span><span class="sxs-lookup"><span data-stu-id="24370-122">Sales</span></span>

    -   <span data-ttu-id="24370-123">Opgelost: wanneer een project dat aan een contractregel is toegewezen, wordt verwijderd en een nieuw project wordt toegewezen, werden de werkelijke records van het nieuwe project niet opnieuw geëvalueerd op basis van de facturerings- en prijsregels die op de contractregel waren gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="24370-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="24370-124">Dit is opgelost in deze release.</span><span class="sxs-lookup"><span data-stu-id="24370-124">This has been fixed in this release.</span></span> <span data-ttu-id="24370-125">De prijzen en werkelijke records van het nieuw toegewezen project worden teruggedraaid en correct opnieuw gemaakt op basis van de prijs- en factureringsregels van de contractregel.</span><span class="sxs-lookup"><span data-stu-id="24370-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="24370-126">De werkelijke records van het niet-toegewezen project zullen als gevolg daarvan ook opnieuw worden geëvalueerd en opnieuw worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="24370-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="24370-127">Opgelost: er is extra validatie toegevoegd aan het veld **Bedrag** van de schattingsregel om ervoor te zorgen dat null-waarden niet worden behouden.</span><span class="sxs-lookup"><span data-stu-id="24370-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="24370-128">Opgelost: wanneer werkelijke waarden zijn bijgewerkt in een project, is er een vernieuwingsknop toegevoegd aan het hoofdformulier van het project, zodat gebruikers de werkelijke waarden opnieuw kunnen synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="24370-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="24370-129">Opgelost: wanneer gebruikers upgraden van 2.X naar 3.X, zijn projecten met de waarde NULL voor de projectnaam toegestaan.</span><span class="sxs-lookup"><span data-stu-id="24370-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]