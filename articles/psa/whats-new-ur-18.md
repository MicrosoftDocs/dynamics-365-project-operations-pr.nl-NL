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
ms.openlocfilehash: b35c2f8f67e1bb75493a8787f1c4d8c2baf74d51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280752"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="60718-103">Project Service Automation, updaterelease 18, v3</span><span class="sxs-lookup"><span data-stu-id="60718-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="60718-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="60718-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="60718-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="60718-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="60718-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="60718-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="60718-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="60718-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="60718-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="60718-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="60718-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 18.</span><span class="sxs-lookup"><span data-stu-id="60718-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="60718-110">Deze versie heeft een buildnummer van V3.10.8.12 en is algemeen beschikbaar via een zelfupdate in april 2020.</span><span class="sxs-lookup"><span data-stu-id="60718-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="60718-111">Updaterelease 18</span><span class="sxs-lookup"><span data-stu-id="60718-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="60718-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="60718-112">Bug fixes</span></span>

<span data-ttu-id="60718-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="60718-113">**Time and Expense**</span></span>

- <span data-ttu-id="60718-114">Opgelost: stromen **Intrekken**, **Aanvragen** en **Goedkeuring annuleren** leiden tot uitzonderingen met onduidelijke foutmeldingen.</span><span class="sxs-lookup"><span data-stu-id="60718-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="60718-115">Opgelost: wanneer **Goedkeuring annuleren** mislukt voor een onkostenpost, wordt geen relevante uitzonderingsfout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="60718-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="60718-116">Opgelost: het rooster voor tijdinvoer verwerkt niet-werkdagen in Australië op onjuiste wijze na omschakeing van de zomertijd in oktober.</span><span class="sxs-lookup"><span data-stu-id="60718-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="60718-117">Opgelost: onjuiste standaardlogica voorkomt het indienen van onkostenposten.</span><span class="sxs-lookup"><span data-stu-id="60718-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="60718-118">Opgelost: als goedkeuring voor tijdinvoer mislukt, blijft de goedkeuring de status **In behandeling** houden.</span><span class="sxs-lookup"><span data-stu-id="60718-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="60718-119">Opgelost: SQL-fouten bij bulkgoedkeuringen (impasse/time-out).</span><span class="sxs-lookup"><span data-stu-id="60718-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="60718-120">Opgelost: significante prestatieproblemen in de gebruikerservaring veroorzaakt door het bijwerken van teamleden tijdens het goedkeuren van tijdsvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="60718-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="60718-121">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="60718-121">**Project Management**</span></span>

- <span data-ttu-id="60718-122">Opgelost: tijdzonemelding verplaatst van de weergave **Afstemming** naar het hoofdformulier **Project**.</span><span class="sxs-lookup"><span data-stu-id="60718-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="60718-123">Opgelost: agendasjabloon gebruikt geen correcte standaardwaarden bij het openen van een nieuw projectformulier.</span><span class="sxs-lookup"><span data-stu-id="60718-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="60718-124">Opgelost: voor op Chromium gebaseerde browsers kunnen gebruikers niet gemakkelijk voorafgaande taken selecteren om ze te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="60718-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="60718-125">Opgelost: bij het maken of kopiëren van **Project vanuit lege sjabloon** worden niet-gerelateerde opdrachten opgehaald.</span><span class="sxs-lookup"><span data-stu-id="60718-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="60718-126">Opgelost: in specifieke randgevallen resulteert het maken van een nieuwe toewijzing vanuit het taakraster in dubbele records.</span><span class="sxs-lookup"><span data-stu-id="60718-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="60718-127">Opgelost: in de handmatige modus kunnen gebruikers de startdatums van taken niet bijwerken tot na de huidige opgeslagen datum.</span><span class="sxs-lookup"><span data-stu-id="60718-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="60718-128">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="60718-128">**Resource Management**</span></span>

- <span data-ttu-id="60718-129">Opgelost: rij voor subtotaal in weergave **Afstemming** berekent op onjuiste wijze de boekingsvariantie na verlenging van boekingen.</span><span class="sxs-lookup"><span data-stu-id="60718-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="60718-130">Opgelost: in de weergave **Afstemming** worden resourcetoewijzingen onjuist weergegeven als de boekbare resource een agenda heeft die niet overeenkomt met de projectagenda.</span><span class="sxs-lookup"><span data-stu-id="60718-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="60718-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="60718-131">**Sales**</span></span>

- <span data-ttu-id="60718-132">Opgelost: wanneer tijdsvermeldingen opnieuw worden goedgekeurd (**Goedkeuren > Annuleren >** opnieuw goedkeuren), wordt een dubbele niet-toerekenbare werkelijke waarde gemaakt.</span><span class="sxs-lookup"><span data-stu-id="60718-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]