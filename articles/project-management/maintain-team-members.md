---
title: Teamleden onderhouden
description: Dit onderwerp bevat informatie over het boeken van benoemde resources aan projectteams en het toewijzen hiervan aan taken.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961845"
---
# <a name="maintain-team-members"></a><span data-ttu-id="af40b-103">Teamleden onderhouden</span><span class="sxs-lookup"><span data-stu-id="af40b-103">Maintain team members</span></span>

<span data-ttu-id="af40b-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="af40b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af40b-105">U kunt een benoemde resource toevoegen aan uw projectteam door ze rechtstreeks voor het team te boeken.</span><span class="sxs-lookup"><span data-stu-id="af40b-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="af40b-106">Ga in Dynamics 365 Project Operations naar **Projecten** en open het project waarvoor u boekt.</span><span class="sxs-lookup"><span data-stu-id="af40b-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="af40b-107">Selecteer op de pagina **Project** op het tabblad **Team** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="af40b-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="af40b-108">Selecteer de boekbare resource in het dialoogvenster **Snelle invoer: Projectteamlid**.</span><span class="sxs-lookup"><span data-stu-id="af40b-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="af40b-109">Het veld **Rol** wordt gevuld met de standaardrol van de resource, indien toegewezen.</span><span class="sxs-lookup"><span data-stu-id="af40b-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="af40b-110">U kunt de rol wijzigen.</span><span class="sxs-lookup"><span data-stu-id="af40b-110">You can change the role.</span></span> 
4. <span data-ttu-id="af40b-111">Selecteer de begin- en einddatums voor de periode waarvoor de resource nodig is en selecteer de toewijzingsmethode van de capaciteit van de resource.</span><span class="sxs-lookup"><span data-stu-id="af40b-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="af40b-112">Als u wilt dat het teamlid een projectfiatteur is, selecteert u **Ja** in het veld **Projectfiatteur**.</span><span class="sxs-lookup"><span data-stu-id="af40b-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="af40b-113">Het teamlid kan ingediende tijd- en onkostenposten voor dit project goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="af40b-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="af40b-114">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="af40b-114">Select **Save**.</span></span>

<span data-ttu-id="af40b-115">U kunt de geboekte resource nu toewijzen aan taken in het project.</span><span class="sxs-lookup"><span data-stu-id="af40b-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="af40b-116">Klik op de pagina **Project** op het tabblad **Planning** en wijs taken aan de nieuwe resource toe.</span><span class="sxs-lookup"><span data-stu-id="af40b-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="af40b-117">De resourcekiezer die wordt gestart vanuit het veld **Resources** in het taakraster bevat de teamleden die u kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="af40b-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="af40b-118">In Project Operations zijn resourceboekingen en taaktoewijzingen niet nauw met elkaar verbonden.</span><span class="sxs-lookup"><span data-stu-id="af40b-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="af40b-119">U kunt taken aan teamleden toewijzen voor meer uren dan hun boekingen dekken in het project wanneer u de resourcekiezer in de planning gebruikt.</span><span class="sxs-lookup"><span data-stu-id="af40b-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="af40b-120">De verschillen tussen boekingen en opdrachten van teamleden worden weergegeven op de tabbladen **Team** en **Afstemming van resources**.</span><span class="sxs-lookup"><span data-stu-id="af40b-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="af40b-121">U kunt de verschillen tussen boekingen en toewijzingen voor resources ook op een meer gedetailleerd niveau afstemmen.</span><span class="sxs-lookup"><span data-stu-id="af40b-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="af40b-122">Gebruik de resourcekiezer op het tabblad **Planning** om boekbare resources te zoeken en te selecteren die nog geen deel uitmaken van het projectteam.</span><span class="sxs-lookup"><span data-stu-id="af40b-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="af40b-123">Deze resources worden weergegeven in de resourcekiezer als **Andere resources**.</span><span class="sxs-lookup"><span data-stu-id="af40b-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="af40b-124">Wanneer u een selectie maakt, wordt de resource toegevoegd aan het projectteam en toegewezen aan de taak, maar er worden geen boekingen gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="af40b-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="af40b-125">U kunt de functie voor uitgebreid boeken van het tabblad **Afstemming** of het **planbord** gebruiken om de capaciteit van de resource voor het project te boeken.</span><span class="sxs-lookup"><span data-stu-id="af40b-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="af40b-126">Nadat een teamlid is geboekt voor uw project, kunt u **Boekingen bijhouden** of het **Planbord** rechtstreeks gebruiken om hun boekingen te beheren.</span><span class="sxs-lookup"><span data-stu-id="af40b-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
