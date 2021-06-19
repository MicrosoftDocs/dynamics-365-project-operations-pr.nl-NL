---
title: Problemen oplossen met het werken in het taakraster
description: Dit onderwerp biedt informatie over het oplossen van problemen, die nodig is bij het werken in het taakraster.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213394"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="03f9f-103">Problemen oplossen met het werken in het taakraster</span><span class="sxs-lookup"><span data-stu-id="03f9f-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="03f9f-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="03f9f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="03f9f-105">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die u kunt tegenkomen tijdens het werken met Cost Management.</span><span class="sxs-lookup"><span data-stu-id="03f9f-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="03f9f-106">Cookies inschakelen</span><span class="sxs-lookup"><span data-stu-id="03f9f-106">Enable cookies</span></span>

<span data-ttu-id="03f9f-107">Project Operations vereist dat cookies van derden worden ingeschakeld om de structuur voor werkspecificatie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="03f9f-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="03f9f-108">Wanneer cookies van derden niet zijn ingeschakeld, ziet u in plaats van taken een lege pagina wanneer u het tabblad **Taken** selecteert op de pagina **Project**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Leeg tabblad wanneer cookies van derden niet zijn ingeschakeld](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="03f9f-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="03f9f-110">Workaround</span></span>
<span data-ttu-id="03f9f-111">Voor Microsoft Edge of Google Chrome-browsers, beschrijven de volgende procedures hoe u uw browserinstellingen kunt bijwerken om cookies van derden in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="03f9f-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="03f9f-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="03f9f-112">Microsoft Edge</span></span>

1. <span data-ttu-id="03f9f-113">Open de Microsoft Edge-browser.</span><span class="sxs-lookup"><span data-stu-id="03f9f-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="03f9f-114">Selecteer in de rechterbovenhoek het **beletselteken** (...) en selecteer vervolgens **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="03f9f-115">Selecteer onder **Cookies en sitemachtigingen**, **Cookies en sitegegevens**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="03f9f-116">Schakel **Cookies van derden blokkeren** uit.</span><span class="sxs-lookup"><span data-stu-id="03f9f-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="03f9f-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="03f9f-117">Google Chrome</span></span>

1. <span data-ttu-id="03f9f-118">Open uw Chrome-browser.</span><span class="sxs-lookup"><span data-stu-id="03f9f-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="03f9f-119">Selecteer in de rechterbovenhoek de drie verticale puntjes en selecteer vervolgens **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="03f9f-120">Selecteer onder **Privacy en beveiliging**, **Cookies en overige sitegegevens**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="03f9f-121">Selecteer **Alle cookies toestaan**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03f9f-122">Als u cookies van derden blokkeert, worden alle cookies en sitegegevens van andere sites geblokkeerd, zelfs als de site is toegestaan op uw uitzonderingenlijst.</span><span class="sxs-lookup"><span data-stu-id="03f9f-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="03f9f-123">PEX-eindpunt</span><span class="sxs-lookup"><span data-stu-id="03f9f-123">PEX Endpoint</span></span>

<span data-ttu-id="03f9f-124">Project Operations vereist dat een projectparameter verwijst naar het PEX-eindpunt.</span><span class="sxs-lookup"><span data-stu-id="03f9f-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="03f9f-125">Dit eindpunt is vereist om te communiceren met de service die wordt gebruikt om de structuur voor werkspecificatie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="03f9f-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="03f9f-126">Als de parameter niet is ingeschakeld, ontvangt u de fout 'De projectparameter is niet geldig'.</span><span class="sxs-lookup"><span data-stu-id="03f9f-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="03f9f-127">Oplossing</span><span class="sxs-lookup"><span data-stu-id="03f9f-127">Workaround</span></span>
 ![Het veld PEX-eindpunt op de projectparameter](media/projectparameter.png)

1. <span data-ttu-id="03f9f-129">Voeg het veld **PEX-eindpunt** toe aan de pagina **Projectparameters**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="03f9f-130">Werk het veld bij met de volgende waarde: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="03f9f-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="03f9f-131">Verwijder het veld uit de pagina **Projectparameters**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="03f9f-132">Bevoegdheden voor Project for the Web</span><span class="sxs-lookup"><span data-stu-id="03f9f-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="03f9f-133">Project Operations is afhankelijk van een externe planningsservice.</span><span class="sxs-lookup"><span data-stu-id="03f9f-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="03f9f-134">De service vereist dat een gebruiker verschillende rollen heeft toegewezen gekregen om te lezen en te schrijven naar entiteiten die verband houden met de structuur voor werkspecificatie.</span><span class="sxs-lookup"><span data-stu-id="03f9f-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="03f9f-135">Deze entiteiten omvatten projecttaken, resourcetoewijzingen en taakafhankelijkheden.</span><span class="sxs-lookup"><span data-stu-id="03f9f-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="03f9f-136">Als een gebruiker de structuur voor werkspecificatie niet kan weergeven wanneer hij naar het tabblad **Taken** gaat, is dit waarschijnlijk omdat Project voor Project Operations niet is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="03f9f-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="03f9f-137">Een gebruiker kan ofwel een beveiligingsrol-fout ontvangen of een fout gerelateerd aan een weigering van toegang.</span><span class="sxs-lookup"><span data-stu-id="03f9f-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="03f9f-138">Oplossing</span><span class="sxs-lookup"><span data-stu-id="03f9f-138">Workaround</span></span>

1. <span data-ttu-id="03f9f-139">Ga naar **Instellingen > Beveiliging > Gebruikers > Toepassingsgebruikers**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Toepassingslezer](media/applicationuser.jpg)
   
2. <span data-ttu-id="03f9f-141">Dubbelklik op de toepassingsgebruikersrecord om het volgende te controleren:</span><span class="sxs-lookup"><span data-stu-id="03f9f-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="03f9f-142">De gebruiker heeft toegang tot het project.</span><span class="sxs-lookup"><span data-stu-id="03f9f-142">The user has access to the project.</span></span> <span data-ttu-id="03f9f-143">Deze verificatie wordt meestal gedaan door ervoor te zorgen dat de gebruiker de beveiligingsrol **Projectleider** heeft.</span><span class="sxs-lookup"><span data-stu-id="03f9f-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="03f9f-144">De gebruiker van de Microsoft Project-toepassing bestaat en is correct geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="03f9f-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="03f9f-145">Als deze gebruiker niet bestaat, kunt uw een nieuwe gebruikersrecord maken.</span><span class="sxs-lookup"><span data-stu-id="03f9f-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="03f9f-146">Selecteer **Nieuwe gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="03f9f-146">Select **New Users**.</span></span> <span data-ttu-id="03f9f-147">Wijzig het inschrijfformulier in **Toepassingsgebruiker** en voeg vervolgens de **Toepassings-id** toe.</span><span class="sxs-lookup"><span data-stu-id="03f9f-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Gegevens van toepassingsgebruiker](media/applicationuserdetails.jpg)

4. <span data-ttu-id="03f9f-149">Controleer of de gebruiker de juiste licentie heeft gekregen en of de service is ingeschakeld in de gegevens van de serviceplannen van de licentie.</span><span class="sxs-lookup"><span data-stu-id="03f9f-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="03f9f-150">Controleer of de gebruiker project.microsoft.com kan openen.</span><span class="sxs-lookup"><span data-stu-id="03f9f-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="03f9f-151">Controleer via de projectparameters of het systeem naar het juiste projecteindpunt verwijst.</span><span class="sxs-lookup"><span data-stu-id="03f9f-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="03f9f-152">Controleer of de gebruiker van de projecttoepassing is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="03f9f-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="03f9f-153">Pas de volgende beveiligingsrollen toe op de gebruiker:</span><span class="sxs-lookup"><span data-stu-id="03f9f-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="03f9f-154">Dataverse-gebruiker</span><span class="sxs-lookup"><span data-stu-id="03f9f-154">Dataverse User</span></span>
  - <span data-ttu-id="03f9f-155">Project Operations-systeem</span><span class="sxs-lookup"><span data-stu-id="03f9f-155">Project Operations System</span></span>
  - <span data-ttu-id="03f9f-156">Projectsysteem</span><span class="sxs-lookup"><span data-stu-id="03f9f-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="03f9f-157">Fout bij het bijwerken van de structuur voor werkspecificatie</span><span class="sxs-lookup"><span data-stu-id="03f9f-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="03f9f-158">Wanneer een of meer updates worden aangebracht in de structuur voor werkspecificatie, mislukken de wijzigingen uiteindelijk en worden deze niet opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="03f9f-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="03f9f-159">Er treedt een fout op in het planningsraster dat aangeeft 'Recente wijzigingen die u hebt aangebracht, konden niet worden opgeslagen'.</span><span class="sxs-lookup"><span data-stu-id="03f9f-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="03f9f-160">Oplossing</span><span class="sxs-lookup"><span data-stu-id="03f9f-160">Workaround</span></span>

1. <span data-ttu-id="03f9f-161">Controleer of de gebruiker de juiste licentie heeft gekregen en of de service is ingeschakeld in de gegevens van de serviceplannen van de licentie.</span><span class="sxs-lookup"><span data-stu-id="03f9f-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="03f9f-162">Controleer of de gebruiker project.microsoft.com kan openen.</span><span class="sxs-lookup"><span data-stu-id="03f9f-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="03f9f-163">Controleer of het systeem naar het juiste projecteindpunt verwijst.</span><span class="sxs-lookup"><span data-stu-id="03f9f-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="03f9f-164">Controleer of de gebruiker van de projecttoepassing is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="03f9f-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="03f9f-165">Pas de volgende beveiligingsrollen toe op de gebruiker:</span><span class="sxs-lookup"><span data-stu-id="03f9f-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="03f9f-166">Dataverse-gebruiker of standaardgebruiker</span><span class="sxs-lookup"><span data-stu-id="03f9f-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="03f9f-167">Project Operations-systeem</span><span class="sxs-lookup"><span data-stu-id="03f9f-167">Project Operations System</span></span>
  - <span data-ttu-id="03f9f-168">Projectsysteem</span><span class="sxs-lookup"><span data-stu-id="03f9f-168">Project System</span></span>
  - <span data-ttu-id="03f9f-169">Twee keer wegschrijven in Project Operations (deze rol is vereist als u het scenario op basis van resource/ niet-voorradige artikelen van project Operations implementeert.)</span><span class="sxs-lookup"><span data-stu-id="03f9f-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
