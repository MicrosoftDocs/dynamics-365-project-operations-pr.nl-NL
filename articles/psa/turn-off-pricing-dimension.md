---
title: Een prijsdimensie uitschakelen
description: Dit onderwerp laat zien hoe u prijsdimensies instelt in de Project Service-oplossing.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014290"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="c1895-103">Een prijsdimensie uitschakelen</span><span class="sxs-lookup"><span data-stu-id="c1895-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c1895-104">U moet uw prijsstrategie mogelijk om de paar jaar controleren en bijwerken.</span><span class="sxs-lookup"><span data-stu-id="c1895-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="c1895-105">Alle updates die u aanbrengt, vereisen mogelijk dat u een bestaande prijsdimensie uitschakelt en een nieuwe maakt.</span><span class="sxs-lookup"><span data-stu-id="c1895-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="c1895-106">U hebt bijvoorbeeld eerder een prijs per **Rol** afgesproken, maar nu hebt u besloten om de prijs te baseren op **Werkervaring.**</span><span class="sxs-lookup"><span data-stu-id="c1895-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="c1895-107">Dit kan vereisen dat u **Rol** uitschakelt als prijsdimensie en van **Werkervaring** een nieuwe prijsdimensie maakt.</span><span class="sxs-lookup"><span data-stu-id="c1895-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="c1895-108">Het uitschakelen van een prijsdimensie, ongeacht of deze standaard of aangepast is, kan worden gedaan door de velden **Van toepassing op kosten** en **Van toepassing op verkoop** van de prijsdimensie in te stellen op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="c1895-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="c1895-109">Als u dit doet, kunt u echter de volgende foutmelding ontvangen.</span><span class="sxs-lookup"><span data-stu-id="c1895-109">However, when you do this, you might receive the following error message.</span></span>

![Fout in bedrijfsproces mogelijk bij het uitschakelen van een prijsdimensie](media/Business-Process-Error.png)


<span data-ttu-id="c1895-111">Dit foutbericht geeft aan dat er prijsrecords zijn die eerder zijn ingesteld voor de dimensie die wordt uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c1895-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="c1895-112">Alle records met **Rolprijs** en **Opslag voor rolprijs** die naar een dimensie verwijzen, moeten worden verwijderd voordat de toepasbaarheid van de dimensie kan worden ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="c1895-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="c1895-113">Deze regel is zowel van toepassing op de standaard prijsdimensies als eventuele aangepaste prijsdimensies die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c1895-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="c1895-114">De reden voor deze validatie is dat Project Service een beperking heeft dat elke **rolprijsrecord** een unieke combinatie van dimensies moet hebben.</span><span class="sxs-lookup"><span data-stu-id="c1895-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="c1895-115">Op een prijslijst met de naam **Amerikaanse kostentarieven2018**, hebt u bijvoorbeeld de volgende rijen voor **Rolprijs**.</span><span class="sxs-lookup"><span data-stu-id="c1895-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="c1895-116">Standaardtitel</span><span class="sxs-lookup"><span data-stu-id="c1895-116">Standard Title</span></span>         | <span data-ttu-id="c1895-117">Organisatie-eenheid</span><span class="sxs-lookup"><span data-stu-id="c1895-117">Org Unit</span></span>    |<span data-ttu-id="c1895-118">Eenheid</span><span class="sxs-lookup"><span data-stu-id="c1895-118">Unit</span></span>   |<span data-ttu-id="c1895-119">Prijs</span><span class="sxs-lookup"><span data-stu-id="c1895-119">Price</span></span>  |<span data-ttu-id="c1895-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="c1895-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="c1895-121">Systeemtechnicus</span><span class="sxs-lookup"><span data-stu-id="c1895-121">Systems Engineer</span></span>|<span data-ttu-id="c1895-122">Contoso VS</span><span class="sxs-lookup"><span data-stu-id="c1895-122">Contoso US</span></span>|<span data-ttu-id="c1895-123">Uur</span><span class="sxs-lookup"><span data-stu-id="c1895-123">Hour</span></span>| <span data-ttu-id="c1895-124">100</span><span class="sxs-lookup"><span data-stu-id="c1895-124">100</span></span>|<span data-ttu-id="c1895-125">USD</span><span class="sxs-lookup"><span data-stu-id="c1895-125">USD</span></span>|
| <span data-ttu-id="c1895-126">Hoofdsysteemtechnicus</span><span class="sxs-lookup"><span data-stu-id="c1895-126">Senior Systems Engineer</span></span>|<span data-ttu-id="c1895-127">Contoso VS</span><span class="sxs-lookup"><span data-stu-id="c1895-127">Contoso US</span></span>|<span data-ttu-id="c1895-128">Uur</span><span class="sxs-lookup"><span data-stu-id="c1895-128">Hour</span></span>| <span data-ttu-id="c1895-129">150</span><span class="sxs-lookup"><span data-stu-id="c1895-129">150</span></span>| <span data-ttu-id="c1895-130">USD</span><span class="sxs-lookup"><span data-stu-id="c1895-130">USD</span></span>|


<span data-ttu-id="c1895-131">Wanneer u **Standaardtitel** als prijsdimensie uitschakelt en de prijsengine van Project Service naar een prijs zoekt, wordt alleen de waarde voor **Organisatie-eenheid** uit de invoercontext gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c1895-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="c1895-132">Als **Organisatie-eenheid** van de invoercontext “Contoso US” is, is het resultaat niet-deterministisch omdat beide rijen overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="c1895-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="c1895-133">Om dit scenario te voorkomen controleert Project Service bij het maken van **Rolprijs** records of de combinatie van dimensies uniek is.</span><span class="sxs-lookup"><span data-stu-id="c1895-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="c1895-134">Als de dimensie is uitgeschakeld nadat de **Rolprijs** records zijn gemaakt, kan deze beperking worden overtreden.</span><span class="sxs-lookup"><span data-stu-id="c1895-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="c1895-135">Daarom moet u voordat u een dimensie uitschakelt, alle rijen voor **Rolprijs** en **Opslag voor rolprijs** verwijderen waarvoor die dimensiewaarde is ingevuld.</span><span class="sxs-lookup"><span data-stu-id="c1895-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]