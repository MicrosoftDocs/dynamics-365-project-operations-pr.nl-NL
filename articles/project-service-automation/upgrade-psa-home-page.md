---
title: Startpagina upgraden
description: Dit onderwerp laat zien waar u belangrijke informatie vindt over de nieuwe en gewijzigde functies in Dynamics 365 Project Service Automation en het proces voor het upgraden naar de nieuwste versie.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750790"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="7fccc-103">Startpagina upgraden</span><span class="sxs-lookup"><span data-stu-id="7fccc-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="7fccc-104">Upgrade uitvoeren van PSA-versie 2.x of 1.x naar versie 3.x</span><span class="sxs-lookup"><span data-stu-id="7fccc-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="7fccc-105">Nieuwe exemplaren</span><span class="sxs-lookup"><span data-stu-id="7fccc-105">New instances</span></span>

<span data-ttu-id="7fccc-106">Vanaf 17 mei 2019 wordt standaard versie 3.x geïnstalleerd wanneer Project Service Automation is geselecteerd tijdens het inrichten van een nieuw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="7fccc-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="7fccc-107">Bestaande exemplaren</span><span class="sxs-lookup"><span data-stu-id="7fccc-107">Existing instances</span></span>

<span data-ttu-id="7fccc-108">Voorheen moesten klanten die een exemplaar van PSA versie 2.x hebben en wilden upgraden naar versie 3.x met de op Unified Client Interface (UCI) gebaseerde versie van PSA, contact opnemen met Microsoft Ondersteuning en de details van hun exemplaar opgeven, zodat de ondersteuning het exemplaar kon upgraden naar versie 3.x.</span><span class="sxs-lookup"><span data-stu-id="7fccc-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="7fccc-109">Vanaf 1 maart 2020 kunnen klanten die een exemplaar van PSA versie 2.x hebben en moeten upgraden naar versie 3.x, hun exemplaren rechtstreeks vanuit de beheerportal upgraden zonder contact op te nemen met Microsoft Ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="7fccc-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="7fccc-110">PSA versie 3.x bevat belangrijke wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="7fccc-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="7fccc-111">Het is gebouwd op de Unified Interface-framework om een verbeterde gebruikerservaring te bieden.</span><span class="sxs-lookup"><span data-stu-id="7fccc-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="7fccc-112">Het nieuwe ontwerp van de app levert een consistente, uniforme gebruikersinterface die een responsief ontwerp volgt voor een optimale weergave op elke schermgrootte of elk apparaat.</span><span class="sxs-lookup"><span data-stu-id="7fccc-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="7fccc-113">Er zijn ook nog andere wijzigingen doorgevoerd in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="7fccc-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="7fccc-114">Er zijn wijzigingen in prijzen, boeken en toewijzen van resources, tijd, onkosten en goedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="7fccc-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="7fccc-115">We adviseren u om de volgende taken te voltooien voordat u begint met het upgradeproces:</span><span class="sxs-lookup"><span data-stu-id="7fccc-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="7fccc-116">Controleer of zowel Dynamics 365 Field Service als Project Service Automation op het geïdentificeerde exemplaar zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="7fccc-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="7fccc-117">Als beide oplossingen zijn geïnstalleerd, moet u beide upgraden voordat u het normale gebruik van het exemplaar kunt hervatten.</span><span class="sxs-lookup"><span data-stu-id="7fccc-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="7fccc-118">Lees de volgende onderwerpen zorgvuldig door.</span><span class="sxs-lookup"><span data-stu-id="7fccc-118">Carefully review the following topics.</span></span> <span data-ttu-id="7fccc-119">Als u zich bewust bent van en inzicht hebt in de wijzigingen tussen versies, zal dat u helpen bij het upgradeproces.</span><span class="sxs-lookup"><span data-stu-id="7fccc-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="7fccc-120">Deze onderwerpen bevatten informatie over de belangrijkste wijzigingen in PSA, samen met overwegingen en aanbevelingen voor het plannen van de upgrade naar versie 3 x.</span><span class="sxs-lookup"><span data-stu-id="7fccc-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="7fccc-121">Wat is er nieuw of gewijzigd in Project Service Automation versie 3</span><span class="sxs-lookup"><span data-stu-id="7fccc-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="7fccc-122">Overwegingen voor de upgrade van Project Service Automation versie 2.x of 1.x naar versie 3</span><span class="sxs-lookup"><span data-stu-id="7fccc-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="7fccc-123">Upgrade uw sandbox-exemplaar om de wijzigingen in uw implementatie te evalueren voordat u uw productie-exemplaar bijwerkt.</span><span class="sxs-lookup"><span data-stu-id="7fccc-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="7fccc-124">Nadat u de eerder genoemde onderwerpen hebt bekeken en gereed bent om een upgrade uit te voeren naar PSA versie 3.x of de op UCI gebaseerde versie, dient u een verzoek in bij Microsoft Ondersteuning om de upgrade beschikbaar te maken vanuit Beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="7fccc-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="7fccc-125">Geef in uw aanvraag de details van uw exemplaar op.</span><span class="sxs-lookup"><span data-stu-id="7fccc-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="7fccc-126">Oudere versies van PSA (PSA versie 2.x) in een nieuw exemplaar</span><span class="sxs-lookup"><span data-stu-id="7fccc-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="7fccc-127">Vanaf 17 mei 2019 hebben alle nieuwe exemplaren UCI als de standaardclient.</span><span class="sxs-lookup"><span data-stu-id="7fccc-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="7fccc-128">Voor de afstemming met deze wijziging worden PSA versie 3.x en Field Service versie 8.x standaard ingericht, omdat deze versies zijn ontworpen om te werken met de UCI-client.</span><span class="sxs-lookup"><span data-stu-id="7fccc-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="7fccc-129">Vanaf 1 maart 2020 kunnen klanten met Dynamics PSA geen nieuwe omgevingen meer maken met oudere versies van PSA, bijvoorbeeld PSA versie 2.x of lager.</span><span class="sxs-lookup"><span data-stu-id="7fccc-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="7fccc-130">Elke nieuwe omgeving krijgt alleen versie 3.x van PSA.</span><span class="sxs-lookup"><span data-stu-id="7fccc-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="7fccc-131">Voor de beste ervaring wanneer u oudere versies van de Field Service- en PSA-toepassingen gebruikt, gaat u naar de pagina **Systeeminstellingen** en selecteert u voor het veld **Alleen de nieuwe Unified Interface gebruiken (aanbevolen)** de optie **Nee** omdat deze versies niet zijn ontworpen om correct te worden geladen in UCI.</span><span class="sxs-lookup"><span data-stu-id="7fccc-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="7fccc-132">Nadat u UCI hebt uitgeschakeld, kunt u deze versies van Field Service en PSA openen en uitvoeren met de oude webclient.</span><span class="sxs-lookup"><span data-stu-id="7fccc-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="7fccc-133">Zie [Alleen Unified Interface inschakelen](../admin/enable-unified-interface-only.md) voor instructies over het uitschakelen van de UCI-client.</span><span class="sxs-lookup"><span data-stu-id="7fccc-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>
