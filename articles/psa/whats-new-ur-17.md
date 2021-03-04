---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 17, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 17, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143699"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="8b0b3-103">Project Service Automation, updaterelease 17, v3</span><span class="sxs-lookup"><span data-stu-id="8b0b3-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8b0b3-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8b0b3-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="8b0b3-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8b0b3-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="8b0b3-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8b0b3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8b0b3-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 17.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="8b0b3-110">Deze versie heeft het buildnummer V3.10.6.34 en is algemeen beschikbaar via een zelf-update vanaf maart 2020.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="8b0b3-111">Updaterelease 17</span><span class="sxs-lookup"><span data-stu-id="8b0b3-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8b0b3-112">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="8b0b3-112">Bug fixes</span></span>

<span data-ttu-id="8b0b3-113">**Algemeen**</span><span class="sxs-lookup"><span data-stu-id="8b0b3-113">**General**</span></span>

- <span data-ttu-id="8b0b3-114">Opgelost: Project Service Automation bijwerken om Team Member-licenties af te dwingen (Hub voor projectresource bevat metagegevens voor Serviceplan voor teamlid 3.x)</span><span class="sxs-lookup"><span data-stu-id="8b0b3-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="8b0b3-115">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="8b0b3-115">**Time and Expense**</span></span>

- <span data-ttu-id="8b0b3-116">Opgelost: het is niet mogelijk om een kostenraming te wijzigen van een prijs die niet nul is naar nul (0).</span><span class="sxs-lookup"><span data-stu-id="8b0b3-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="8b0b3-117">De wijziging wordt genegeerd.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-117">The change is ignored.</span></span>

<span data-ttu-id="8b0b3-118">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="8b0b3-118">**Project Management**</span></span>

- <span data-ttu-id="8b0b3-119">Opgelost: er is een controle op null-waarden toegevoegd aan de positienaam van een teamlid.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="8b0b3-120">Opgelost: het veld **msdyn_userresourceid** in de entiteit **msdyn_resourceassignment** is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="8b0b3-121">Opgelost: door upgrade van 2.x naar 3.x worden nu lege inspanningscontouren verwerkt bij taakopdrachten.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="8b0b3-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8b0b3-122">**Sales**</span></span>

- <span data-ttu-id="8b0b3-123">Opgelost: door **Invoice.PreValidateInvoiceUpdate** wordt nu het scenario van het toewijzen van recordeigenaren op de juiste manier verwerkt.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="8b0b3-124">Opgelost: wanneer de transactieklasse is **Tijd**, is **UnitGroup** niet bewerkbaar voor alle entiteiten, waaronder **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** en **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="8b0b3-125">**Eenheid** is echter niet bewerkbaar voor **JournalLine** en **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="8b0b3-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


