---
title: Een betalingsbewijs matchen met onkosten met behulp van OCR
description: Dit onderwerp bevat informatie over de OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124317"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="abca3-103">Een betalingsbewijs matchen met onkosten met behulp van OCR</span><span class="sxs-lookup"><span data-stu-id="abca3-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="abca3-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="abca3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abca3-105">De invoer van kosten is verbeterd door de introductie van OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen.</span><span class="sxs-lookup"><span data-stu-id="abca3-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="abca3-106">Deze functionaliteit is ontworpen om de gebruikerservaring te verbeteren bij het maken van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="abca3-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="abca3-107">Belangrijke functies</span><span class="sxs-lookup"><span data-stu-id="abca3-107">Key features</span></span>

- <span data-ttu-id="abca3-108">Het systeem extraheert de naam van de winkel, de datum en het totale bedrag uit de betalingsbewijzen.</span><span class="sxs-lookup"><span data-stu-id="abca3-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="abca3-109">Het systeem probeert om niet-gekoppelde betalingsbewijzen te matchen met niet-gekoppelde onkostentransacties.</span><span class="sxs-lookup"><span data-stu-id="abca3-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="abca3-110">U kunt handmatig ingevoerde onkostentransacties maken op basis van betalingsbewijzen.</span><span class="sxs-lookup"><span data-stu-id="abca3-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="abca3-111">Betalingsbewijzen koppelen aan een onkostennota</span><span class="sxs-lookup"><span data-stu-id="abca3-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="abca3-112">Als u betalingsbewijzen die creditcardtransacties omvatten, automatisch wilt koppelen bij het maken van een onkostennota, neemt u de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="abca3-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="abca3-113">Open de werkruimte **Onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="abca3-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="abca3-114">Controleer op het tabblad **Ontvangsten** of de niet-gekoppelde betalingsbewijzen bestaan.</span><span class="sxs-lookup"><span data-stu-id="abca3-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="abca3-115">U kunt ook betalingsbewijzen uploaden op het tabblad **Ontvangsten**.</span><span class="sxs-lookup"><span data-stu-id="abca3-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="abca3-116">Controleer op het tabblad **Onkosten** of de niet-gekoppelde onkosten bestaan.</span><span class="sxs-lookup"><span data-stu-id="abca3-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="abca3-117">Meestal importeert degene die verantwoordelijk is voor de onkostenadministratie, deze onkosten vanuit de creditcardprovider.</span><span class="sxs-lookup"><span data-stu-id="abca3-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="abca3-118">Selecteer **Nieuwe onkostennota**.</span><span class="sxs-lookup"><span data-stu-id="abca3-118">Select **New expense report**.</span></span> <span data-ttu-id="abca3-119">U ziet dat u bij het maken van een onkostennota nu niet alleen onkosten, maar ook betalingsbewijzen kunt opnemen.</span><span class="sxs-lookup"><span data-stu-id="abca3-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="abca3-120">Als u zowel onkosten als betalingsbewijzen toevoegt, wordt het automatisch matchen van betalingsbewijzen met onkosten geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="abca3-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="abca3-121">Betalingsbewijzen maken of matchen voor een onkostennota</span><span class="sxs-lookup"><span data-stu-id="abca3-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="abca3-122">Voer de volgende stappen uit om onkosten aan te maken of om onkosten te matchen op basis van een betalingsbewijs.</span><span class="sxs-lookup"><span data-stu-id="abca3-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="abca3-123">Ga in een onkostennota naar het tabblad **Ontvangsten** en koppel een betalingsbewijs door **Ontvangsten toevoegen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="abca3-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="abca3-124">Onder de geüploade afbeelding van het betalingsbewijs vindt u de opties **Maken** en **Matchen**.</span><span class="sxs-lookup"><span data-stu-id="abca3-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="abca3-125">Selecteer **Maken** om een handmatig ingevoerde onkostentransactie aan te maken en de waarden in te vullen die uit het betalingsbewijs kunnen worden geëxtraheerd.</span><span class="sxs-lookup"><span data-stu-id="abca3-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="abca3-126">Als u **Matchen** selecteert, probeert het systeem bestaande onkosten te matchen met het betalingsbewijs.</span><span class="sxs-lookup"><span data-stu-id="abca3-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="abca3-127">Installatie</span><span class="sxs-lookup"><span data-stu-id="abca3-127">Installation</span></span>

<span data-ttu-id="abca3-128">Als u deze geavanceerde mogelijkheden voor onkosten wilt gebruiken, installeert u de invoegtoepassing Expense Management Service voor Microsoft Dynamics 365 Finance en schakelt u de functies in in uw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="abca3-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="abca3-129">U kunt de invoegtoepassing openen vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="abca3-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="abca3-130">Meld u aan bij LCS en open de gewenste omgeving.</span><span class="sxs-lookup"><span data-stu-id="abca3-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="abca3-131">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="abca3-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="abca3-132">Selecteer **Onderhouden** of scrol omlaag naar het sneltabblad **Omgevingsinvoegtoepassingen**.</span><span class="sxs-lookup"><span data-stu-id="abca3-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="abca3-133">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="abca3-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="abca3-134">Selecteer **Expense Management Service**.</span><span class="sxs-lookup"><span data-stu-id="abca3-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="abca3-135">Volg de installatiehandleiding en ga akkoord met de algemene voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="abca3-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="abca3-136">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="abca3-136">Select **Install**.</span></span>

<span data-ttu-id="abca3-137">Schakel in de werkruimte **Functiebeheer** de volgende functies in:</span><span class="sxs-lookup"><span data-stu-id="abca3-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="abca3-138">Opnieuw ontworpen onkostennota's</span><span class="sxs-lookup"><span data-stu-id="abca3-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="abca3-139">Automatisch onkosten matchen en maken op basis van een betalingsbewijs</span><span class="sxs-lookup"><span data-stu-id="abca3-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="abca3-140">Wanneer u deze functies inschakelt, vinden de volgende acties plaats:</span><span class="sxs-lookup"><span data-stu-id="abca3-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="abca3-141">De bestaande werkruimte **Onkostenbeheer** wordt vervangen door de nieuwe werkruimte.</span><span class="sxs-lookup"><span data-stu-id="abca3-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="abca3-142">Er wordt een nieuw menu-item voor de zichtbaarheid van onkostenvelden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="abca3-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="abca3-143">U kunt de voormalige pagina **Onkostennota's** nog steeds openen door naar **Onkostenbeheer > Mijn onkosten > Onkostennota's** te gaan.</span><span class="sxs-lookup"><span data-stu-id="abca3-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="abca3-144">Via werkstromen en goedkeuringen komt u nog steeds uit bij de bestaande pagina met onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="abca3-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="abca3-145">Betalingsbewijzen worden verwerkt via Microsoft Azure Cognitive Services en metagegevens worden geëxtraheerd en toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="abca3-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="abca3-146">Er wordt een optie toegevoegd waarmee u een onkostennota kunt maken die gematchte niet-gekoppelde betalingsbewijzen bevat.</span><span class="sxs-lookup"><span data-stu-id="abca3-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="abca3-147">Met een optie die aan onkostennota's wordt toegevoegd, kunt u een onkostenregel maken op basis van een betalingsbewijs of wordt geprobeerd een bestaand betalingsbewijs te matchen met een bestaande onkostenregel.</span><span class="sxs-lookup"><span data-stu-id="abca3-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="abca3-148">Veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="abca3-148">Frequently asked questions</span></span>

<span data-ttu-id="abca3-149">**Gebruikt Microsoft mijn gegevens voor zijn modellen?**</span><span class="sxs-lookup"><span data-stu-id="abca3-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="abca3-150">Nee, Microsoft heeft een algemeen Machine Learning-model gebouwd voor zijn service voor de verwerking van betalingsbewijzen.</span><span class="sxs-lookup"><span data-stu-id="abca3-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="abca3-151">Dit model is niet gebaseerd op de betalingsbewijzen die u uploadt.</span><span class="sxs-lookup"><span data-stu-id="abca3-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="abca3-152">**Waar is deze functie beschikbaar en waar vindt de gegevensverwerking plaats?**</span><span class="sxs-lookup"><span data-stu-id="abca3-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="abca3-153">Momenteel worden de Verenigde Staten ondersteund.</span><span class="sxs-lookup"><span data-stu-id="abca3-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="abca3-154">**Waar gaan mijn betalingsbewijzen naartoe?**</span><span class="sxs-lookup"><span data-stu-id="abca3-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="abca3-155">Finance neemt contact op met Cognitive Services om de veldgegevens te extraheren.</span><span class="sxs-lookup"><span data-stu-id="abca3-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="abca3-156">Cognitive Services bewaart gedurende maximaal 24 uur een kopie van uw betalingsbewijs terwijl de verwerking plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="abca3-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="abca3-157">Nadat de verwerking is voltooid, verwijdert Cognitive Services het betalingsbewijs.</span><span class="sxs-lookup"><span data-stu-id="abca3-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="abca3-158">Betalingsbewijzen worden nog steeds opgeslagen in Finance.</span><span class="sxs-lookup"><span data-stu-id="abca3-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="abca3-159">Zie [Het begrijpen van betalingsbewijzen mogelijk maken met de nieuwe mogelijkheid van Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="abca3-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
