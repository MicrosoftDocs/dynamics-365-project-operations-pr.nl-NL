---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 13, v3
description: Dit onderwerp bevat informatie over wat er nieuw en gewijzigd is in Project Service Automation updaterelease 13, v3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121617"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="a786a-103">Project Service Automation, updaterelease 13, v3</span><span class="sxs-lookup"><span data-stu-id="a786a-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="a786a-104">Met genoegen kondigen we de nieuwste update voor de toepassing Dynamics 365 Project Service Automation (PSA) aan.</span><span class="sxs-lookup"><span data-stu-id="a786a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a786a-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="a786a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a786a-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a786a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a786a-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365. Hierin gaat u naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="a786a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a786a-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a786a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a786a-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 13.</span><span class="sxs-lookup"><span data-stu-id="a786a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="a786a-110">Deze versie heeft het buildnummer V3.10.3.18 en komt beschikbaar volgens de volgende planning:</span><span class="sxs-lookup"><span data-stu-id="a786a-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="a786a-111">**Algemene beschikbaarheid (zelf-update):** november 2019</span><span class="sxs-lookup"><span data-stu-id="a786a-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="a786a-112">**Automatische update**: december 2019</span><span class="sxs-lookup"><span data-stu-id="a786a-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="a786a-113">Updaterelease 13</span><span class="sxs-lookup"><span data-stu-id="a786a-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="a786a-114">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="a786a-114">Bug fixes</span></span>

- <span data-ttu-id="a786a-115">Tijd en onkosten</span><span class="sxs-lookup"><span data-stu-id="a786a-115">Time and Expense</span></span>

     - <span data-ttu-id="a786a-116">Opgelost: zoekfunctionaliteit op de pagina **Onkostengoedkeuring** werkt niet wanneer wordt gezocht op kosten.</span><span class="sxs-lookup"><span data-stu-id="a786a-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="a786a-117">Resourcebeheer</span><span class="sxs-lookup"><span data-stu-id="a786a-117">Resource Management</span></span>

     - <span data-ttu-id="a786a-118">Opgelost: getallen in de afstemming worden nu rechts uitgelijnd.</span><span class="sxs-lookup"><span data-stu-id="a786a-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="a786a-119">Opgelost: benoemde resources kunnen niet worden toegewezen aan taken via het tabblad **Planning**.</span><span class="sxs-lookup"><span data-stu-id="a786a-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="a786a-120">Projectbeheer</span><span class="sxs-lookup"><span data-stu-id="a786a-120">Project Management</span></span>

     - <span data-ttu-id="a786a-121">Opgelost: uitzondering met verwijzing naar lege waarde treedt op bij het toewijzen van een teamlid wanneer in het **Transactietype** setup-informatie ontbreekt voor **Eenheid** en **Standaardgroep**.</span><span class="sxs-lookup"><span data-stu-id="a786a-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="a786a-122">Sales</span><span class="sxs-lookup"><span data-stu-id="a786a-122">Sales</span></span>

     - <span data-ttu-id="a786a-123">Opgelost: dubbele transactietyperecords retourneren een fout wanneer rolprijsrecords worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a786a-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="a786a-124">Opgelost: extra knoppen voor **Nieuwe verkoopkans**, **Prijsopgave**, **Orderregel** en **Product toevoegen** zijn zichtbaar in opdrachten voor Verkoopkansen, Prijsopgaven, Bestelproducten en het projectgebaseerde regelsubraster.</span><span class="sxs-lookup"><span data-stu-id="a786a-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


