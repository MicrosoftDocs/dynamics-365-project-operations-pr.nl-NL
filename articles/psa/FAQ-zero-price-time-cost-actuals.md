---
title: Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van tijd?
description: Het probleem oplossen waarbij de prijs standaard op nul wordt gezet voor werkelijke kostenwaarden op basis van tijd.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146252"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="cee3a-103">Waarom wordt de prijs standaard op nul gezet voor de werkelijke kostenwaarden op basis van tijd?</span><span class="sxs-lookup"><span data-stu-id="cee3a-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cee3a-104">Dit artikel is van toepassing op werkelijke waarden waarvoor de transactieklasse is ingesteld op Tijd en het transactietype Kosten is.</span><span class="sxs-lookup"><span data-stu-id="cee3a-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="cee3a-105">Met de volgende drie controles kunt u vaststellen waarom de prijs standaard op 0 wordt gezet voor werkelijke kostenwaarden op basis van tijd.</span><span class="sxs-lookup"><span data-stu-id="cee3a-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="cee3a-106">Controle 1: De kostprijslijst voor het project identificeren</span><span class="sxs-lookup"><span data-stu-id="cee3a-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="cee3a-107">Zoek het project in het projectveld voor de werkelijke waarde en ga naar de projectpagina.</span><span class="sxs-lookup"><span data-stu-id="cee3a-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="cee3a-108">Klik op de koppeling voor de contracterende eenheid in het veld.</span><span class="sxs-lookup"><span data-stu-id="cee3a-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="cee3a-109">Controleer op de pagina Contracterende eenheid of voor de contracterende eenheid een prijslijst bestaat in het raster Kostprijslijsten.</span><span class="sxs-lookup"><span data-stu-id="cee3a-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="cee3a-110">Als er meerdere prijslijsten zijn, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="cee3a-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="cee3a-111">Project Service ondersteunt slechts één prijslijst per organisatie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="cee3a-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="cee3a-112">Verwijder alle prijslijsten uit deze entiteit tot er nog slechts één prijslijst is toegevoegd in het raster Kostprijslijsten van de organisatie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="cee3a-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="cee3a-113">Als er geen prijslijsten aan de organisatie-eenheid zijn gekoppeld, controleert u de valuta van de organisatie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="cee3a-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="cee3a-114">Ga naar Project Service en vervolgens naar Parameters om het tabblad Prijslijsten te openen. Controleer of er prijslijsten bestaan waarvoor de context is ingesteld op Kosten en waarvan de valuta overeenkomt met die van de organisatie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="cee3a-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="cee3a-115">Als er geen prijslijsten zijn die voldoen aan die criteria, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="cee3a-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="cee3a-116">Zorg ervoor dat er minstens één prijslijst is waarvoor de context op Kosten is ingesteld en waarvan de valuta overeenkomt met de valuta van de organisatie-eenheid.</span><span class="sxs-lookup"><span data-stu-id="cee3a-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="cee3a-117">Neem ook de rest van dit document door om nog meer controles uit te voeren als er meerdere prijslijsten voldoen aan die criteria.</span><span class="sxs-lookup"><span data-stu-id="cee3a-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="cee3a-118">Controle 2: Zijn de hierboven geïdentificeerde prijslijsten geldig voor de specifieke datum van de werkelijke kostenwaarde op basis van tijd?</span><span class="sxs-lookup"><span data-stu-id="cee3a-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="cee3a-119">Een prijslijst wordt in Project Service pas voor standaardprijzen gebruikt als deze prijslijst van toepassing is op de datum van de werkelijke kostenwaarde op basis van tijd.</span><span class="sxs-lookup"><span data-stu-id="cee3a-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="cee3a-120">Controleer het volgende om te bepalen of de hierboven geïdentificeerde prijslijsten van toepassing zijn:</span><span class="sxs-lookup"><span data-stu-id="cee3a-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="cee3a-121">Controleer of de begin- en einddatums op het tabblad Algemeen voor de toegevoegde prijslijsten niet leeg zijn.</span><span class="sxs-lookup"><span data-stu-id="cee3a-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="cee3a-122">Als de begin- en einddatums van de bovenstaande prijslijsten leeg zijn, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="cee3a-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="cee3a-123">Controleer of een van de geïdentificeerde prijslijsten van toepassing is op de begindatum van uw werkelijke kostenwaarde op basis van tijd.</span><span class="sxs-lookup"><span data-stu-id="cee3a-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="cee3a-124">De datum van de werkelijke kostenwaarde op basis van tijd moet bijvoorbeeld binnen de begin- en einddatum in de prijslijst liggen.</span><span class="sxs-lookup"><span data-stu-id="cee3a-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="cee3a-125">Als geen van de prijslijsten van toepassing is op de datum van de werkelijke kostenwaarden op basis van tijd, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="cee3a-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="cee3a-126">Wijzig de begin- en einddatums van de prijslijst om ervoor te zorgen dat de prijslijst de datum van de werkelijke kostenwaarden op basis van tijd dekt.</span><span class="sxs-lookup"><span data-stu-id="cee3a-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="cee3a-127">Als meerdere prijslijsten van toepassing zijn op de datum van de werkelijke kostenwaarde op basis van tijd, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="cee3a-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="cee3a-128">U kunt dit probleem verhelpen door de begin- en einddatums van de prijslijst(en) te bewerken zodat de datum van de werkelijke kostenwaarde op basis van tijd door slechts één prijslijst wordt gedekt.</span><span class="sxs-lookup"><span data-stu-id="cee3a-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="cee3a-129">Als de datum van de werkelijke kostenwaarde op basis van tijd door slechts één prijslijst wordt gedekt, gaat u verder met de volgende controle in het document.</span><span class="sxs-lookup"><span data-stu-id="cee3a-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="cee3a-130">Zodra u de vereiste correcties hebt doorgevoerd, maakt u een nieuwe tijdvermelding, keurt u deze goed en verifieert u of voor de werkelijke kostenwaarde op basis van tijd een geldige prijs wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cee3a-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="cee3a-131">Controle 3: Bevat de prijslijst voor de prijsdimensies een prijs voor de werkelijke kostenwaarde op basis van tijd?</span><span class="sxs-lookup"><span data-stu-id="cee3a-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="cee3a-132">Als u controles 1 en 2 hebt uitgevoerd, moet u nu slechts één prijslijst hebben die geldt voor de datum van de werkelijke kostenwaarde op basis van tijd.</span><span class="sxs-lookup"><span data-stu-id="cee3a-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="cee3a-133">Open deze prijslijst en ga naar het tabblad Rolprijzen. Controleer of in het raster een rij bestaat voor de prijsdimensies van de werkelijke kostenwaarde op basis van tijd.</span><span class="sxs-lookup"><span data-stu-id="cee3a-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="cee3a-134">Als in het raster geen rij voor de prijsdimensies van de werkelijke kostenwaarde op basis van tijd bestaat, hebt u het probleem gevonden.</span><span class="sxs-lookup"><span data-stu-id="cee3a-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="cee3a-135">Maak in het raster Rolprijzen een rij voor de prijsdimensies van uw werkelijke kostenwaarde op basis van tijd.</span><span class="sxs-lookup"><span data-stu-id="cee3a-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="cee3a-136">Maak vervolgens een nieuwe tijdvermelding, keur deze goed en verifieer of voor de werkelijke kostenwaarde op basis van tijd een geldige prijs wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cee3a-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="cee3a-137">Dien een ondersteuningsticket in als na het uitvoeren van de bovenstaande controles voor u nog steeds geen geldige prijs wordt weergegeven voor de werkelijke kostenwaarde op basis van tijd.</span><span class="sxs-lookup"><span data-stu-id="cee3a-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



