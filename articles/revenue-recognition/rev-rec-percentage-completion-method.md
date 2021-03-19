---
title: Projecten met omzetschattingen met een vaste prijs
description: Dit onderwerp bevat informatie over opbrengsten met een vaste prijs in projecten.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278907"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="3d522-103">Projecten met omzetschattingen met een vaste prijs</span><span class="sxs-lookup"><span data-stu-id="3d522-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="3d522-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="3d522-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3d522-105">Wanneer u een projectcontractregel maakt met de volgende kenmerken in Dynamics 365 Project Operations voor Microsoft Dataverse, maakt het systeem automatisch een project met een geschatte omzet met een vaste prijs.</span><span class="sxs-lookup"><span data-stu-id="3d522-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="3d522-106">De gegevens in dit project worden gebaseerd op het volgende:</span><span class="sxs-lookup"><span data-stu-id="3d522-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="3d522-107">Een factureringsmethode met een vaste prijs.</span><span class="sxs-lookup"><span data-stu-id="3d522-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="3d522-108">Een gekoppeld project.</span><span class="sxs-lookup"><span data-stu-id="3d522-108">An associated project.</span></span>
  - <span data-ttu-id="3d522-109">Er is minstens één mijlpaal gedefinieerd op het tabblad **Factuurschema** op de pagina **Projectcontractregel**.</span><span class="sxs-lookup"><span data-stu-id="3d522-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="3d522-110">Projecten met omzetschattingen met een vaste prijs beoordelen</span><span class="sxs-lookup"><span data-stu-id="3d522-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="3d522-111">Voer de volgende stappen uit om projecten met een geschatte omzet met een vaste prijs te bekijken:</span><span class="sxs-lookup"><span data-stu-id="3d522-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="3d522-112">Ga in de Dynamics 365 Finance-omgeving naar **Projectbeheer en boekhouding** > **Projecten** > **Projecten met omzetschattingen met een vaste prijs**.</span><span class="sxs-lookup"><span data-stu-id="3d522-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="3d522-113">Selecteer het project dat u wilt bekijken en dubbelklik op de **Schattingsproject-id** om de record te openen en de details van het project te bekijken.</span><span class="sxs-lookup"><span data-stu-id="3d522-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="3d522-114">Vouw het tabblad **Project** uit. U ziet één project in het raster **Geselecteerde projecten**.</span><span class="sxs-lookup"><span data-stu-id="3d522-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="3d522-115">Het systeem gebruikt dit als standaardproject omdat dit het project is dat is gekoppeld aan de projectcontractregel.</span><span class="sxs-lookup"><span data-stu-id="3d522-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="3d522-116">Als u de koppeling wilt wijzigen, selecteert u aanvullende projecten en voegt u ze toe aan het raster **Geselecteerde projecten**.</span><span class="sxs-lookup"><span data-stu-id="3d522-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="3d522-117">Als er meerdere projecten zijn geselecteerd in dit raster, worden het projectpercentage van voltooiing en omzetramingen samen berekend voor alle geselecteerde projecten.</span><span class="sxs-lookup"><span data-stu-id="3d522-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="3d522-118">Projectkosten, inkomstenprofiel, kostensjabloon en de periodecode kunnen handmatig worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="3d522-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="3d522-119">Als ze niet handmatig worden ingesteld, worden de standaardwaarden gebruikt van de eerste schattingsberekening voor het project met behulp van de regels die zijn geconfigureerd voor projectkosten- en opbrengstprofielen.</span><span class="sxs-lookup"><span data-stu-id="3d522-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]