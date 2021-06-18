---
title: De integratie van Project Operations per rechtspersoon configureren
description: Dit onderwerp bevat informatie over het instellen van de integratie per rechtspersoon in Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000070"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="d81bc-103">De integratie van Project Operations per rechtspersoon configureren</span><span class="sxs-lookup"><span data-stu-id="d81bc-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="d81bc-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="d81bc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d81bc-105">Dit onderwerp leidt u door de stappen die nodig zijn om Dynamics 365 Project Operations te configureren per rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d81bc-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="d81bc-106">Functietoetsen in Dynamics 365 Finance inschakelen</span><span class="sxs-lookup"><span data-stu-id="d81bc-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="d81bc-107">Voer de volgende stappen uit om de vereiste functies in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="d81bc-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="d81bc-108">Ga in Dynamics 365 Finance naar de werkruimte **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="d81bc-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="d81bc-109">Zoek in **Lijst met functies** naar de volgende functies en schakel ze in:</span><span class="sxs-lookup"><span data-stu-id="d81bc-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="d81bc-110">**Meerdere contractregels inschakelen voor een project**</span><span class="sxs-lookup"><span data-stu-id="d81bc-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="d81bc-111">**Project Operations inschakelen in Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="d81bc-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="d81bc-112">Als **Functietoetsen** niet wordt vermeld, controleert u of uw Finance-versie voldoet aan de minimale versievereiste (toepassingsversie 10.0.13 met alle kwaliteitsupdates toegepast of hoger).</span><span class="sxs-lookup"><span data-stu-id="d81bc-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="d81bc-113">Selecteer **Controleren op updates** om de lijst met functies te vernieuwen.</span><span class="sxs-lookup"><span data-stu-id="d81bc-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="d81bc-114">Het implementatiescenario van Project Operations voor een rechtspersoon definiëren</span><span class="sxs-lookup"><span data-stu-id="d81bc-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="d81bc-115">U kunt Project Operations in Dynamics 365 Customer Engagement inschakelen op het niveau van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="d81bc-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="d81bc-116">U kunt één rechtspersoon hebben die Project Operations gebruikt in Dynamics 365 Customer Engagement voor scenario's op basis van resources/niet-voorradige artikelen.</span><span class="sxs-lookup"><span data-stu-id="d81bc-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="d81bc-117">In dezelfde omgeving kunt u nog een rechtspersoon hebben die Project Operations gebruikt voor scenario's op basis van voorradige artikelen/productieorders.</span><span class="sxs-lookup"><span data-stu-id="d81bc-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="d81bc-118">Ga in Dynamics 365 Finance naar **Projectmanagement en financiële administratie** > **Instellen** > **Algemene parameters voor Projectmanagement en financiële administratie**.</span><span class="sxs-lookup"><span data-stu-id="d81bc-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="d81bc-119">Selecteer in de lijst met beschikbare rechtspersonen de entiteiten waarvoor meerdere contractregels en Project Operations in Dynamics 365 Customer Engagement-functies worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d81bc-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="d81bc-120">Laat rechtspersonen die Project Operations gebruiken voor scenario's op basis van voorradige artikelen/productieorders uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d81bc-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="d81bc-121">Een rechtspersoon kan alleen worden geselecteerd als deze geen bestaande projecten heeft.</span><span class="sxs-lookup"><span data-stu-id="d81bc-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="d81bc-122">Parameters voor Projectbeheer en financiële administratie configureren</span><span class="sxs-lookup"><span data-stu-id="d81bc-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="d81bc-123">Elke rechtspersoon die Project Operations gebruikt in Dynamics 365 Customer Engagement heeft een set standaardparameters nodig.</span><span class="sxs-lookup"><span data-stu-id="d81bc-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="d81bc-124">Deze parameters zijn geconfigureerd op het tabblad **Project Operations** op de pagina **Parameters voor Projectbeheer en financiële administratie** bladzijde.</span><span class="sxs-lookup"><span data-stu-id="d81bc-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="d81bc-125">De parameters zijn:</span><span class="sxs-lookup"><span data-stu-id="d81bc-125">The parameters are:</span></span>

  - <span data-ttu-id="d81bc-126">**Standaardwaarden voor factureringstype**: Project Operations gebruikt een vaste set standaardinstellingen voor factureringstypes die moeten worden toegewezen aan regeleigenschappen in Finance.</span><span class="sxs-lookup"><span data-stu-id="d81bc-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="d81bc-127">Maak een record voor elk factureringstype: **Niet gespecificeerd**, **Toerekenbaar**, **Niet-toerekenbaar**, **Gratis** en **Niet beschikbaar**.</span><span class="sxs-lookup"><span data-stu-id="d81bc-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="d81bc-128">**Standaardinstellingen projectcategorie**: selecteer de standaardprojectcategorieën die voor elk transactietype moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d81bc-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="d81bc-129">Deze standaardinstellingen worden gebruikt in **Integratiejournaal in Project Operations** en in schattingen waar geen transactiecategorie is gespecificeerd voor de werkelijke projectwaarden.</span><span class="sxs-lookup"><span data-stu-id="d81bc-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="d81bc-130">**Prognoses**: selecteer het prognosemodel dat moet worden gebruikt voor schattingen van tijd en onkosten.</span><span class="sxs-lookup"><span data-stu-id="d81bc-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]