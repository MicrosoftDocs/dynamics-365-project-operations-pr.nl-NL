---
title: Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen
description: Dit onderwerp bevat informatie over het bijwerken van kenmerken van invoegtoepassingen voor prijsdimensies.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147062"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="c3218-103">Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen</span><span class="sxs-lookup"><span data-stu-id="c3218-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="c3218-104">Als u de functies voor prijsopgaven en contracten van de Project Service Automation (PSA) niet gebruikt, kunt u dit onderwerp overslaan.</span><span class="sxs-lookup"><span data-stu-id="c3218-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="c3218-105">Er wordt in dit onderwerp vanuit gegaan dat u de procedures hebt voltooid in de onderwerpen [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md), [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](field-references.md) en [Aangepaste velden instellen als prijsdimensies](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="c3218-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="c3218-106">Als u deze procedures niet hebt voltooid, gaat u terug, voltooit u deze en keert u terug naar dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="c3218-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="c3218-107">Wanneer details voor een prijsopgaveregel zijn gemaakt op de pagina **Prijsopgaveregel** voor een project, maakt het systeem twee schattingsregels op de achtergrond, één regel voor de kostenzijde van de schatting en één voor verkoopzijde.</span><span class="sxs-lookup"><span data-stu-id="c3218-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="c3218-108">Dit is hetzelfde voor projectcontractregels.</span><span class="sxs-lookup"><span data-stu-id="c3218-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="c3218-109">Wanneer u een wijziging aanbrengt in de hoeveelheid of een veld aan de kostenzijde, wordt die wijziging doorgegeven aan de verkoopzijde.</span><span class="sxs-lookup"><span data-stu-id="c3218-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="c3218-110">Dit is mogelijk vanwege de volgende invoegtoepassingen die opnieuw moeten worden geregistreerd na een wijziging in de prijsdimensies.</span><span class="sxs-lookup"><span data-stu-id="c3218-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="c3218-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="c3218-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="c3218-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="c3218-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="c3218-113">In de volgende stappen wordt het proces van het registreren van de invoegtoepassingen uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="c3218-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="c3218-114">Open **PluginRegistrationTool** en maak verbinding met uw online-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="c3218-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="c3218-115">Klik op **Zoeken** en zoek de invoegtoepassing om bij te werken.</span><span class="sxs-lookup"><span data-stu-id="c3218-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Schermopname van de zoekstructuur](media/PRT-1.png)

3. <span data-ttu-id="c3218-117">Nadat de invoegtoepassing is gevonden, selecteert u deze en klikt u op **Selecteren op hoofdformulier**.</span><span class="sxs-lookup"><span data-stu-id="c3218-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="c3218-118">Selecteer de stap van de invoegtoepassing, klik met de rechtermuisknop en selecteer **Bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="c3218-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Schermopname van de invoegtoepassing dit moet worden bijgewerkt](media/PRT-2.png)
 
5. <span data-ttu-id="c3218-120">Klik in het venster Bijwerken op het beletselteken (**...**) in de filterkenmerken.</span><span class="sxs-lookup"><span data-stu-id="c3218-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Schermopname van de configuratiegegevens voor Bestaande stap bijwerken](media/PRT-3.png)
 
6. <span data-ttu-id="c3218-122">Selecteer de selectievakjes met prijskenmerken.</span><span class="sxs-lookup"><span data-stu-id="c3218-122">Select the pricing attribute check boxes.</span></span>

 ![Schermopname met het ingeschakelde selectievakje voor prijskenmerken](media/PRT-4.png)

7. <span data-ttu-id="c3218-124">Klik op **OK** om de pagina te sluiten en selecteer vervolgens **Stap bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="c3218-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Schermopname met de knop "Stap bijwerken"](media/PRT-5.png)
 
8. <span data-ttu-id="c3218-126">Herhaal dit proces voor de tweede invoegtoepassing **PreOperationQuoteLineDetail - update van msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="c3218-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="c3218-127">Sluit het registratiehulpprogramma.</span><span class="sxs-lookup"><span data-stu-id="c3218-127">Close the plug-in registration tool.</span></span>

