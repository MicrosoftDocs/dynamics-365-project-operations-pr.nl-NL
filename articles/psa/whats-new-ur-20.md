---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 20, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 20, v3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147107"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="eaa3d-103">Project Service Automation, updaterelease 20, v3</span><span class="sxs-lookup"><span data-stu-id="eaa3d-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="eaa3d-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="eaa3d-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eaa3d-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eaa3d-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="eaa3d-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="eaa3d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eaa3d-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 20.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="eaa3d-110">Deze versie heeft buildnummer V 3.10.31.37 en is algemeen beschikbaar via een zelfupdate in juni 2020.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="eaa3d-111">Updaterelease 20</span><span class="sxs-lookup"><span data-stu-id="eaa3d-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eaa3d-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="eaa3d-112">Bug fixes</span></span>

<span data-ttu-id="eaa3d-113">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="eaa3d-113">**Project Management**</span></span>

<span data-ttu-id="eaa3d-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="eaa3d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="eaa3d-115">Het importeren van projectteamleden met een toewijzingsmethode waarvoor uren nodig zijn, resulteert in een onduidelijk foutbericht wanneer de opgegeven uren nul zijn.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="eaa3d-116">Gebruikers ontvangen een onjuiste fout wanneer het maximale aantal tekens is ingevoerd in het veld **Omschrijving** voor een projecttaak.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="eaa3d-117">De pagina **Microsoft Dynamics 365 Project Service Automation-invoegtoepassing downloaden** verwijst naar de Engelse downloadpagina wanneer de taalinstellingen van de gebruiker zijn ingesteld op Japans.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="eaa3d-118">Als er een serverfout optreedt, blijft het synchronisatielabel op het tabblad **Schema** van het formulier **Projecten** soms bestaan.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="eaa3d-119">Bij het wijzigen van een taak worden redundante taakupdates naar de server gestuurd.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="eaa3d-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="eaa3d-120">**Sales**</span></span>

<span data-ttu-id="eaa3d-121">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="eaa3d-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="eaa3d-122">Als op het formulier **Contract** wordt gedubbelklikt op **Factuur maken**, worden twee facturen gemaakt voor één record met werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="eaa3d-123">In Internet Explorer11 kunnen gebruikers geen onkostenboekingen maken.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="eaa3d-124">Terugboeking van kosten en terugboeking van niet-gefactureerde werkelijke verkoopwaarden zijn niet gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="eaa3d-125">Met de knop **Werkelijke waarden vernieuwen** op het formulier **Project** worden niet de **Werkelijke taakuren** vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="eaa3d-126">De invoegtoepassing **PreValidateprojectTeamMemberCreate** kan dubbele generieke boekbare resources creëren wanneer het kenmerk **msdyn_isgenericresourceprojectscoped** op **Onwaar** is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="eaa3d-127">Met **Herberekenen** wist u de toerekenbare kosten van productgebaseerde prijsopgaveregeldetails en contractregeldetails.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="eaa3d-128">In specifieke scenario's geeft de invoegtoepassing **PostEstimateLineUpdate** een uitzonderingsfout met een null-referentie weer.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="eaa3d-129">De duur van de tijdsfase in de grafiek **Winstgevendheidsanalyse** komt niet overeen met de duur van de kosten in de prijsopgaveregeldetails voor de vaste prijs.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="eaa3d-130">Eenheids- en eenheidsgroepwaarden worden niet correct standaard ingesteld voor onkostencategorieën in de formulieren **Contractregeldetails** en **Prijsopgaveregeldetails**.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="eaa3d-131">De lijsten met **Kostprijs organisatie-eenheid** staan overlappingen in de geldigheidsdatums toe.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="eaa3d-132">Het is gebruikers niet toegestaan **OrgUnit** te wijzigen wanneer het ordertype niet op werk is gebaseerd omdat dit zal leiden tot een uitzonderingsfout met een null-referentie.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="eaa3d-133">Wanneer u uit het formulier **Prijsopgaveregeldetails** probeert terug te gaan naar het tabblad **Prijsopgave**, wordt het formulier vernieuwd en verschijnt het tabblad **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="eaa3d-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
