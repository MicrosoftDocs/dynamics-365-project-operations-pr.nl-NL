---
title: Prijslijsten deactiveren
description: In dit onderwerp wordt uitgelegd hoe u ongebruikte of oude prijslijsten kunt deactiveren of verwijderen.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001330"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="66fa2-103">Prijslijsten deactiveren</span><span class="sxs-lookup"><span data-stu-id="66fa2-103">Deactivate price lists</span></span> 

<span data-ttu-id="66fa2-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="66fa2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="66fa2-105">Als u oude of ongebruikte prijslijsten wilt verwijderen uit Dynamics 365 Project Operations, zijn er twee stappen die u moet doorlopen.</span><span class="sxs-lookup"><span data-stu-id="66fa2-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="66fa2-106">Verwijder of wis de prijslijst van specifieke pagina's.</span><span class="sxs-lookup"><span data-stu-id="66fa2-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="66fa2-107">Deactiveer of verwijder de prijslijst uit de actieve prijslijsten op de pagina **Prijslijsten**.</span><span class="sxs-lookup"><span data-stu-id="66fa2-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="66fa2-108">U moet beide stappen voltooien om een prijslijst volledig te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="66fa2-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="66fa2-109">Het volstaat niet om alleen stap 2, het direct verwijderen of deactiveren van de prijslijst uit de weergave Actieve prijslijsten, uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="66fa2-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="66fa2-110">U moet ook de koppeling van deze prijslijst verwijderen uit alle plaatsen genoemd in stap 1.</span><span class="sxs-lookup"><span data-stu-id="66fa2-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="66fa2-111">De prijslijst van specifieke pagina's verwijderen</span><span class="sxs-lookup"><span data-stu-id="66fa2-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="66fa2-112">Als u een prijslijst uit Project Operations wilt verwijderen, gaat u naar de volgende pagina's:</span><span class="sxs-lookup"><span data-stu-id="66fa2-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="66fa2-113">De pagina **Projectparameters** > het tabblad **Prijslijsten**</span><span class="sxs-lookup"><span data-stu-id="66fa2-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="66fa2-114">De pagina **Organisatie-eenheid** > het raster **Prijslijsten**</span><span class="sxs-lookup"><span data-stu-id="66fa2-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="66fa2-115">De pagina **Account** > het raster **Prijslijsten voor project**</span><span class="sxs-lookup"><span data-stu-id="66fa2-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="66fa2-116">De pagina **Projectprijsopgaven** > het raster **Prijslijsten voor project**: dit is van toepassing op alle actieve projectprijsopgaven.</span><span class="sxs-lookup"><span data-stu-id="66fa2-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="66fa2-117">De pagina **Projectcontracten** > het raster **Prijslijsten voor project**: dit is van toepassing op alle actieve contracten.</span><span class="sxs-lookup"><span data-stu-id="66fa2-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="66fa2-118">Voor elke pagina moet u de prijslijst selecteren die u wilt verwijderen en vervolgens **Verwijderen** selecteren.</span><span class="sxs-lookup"><span data-stu-id="66fa2-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="66fa2-119">De prijslijst uit de actieve prijslijsten op de pagina Prijslijsten verwijderen of deactiveren</span><span class="sxs-lookup"><span data-stu-id="66fa2-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="66fa2-120">Als u een prijslijst uit de actieve prijslijsten wilt verwijderen, gaat u naar **Verkoop** > **Klanten** > **Prijslijsten**.</span><span class="sxs-lookup"><span data-stu-id="66fa2-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="66fa2-121">Selecteer de prijslijst die u wilt verwijderen en selecteer vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="66fa2-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="66fa2-122">Als naar de prijslijst wordt verwezen in bestaande transacties, kunt u deze niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="66fa2-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="66fa2-123">Als dit gebeurt, kunt u de prijslijst deactiveren, zodat deze in geen enkele weergave wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="66fa2-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="66fa2-124">Om de prijslijst te deactiveren, selecteert u de prijslijst opnieuw en selecteert u vervolgens **Deactiveren**.</span><span class="sxs-lookup"><span data-stu-id="66fa2-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
