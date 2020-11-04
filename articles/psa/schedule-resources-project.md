---
title: Resources inplannen voor een project
description: Informatie over resources plannen voor een project in Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074770"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="06799-103">Resources plannen voor een project (Project Service)</span><span class="sxs-lookup"><span data-stu-id="06799-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="06799-104">U kunt de beschikbaarheid van de resource weergeven om een algemeen overzicht te krijgen van hoe uw resources worden geboekt, of u kunt de weergave met vaardigheden, team, de locatie, en andere opties filteren.</span><span class="sxs-lookup"><span data-stu-id="06799-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="06799-105">Het planbord geeft de lijst met resources en hun beschikbaarheid weer.</span><span class="sxs-lookup"><span data-stu-id="06799-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="06799-106">Selecteer een weergavemodus om beschikbaarheid weer te geven op **Uren** , **Dag** , **Week** of **Maand**.</span><span class="sxs-lookup"><span data-stu-id="06799-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="06799-107">Voordat u het planbord gebruikt, moet u dit configureren.</span><span class="sxs-lookup"><span data-stu-id="06799-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="06799-108">Zie [Configureer het planningsbord (Field Service, Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="06799-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="06799-109">Als u een oudere versie gebruikt, raadpleegt u voor resourcebeschikbaarheid [De beschikbaarheid van resources weergeven](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="06799-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="06799-110">Als u de boekingsfunctionaliteit, geo-coding en locatieservices van het planbord wilt gebruiken, moet u de kaarten inschakelen.</span><span class="sxs-lookup"><span data-stu-id="06799-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="06799-111">Selecteer in het hoofdmenu **Resourceplanning** > **Beheer**.</span><span class="sxs-lookup"><span data-stu-id="06799-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="06799-112">Klik op **Planningsparameters**.</span><span class="sxs-lookup"><span data-stu-id="06799-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="06799-113">Open de record en schuif omlaag naar de sectie **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="06799-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="06799-114">Kies in het veld **Verbinden met Kaarten** de waarde **Ja**.</span><span class="sxs-lookup"><span data-stu-id="06799-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="06799-115">Accepteer de voorwaarden en sla de record op.</span><span class="sxs-lookup"><span data-stu-id="06799-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="06799-116">Selecteer in het hoofdmenu **Project Service** > **Planbord**.</span><span class="sxs-lookup"><span data-stu-id="06799-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="06799-117">Vanaf dit punt zijn er verschillende manieren om een boekingsvereiste handmatig te plannen.</span><span class="sxs-lookup"><span data-stu-id="06799-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="06799-118">Kies de methode die voor u het beste is.</span><span class="sxs-lookup"><span data-stu-id="06799-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="06799-119">Beschikbare resources zoeken</span><span class="sxs-lookup"><span data-stu-id="06799-119">Find available resources</span></span>

1.  <span data-ttu-id="06799-120">Klik in de lijst **Boekingsvereisten** met de rechtermuisknop op een ongeplande boeking en kies een van de volgende:</span><span class="sxs-lookup"><span data-stu-id="06799-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="06799-121">Kies **Beschikbaarheid zoeken - Huidige resources** om beschikbare resources te zoeken in de lijst met resources in het planbord.</span><span class="sxs-lookup"><span data-stu-id="06799-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="06799-122">Kies **Beschikbaarheid zoeken - Alle resources** om beschikbare resources te zoeken onder de resources in het systeem.</span><span class="sxs-lookup"><span data-stu-id="06799-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="06799-123">Wanneer u dit doet, tonen de filters de opties voor de geselecteerde boekingsvereisten.</span><span class="sxs-lookup"><span data-stu-id="06799-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="06799-124">Als u een beschikbaar tijdvak ziet, klikt u met de rechtermuisknop op het tijdvak in het planbord en kiest u **Hier boeken**.</span><span class="sxs-lookup"><span data-stu-id="06799-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="06799-125">U kunt ook de boekingsvereiste verslepen en in het beschikbare tijdvak neerzetten.</span><span class="sxs-lookup"><span data-stu-id="06799-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="06799-126">Een resource boeken met de dagweergave en nog niet-volgeboekte personen vinden</span><span class="sxs-lookup"><span data-stu-id="06799-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="06799-127">Selecteer **Weergavemodus** in het planbord en selecteer **Dagen**.</span><span class="sxs-lookup"><span data-stu-id="06799-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="06799-128">Dit opent een rasterweergave waarin is weergegeven hoeveel uur per dag een resource is geboekt en op welke dagen ze beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="06799-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="06799-129">Klik op de naam van de resource die u wilt boeken en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="06799-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="06799-130">Klik in het dialoogvenster **Resourceboekingen (maken)** , kies het project waarvoor u de resource wilt boeken samen met de boekingsmethode en de start- en eindtijden.</span><span class="sxs-lookup"><span data-stu-id="06799-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="06799-131">Selecteer **Boeken** als u klaar bent.</span><span class="sxs-lookup"><span data-stu-id="06799-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="06799-132">Weergeven op het planbord</span><span class="sxs-lookup"><span data-stu-id="06799-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="06799-133">Selecteer een niet-geplande boekingsvereiste in de lijst onderaan de pagina.</span><span class="sxs-lookup"><span data-stu-id="06799-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="06799-134">Sleep de boekingsvereiste naar een beschikbare resource/tijdvak op het planbord.</span><span class="sxs-lookup"><span data-stu-id="06799-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="06799-135">Selecteer **Boeken** als u klaar bent.</span><span class="sxs-lookup"><span data-stu-id="06799-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="06799-136">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="06799-136">Additional resources</span></span>  
 [<span data-ttu-id="06799-137">Resourcemanager-handleiding</span><span class="sxs-lookup"><span data-stu-id="06799-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
