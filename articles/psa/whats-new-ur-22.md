---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 22, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 22, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126612"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="41992-103">Project Service Automation, updaterelease 22, v3</span><span class="sxs-lookup"><span data-stu-id="41992-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="41992-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="41992-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="41992-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="41992-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="41992-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="41992-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="41992-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="41992-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="41992-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="41992-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="41992-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 22.</span><span class="sxs-lookup"><span data-stu-id="41992-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="41992-110">Deze versie heeft buildnummer V 3.10.33.48 en is algemeen beschikbaar via een zelfupdate in juni 2020.</span><span class="sxs-lookup"><span data-stu-id="41992-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="41992-111">Updaterelease 22</span><span class="sxs-lookup"><span data-stu-id="41992-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="41992-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="41992-112">Bug fixes</span></span>



<span data-ttu-id="41992-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="41992-113">**Time and Expense**</span></span>

<span data-ttu-id="41992-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="41992-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="41992-115">**Tijdsvermeldingen** worden na het importeren niet automatisch toegevoegd aan het tijdsvermeldingenschema.</span><span class="sxs-lookup"><span data-stu-id="41992-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="41992-116">De datumkiezer van het raster **Tijdsvermelding** herkent de regionale instellingen van een gebruiker niet.</span><span class="sxs-lookup"><span data-stu-id="41992-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="41992-117">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="41992-117">**Resource Management**</span></span>

<span data-ttu-id="41992-118">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="41992-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="41992-119">In handmatige modus worden wijzigingen in **Resourcetoewijzings** contouren niet herkend bij het genereren van **Resourcevereisten**.</span><span class="sxs-lookup"><span data-stu-id="41992-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="41992-120">**Resourceaanvragen** ondersteunen geen aangepaste aanvraagstatussen.</span><span class="sxs-lookup"><span data-stu-id="41992-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="41992-121">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="41992-121">**Project Management**</span></span>

<span data-ttu-id="41992-122">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="41992-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="41992-123">Als u dubbelklikt op EstimateGridControl, worden getallen in de Nederlandse indeling niet correct geparseerd.</span><span class="sxs-lookup"><span data-stu-id="41992-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="41992-124">Toegewezen uren worden niet correct bijgewerkt wanneer toewijzingen worden gewijzigd met de Microsoft Project-desktopclient-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="41992-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="41992-125">De rasters voor Projecten bijhouden en Schattingen geven een onjuiste valutacode voor verkoop weer wanneer de contractvaluta anders is dan de valuta van de klant en de organisatie is geconfigureerd om valutacodes weer te geven in plaats van valutasymbolen.</span><span class="sxs-lookup"><span data-stu-id="41992-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="41992-126">De einddatum van een teamlid telt één dag op als het werkuurschema 24 uur per dag is.</span><span class="sxs-lookup"><span data-stu-id="41992-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="41992-127">In de projectplanning leidt het toevoegen van een transactiecategorie aan een taak niet tot automatisch opslaan.</span><span class="sxs-lookup"><span data-stu-id="41992-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="41992-128">De volgende fout wordt weergegeven bij het toevoegen van een teamlid aan de projectsjabloon: "Resourcevereisten kunnen niet worden gekoppeld aan projectsjablonen".</span><span class="sxs-lookup"><span data-stu-id="41992-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="41992-129">Lintregelscript "msdyn.Approval.CanApproveOrReject" geeft een time-outfout weer.</span><span class="sxs-lookup"><span data-stu-id="41992-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="41992-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="41992-130">**Sales**</span></span>

<span data-ttu-id="41992-131">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="41992-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="41992-132">Validatiefoutbericht wordt niet weergegeven wanneer een kostprijslijst is geselecteerd bij het opzoeken van prijslijsten op het formulier/de entiteit 'Projectprijslijst nieuwe prijsopgave'.</span><span class="sxs-lookup"><span data-stu-id="41992-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="41992-133">Als u de prijsopgave als gewonnen sluit, navigeert u niet naar het gemaakte contract als een BPF die aan de prijsopgave is gekoppeld, zich in de laatste fase bevindt.</span><span class="sxs-lookup"><span data-stu-id="41992-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="41992-134">Omkeren van **Niet-gefactureerde verkopen** is gekoppeld aan de oorspronkelijke kosten wanneer een tijdsvermelding wordt teruggeroepen.</span><span class="sxs-lookup"><span data-stu-id="41992-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="41992-135">Nadat u de knop **Bevestigen** hebt geselecteerd, verandert de factuurstatus niet in **Bevestigd** tenzij de factuur wordt vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="41992-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
