---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 21, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 21, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126702"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="3a98e-103">Project Service Automation, updaterelease 21, v3</span><span class="sxs-lookup"><span data-stu-id="3a98e-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="3a98e-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3a98e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3a98e-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="3a98e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3a98e-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3a98e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3a98e-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="3a98e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3a98e-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3a98e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3a98e-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 21.</span><span class="sxs-lookup"><span data-stu-id="3a98e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="3a98e-110">Deze versie heeft buildnummer V 3.10.32.50 en is algemeen beschikbaar via een zelfupdate in juni 2020.</span><span class="sxs-lookup"><span data-stu-id="3a98e-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="3a98e-111">Updaterelease 21</span><span class="sxs-lookup"><span data-stu-id="3a98e-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3a98e-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="3a98e-112">Bug fixes</span></span>

<span data-ttu-id="3a98e-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="3a98e-113">**Time and Expense**</span></span>

<span data-ttu-id="3a98e-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3a98e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a98e-115">Bij het hosten van het besturingselement **Tijdinvoerraster** in Dashboards gebruikt het raster niet de volledige breedte van de dashboardrastercontainer.</span><span class="sxs-lookup"><span data-stu-id="3a98e-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="3a98e-116">Voor specifieke tijdzones geeft het rasterbesturingselement **Tijdinvoer** geen records weer.</span><span class="sxs-lookup"><span data-stu-id="3a98e-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="3a98e-117">Tijdinvoer van na 21.00 uur verschijnt op de verkeerde dag.</span><span class="sxs-lookup"><span data-stu-id="3a98e-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="3a98e-118">Gebruikers kunnen geen onkosten indienen als de onkostencategorie **Betalingsbewijs vereist** geen waarde bevat.</span><span class="sxs-lookup"><span data-stu-id="3a98e-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="3a98e-119">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="3a98e-119">**Resource Management**</span></span>

<span data-ttu-id="3a98e-120">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3a98e-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a98e-121">Inactieve boekingen worden weergegeven in de weergave **Afstemming**.</span><span class="sxs-lookup"><span data-stu-id="3a98e-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="3a98e-122">Er ontbrak validatie aan algemene resource-vervulling om ervoor te zorgen dat er een geldige boekingsstatus bestaat.</span><span class="sxs-lookup"><span data-stu-id="3a98e-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="3a98e-123">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="3a98e-123">**Project Management**</span></span>

<span data-ttu-id="3a98e-124">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3a98e-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a98e-125">De **Project** formulierrasters ( **Resourcetoewijzing**, **Taak**, weergave **Afstemming**, **Onkostenschattingen**) blijven bewerkbaar, ook als een project niet actief is.</span><span class="sxs-lookup"><span data-stu-id="3a98e-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="3a98e-126">Dubbele klanten kunnen niet worden samengevoegd met klanten die zijn gekoppeld aan bevestigde projectcontracten.</span><span class="sxs-lookup"><span data-stu-id="3a98e-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="3a98e-127">Wanneer een resource zonder geldige kalender agenda wordt toegevoegd, geeft het systeem geen gebruiksvriendelijke foutmelding.</span><span class="sxs-lookup"><span data-stu-id="3a98e-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="3a98e-128">De knop **Taak toevoegen** op het taakraster is ingeschakeld wanneer het project is gekoppeld aan **Microsoft project-invoegtoepassing**.</span><span class="sxs-lookup"><span data-stu-id="3a98e-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="3a98e-129">Inspanning groeit oncontroleerbaar wanneer een taak met een categorie wordt toegewezen aan een resource met een rol waarvoor een kostprijs is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="3a98e-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="3a98e-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3a98e-130">**Sales**</span></span>

<span data-ttu-id="3a98e-131">De volgende verbeteringen zijn aangebracht:</span><span class="sxs-lookup"><span data-stu-id="3a98e-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="3a98e-132">**Factuurfrequentie** en **Begin facturering** zijn verplaatst naar het tabblad **Factuurschema**.</span><span class="sxs-lookup"><span data-stu-id="3a98e-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="3a98e-133">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="3a98e-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a98e-134">**Totale verkoopprijs** is nul (0) voor **Categorie** ondanks dat **Rol** een totale verkoopprijs heeft die niet nul is.</span><span class="sxs-lookup"><span data-stu-id="3a98e-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="3a98e-135">Klanten kunnen de waarde van het veld **Factuurstatus** niet wijzigen in **Gereed voor facturering** wanneer een ander aangepast proces een extra veld bijwerkt.</span><span class="sxs-lookup"><span data-stu-id="3a98e-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="3a98e-136">De knop **Factuurregels vernieuwen** kan meerdere gedupliceerde regels maken als deze herhaaldelijk wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3a98e-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="3a98e-137">De knop **Prijzen bijwerken** werkt niet in het subraster **Rolprijzen** in het formulier **Snelle weergave**.</span><span class="sxs-lookup"><span data-stu-id="3a98e-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="3a98e-138">De logica voor **Oplossing verkoopprijslijst** behandelt tijdzones onjuist, wat resulteert in de verkeerde selectie van prijslijsten.</span><span class="sxs-lookup"><span data-stu-id="3a98e-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="3a98e-139">De **Totale werkelijke kosten** van een project kunnen een fractie afwijken nadat een enkele tijdpost is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="3a98e-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="3a98e-140">De logica voor **Prijsoplossing** geeft geen gebruiksvriendelijke foutmelding if **Opgehaalde rolprijs** geen waarden bevat in de velden **'Primaire eenheid'** en **'Prijs in primaire eenheid'**.</span><span class="sxs-lookup"><span data-stu-id="3a98e-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
