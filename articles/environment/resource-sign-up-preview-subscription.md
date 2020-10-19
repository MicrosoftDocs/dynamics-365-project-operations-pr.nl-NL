---
title: Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen
description: Dit onderwerp bevat informatie over het abonneren op en inrichten van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948822"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="df15c-103">Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="df15c-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="df15c-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="df15c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="df15c-105">Dit onderwerp geeft aan hoe u zich abonneert op de preview-/partneraanbieding en hoe u de Project Operations-omgeving implementeert voor scenario's op basis van resources/niet-voorradige artikelen.</span><span class="sxs-lookup"><span data-stu-id="df15c-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df15c-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="df15c-106">Prerequisites</span></span>

- <span data-ttu-id="df15c-107">U ontvangt een e-mail waarin u wordt uitgenodigd om deel te nemen aan de preview.</span><span class="sxs-lookup"><span data-stu-id="df15c-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="df15c-108">U kunt een preview aanvragen op de [website van Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="df15c-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="df15c-109">De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant.</span><span class="sxs-lookup"><span data-stu-id="df15c-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="df15c-110">Voor het implementeren van een Finance-omgeving is een geldig Azure-abonnement vereist dat per omgeving wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="df15c-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="df15c-111">U kunt het bestaande abonnement van uw organisatie gebruiken of een [Azure-proefversie](https://azure.microsoft.com/en-us/free/) starten.</span><span class="sxs-lookup"><span data-stu-id="df15c-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="df15c-112">De CDS-omgeving wordt gedurende een beperkte periode van 30 dagen gratis ter beschikking gesteld.</span><span class="sxs-lookup"><span data-stu-id="df15c-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="df15c-113">Abonneren</span><span class="sxs-lookup"><span data-stu-id="df15c-113">Subscribe</span></span>

<span data-ttu-id="df15c-114">Wanneer uw [preview-aanvraag](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) wordt goedgekeurd, ontvangt u twee aanbiedingen van Microsoft per e-mail.</span><span class="sxs-lookup"><span data-stu-id="df15c-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="df15c-115">Met deze aanbiedingen kunt u de preview van Project Operations implementeren:</span><span class="sxs-lookup"><span data-stu-id="df15c-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="df15c-116">Dynamics 365 Project Operations, proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="df15c-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="df15c-117">Dynamics 365 for Finance and Operations-proefversie voor preview.</span><span class="sxs-lookup"><span data-stu-id="df15c-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df15c-118">Slechts één persoon, de tenantbeheerder, in een organisatie mag deze taak uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="df15c-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="df15c-119">Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="df15c-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="df15c-120">Dynamics 365 Project Operations, proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="df15c-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="df15c-121">Wissel de eerste aanbieding voor de **proefversie van Dynamics 365 Project Operations** in via de URL in uw welkomste-mail.</span><span class="sxs-lookup"><span data-stu-id="df15c-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Eerste aanbieding](./media/1FirstOffer.png)

2. <span data-ttu-id="df15c-123">Controleer of u bent aangemeld als de gebruiker die tot de organisatie behoort die zich op de service zal abonneren.</span><span class="sxs-lookup"><span data-stu-id="df15c-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="df15c-124">Ga verder met het inwisselen van de aanbieding.</span><span class="sxs-lookup"><span data-stu-id="df15c-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="df15c-125">Selecteer **Ja, voeg het toe aan mijn account**.</span><span class="sxs-lookup"><span data-stu-id="df15c-125">Select **Yes, add it to my account**.</span></span>

![Aanbieding inwisselen](./media/2RedeemFirstOffer.png)

![Aanbieding bevestigen](./media/3ConfirmFirstOffer.png)

![Aanbieding ingewisseld](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="df15c-129">Dynamics 365 Finance-proefversie voor preview</span><span class="sxs-lookup"><span data-stu-id="df15c-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="df15c-130">Herhaal dezelfde stappen met de tweede aanbieding uit de welkomstmail.</span><span class="sxs-lookup"><span data-stu-id="df15c-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="df15c-131">Licenties toewijzen</span><span class="sxs-lookup"><span data-stu-id="df15c-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df15c-132">U hebt toegang als beheerder nodig tot de Office 365-portal van uw organisatie om de volgende stappen te voltooien.</span><span class="sxs-lookup"><span data-stu-id="df15c-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="df15c-133">Ga naar [Microsoft 365-beheercentrum](https://portal.office.com/) om licenties aan uw gebruikers toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="df15c-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office-beheerportal](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="df15c-135">Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="df15c-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licenties toewijzen](./media/6AssignLicenses.png)

3. <span data-ttu-id="df15c-137">Controleer of de Project Operations-licentie is geselecteerd en selecteer **Wijzigingen opslaan**.</span><span class="sxs-lookup"><span data-stu-id="df15c-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="df15c-138">De Finance-proefaanbieding hoeft niet aan een gebruiker te worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="df15c-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="df15c-139">Een nieuw project in LCS starten</span><span class="sxs-lookup"><span data-stu-id="df15c-139">Start a new project in LCS</span></span>

<span data-ttu-id="df15c-140">Maak een nieuw LCS-project zoals beschreven in het onderwerp [Een nieuw project starten in LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="df15c-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="df15c-141">Een Azure-abonnement toevoegen aan een LCS-project</span><span class="sxs-lookup"><span data-stu-id="df15c-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="df15c-142">Om deze taak te voltooien volgt u de stappen in het onderwerp [Een Azure-abonnement toevoegen aan het LCS-project](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="df15c-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="df15c-143">Implementeer een Finance-demo-omgeving met Project Operations voor scenario's met resources/niet-voorradige artikelen</span><span class="sxs-lookup"><span data-stu-id="df15c-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="df15c-144">Volg de richtlijnen in het onderwerp [Een nieuwe omgeving inrichten](resource-provision-new-environment.md) om de implementatie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="df15c-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="df15c-145">Gebruik het implementatietype [demo-omgeving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) voor preview.</span><span class="sxs-lookup"><span data-stu-id="df15c-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="df15c-146">Gegevens voor CDS-installatie en configuratie installeren</span><span class="sxs-lookup"><span data-stu-id="df15c-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="df15c-147">Installeer CDS-installatie- en configuratiegegevens zoals beschreven in het onderwerp [Configuratiegegevens instellen en toepassen in Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="df15c-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

