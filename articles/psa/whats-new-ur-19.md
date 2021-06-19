---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 19, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 19, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 7812bc41f32f9d4116c63990059f7dbc0351cf9e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006595"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="f4a52-103">Project Service Automation, updaterelease 19, v3</span><span class="sxs-lookup"><span data-stu-id="f4a52-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f4a52-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f4a52-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f4a52-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="f4a52-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f4a52-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f4a52-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f4a52-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="f4a52-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f4a52-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f4a52-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f4a52-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 19.</span><span class="sxs-lookup"><span data-stu-id="f4a52-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="f4a52-110">Deze versie heeft een buildnummer van V3.10.30.41 en is algemeen beschikbaar via een zelfupdate in mei 2020.</span><span class="sxs-lookup"><span data-stu-id="f4a52-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="f4a52-111">Updaterelease 19</span><span class="sxs-lookup"><span data-stu-id="f4a52-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f4a52-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="f4a52-112">Bug fixes</span></span>

<span data-ttu-id="f4a52-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="f4a52-113">**Time and Expense**</span></span>

<span data-ttu-id="f4a52-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="f4a52-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="f4a52-115">Fouten die zijn afgeleid van geïmporteerde tijdsvermeldingen, worden niet correct weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4a52-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="f4a52-116">Tijdsvermeldingsraster ondersteunt niet velden van het type **Alleen datum**.</span><span class="sxs-lookup"><span data-stu-id="f4a52-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="f4a52-117">Projectresources kunnen geen kosten maken met een project.</span><span class="sxs-lookup"><span data-stu-id="f4a52-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="f4a52-118">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="f4a52-118">**Project Management**</span></span>

<span data-ttu-id="f4a52-119">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="f4a52-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="f4a52-120">Dieper onderliggende taak veroorzaakt een onjuiste inspanningsschatting tijdens de voltooiingsberekening (EAC).</span><span class="sxs-lookup"><span data-stu-id="f4a52-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="f4a52-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f4a52-121">**Sales**</span></span>

<span data-ttu-id="f4a52-122">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="f4a52-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="f4a52-123">De actie **Herberekenen** werkt niet met onkostencontractregeldetails of prijsopgaveregeldetails.</span><span class="sxs-lookup"><span data-stu-id="f4a52-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="f4a52-124">**Prijzen bijwerken** ontbreekt voor kostenramingen.</span><span class="sxs-lookup"><span data-stu-id="f4a52-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="f4a52-125">Klanten kunnen geen redenen voor aangepaste contractstatus selecteren op de pagina **Projectcontract**.</span><span class="sxs-lookup"><span data-stu-id="f4a52-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="f4a52-126">Klanten ervaren verminderde prestaties bij het maken van een aangepaste prijslijst op basis van een prijsopgave.</span><span class="sxs-lookup"><span data-stu-id="f4a52-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="f4a52-127">Klanten ervaren inconsistenties met standaardwaarden voor **eenheid** op de pagina's **Prijsopgaveregeldetails** en **Contractregeldetails**.</span><span class="sxs-lookup"><span data-stu-id="f4a52-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="f4a52-128">Als niet-toerekenbare transactiecategorie-items worden toegevoegd aan een toerekenbare contractregel, wordt geen rekening gehouden met het factureringstype **Niet-toerekenbaar** van de transactiecategorie.</span><span class="sxs-lookup"><span data-stu-id="f4a52-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="f4a52-129">Klanten kunnen de nieuw toegevoegde rollen en categorie niet gebruiken in eerder gemaakte contracten.</span><span class="sxs-lookup"><span data-stu-id="f4a52-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="f4a52-130">Klanten ervaren verminderde prestaties door onnodig ophalen in PreValidateprojectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="f4a52-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="f4a52-131">Rollen die zijn ingesteld als niet-toerekenbaar in de lijst **Resourcecategorieën**, moeten aan het tabblad **Toerekenbare rollen** worden toegevoegd als **Niet-toerekenbaar** op de contractregel voor een project.</span><span class="sxs-lookup"><span data-stu-id="f4a52-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="f4a52-132">Klanten kunnen verminderde prestaties ervaren bij het maken van een project omdat met **GetBookableResourceIdFromUser** alle kolommen met boekbare resources worden opgehaald in plaats van alleen de primaire id.</span><span class="sxs-lookup"><span data-stu-id="f4a52-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="f4a52-133">In de entiteit **TransactionType** ontbreekt de update-invoegtoepassing voor prevalidatie die voorkomt dat gebruikers **Eenheden** en **UnitGroups** invoeren die niet geldig zijn voor transactietypen.</span><span class="sxs-lookup"><span data-stu-id="f4a52-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="f4a52-134">De stap **Verwijderen** werkt niet voor het importeren van tijdsvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="f4a52-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]