---
title: Het pas ik de bedrijfsprocesstroom Projectfasen aan?
description: Een overzicht van de manier waarop u de bedrijfsprocesstroom Projectfasen aanpast.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125027"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="96c95-103">Het pas ik de bedrijfsprocesstroom Projectfasen aan?</span><span class="sxs-lookup"><span data-stu-id="96c95-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="96c95-104">Er bestaat een bekende beperking in eerdere versies van de Project Service-toepassing dat de namen van de fasen in de bedrijfsprocesstroom Projectfasen exact moeten overeenkomen met de verwachte Engelse namen (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="96c95-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="96c95-105">Anders werkt de bedrijfslogica, die is gebaseerd op de Engelse fasenamen, niet zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="96c95-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="96c95-106">Daarom zijn vertrouwde acties, zoals **Proces omwisselen** of **Proces bewerken**, niet beschikbaar in het projectformulier en het aanpassen van de bedrijfsprocesstroom wordt niet aangeraden.</span><span class="sxs-lookup"><span data-stu-id="96c95-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="96c95-107">Deze beperking is opgelost in versie 2.4.5.48 en hoger.</span><span class="sxs-lookup"><span data-stu-id="96c95-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="96c95-108">Dit artikel bevat voorgestelde oplossingen als u de standaardbedrijfsprocesstroom moet aanpassen voor eerdere versies.</span><span class="sxs-lookup"><span data-stu-id="96c95-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="96c95-109">Bedrijfslogica vereist een exacte overeenkomst met Engels fasenamen</span><span class="sxs-lookup"><span data-stu-id="96c95-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="96c95-110">De bedrijfsprocesstroom Projectfasen bevat bedrijfslogica die het volgende gedrag aanstuurt in de app:</span><span class="sxs-lookup"><span data-stu-id="96c95-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="96c95-111">Wanneer het project aan een offerte wordt gekoppeld, wordt de bedrijfsprocesstroom ingesteld op de fase **Quote**.</span><span class="sxs-lookup"><span data-stu-id="96c95-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="96c95-112">Wanneer het project aan een contract wordt gekoppeld, wordt de bedrijfsprocesstroom ingesteld op de fase **Plan**.</span><span class="sxs-lookup"><span data-stu-id="96c95-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="96c95-113">Wanneer de bedrijfsprocesstroom in de fase **Close** terechtkomt, wordt de projectrecord gedeactiveerd.</span><span class="sxs-lookup"><span data-stu-id="96c95-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="96c95-114">Wanneer het project wordt gedeactiveerd, zijn het projectformulier en de structuur voor werkspecificatie alleen-lezen, worden de benoemde resourceboekingen vrijgegeven en worden eventueel gekoppelde prijslijsten gedeactiveerd.</span><span class="sxs-lookup"><span data-stu-id="96c95-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="96c95-115">De bedrijfslogica is voor de projectfasen afhankelijk van de Engelse namen.</span><span class="sxs-lookup"><span data-stu-id="96c95-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="96c95-116">De afhankelijkheid van de Engelse fasenamen is de belangrijkste reden waarom aanpassingen van de bedrijfsprocesstroom Projectfasen niet wordt aangeraden en waarom u gangbare bedrijfsprocesstroomacties als **Proces omwisselen** of **Proces bewerken** niet tegenkomt in de projectentiteit.</span><span class="sxs-lookup"><span data-stu-id="96c95-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="96c95-117">Wat gebeurt er als de fasenamen niet overeenkomen met de Engelse namen?</span><span class="sxs-lookup"><span data-stu-id="96c95-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="96c95-118">Als in versie 1.x van de Project Service-app op het 8.2-platform de fasenamen in de bedrijfsprocesstroom niet exact overeenkomen met de Engelse fasenamen, wordt de bedrijfslogica waarmee de juiste fase voor prijsopgaven of contracten wordt ingesteld, of het project wordt gesloten, overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="96c95-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="96c95-119">Er worden geen foutberichten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="96c95-119">No error messages are displayed.</span></span> <span data-ttu-id="96c95-120">Daarom lijkt het alsof u de bedrijfsprocesstroom Projectfasen kunt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="96c95-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="96c95-121">U zult er echter achterkomen dat de automatische processen voor prijsopgaven, contracten en het sluiten van projecten niet werken.</span><span class="sxs-lookup"><span data-stu-id="96c95-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="96c95-122">In versie 2.4.4.30 of eerder van de Project Service-app op het 9.0-platform was er een aanzienlijke architectuurverandering in bedrijfsprocesstromen, waarvoor de bedrijfslogica van bedrijfsprocesstromen moest worden herschreven.</span><span class="sxs-lookup"><span data-stu-id="96c95-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="96c95-123">Als gevolg daarvan wordt er een foutbericht weergegeven als de namen van procesfasen niet overeenkomen met de verwachte Engelse namen.</span><span class="sxs-lookup"><span data-stu-id="96c95-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="96c95-124">Als u de bedrijfsprocesstroom Projectfasen voor de projectentiteit wilt aanpassen, kunt u alleen nieuwe fasen toevoegen aan de standaardbedrijfsprocesstroom voor de projectentiteit en de fasen **Quote**, **Plan** en **Close** ongewijzigd laten.</span><span class="sxs-lookup"><span data-stu-id="96c95-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="96c95-125">Deze beperking zorgt ervoor dat u geen fouten over de bedrijfslogica ontvangt omdat er Engels fasenamen worden verwacht in de bedrijfsprocesstroom.</span><span class="sxs-lookup"><span data-stu-id="96c95-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="96c95-126">In versie 2.4.5.48 of hoger is de in dit artikel beschreven bedrijfslogica verwijderd uit de standaardbedrijfsprocesstroom voor de projectentiteit.</span><span class="sxs-lookup"><span data-stu-id="96c95-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="96c95-127">Wanneer u bijwerkt naar die versie of hoger, kunt u de standaardbedrijfsprocesstroom aanpassen of vervangen door een van uw eigen bedrijfsprocesstromen.</span><span class="sxs-lookup"><span data-stu-id="96c95-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="96c95-128">Oplossingen voor eerdere versies</span><span class="sxs-lookup"><span data-stu-id="96c95-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="96c95-129">Als een upgrade geen optie is, kunt u de bedrijfsprocesstroom Projectfasen voor de projectentiteit op een van deze twee manieren aanpassen:</span><span class="sxs-lookup"><span data-stu-id="96c95-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="96c95-130">Voeg extra fasen toe aan de standaardconfiguratie terwijl u de Engelse fasenamen **Quote**, **Plan** en **Close** behoudt.</span><span class="sxs-lookup"><span data-stu-id="96c95-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Schermafbeelding van het toevoegen van fasen aan de standaardconfiguratie](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="96c95-132">Maak uw eigen bedrijfsprocesstroom en stel deze in als de primaire bedrijfsprocesstroom voor de projectentiteit. In dat geval kunt u de gewenste fasenamen instellen.</span><span class="sxs-lookup"><span data-stu-id="96c95-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="96c95-133">Als u echter dezelfde standaardprojectfasen **Quote**, **Plan** en **Close** wilt gebruiken, moet u enkele aanpassingen doorvoeren.</span><span class="sxs-lookup"><span data-stu-id="96c95-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="96c95-134">De meer complexe logica heeft betrekking op de sluiting van het project, die u nog wel kunt wel activeren door de projectrecord te deactiveren.</span><span class="sxs-lookup"><span data-stu-id="96c95-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF-aanpassing](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="96c95-136">Extra overwegingen voor appversie 2.4.4.30 of eerder van Project Service of op platform 9.0</span><span class="sxs-lookup"><span data-stu-id="96c95-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="96c95-137">Wanneer in Project Service 2.4.4.30 of eerdere versies op platform 9.0 aangepaste bedrijfsprocesstromen worden gebruikt, worden het veld **Fasenaam** voor de projectentiteit in het diagram **Project per fase** en projectlijstweergaven niet bijgewerkt omdat deze zijn gekoppeld aan de standaardbedrijfsprocesstroom Projectfasen.</span><span class="sxs-lookup"><span data-stu-id="96c95-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="96c95-138">U lost dit probleem als volgt op:</span><span class="sxs-lookup"><span data-stu-id="96c95-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="96c95-139">Voeg een aangepast veld toe om de huidige bedrijfsprocesstroomfase vast te leggen die wordt bijgewerkt terwijl de gebruiker de aangepaste bedrijfsprocesstroom doorloopt.</span><span class="sxs-lookup"><span data-stu-id="96c95-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="96c95-140">Wijzig het diagram **Project per fase** om met uw aangepaste velden te werken in plaats van met de standaardconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="96c95-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="96c95-141">Stappen om uw eigen bedrijfsprocesstroom voor de projectentiteit te maken</span><span class="sxs-lookup"><span data-stu-id="96c95-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="96c95-142">Ga als volgt te werk om uw eigen bedrijfsprocesstroom voor de projectentiteit te maken:</span><span class="sxs-lookup"><span data-stu-id="96c95-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="96c95-143">Ga naar **Instellingen** > **Verwerkingscentrum**.</span><span class="sxs-lookup"><span data-stu-id="96c95-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="96c95-144">Kopieer de bedrijfsprocesstroom Projectfasen niet omdat dan ook de bedrijfslogica van Project Service wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="96c95-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Proces maken](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="96c95-146">Gebruik de procesontwerper om de gewenste fasenamen te maken.</span><span class="sxs-lookup"><span data-stu-id="96c95-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="96c95-147">Als u dezelfde functionaliteit als de standaardfasen voor **Quote**, **Plan** en **Close** wilt gebruiken, moet u deze maken op basis van de fasenamen van uw aangepaste bedrijfsprocesstroom.</span><span class="sxs-lookup"><span data-stu-id="96c95-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Schermafbeelding van procesontwerper om bedrijfsprocesstromen aan te passen](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="96c95-149">Klik in de procesontwerper op **Orderprocesstroom** om de aangepaste bedrijfsprocesstroom als primaire bedrijfsprocesstroom voor de projectentiteit in te stellen door deze boven de bedrijfsprocesstroom Projectfasen boven aan de lijst te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="96c95-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="96c95-150">Schermafbeelding van het gebruik van Orderprocesstroom</span><span class="sxs-lookup"><span data-stu-id="96c95-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="96c95-151">De volgende stappen gelden voor Project Service-app 2.4.4.30 of eerder op het 9.0-platform.</span><span class="sxs-lookup"><span data-stu-id="96c95-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="96c95-152">Voeg een nieuw aangepast veld aan de projectentiteit toe om de aangepaste fasen in uw aangepaste bedrijfsprocesstroom vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="96c95-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="96c95-153">U moet bedrijfslogica (invoegtoepassing/werkstroom) toevoegen om dit veld bij te werken wanneer de fase in de aangepaste bedrijfsprocesstroom wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="96c95-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Schermafbeelding van het aanpassen van een projectentiteit](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="96c95-155">Wijzig het diagram **Project per fase** om uw nieuwe aangepaste veld voor fasen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="96c95-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Schermafbeelding van het gebruik van het diagram Project per fase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="96c95-157">Wijzig de weergaven voor de projectentiteit om uw nieuwe aangepaste veld voor fasen op te nemen.</span><span class="sxs-lookup"><span data-stu-id="96c95-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Schermafbeelding van het wijzigen van weergaven in de projectentiteit](media/FAQ-Customize-BPF-8-720.png)

