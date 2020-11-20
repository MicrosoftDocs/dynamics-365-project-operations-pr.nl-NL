---
title: Een prijslijst maken
description: Informatie over een prijslijst maken in Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 08d93ad86d782922df6b22370749628ddbdc0718
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122022"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="96be5-103">Een prijslijst maken (Project Service)</span><span class="sxs-lookup"><span data-stu-id="96be5-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="96be5-104">De prijslijsten bevatten een sjabloon dat uw accountbeheer kan gebruiken voor het maken van offertes en projecten en voor het vaststellen van de kosten van een project.</span><span class="sxs-lookup"><span data-stu-id="96be5-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="96be5-105">Ze bieden een regelitem-lijst van rollen en kosten en de prijs die u voor elk zult vragen.</span><span class="sxs-lookup"><span data-stu-id="96be5-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="96be5-106">U kunt meerdere prijslijsten maken zodat u afzonderlijke prijsstructuren kunt hanteren voor voor regio's waarin u uw producten verkoopt of voor verschillende verkoopkanalen.</span><span class="sxs-lookup"><span data-stu-id="96be5-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="96be5-107">Het is een goed idee om ten minste één prijslijst in te stellen voor elke valuta die u van plan bent uw klanten in te dienen.</span><span class="sxs-lookup"><span data-stu-id="96be5-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="96be5-108">Als u financiële ramingen voor het te leveren werk wilt maken, zorgt u ervoor dat elk project een steunende kosten en verkoopprijslijst heeft.</span><span class="sxs-lookup"><span data-stu-id="96be5-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="96be5-109">Stel een standaardprijslijst voor kosten en verkopen in, die van toepassing is op alle projecten gemaakt in uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="96be5-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="96be5-110">Prijslijsten hangen af van rollen en onkostencategorieën, dus voordat u een prijslijst maakt moet u de rollen en de onkostencategorieën hebben geconfigureerd die u wilt gebruiken bij het maken van de prijslijst.</span><span class="sxs-lookup"><span data-stu-id="96be5-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="96be5-111">Ga naar **Project Service > Prijslijsten**.</span><span class="sxs-lookup"><span data-stu-id="96be5-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="96be5-112">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="96be5-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="96be5-113">In **Context** selecteer of deze prijslijst voor **Kosten**, **Kopen** of **Verkoop** is.</span><span class="sxs-lookup"><span data-stu-id="96be5-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="96be5-114">In het vak **Naam**, typ een naam voor de prijslijst.</span><span class="sxs-lookup"><span data-stu-id="96be5-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="96be5-115">In **Valuta** selecteert u de valuta voor facturering of kosten die u gaat gebruiken.</span><span class="sxs-lookup"><span data-stu-id="96be5-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="96be5-116">In **Tijdseenheid**, geeft u de tijd op waarvoor de prijs van toepassing is, zoals dag of uur.</span><span class="sxs-lookup"><span data-stu-id="96be5-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="96be5-117">Vul de gewenste waarden in voor **Begindatum**, **Einddatum** en **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="96be5-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="96be5-118">Klik op **Opslaan** om de record te maken zodat u deze verder kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="96be5-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="96be5-119">Om een rolprijs aan de prijslijst toe te voegen, klikt u op **+** onder **Rolprijzen**.</span><span class="sxs-lookup"><span data-stu-id="96be5-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="96be5-120">In het deelvenster **Rolprijs**, geef de details in en klik vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="96be5-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96be5-121">Blijf zo nodig rolprijzen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="96be5-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="96be5-122">Klik wanneer u klaar bent op de knop **Opslaan** rechtsonder in het scherm.</span><span class="sxs-lookup"><span data-stu-id="96be5-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="96be5-123">Om een onkostencategorie aan de prijslijst toe te voegen, klikt u op **+** onder **Categorieprijzen**.</span><span class="sxs-lookup"><span data-stu-id="96be5-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="96be5-124">In het deelvenster **Transactiecategorieprijs**, geef de details in en klik vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="96be5-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96be5-125">Blijf zo nodig categorieprijzen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="96be5-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="96be5-126">Klik wanneer u klaar bent op de knop **Opslaan** rechtsonder in het scherm.</span><span class="sxs-lookup"><span data-stu-id="96be5-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="96be5-127">Om prijslijstitems aan de prijslijst toe te voegen, klik op **+** onder **Prijslijstitems**.</span><span class="sxs-lookup"><span data-stu-id="96be5-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="96be5-128">In het deelvenster **Prijslijstitem**, geef de details in en klik vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="96be5-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96be5-129">Blijf zo nodig prijslijstitems toevoegen.</span><span class="sxs-lookup"><span data-stu-id="96be5-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="96be5-130">Klik wanneer u klaar bent op de knop **Opslaan** rechtsonder in het scherm.</span><span class="sxs-lookup"><span data-stu-id="96be5-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="96be5-131">Om de relaties van het rayon aan de prijslijst toe te voegen, klik op **+** onder **Relaties van het rayon**.</span><span class="sxs-lookup"><span data-stu-id="96be5-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="96be5-132">In het venster **Nieuwe connectie**, geef de details in en klik vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="96be5-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="96be5-133">Blijf zo nodig relaties van het rayon toevoegen.</span><span class="sxs-lookup"><span data-stu-id="96be5-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="96be5-134">Klik wanneer u klaar bent op de knop **Opslaan** rechtsonder in het scherm.</span><span class="sxs-lookup"><span data-stu-id="96be5-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="96be5-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="96be5-135">See Also</span></span>  
 [<span data-ttu-id="96be5-136">Project Service Automation configureren</span><span class="sxs-lookup"><span data-stu-id="96be5-136">Configure Project Service Automation</span></span>](../psa/configure.md)
