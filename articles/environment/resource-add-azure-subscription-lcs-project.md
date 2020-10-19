---
title: Een Azure-abonnement toevoegen aan een LCS-project
description: Dit onderwerp biedt informatie over hoe u uw Azure-abonnement kunt verbinden met een LCS-project.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948821"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="c357d-103">Een Azure-abonnement toevoegen aan een LCS-project</span><span class="sxs-lookup"><span data-stu-id="c357d-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="c357d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="c357d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c357d-105">Gehoste cloudomgevingen moeten worden geïmplementeerd met een bestaand Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="c357d-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="c357d-106">Dit onderwerp wordt uitgelegd hoe u uw bestaande Azure-abonnement kunt verbinden met een LCS-project.</span><span class="sxs-lookup"><span data-stu-id="c357d-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="c357d-107">Beheerderstoestemming verlenen</span><span class="sxs-lookup"><span data-stu-id="c357d-107">Grant admin consent</span></span>

1. <span data-ttu-id="c357d-108">Selecteer in uw LCS-project in de sectie **Omgevingen** de optie **Microsoft Azure-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="c357d-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Instellingen voor Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="c357d-110">Op de pagina **Projectinstellingen** op het tabblad **Azure-connectors** selecteert u **Autoriseren**.</span><span class="sxs-lookup"><span data-stu-id="c357d-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="c357d-111">Hierdoor kunnen omgevingen worden ingezet voor dit project.</span><span class="sxs-lookup"><span data-stu-id="c357d-111">This allows environments to be deployed to this project.</span></span>

![Azure-connectors](./media/2AzureConnectors.png)

3. <span data-ttu-id="c357d-113">Selecteer opnieuw **Autoriseren** voor toestemming van de beheerder.</span><span class="sxs-lookup"><span data-stu-id="c357d-113">Select **Authorize** again to provide admin consent.</span></span>

![Beheerderstoestemming verlenen](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="c357d-115">Accepteer het machtigingenverzoek.</span><span class="sxs-lookup"><span data-stu-id="c357d-115">Accept the permissions request.</span></span>

![Machtigingsverzoek accepteren](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="c357d-117">De autorisatie is nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="c357d-117">The authorization is now complete.</span></span> 

![Autorisatie geslaagd](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="c357d-119">Dynamics Deployment Services toegang geven tot uw Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="c357d-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="c357d-120">Ga naar [Facturering Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) en selecteer uw abonnement.</span><span class="sxs-lookup"><span data-stu-id="c357d-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="c357d-121">Dynamics Deployment Services heeft toegang nodig tot dit abonnement om omgevingen te kunnen implementeren.</span><span class="sxs-lookup"><span data-stu-id="c357d-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Details van Azure-abonnement](./media/6AzureSubscription.png)

2. <span data-ttu-id="c357d-123">Selecteer **Toegangsbeheer (IAM)** in het navigatiedeelvenster en selecteer vervolgens **Roltoewijzing toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c357d-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="c357d-124">Selecteer in de schuifregelaar aan de rechterkant **Rol van inzender** en zoek en selecteer in de weergegeven lijst **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="c357d-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="c357d-125">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c357d-125">Select **Save**.</span></span>

![Toegang tot abonnement](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="c357d-127">Een abonnementsconnector toevoegen aan een LCS-project</span><span class="sxs-lookup"><span data-stu-id="c357d-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="c357d-128">In uw LCS-project op de pagina **Microsoft Azure-instellingen** selecteert u **Toevoegen** om een nieuwe connector toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c357d-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="c357d-129">Voer de id van uw Azure-abonnement in.</span><span class="sxs-lookup"><span data-stu-id="c357d-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="c357d-130">U vindt uw Azure-abonnements-id in de [Azure-portal](https://ms.portal.azure.com/), onder **Instellingen** linksonder in het scherm.</span><span class="sxs-lookup"><span data-stu-id="c357d-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="c357d-131">In het veld **Configureer om Azure Resource Manager te gebruiken** selecteert u **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c357d-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="c357d-132">Zorg ervoor dat het AAD-tenantdomein van het Azure-abonnement overeenkomt met het Azure-abonnement dat eigenaar is van het gebruikte domein en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="c357d-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="c357d-133">Selecteer in het scherm **Microsoft Azure instellen** **Volgende** om te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="c357d-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="c357d-134">Als u op dit scherm een foutmelding krijgt, gaat u terug naar de sectie [Dynamics Deployment Services toegang geven tot uw Azure-abonnement](#provide) in dit onderwerp en voltooi alle stappen.</span><span class="sxs-lookup"><span data-stu-id="c357d-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="c357d-135">Download het Azure Management Certificate naar een lokale map op uw computer en upload het vervolgens naar Azure Management Portal via **Instellingen** > **Beheercertificaten**.</span><span class="sxs-lookup"><span data-stu-id="c357d-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="c357d-136">Met dit certificaat kan LCS namens u communiceren met Azure.</span><span class="sxs-lookup"><span data-stu-id="c357d-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="c357d-137">U kunt deze stap overslaan als uw gebruiker toegang heeft tot het abonnement.</span><span class="sxs-lookup"><span data-stu-id="c357d-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="c357d-138">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="c357d-138">Select  **Next**.</span></span>
8. <span data-ttu-id="c357d-139">Selecteer de Azure-regio waarin u wilt implementeren en selecteer een datacenter bij de locatie waar u dit systeem wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c357d-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="c357d-140">Selecteer **Verbinding maken**.</span><span class="sxs-lookup"><span data-stu-id="c357d-140">Select  **Connect**.</span></span>

<span data-ttu-id="c357d-141">U hebt uw Azure-abonnement met succes verbonden.</span><span class="sxs-lookup"><span data-stu-id="c357d-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="c357d-142">U kunt nu gehoste Dynamics 365 Finance-cloudomgevingen implementeren.</span><span class="sxs-lookup"><span data-stu-id="c357d-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


