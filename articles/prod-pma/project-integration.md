---
title: Microsoft Project Client-integratie
description: Het plannen en bijhouden van een projectplanning kan complex zijn, dus projectmanagers moeten tools gebruiken die hen helpen bij het beheren van deze taak. Integratie met Microsoft Project Client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289318"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="f42ea-104">Microsoft Project Client-integratie</span><span class="sxs-lookup"><span data-stu-id="f42ea-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f42ea-105">Het plannen en bijhouden van een projectplanning kan complex zijn, dus projectmanagers moeten tools gebruiken die hen helpen bij het beheren van deze taak.</span><span class="sxs-lookup"><span data-stu-id="f42ea-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="f42ea-106">Integratie met Microsoft Project Client biedt ondersteuning voor het openen en beheren van een projectstructuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="f42ea-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="f42ea-107">De projectmanager kan eventuele wijzigingen terug publiceren naar de Dynamics 365 Finance-projectstructuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="f42ea-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="f42ea-108">Als u de update van juli (versie 10.0.4) gebruikt, moet u KB 4054797 en 4055884 installeren.</span><span class="sxs-lookup"><span data-stu-id="f42ea-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="f42ea-109">De invoegtoepassing Microsoft project Client configureren</span><span class="sxs-lookup"><span data-stu-id="f42ea-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="f42ea-110">Om de integratie met Microsoft Project Client mogelijk te maken, moet een Microsoft Dynamics 365-invoegtoepassing worden geïnstalleerd in de Microsoft Project-clienttoepassing van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="f42ea-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="f42ea-111">Dit doet u door de **Werkruimte voor projectmanagement** te openen.</span><span class="sxs-lookup"><span data-stu-id="f42ea-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="f42ea-112">•   Klik op **Project Client-invoegtoepassing configureren** vanuit de sectie **Koppelingen** > **Instelling** van de werkruimte.</span><span class="sxs-lookup"><span data-stu-id="f42ea-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="f42ea-113">•   Klik op **Openen** en vervolgens op **Uitvoeren** als daarom gevraagd wordt.</span><span class="sxs-lookup"><span data-stu-id="f42ea-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="f42ea-114">Een bestaande conceptstructuur voor werkspecificatie openen en bewerken in Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f42ea-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="f42ea-115">Als een project in Dynamics 365 Finance al een structuur voor werkspecificatie heeft gemaakt, kan de structuur voor werkspecificatie worden geopend in de toepassing Microsoft Project Client als de structuur voor werkspecificatie zich in een conceptstatus bevindt.</span><span class="sxs-lookup"><span data-stu-id="f42ea-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="f42ea-116">U kunt openen vanaf de pagina **Project** door op de koppeling **Openen in Microsoft Project** te klikken op het tabblad **Plannen**. Deze pagina kan ook worden geopend vanuit de Microsoft Project Client-toepassing door op **Openen** te klikken op het tabblad **Microsoft Dynamics 365**. Selecteer de **rechtspersoon** en het **project** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f42ea-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="f42ea-117">Als u Internet Explorer als uw browser gebruikt, moet u op **Opslaan** klikken om handmatig te openen vanaf de locatie waarnaar het bestand is gedownload.</span><span class="sxs-lookup"><span data-stu-id="f42ea-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="f42ea-118">Of klik op **Opslaan en openen** om het bestand te openen in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f42ea-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="f42ea-119">Wijzig de bestandsnaam niet tijdens het opslaan.</span><span class="sxs-lookup"><span data-stu-id="f42ea-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="f42ea-120">Voordat u het bestand bewerkt met Microsoft Project Client, moet u het eerst controleren. Klik op **Uitchecken** op het tabblad **Microsoft Dynamics 365**. Dit voorkomt dat andere gebruikers de structuur voor werkspecificatie tegelijkertijd kunnen bewerken binnen Finance.</span><span class="sxs-lookup"><span data-stu-id="f42ea-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="f42ea-121">Als u de structuur voor werkspecificatie wilt publiceren nadat eventuele bewerkingen zijn voltooid, klikt u op **Inhecken** op het tabblad **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="f42ea-122">Als er al een projectteam is toegevoegd aan het project in Finance, wordt de resourcelijst gevuld met de teamleden.</span><span class="sxs-lookup"><span data-stu-id="f42ea-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="f42ea-123">Als er nog geen projectteam aan het project is toegevoegd, kunt u resources selecteren en het team samenstellen binnen Microsoft Project Client door op de knop **Resources** te klikken op het tabblad **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="f42ea-124">De volgende gegevens worden teruggesynchroniseerd naar Finance als onderdeel van het incheckproces:</span><span class="sxs-lookup"><span data-stu-id="f42ea-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="f42ea-125">•   Taaknaam</span><span class="sxs-lookup"><span data-stu-id="f42ea-125">•   Task name</span></span>

<span data-ttu-id="f42ea-126">•   Begindatum</span><span class="sxs-lookup"><span data-stu-id="f42ea-126">•   Start date</span></span>

<span data-ttu-id="f42ea-127">•   Einddatum</span><span class="sxs-lookup"><span data-stu-id="f42ea-127">•   Finish date</span></span>

<span data-ttu-id="f42ea-128">•   Voorgaande elementen</span><span class="sxs-lookup"><span data-stu-id="f42ea-128">•   Predecessors</span></span>

<span data-ttu-id="f42ea-129">•   Resourcenamen</span><span class="sxs-lookup"><span data-stu-id="f42ea-129">•   Resource names</span></span>

<span data-ttu-id="f42ea-130">•   Categorie</span><span class="sxs-lookup"><span data-stu-id="f42ea-130">•   Category</span></span>

<span data-ttu-id="f42ea-131">•   Resourcecategorie</span><span class="sxs-lookup"><span data-stu-id="f42ea-131">•   Resource category</span></span>

<span data-ttu-id="f42ea-132">•   Werkuren</span><span class="sxs-lookup"><span data-stu-id="f42ea-132">•   Work hours</span></span>

<span data-ttu-id="f42ea-133">•   Notities</span><span class="sxs-lookup"><span data-stu-id="f42ea-133">•   Notes</span></span>

<span data-ttu-id="f42ea-134">•   Prioriteit</span><span class="sxs-lookup"><span data-stu-id="f42ea-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="f42ea-135">Als u andere kolommen aan uw Microsoft Project Client-bestand toevoegt, worden deze niet in het bestand opgeslagen en worden ze niet weergegeven wanneer het bestand opnieuw wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="f42ea-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f42ea-136">De structuur voor werkspecificatie maken voor een bestaand project met Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f42ea-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f42ea-137">Als u een nieuwe structuur voor werkspecificatie wilt maken Microsoft Project Client, voert u deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="f42ea-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="f42ea-138">Open Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f42ea-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f42ea-139">Klik op het tabblad **Microsoft Dynamics 365** op **Openen**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="f42ea-140">Selecteer de **rechtspersoon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="f42ea-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="f42ea-141">Selecteer het **project**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="f42ea-142">Klik op **Uitchecken** op het tabblad **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="f42ea-143">Als u gereed bent om naar Finance te publiceren, klikt u op **Inchecken** op het tabblad **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f42ea-144">De bestaande structuur voor werkspecificatie vervangen voor een bestaand project met Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f42ea-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f42ea-145">Volg deze stappen om een nieuwe structuur voor werkspecificatie te maken met Microsoft Project Client en een bestaande structuur voor werkspecificatie te vervangen voor een bestaand project:</span><span class="sxs-lookup"><span data-stu-id="f42ea-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="f42ea-146">Open de Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f42ea-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f42ea-147">Maak de planning in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f42ea-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f42ea-148">Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Bestaand project vervangen**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="f42ea-149">Selecteer de **rechtspersoon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="f42ea-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f42ea-150">Selecteer het **project**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="f42ea-151">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="f42ea-152">Een nieuw project makien vanuit Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="f42ea-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="f42ea-153">Open de Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f42ea-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f42ea-154">Maak de planning in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="f42ea-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f42ea-155">Klik op het tabblad **Microsoft Dynamics 365** op **Wijzigingen opslaan** > **Opslaan naar nieuw project**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="f42ea-156">Selecteer de **rechtspersoon** voor het project.</span><span class="sxs-lookup"><span data-stu-id="f42ea-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f42ea-157">Voer de **project-id** in, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="f42ea-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="f42ea-158">Voer de **projectnaam** in.</span><span class="sxs-lookup"><span data-stu-id="f42ea-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="f42ea-159">Selecteer het **projecttype**, de **projectgroep** en de **projectcontract-id**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="f42ea-160">U kunt ook een nieuw projectcontract maken door op **Nieuw** te klikken.</span><span class="sxs-lookup"><span data-stu-id="f42ea-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="f42ea-161">Selecteer de **agenda** die moet worden gebruikt voor het toewijzen van resources.</span><span class="sxs-lookup"><span data-stu-id="f42ea-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="f42ea-162">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="f42ea-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]