---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 31, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 31, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999125"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="ac33c-103">Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 31, v3</span><span class="sxs-lookup"><span data-stu-id="ac33c-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ac33c-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ac33c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ac33c-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="ac33c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ac33c-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ac33c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ac33c-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="ac33c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ac33c-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ac33c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ac33c-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 31.</span><span class="sxs-lookup"><span data-stu-id="ac33c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="ac33c-110">Deze versie heeft een buildnummer van V3.10.52.77 en is algemeen beschikbaar via een zelfupdate in mei 2021.</span><span class="sxs-lookup"><span data-stu-id="ac33c-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="ac33c-111">Updaterelease 31</span><span class="sxs-lookup"><span data-stu-id="ac33c-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ac33c-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="ac33c-112">Bug fixes</span></span>

<span data-ttu-id="ac33c-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="ac33c-113">**Time and Expense**</span></span>

<span data-ttu-id="ac33c-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="ac33c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac33c-115">De opdrachtknoppen voor tijdinvoer op de pagina **Boekbare resource** waren verwarrend.</span><span class="sxs-lookup"><span data-stu-id="ac33c-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="ac33c-116">Er werd een null-referentie-uitzondering gegenereerd in **Project.SetTrackingFields** bij het goedkeuren van een tijdinvoer.</span><span class="sxs-lookup"><span data-stu-id="ac33c-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="ac33c-117">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="ac33c-117">**Resource Management**</span></span>

<span data-ttu-id="ac33c-118">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="ac33c-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac33c-119">**Teamlid maken** geeft de metadata-instelling van de boekingsinstellingen niet correct weer voor **Standaardstatus van vastgelegde boeking**.</span><span class="sxs-lookup"><span data-stu-id="ac33c-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="ac33c-120">Bij het upgraden van PSA 1.X naar 3.X mislukt het upgradeproces bij **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="ac33c-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="ac33c-121">**Verkoop**</span><span class="sxs-lookup"><span data-stu-id="ac33c-121">**Sales**</span></span>

<span data-ttu-id="ac33c-122">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="ac33c-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac33c-123">Werkelijke opbrengst converteert de bedragen naar de projectvaluta in het traceringsraster.</span><span class="sxs-lookup"><span data-stu-id="ac33c-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="ac33c-124">De standaardvaluta is onduidelijk bij het maken van dagboekregels, prijsopgaveregels en contractregels in scenario's waarin de basisvaluta van een organisatie verschilt van de projectvaluta.</span><span class="sxs-lookup"><span data-stu-id="ac33c-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="ac33c-125">De query **In afwachting van correctiejournaalvalidatie** filtert niet op project.</span><span class="sxs-lookup"><span data-stu-id="ac33c-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="ac33c-126">De resterende omzet wordt onjuist berekend voor een project.</span><span class="sxs-lookup"><span data-stu-id="ac33c-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="ac33c-127">Prijsopgaven op basis van een contactpersoon mislukken als ze worden gemaakt zonder prijslijst.</span><span class="sxs-lookup"><span data-stu-id="ac33c-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="ac33c-128">Er wordt geen verwerkingsdraaischijf weergegeven wanneer u **Factuur bevestigen** selecteert.</span><span class="sxs-lookup"><span data-stu-id="ac33c-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="ac33c-129">Er wordt geen verwerkingsdraaischijf weergegeven wanneer u **Factuur maken** selecteert.</span><span class="sxs-lookup"><span data-stu-id="ac33c-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="ac33c-130">Als u een prijsopgave sluit als verloren, worden de boekingen niet geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="ac33c-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







