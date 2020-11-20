---
title: Dagvergoedingen
description: Dit onderwerp geeft informatie over de dagvergoedingsregels die worden gebruikt in Onkostenbeheer.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128502"
---
# <a name="per-diems"></a><span data-ttu-id="9cbfa-103">Dagvergoedingen</span><span class="sxs-lookup"><span data-stu-id="9cbfa-103">Per diems</span></span>

<span data-ttu-id="9cbfa-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="9cbfa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="9cbfa-105">Een dagvergoeding is een toelage die wordt betaald aan een werknemer die voor zijn werk reist.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="9cbfa-106">In Onkostenbeheer kunt u dagvergoedingsregels maken voor verschillende reissituaties.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="9cbfa-107">Dagtarieven kunnen worden gebaseerd op de tijd van het jaar, de reislocatie of beide.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="9cbfa-108">Wanneer u een dagvergoeding maakt, kunt u specificeren dat een percentage van de dagvergoeding wordt ingehouden als een werknemer gratis maaltijden of diensten ontvangt.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="9cbfa-109">U kunt ook een minimum en maximum aantal uren instellen dat het dagtarief van toepassing kan zijn op de reis van een werknemer.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="9cbfa-110">Configuratie</span><span class="sxs-lookup"><span data-stu-id="9cbfa-110">Configuration</span></span> 

1. <span data-ttu-id="9cbfa-111">Als u locaties voor dagvergoedingen wilt toevoegen gaat u naar **Instellen** > **Berekeningen en codes** > **Locaties voor dagvergoedingen**.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="9cbfa-112">Selecteer voor elk van de hierboven toegevoegde locaties een dagtarief en valuta die geldig zijn tussen een specifieke begin- en einddatum voor hotel, maaltijden en andere onkosten.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="9cbfa-113">Dagvergoedingen en valuta's worden geconfigureerd onder **Instellen** > **Berekeningen en codes** > **Dagvergoedingen**.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="9cbfa-114">Configureer op de pagina **Locaties voor dagvergoedingen** de tariefniveaus.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="9cbfa-115">Definieer met tariefniveaus de procentuele verdeling van een dagvergoeding voor hotel-, maaltijd- en andere uitgaven.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="9cbfa-116">Om de vergoeding voor ontbijt, lunch of diner op te geven, werkt u de velden op de pagina **Parameters voor onkostenbeheer** bij op het tabblad **Dagvergoeding**.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="9cbfa-117">Onkosten voor dagvergoedingen indienen</span><span class="sxs-lookup"><span data-stu-id="9cbfa-117">Submit expenses using per diem</span></span>
<span data-ttu-id="9cbfa-118">Als u onkosten wilt indienen met dagvergoedingen, gebruikt u de onkostencategorie **Dagvergoeding** wanneer u een onkostendeclaratie maakt.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="9cbfa-119">Voer **Dagvergoeding vanaf datum**, **Dagvergoeding tot datum** en **Locatie voor dagvergoeding** in.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="9cbfa-120">Het bedrag wordt berekend op basis van de dagtarieven voor de geselecteerde locatie en de maaltijdvergoeding wordt berekend op basis van de tariefniveaus voor dagvergoeding.</span><span class="sxs-lookup"><span data-stu-id="9cbfa-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
