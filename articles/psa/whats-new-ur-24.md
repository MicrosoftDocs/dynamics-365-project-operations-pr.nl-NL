---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 24, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 24, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a37e71be2cce259d8aed0621d13393b6bbe4199
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126567"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="3f7dc-103">Project Service Automation, updaterelease 24, v3</span><span class="sxs-lookup"><span data-stu-id="3f7dc-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="3f7dc-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3f7dc-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3f7dc-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3f7dc-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3f7dc-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3f7dc-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3f7dc-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 24.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="3f7dc-110">Deze versie heeft het buildnummer V 3.10.42.43 en is algemeen beschikbaar via een zelf-update vanaf oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="3f7dc-111">Updaterelease 24</span><span class="sxs-lookup"><span data-stu-id="3f7dc-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3f7dc-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="3f7dc-112">Bug fixes</span></span>

<span data-ttu-id="3f7dc-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3f7dc-113">**Sales**</span></span>

<span data-ttu-id="3f7dc-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3f7dc-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f7dc-115">Probleem bij het instellen van de standaardprijslijst van producten.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="3f7dc-116">De prestaties van Prijsopgave winnen zijn traag vanwege de ingesloten prijslijst en het kopiëren van de rolprijsrecords.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="3f7dc-117">**Projectcontract/Verkoophub** > **Productregelartikel/Orderregelhoeveelheid** wordt automatisch afgerond op het dichtstbijzijnde gehele getal.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="3f7dc-118">Stel systeemprivileges in bij het lezen van prijslijsten.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="3f7dc-119">Kopieer de klantadresvelden **address1_freighttermscode** en **address1_shippingmethodcode** naar Prijsopgave/Order.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="3f7dc-120">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="3f7dc-120">**Time and Expense**</span></span>

<span data-ttu-id="3f7dc-121">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3f7dc-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f7dc-122">Het **tijdinvoerraster** biedt geen ondersteuning voor het gedrag van de tijd **Alleen datum**.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="3f7dc-123">**Tijdsvermelding** wordt niet automatisch vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="3f7dc-124">Handmatig vernieuwen is vereist.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-124">A manual refresh is required.</span></span>
- <span data-ttu-id="3f7dc-125">De tijdsvermeldingen van een toewijzing kunnen niet worden geïmporteerd als er een pauze (0 uur) is opgenomen in de toewijzingen van een resource.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="3f7dc-126">Stel bij het maken van een tijdsvermelding het begin op dezelfde waarde in als **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="3f7dc-127">Schakel bulkbewerking opnieuw in voor tijdsvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="3f7dc-128">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="3f7dc-128">**Resource Management**</span></span>

<span data-ttu-id="3f7dc-129">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3f7dc-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f7dc-130">Als u de status van een interdagboeking zonder vereiste probeert bij te werken, wordt een null-ref-uitzondering gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="3f7dc-131">Fout bij het laden van de weergave **Vereffening**.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="3f7dc-132">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="3f7dc-132">**Project Management**</span></span>

<span data-ttu-id="3f7dc-133">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3f7dc-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="3f7dc-134">Wanneer u in **Projectplanning** de waarde **Handmatig** in **Auto** wijzigt, wordt automatisch opslaan niet voltooid.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="3f7dc-135">Onkosten mogen niet worden meegerekend voor variantie in het raster **Projectschattingen**.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="3f7dc-136">Inconsistent gedrag voor kolommen op het tabblad **Schattingen** tijdens het laden en het wijzigen van het type **Tijdsfase**.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="3f7dc-137">De werkelijke kosten van een project komen mogelijk niet overeen met de totalen van **Werkelijke waarden**.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="3f7dc-138">**Geschatte einddatum** op het tabblad **Samenvatting** komt niet overeen met de **WBS-planning**.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="3f7dc-139">**Werkelijke uren bijwerken** werkt niet bij verkleinen van inspringing.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="3f7dc-140">Een projectmanager buiten de hoofdmap **BU** kan geen project maken.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="3f7dc-141">Wijzigingen in taak of categorie voor **Kostenramingen** worden niet bewaard.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="3f7dc-142">**Kopie van contract** kopieert de factuurplanningen en de uitvoeringsstatus.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="3f7dc-143">De knop **Werkelijke waarden vernieuwen** berekent overzichtstaken onjuist.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="3f7dc-144">Microsoft Project-invoegtoepassing: herstel de fout met de null-referentie als een teamlid een lege resource-eenheid heeft.</span><span class="sxs-lookup"><span data-stu-id="3f7dc-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

