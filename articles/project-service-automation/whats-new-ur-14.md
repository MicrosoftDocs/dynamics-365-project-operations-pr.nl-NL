---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 14, v3
description: Dit onderwerp bevat informatie over wat er nieuw en gewijzigd is in Project Service Automation updaterelease 14, v3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750753"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="eda81-103">Wat is er nieuw of gewijzigd in Project Service Automation v3, updaterelease 14</span><span class="sxs-lookup"><span data-stu-id="eda81-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="eda81-104">Met genoegen kondigen we de nieuwste update voor de toepassing Dynamics 365 Project Service Automation (PSA) aan.</span><span class="sxs-lookup"><span data-stu-id="eda81-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="eda81-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="eda81-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eda81-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="eda81-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eda81-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365. Hierin gaat u naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="eda81-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="eda81-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="eda81-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eda81-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor PSA v3, updaterelease 14.</span><span class="sxs-lookup"><span data-stu-id="eda81-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="eda81-110">Deze versie heeft het buildnummer V3.10.4.21 en komt beschikbaar volgens de volgende planning:</span><span class="sxs-lookup"><span data-stu-id="eda81-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="eda81-111">**Algemene beschikbaarheid (zelf-update):** januari 2020</span><span class="sxs-lookup"><span data-stu-id="eda81-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="eda81-112">**Automatische update:** februari 2020</span><span class="sxs-lookup"><span data-stu-id="eda81-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="eda81-113">Updaterelease 14</span><span class="sxs-lookup"><span data-stu-id="eda81-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="eda81-114">Verbeteringen</span><span class="sxs-lookup"><span data-stu-id="eda81-114">Enhancements</span></span>

- <span data-ttu-id="eda81-115">Sales</span><span class="sxs-lookup"><span data-stu-id="eda81-115">Sales</span></span>

     - <span data-ttu-id="eda81-116">Aangepaste veldwaarden van **Details van prijsopgaveregel** worden gekopieerd naar **Details van projectcontractregels** wanneer een prijsopgave wordt bijgewerkt naar **Afsluiten als binnengehaald**.</span><span class="sxs-lookup"><span data-stu-id="eda81-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="eda81-117">Bevestigde projecten kunnen worden **afgesloten als gemist**.</span><span class="sxs-lookup"><span data-stu-id="eda81-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="eda81-118">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="eda81-118">Resource Management</span></span>

     - <span data-ttu-id="eda81-119">Bij het uitbreiden van boekingen wordt gebruikers met een bevestigingsdialoogvenster gevraagd om boekingsresultaten samen te vatten en een link naar Boekingen bijhouden op te geven.</span><span class="sxs-lookup"><span data-stu-id="eda81-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="eda81-120">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="eda81-120">Bug fixes</span></span>

- <span data-ttu-id="eda81-121">Tijd en onkosten</span><span class="sxs-lookup"><span data-stu-id="eda81-121">Time and Expense</span></span>

     - <span data-ttu-id="eda81-122">Opgelost: verbeterde gebruikerservaring wanneer de gebruiker geen items heeft geselecteerd om te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="eda81-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="eda81-123">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="eda81-123">Resource Management</span></span>

     - <span data-ttu-id="eda81-124">Opgelost: als een resource meerdere keren wordt geboekt, treedt een overflow van de naam van de te boeken resource op.</span><span class="sxs-lookup"><span data-stu-id="eda81-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="eda81-125">Sales</span><span class="sxs-lookup"><span data-stu-id="eda81-125">Sales</span></span>

     - <span data-ttu-id="eda81-126">Opgelost: de totale verkoopprijs wordt niet berekend totdat de gebruiker ook een kostprijs invoert voor geschatte onkosten voor een project.</span><span class="sxs-lookup"><span data-stu-id="eda81-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="eda81-127">Opgelost: een offerte afsluiten als **binnengehaald** mislukt als het bijbehorende projectcontract niet de status **Concept** heeft.</span><span class="sxs-lookup"><span data-stu-id="eda81-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

