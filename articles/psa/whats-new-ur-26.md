---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 26, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 26, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143552"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="2a6e6-103">Project Service Automation, updaterelease 26, v3</span><span class="sxs-lookup"><span data-stu-id="2a6e6-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2a6e6-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2a6e6-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2a6e6-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2a6e6-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2a6e6-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2a6e6-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2a6e6-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 26, V3.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="2a6e6-110">Deze versie heeft buildnummer V3.10.44.59 en is algemeen beschikbaar via een zelfupdate in december 2020.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="2a6e6-111">Updaterelease 26</span><span class="sxs-lookup"><span data-stu-id="2a6e6-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2a6e6-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="2a6e6-112">Bug fixes</span></span>

<span data-ttu-id="2a6e6-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="2a6e6-113">**Time and Expense**</span></span>

<span data-ttu-id="2a6e6-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2a6e6-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e6-115">Gebruikers kunnen de taak wijzigen voor een tijdsvermelding die is goedgekeurd/ingediend.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="2a6e6-116">"Objectreferentie niet ingesteld"-fout bij het opslaan van tijdsvermelding.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="2a6e6-117">Bij het importeren van tijdsvermeldingen uit resourcetoewijzingen worden tijdsvermeldingen gemaakt met de onjuiste DateTime-waarden.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="2a6e6-118">Wanneer Project Service Automation en de Field Service-app beide zijn geïnstalleerd, wordt de knop **Nieuw** twee keer weergegeven op de opdrachtbalk voor tijdsvermeldingen in de Field Service-app.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="2a6e6-119">Celupdates voor **Eenheid toestaan** en **Eenhedengroep** werken nu in het raster **Onkostenschattingen**.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="2a6e6-120">Formulier **Update tijdsvermelding bewerken** omvat **Tijdlijn**.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="2a6e6-121">Tijdgoedkeuringen voor niet-projectgebonden tijdsvermeldingen blokkeren het systeem bij het zoeken naar een projectgoedkeurdersrol.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="2a6e6-122">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="2a6e6-122">**Resource Management**</span></span>

<span data-ttu-id="2a6e6-123">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2a6e6-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e6-124">Validatie toegevoegd in de invoegtoepassing **PostprojectCreate** om te controleren op een primaire vereiste voordat u deze maakt.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="2a6e6-125">Formulier voor snelle invoer van **projectteamlid** genereert een null-verwijzingsuitzondering als velden uit het formulier worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="2a6e6-126">Het genereren van vereisten voor 12 uur gedurende 1 jaar zal mislukken.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="2a6e6-127">Verbeterde foutmelding voor null-verwijzingsuitzondering tijdens het maken van resourcevereisten.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="2a6e6-128">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="2a6e6-128">**Project Management**</span></span>

<span data-ttu-id="2a6e6-129">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2a6e6-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e6-130">Verbeterde validatie om een null-verwijzingsuitzondering op te lossen die is gegenereerd in de invoegtoepassing **PreprojectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="2a6e6-131">Projecten die zijn gepubliceerd door de Microsoft Project-desktopinvoegtoepassing, verwijderen niet-toegewezen toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="2a6e6-132">Nieuwe validatie toegevoegd wanneer de projectverwijzing van een taak ongeldig is vanwege een null-verwijzingsuitzondering in de invoegtoepassing **PreValidateprojectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="2a6e6-133">Het raster Teamlid toont geen afzonderlijke toewijzingen in de teamlidrecord.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="2a6e6-134">Nieuwe validatie- en foutmeldingen toegevoegd vanwege een null-verwijzingsuitzondering in de invoegtoepassing **PreprojectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="2a6e6-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2a6e6-135">**Sales**</span></span>

<span data-ttu-id="2a6e6-136">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="2a6e6-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e6-137">Bij het selecteren van een projectgebaseerde regel in een prijsopgave of contract, mag de knop **Suggestie** alleen zichtbaar zijn bij het selecteren van een productgebaseerde regel die is gekoppeld aan een bestaand product.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="2a6e6-138">Splits bevoegdheid **Create_Product** van bevoegdheid **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="2a6e6-139">Het verwijderen van een factuurregel veroorzaakt een null-verwijzingsfout op **MarkReadyToInvoiceForproductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="2a6e6-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
