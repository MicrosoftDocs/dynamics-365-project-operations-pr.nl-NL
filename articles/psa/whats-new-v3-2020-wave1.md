---
title: Wat is er nieuw of gewijzigd in Project Service Automation versie 3.x, wave 1 van 2020
description: In dit onderwerp vindt u informatie over wat er nieuw en gewijzigd is in Project Service Automation versie 3, wave 1 van 2020.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074510"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="9adf1-103">Wat is er nieuw of gewijzigd in Project Service Automation versie 3, wave 1 van 2020</span><span class="sxs-lookup"><span data-stu-id="9adf1-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="9adf1-104">In dit onderwerp worden belangrijke overwegingen belicht voor upgraden, wanneer u wilt overstappen naar de nieuwste release van Project Service Automation (PSA) versie 3.x, wave 1 van 2020.</span><span class="sxs-lookup"><span data-stu-id="9adf1-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="9adf1-105">Tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="9adf1-105">Time entry</span></span>
<span data-ttu-id="9adf1-106">De tijdinvoerervaring is uitgebreid en biedt nu mogelijkheden voor het uitbreiden van tijdinvoer naar meer klantenscenario's.</span><span class="sxs-lookup"><span data-stu-id="9adf1-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="9adf1-107">Dit omvat de mogelijkheid om invoertypen toe te voegen, die nu specifiek gedrag aansturen op basis van de veldschemanaam **Instellingen voor tijdinvoer** , weergegeven als **Tijdsbron**.</span><span class="sxs-lookup"><span data-stu-id="9adf1-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings** , displayed as **Time Source**.</span></span> <span data-ttu-id="9adf1-108">De nieuwe oplossing TESA (Time, Expense, Statusing and Approvals) is toegevoegd om deze functionaliteit te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="9adf1-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="9adf1-109">Overwegingen voor het upgraden</span><span class="sxs-lookup"><span data-stu-id="9adf1-109">Upgrade consideration</span></span>
<span data-ttu-id="9adf1-110">Ter ondersteuning van deze functionaliteit zijn de rollen in PSA bijgewerkt met nieuwe rechten.</span><span class="sxs-lookup"><span data-stu-id="9adf1-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="9adf1-111">Deze rechten verlenen leestoegang tot de nieuwe entiteit **Instellingen voor tijdinvoer**.</span><span class="sxs-lookup"><span data-stu-id="9adf1-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="9adf1-112">Gebruikers die tijd moeten kunnen invoeren, moeten de gebruikersrol **Tijdinvoergebruiker** hebben naast bestaande rollen.</span><span class="sxs-lookup"><span data-stu-id="9adf1-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="9adf1-113">Deze rol omvat de nieuwe functionaliteit en zorgt ervoor dat tijdinvoer blijft werken.</span><span class="sxs-lookup"><span data-stu-id="9adf1-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="9adf1-114">Als u bovendien aangepaste app-modules hebt die alle formulieren voor de entiteit tijdsvermeldingen bevatten, moet u het **Formulier voor snelle invoer van TESA-tijdsvermeldingen** uit de module verwijderen.</span><span class="sxs-lookup"><span data-stu-id="9adf1-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="9adf1-115">Momenteel uitgebreide wijzigingen in tijdinvoer</span><span class="sxs-lookup"><span data-stu-id="9adf1-115">Currently extended time entry changes</span></span>
<span data-ttu-id="9adf1-116">Om de impact voor huidige gebruikers van tijdinvoer zo klein mogelijk te houden, is deze rolverandering de enige kernvereiste die nodig is om tijdinvoer te blijven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9adf1-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="9adf1-117">Als u aangepaste weergaven of afzonderlijke tijdinvoerervaringen hebt gemaakt, moet u de velden **Instellingen voor tijdinvoer** instellen op de juiste PSA-waarde.</span><span class="sxs-lookup"><span data-stu-id="9adf1-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
