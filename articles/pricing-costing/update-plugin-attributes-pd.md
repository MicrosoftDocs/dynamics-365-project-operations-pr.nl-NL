---
title: Kenmerken van invoegtoepassingen bijwerken met nieuwe prijsdimensies
description: Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643212"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="884b5-103">Kenmerken van invoegtoepassingen bijwerken met nieuwe prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="884b5-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="884b5-104">Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="884b5-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="884b5-105">Dit onderwerp is alleen van toepassing op de offerte- en contractfuncties in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="884b5-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="884b5-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="884b5-106">Prerequisites</span></span>
<span data-ttu-id="884b5-107">Voordat u de stappen in dit onderwerp voltooit, moet u de procedures in de volgende onderwerpen hebben voltooid:</span><span class="sxs-lookup"><span data-stu-id="884b5-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="884b5-108">Aangepaste velden en entiteiten maken</span><span class="sxs-lookup"><span data-stu-id="884b5-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="884b5-109">Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten </span><span class="sxs-lookup"><span data-stu-id="884b5-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="884b5-110">[Aangepaste velden instellen als prijsdimensies](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="884b5-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="884b5-111">Als u deze procedures niet hebt voltooid, voltooit u ze en keert u terug naar dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="884b5-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="884b5-112">Een invoegtoepassing registreren</span><span class="sxs-lookup"><span data-stu-id="884b5-112">Register a plug-in</span></span>
<span data-ttu-id="884b5-113">Wanneer een detail van een prijsopgaveregel wordt gemaakt op de pagina **Prijsopgaveregel** voor een projectprijsopgaveregel, creëert het systeem twee schattingsregels.</span><span class="sxs-lookup"><span data-stu-id="884b5-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="884b5-114">De ene regel is voor de kostenzijde van de schatting en de andere regel is voor de verkoopzijde.</span><span class="sxs-lookup"><span data-stu-id="884b5-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="884b5-115">Dit is hetzelfde voor projectcontractregels.</span><span class="sxs-lookup"><span data-stu-id="884b5-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="884b5-116">Wanneer u een wijziging aanbrengt in de hoeveelheid of een veld aan de kostenzijde, wordt die wijziging ook gemaakt aan de verkoopzijde.</span><span class="sxs-lookup"><span data-stu-id="884b5-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="884b5-117">Dit is mogelijk doordat de PreOperation-invoegtoepassingen voor de entiteiten prijsopgaveregeldetail en contractregeldetail specifieke kenmerken aan de kostenzijde koppelen met de verkoopzijde van de transactie.</span><span class="sxs-lookup"><span data-stu-id="884b5-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="884b5-118">Als u wijzigingen in de prijsdimensiewaarden aan de verkoopzijde ook aan de kostenzijde wilt doorvoeren, moeten de volgende invoegtoepassingen opnieuw worden geregistreerd nadat u wijzigingen in een prijsdimensie hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="884b5-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="884b5-119">Deze invoegtoepassingen moeten worden bijgewerkt en opnieuw geregistreerd:</span><span class="sxs-lookup"><span data-stu-id="884b5-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="884b5-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="884b5-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="884b5-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="884b5-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="884b5-122">Voer de volgende stappen uit om de invoegtoepassingen bij te werken en opnieuw te registreren.</span><span class="sxs-lookup"><span data-stu-id="884b5-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="884b5-123">Open **PluginRegistrationTool** en maak verbinding met uw Project Operations Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="884b5-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="884b5-124">Selecteer **Zoeken** en typ de eerste paar letters van de invoegtoepassing die moet worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="884b5-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="884b5-125">Nadat de invoegtoepassing is gevonden, selecteert u deze en selecteer u **Selecteren op hoofdformulier**.</span><span class="sxs-lookup"><span data-stu-id="884b5-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="884b5-126">Selecteer de stap **Update msdyn_orderlinetransaction**, klik met de rechtermuisknop en selecteer **Bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="884b5-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="884b5-127">Selecteer op de pagina **Bijwerken** het beletselteken (**...**) in de filterkenmerken.</span><span class="sxs-lookup"><span data-stu-id="884b5-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="884b5-128">Het venster met filterkenmerken wordt geopend en biedt een lijst met alle kenmerken in de entiteit en de prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="884b5-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="884b5-129">Schakel de selectievakjes in voor de prijsdimensiekenmerken.</span><span class="sxs-lookup"><span data-stu-id="884b5-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="884b5-130">Selecteer **OK** om de pagina te sluiten en selecteer vervolgens **Stap bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="884b5-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="884b5-131">Herhaal stap 2 tot 7 voor de tweede invoegtoepassing, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="884b5-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="884b5-132">Werk voor deze invoegtoepassing de stap **Update msdyn_quotelinetransaction** bij.</span><span class="sxs-lookup"><span data-stu-id="884b5-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="884b5-133">Sluit **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="884b5-133">Close **PluginRegistrationTool**.</span></span>
