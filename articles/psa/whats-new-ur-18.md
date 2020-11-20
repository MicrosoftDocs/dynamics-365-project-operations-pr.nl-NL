---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 18, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 18, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119862"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="18736-103">Project Service Automation, updaterelease 18, v3</span><span class="sxs-lookup"><span data-stu-id="18736-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="18736-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="18736-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="18736-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="18736-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="18736-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="18736-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="18736-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="18736-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="18736-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="18736-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="18736-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 18.</span><span class="sxs-lookup"><span data-stu-id="18736-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="18736-110">Deze versie heeft een buildnummer van V3.10.8.12 en is algemeen beschikbaar via een zelfupdate in april 2020.</span><span class="sxs-lookup"><span data-stu-id="18736-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="18736-111">Updaterelease 18</span><span class="sxs-lookup"><span data-stu-id="18736-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="18736-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="18736-112">Bug fixes</span></span>

<span data-ttu-id="18736-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="18736-113">**Time and Expense**</span></span>

- <span data-ttu-id="18736-114">Opgelost: stromen **Intrekken**, **Aanvragen** en **Goedkeuring annuleren** leiden tot uitzonderingen met onduidelijke foutmeldingen.</span><span class="sxs-lookup"><span data-stu-id="18736-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="18736-115">Opgelost: wanneer **Goedkeuring annuleren** mislukt voor een onkostenpost, wordt geen relevante uitzonderingsfout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="18736-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="18736-116">Opgelost: het rooster voor tijdinvoer verwerkt niet-werkdagen in Australië op onjuiste wijze na omschakeing van de zomertijd in oktober.</span><span class="sxs-lookup"><span data-stu-id="18736-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="18736-117">Opgelost: onjuiste standaardlogica voorkomt het indienen van onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="18736-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="18736-118">Opgelost: als goedkeuring voor tijdinvoer mislukt, blijft de goedkeuring de status **In behandeling** houden.</span><span class="sxs-lookup"><span data-stu-id="18736-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="18736-119">Opgelost: SQL-fouten bij bulkgoedkeuringen (impasse/time-out).</span><span class="sxs-lookup"><span data-stu-id="18736-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="18736-120">Opgelost: significante prestatieproblemen in de gebruikerservaring veroorzaakt door het bijwerken van teamleden tijdens het goedkeuren van tijdsvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="18736-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="18736-121">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="18736-121">**Project Management**</span></span>

- <span data-ttu-id="18736-122">Opgelost: tijdzonemelding verplaatst van de weergave **Afstemming** naar het hoofdformulier **Project**.</span><span class="sxs-lookup"><span data-stu-id="18736-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="18736-123">Opgelost: agendasjabloon gebruikt geen correcte standaardwaarden bij het openen van een nieuw projectformulier.</span><span class="sxs-lookup"><span data-stu-id="18736-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="18736-124">Opgelost: voor op Chromium gebaseerde browsers kunnen gebruikers niet gemakkelijk voorafgaande taken selecteren om ze te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="18736-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="18736-125">Opgelost: bij het maken of kopiëren van **Project vanuit lege sjabloon** worden niet-gerelateerde opdrachten opgehaald.</span><span class="sxs-lookup"><span data-stu-id="18736-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="18736-126">Opgelost: in specifieke randgevallen resulteert het maken van een nieuwe toewijzing vanuit het taakraster in dubbele records.</span><span class="sxs-lookup"><span data-stu-id="18736-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="18736-127">Opgelost: in de handmatige modus kunnen gebruikers de startdatums van taken niet bijwerken tot na de huidige opgeslagen datum.</span><span class="sxs-lookup"><span data-stu-id="18736-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="18736-128">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="18736-128">**Resource Management**</span></span>

- <span data-ttu-id="18736-129">Opgelost: rij voor subtotaal in weergave **Afstemming** berekent op onjuiste wijze de boekingsvariantie na verlenging van boekingen.</span><span class="sxs-lookup"><span data-stu-id="18736-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="18736-130">Opgelost: in de weergave **Afstemming** worden resourcetoewijzingen onjuist weergegeven als de boekbare resource een agenda heeft die niet overeenkomt met de projectagenda.</span><span class="sxs-lookup"><span data-stu-id="18736-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="18736-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="18736-131">**Sales**</span></span>

- <span data-ttu-id="18736-132">Opgelost: wanneer tijdsvermeldingen opnieuw worden goedgekeurd (**Goedkeuren > Annuleren >** opnieuw goedkeuren), wordt een dubbele niet-toerekenbare werkelijke waarde gemaakt.</span><span class="sxs-lookup"><span data-stu-id="18736-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
