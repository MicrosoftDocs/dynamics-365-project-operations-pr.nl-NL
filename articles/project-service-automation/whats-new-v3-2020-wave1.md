---
title: Wat is er nieuw of gewijzigd in Project Service Automation versie 3.x, wave 1 van 2020
description: In dit onderwerp vindt u informatie over wat er nieuw en gewijzigd is in Project Service Automation versie 3, wave 1 van 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750750"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="bdeb7-103">Wat is er nieuw of gewijzigd in Project Service Automation versie 3, wave 1 van 2020</span><span class="sxs-lookup"><span data-stu-id="bdeb7-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="bdeb7-104">In dit onderwerp worden belangrijke overwegingen belicht voor upgraden, wanneer u wilt overstappen naar de nieuwste release van Project Service Automation (PSA) versie 3.x, wave 1 van 2020.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="bdeb7-105">Tijdsvermelding</span><span class="sxs-lookup"><span data-stu-id="bdeb7-105">Time entry</span></span>
<span data-ttu-id="bdeb7-106">De tijdinvoerervaring is uitgebreid en biedt nu mogelijkheden voor het uitbreiden van tijdinvoer naar meer klantenscenario's.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="bdeb7-107">Dit omvat de mogelijkheid om invoertypen toe te voegen, die nu specifiek gedrag aansturen op basis van de veldschemanaam **Instellingen voor tijdinvoer**, weergegeven als **Tijdsbron**.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="bdeb7-108">Overwegingen voor het upgraden</span><span class="sxs-lookup"><span data-stu-id="bdeb7-108">Upgrade consideration</span></span>
<span data-ttu-id="bdeb7-109">Ter ondersteuning van deze functionaliteit zijn de rollen in PSA bijgewerkt met nieuwe rechten.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="bdeb7-110">Deze rechten verlenen leestoegang tot de nieuwe entiteit **Instellingen voor tijdinvoer**.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="bdeb7-111">Gebruikers die tijd moeten kunnen invoeren, moeten de gebruikersrol **Tijdinvoergebruiker** hebben naast bestaande rollen.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="bdeb7-112">Deze rol omvat de nieuwe functionaliteit en zorgt ervoor dat tijdinvoer blijft werken.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="bdeb7-113">Momenteel uitgebreide wijzigingen in tijdinvoer</span><span class="sxs-lookup"><span data-stu-id="bdeb7-113">Currently extended time entry changes</span></span>
<span data-ttu-id="bdeb7-114">Om de impact voor huidige gebruikers van tijdinvoer zo klein mogelijk te houden, is deze rolverandering de enige kernvereiste die nodig is om tijdinvoer te blijven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="bdeb7-115">Als u aangepaste weergaven of afzonderlijke tijdinvoerervaringen hebt gemaakt, moet u de velden **Instellingen voor tijdinvoer** instellen op de juiste PSA-waarde.</span><span class="sxs-lookup"><span data-stu-id="bdeb7-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
