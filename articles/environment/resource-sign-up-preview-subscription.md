---
title: Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen
description: Dit onderwerp bevat informatie over het abonneren op en inrichten van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276837"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="8fcd4-103">Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="8fcd4-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="8fcd4-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="8fcd4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8fcd4-105">Dit onderwerp geeft aan hoe u zich abonneert op de preview-/partneraanbieding en hoe u de Project Operations-omgeving implementeert voor scenario's op basis van resources/niet-voorradige artikelen.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8fcd4-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="8fcd4-106">Prerequisites</span></span>

- <span data-ttu-id="8fcd4-107">U ontvangt een e-mail waarin u wordt uitgenodigd om deel te nemen aan de preview.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="8fcd4-108">U kunt een preview aanvragen op de [website van Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="8fcd4-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="8fcd4-109">De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="8fcd4-110">Voor het implementeren van een Finance-omgeving is een geldig Azure-abonnement vereist dat per omgeving wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="8fcd4-111">U kunt het bestaande abonnement van uw organisatie gebruiken of een [Azure-proefversie](https://azure.microsoft.com/en-us/free/) starten.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="8fcd4-112">De CDS-omgeving wordt gedurende een beperkte periode van 30 dagen gratis ter beschikking gesteld.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="8fcd4-113">Abonneren</span><span class="sxs-lookup"><span data-stu-id="8fcd4-113">Subscribe</span></span>

<span data-ttu-id="8fcd4-114">Wanneer uw [preview-aanvraag](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) wordt goedgekeurd, ontvangt u drie aanbiedingen van Microsoft per e-mail.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="8fcd4-115">Met deze aanbiedingen kunt u de preview van Project Operations implementeren:</span><span class="sxs-lookup"><span data-stu-id="8fcd4-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="8fcd4-116">Dynamics 365 Project Operations (CRM) - proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="8fcd4-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="8fcd4-117">Office 365 Project Operations - proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="8fcd4-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="8fcd4-118">Dynamics 365 Finance - proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="8fcd4-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fcd4-119">Slechts één persoon, de tenantbeheerder, in een organisatie mag deze taak uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="8fcd4-120">Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="8fcd4-121">Dynamics 365 Project Operations (CRM) - proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="8fcd4-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="8fcd4-122">Voordat u begint, moet u ervoor zorgen dat u bent aangemeld bij een browser met de werkaccount van de gebruiker in de gewenste tenant voor de preview van Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="8fcd4-123">Wissel de eerste aanbiedingscode **Dynamics 365 Project Operations (CRM) - proefversie voor preview** in door de in de browser-URL te plakken.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Aanbieding inwisselen](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="8fcd4-125">Bevestig uw order.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-125">Confirm your order.</span></span>

![De order bevestigen](./media/17ConfirmOrderNew.png)

<span data-ttu-id="8fcd4-127">U ziet dat de aanbieding voor bevestiging met succes is ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-127">You will see confirmation offer was successfully redeemed.</span></span>

![Bevestiging](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="8fcd4-129">Office 365 Project Operations - proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="8fcd4-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="8fcd4-130">Herhaal dezelfde stappen als bij de eerste aanbiedingscode.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="8fcd4-131">Zorg ervoor dat u de tweede aanbiedingscode toevoegt met dezelfde gebruikersaccount die is gebruikt bij de eerste aanbiedingscode.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="8fcd4-132">Dynamics 365 Finance-proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="8fcd4-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="8fcd4-133">Herhaal dezelfde stappen met de laatste aanbieding uit de welkomstmail.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="8fcd4-134">Licenties toewijzen</span><span class="sxs-lookup"><span data-stu-id="8fcd4-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fcd4-135">U hebt toegang als beheerder nodig tot de Microsoft 365-portal van uw organisatie om de volgende stappen te voltooien.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="8fcd4-136">Ga naar [Microsoft 365-beheercentrum](https://portal.office.com/) om de licenties aan uw gebruikers toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Startpagina van het Beheercentrum](./media/14AdminPortal.png)

2. <span data-ttu-id="8fcd4-138">Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licenties toewijzen](./media/15AssignLicenses.png)

3. <span data-ttu-id="8fcd4-140">Controleer of de licentie voor **Dynamics 365 Project Operations (CRM) Preview** en **Office 365 Project Operations - Preview** is geselecteerd en selecteer **Wijzigingen opslaan**.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="8fcd4-141">De Finance-proefaanbieding hoeft niet aan een gebruiker te worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="8fcd4-142">Een nieuw project in LCS starten</span><span class="sxs-lookup"><span data-stu-id="8fcd4-142">Start a new project in LCS</span></span>

<span data-ttu-id="8fcd4-143">Maak een nieuw LCS-project zoals beschreven in het onderwerp [Een nieuw project starten in LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="8fcd4-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="8fcd4-144">Een Azure-abonnement toevoegen aan een LCS-project</span><span class="sxs-lookup"><span data-stu-id="8fcd4-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="8fcd4-145">Om deze taak te voltooien volgt u de stappen in het onderwerp [Een Azure-abonnement toevoegen aan het LCS-project](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="8fcd4-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="8fcd4-146">Implementeer een Finance-demo-omgeving met Project Operations voor scenario's met resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="8fcd4-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="8fcd4-147">Volg de richtlijnen in het onderwerp [Een nieuwe omgeving inrichten](resource-provision-new-environment.md) om de implementatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="8fcd4-148">Gebruik het implementatietype [demo-omgeving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) voor preview.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="8fcd4-149">Gegevens voor CDS-installatie en configuratie installeren</span><span class="sxs-lookup"><span data-stu-id="8fcd4-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="8fcd4-150">Installeer CDS-installatie- en configuratiegegevens zoals beschreven in het onderwerp [Configuratiegegevens instellen en toepassen in Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="8fcd4-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="8fcd4-151">Voltooi deze stap pas nadat de demo-omgeving van Finance is geïmplementeerd en de demogegevens in FO gereed zijn.</span><span class="sxs-lookup"><span data-stu-id="8fcd4-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]