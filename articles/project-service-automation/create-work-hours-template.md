---
title: Een nieuwe werkurensjabloon maken
description: Informatie over een werkurensjabloon maken in Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750782"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="20272-103">Een werkurensjabloon maken (Project Service)</span><span class="sxs-lookup"><span data-stu-id="20272-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="20272-104">Voordat u projectplannings kunt maken, moet u aan setup een projectkalender nodig nodig waarmee het aantal werkuren bepalen per dag in de planning en de onderneming te matchen.</span><span class="sxs-lookup"><span data-stu-id="20272-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="20272-105">Dit doet u met een sjabloon met de werkuren, gegevens over werkuren per dag, vrije dagen, korting en andere momenten bevat.</span><span class="sxs-lookup"><span data-stu-id="20272-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="20272-106">Wanneer u een gebruiker maken, koppelt u een prijsbeleid werksjabloon aan de projectkalender als u de planning voor het project te passen.</span><span class="sxs-lookup"><span data-stu-id="20272-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="20272-107">Er zijn twee manieren waarop u een sjabloon met de werkuren kunt maken:</span><span class="sxs-lookup"><span data-stu-id="20272-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="20272-108">U kunt een werkurensjabloon maken op basis van de agenda van een resource.</span><span class="sxs-lookup"><span data-stu-id="20272-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="20272-109">U kunt een nieuwe werkurensjabloon maken.</span><span class="sxs-lookup"><span data-stu-id="20272-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="20272-110">U kunt een sjabloon maken van werkuren in de kalender van een bron wordt gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="20272-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="20272-111">Ga naar **Project Service > Resources**.</span><span class="sxs-lookup"><span data-stu-id="20272-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="20272-112">Selecteer de resource waarop u de werkuren wilt baseren.</span><span class="sxs-lookup"><span data-stu-id="20272-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="20272-113">Klik op **Agenda opslaan als**, typ een naam voor de werkurensjabloon en klik vervolgens op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="20272-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="20272-114">Wanneer u klaar bent, klikt u op **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="20272-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="20272-115">Klik op de knop **Opslaan** rechtsonder in het scherm.</span><span class="sxs-lookup"><span data-stu-id="20272-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="20272-116">Maak een nieuwe sjabloon van werkuren.</span><span class="sxs-lookup"><span data-stu-id="20272-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="20272-117">Ga naar **Project Service > Werkurensjablonen**.</span><span class="sxs-lookup"><span data-stu-id="20272-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="20272-118">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="20272-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="20272-119">Typ een beschrijvende naam voor de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="20272-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="20272-120">Selecteer een resource hebt geselecteerd als basis- de werkuren, en klik vervolgens op **Opslaan**</span><span class="sxs-lookup"><span data-stu-id="20272-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="20272-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="20272-121">See Also</span></span>  
 [<span data-ttu-id="20272-122">Resources configureren</span><span class="sxs-lookup"><span data-stu-id="20272-122">Set up resources</span></span>](../project-service/set-up-resources.md)
