---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 28, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 28, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280212"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="4d0e4-103">Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 28, v3</span><span class="sxs-lookup"><span data-stu-id="4d0e4-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4d0e4-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4d0e4-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4d0e4-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4d0e4-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4d0e4-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4d0e4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4d0e4-109">Dit onderwerp geeft een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation V3, Updateversie 28. Deze versie heeft buildnummer V3.10.46.32 en is algemeen beschikbaar via een zelfupdate in januari 2021.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="4d0e4-110">Updaterelease 28</span><span class="sxs-lookup"><span data-stu-id="4d0e4-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4d0e4-111">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="4d0e4-111">Bug fixes</span></span>

<span data-ttu-id="4d0e4-112">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="4d0e4-112">**Time and Expense**</span></span>

<span data-ttu-id="4d0e4-113">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="4d0e4-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="4d0e4-114">Gebruikers kunnen **Bulkbewerking** gebruiken om tijdsvermeldingen die zijn goedgekeurd en ingediend bij te werken.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="4d0e4-115">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="4d0e4-115">**Project Management**</span></span>

<span data-ttu-id="4d0e4-116">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="4d0e4-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="4d0e4-117">In gevallen waarin de taak-GUID wordt geïnterpreteerd als een getal, kunnen taken niet worden geopend voor bewerking met **Taak bewerken** in het lint op de pagina **Structuur voor werkspecificatie**.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="4d0e4-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4d0e4-118">**Sales**</span></span>

<span data-ttu-id="4d0e4-119">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="4d0e4-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="4d0e4-120">Er wordt een null-referentie-uitzondering gegenereerd wanneer de invoegtoepassing **GetEstimatesForproject** wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="4d0e4-121">**Markeren als klaar voor facturering** op het mijlpaalraster werkt kenmerken slechts gedeeltelijk bij, behalve voor het kenmerk **InvoiceStatus**, dat wel wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="4d0e4-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]