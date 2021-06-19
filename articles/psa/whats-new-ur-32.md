---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 32, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 32, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129660"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="348f5-103">Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 32, v3</span><span class="sxs-lookup"><span data-stu-id="348f5-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="348f5-104">We zijn verheugd de laatste update aan te kondigen voor de Microsoft Dynamics 365 Project Service Automation-app.</span><span class="sxs-lookup"><span data-stu-id="348f5-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="348f5-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="348f5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="348f5-106">Deze app is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="348f5-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="348f5-107">Als u naar deze release wilt bijwerken, gaat u naar de pagina met online-oplossingen in het Beheercentrum voor Dynamics 365 en installeert u de update.</span><span class="sxs-lookup"><span data-stu-id="348f5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="348f5-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="348f5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="348f5-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 32.</span><span class="sxs-lookup"><span data-stu-id="348f5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="348f5-110">Deze versie heeft het buildnummer V3.10.53.108 en is algemeen beschikbaar via een zelfupdate in juni 2021.</span><span class="sxs-lookup"><span data-stu-id="348f5-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="348f5-111">Updaterelease 32</span><span class="sxs-lookup"><span data-stu-id="348f5-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="348f5-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="348f5-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="348f5-113">Algemeen</span><span class="sxs-lookup"><span data-stu-id="348f5-113">General</span></span>

- <span data-ttu-id="348f5-114">Wanneer een grote upgrade mislukt, moeten alleen de belangrijkste toegangspunten van de toepassing worden geblokkeerd om ervoor te zorgen dat gedeelde entiteiten nog steeds toegankelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="348f5-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="348f5-115">Tijd en onkosten</span><span class="sxs-lookup"><span data-stu-id="348f5-115">Time and Expense</span></span>

<span data-ttu-id="348f5-116">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="348f5-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="348f5-117">Met **TimeEntriesImportFromResourceAssignment** worden de begin- en eindtijden van het toewijzingscontoursegment van de resource niet behouden.</span><span class="sxs-lookup"><span data-stu-id="348f5-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="348f5-118">Wanneer u **Vermelding openen** in het raster **Tijdsvermelding** selecteert, is het mogelijk dat u geen andere formulieren kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="348f5-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="348f5-119">Terwijl u toewijzingen importeert naar tijdsvermeldingen, kan de clientcodequery een lange URL genereren die mislukt voor de query.</span><span class="sxs-lookup"><span data-stu-id="348f5-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="348f5-120">In het raster **Tijdsvermelding** blijft de focus, nadat een waarde uit een cel is verwijderd, niet in het raster.</span><span class="sxs-lookup"><span data-stu-id="348f5-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="348f5-121">De knop **Afwijzen** is verwijderd uit de weergave **Goedkeuringen verwerken** voor moderne goedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="348f5-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="348f5-122">De stabiliteit en prestaties van bulkgoedkeuring voor tijdsvermeldingen worden beïnvloed door impasses en het niet adequaat afhandelen van aanpassingen die verband houden met de entiteit **Tijdsvermelding**.</span><span class="sxs-lookup"><span data-stu-id="348f5-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="348f5-123">Projectplanning</span><span class="sxs-lookup"><span data-stu-id="348f5-123">Project Planning</span></span>

- <span data-ttu-id="348f5-124">Er wordt een null-referentie-uitzondering gegenereerd wanneer u een project bijwerkt dat een null-waarde heeft in het veld **Contracterende eenheid**.</span><span class="sxs-lookup"><span data-stu-id="348f5-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="348f5-125">Met **Projecttotalen vernieuwen** worden de resterende kosten en resterende verkopen van een project onjuist berekend.</span><span class="sxs-lookup"><span data-stu-id="348f5-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="348f5-126">Overbodige prijsberekeningen zijn van invloed op de prestaties die verband houden met updates van de resourcetoewijzingscontouren.</span><span class="sxs-lookup"><span data-stu-id="348f5-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="348f5-127">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="348f5-127">Resource Management</span></span>

<span data-ttu-id="348f5-128">Het volgende probleem is opgelost:</span><span class="sxs-lookup"><span data-stu-id="348f5-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="348f5-129">Wanneer de agendacapaciteit van een boekbare resource meer dan 1 is, herkent Project Service Automation de capaciteit ten onrechte als 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="348f5-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="348f5-130">Daarom treedt er een oneindige lus op in de planningsweergave.</span><span class="sxs-lookup"><span data-stu-id="348f5-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="348f5-131">Verkoop</span><span class="sxs-lookup"><span data-stu-id="348f5-131">Sales</span></span>

<span data-ttu-id="348f5-132">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="348f5-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="348f5-133">Wanneer een journaalregel wordt gemaakt met een aangepast transactietype, treedt de volgende null-referentie-uitzondering op: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="348f5-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="348f5-134">Rollen en categorieën die zijn gedeactiveerd voordat een offerte wordt gekopieerd, mogen niet worden toegevoegd aan factureerbare rollen en categorieën van de nieuw gekopieerde offerte.</span><span class="sxs-lookup"><span data-stu-id="348f5-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="348f5-135">De documentdatum en boekhouddatum komen niet overeen met de begindatum die is opgegeven op een factuurregeldetail dat rechtstreeks op een conceptfactuur wordt aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="348f5-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="348f5-136">Null-referentie-uitzonderingen worden gegenereerd in scenario's die verband houden met het deactiveren van rollen en categorieën voordat een offerte wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="348f5-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="348f5-137">Met de actie **Prijzen bijwerken** op de pagina **Projecten** worden geen kostenschattingen en materiaalschattingen bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="348f5-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
