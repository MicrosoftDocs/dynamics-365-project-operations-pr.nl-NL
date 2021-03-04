---
title: Verwerking van betalingsbewijzen
description: Dit onderwerp bevat informatie over de OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen. Deze functie is ontworpen om de gebruikerservaring te verbeteren bij het maken van onkostendeclaraties in Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960286"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="56366-104">Verwerking van betalingsbewijzen</span><span class="sxs-lookup"><span data-stu-id="56366-104">Expense receipt processing</span></span>

<span data-ttu-id="56366-105">De invoer van kosten is verbeterd door de introductie van OCR-verwerking (optische tekenherkenning) voor betalingsbewijzen.</span><span class="sxs-lookup"><span data-stu-id="56366-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="56366-106">Deze functie is ontworpen om de gebruikerservaring te verbeteren bij het maken van onkostendeclaraties.</span><span class="sxs-lookup"><span data-stu-id="56366-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="56366-107">Belangrijke functies</span><span class="sxs-lookup"><span data-stu-id="56366-107">Key features</span></span>

- <span data-ttu-id="56366-108">De naam van de winkel, de datum en het totale bedrag worden uit de betalingsbewijzen gehaald.</span><span class="sxs-lookup"><span data-stu-id="56366-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="56366-109">De functie probeert om niet-gekoppelde betalingsbewijzen te matchen met niet-gekoppelde onkostentransacties.</span><span class="sxs-lookup"><span data-stu-id="56366-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="56366-110">Gebruikers kunnen handmatig ingevoerde onkostentransacties maken op basis van betalingsbewijzen.</span><span class="sxs-lookup"><span data-stu-id="56366-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="56366-111">Gebruiksvoorbeelden</span><span class="sxs-lookup"><span data-stu-id="56366-111">Usage examples</span></span>

<span data-ttu-id="56366-112">Als u betalingsbewijzen die creditcardtransacties omvatten, automatisch wilt koppelen bij het maken van een onkostendeclaratie, doet u het volgende:</span><span class="sxs-lookup"><span data-stu-id="56366-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="56366-113">Open de werkruimte **Onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="56366-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="56366-114">Controleer op het tabblad **Ontvangsten** of de niet-gekoppelde betalingsbewijzen bestaan.</span><span class="sxs-lookup"><span data-stu-id="56366-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="56366-115">U kunt ook betalingsbewijzen uploaden op het tabblad **Ontvangsten**.</span><span class="sxs-lookup"><span data-stu-id="56366-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="56366-116">Controleer op het tabblad **Onkosten** of de niet-gekoppelde onkosten bestaan.</span><span class="sxs-lookup"><span data-stu-id="56366-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="56366-117">Meestal importeert degene die verantwoordelijk is voor de onkostenadministratie, deze onkosten vanuit de creditcardprovider.</span><span class="sxs-lookup"><span data-stu-id="56366-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="56366-118">Selecteer **Nieuwe onkostennota**.</span><span class="sxs-lookup"><span data-stu-id="56366-118">Select **New expense report**.</span></span> <span data-ttu-id="56366-119">U ziet dat u bij het maken van een onkostennota nu niet alleen onkosten, maar ook betalingsbewijzen kunt opnemen.</span><span class="sxs-lookup"><span data-stu-id="56366-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="56366-120">Als u zowel onkosten als betalingsbewijzen toevoegt, wordt het automatisch matchen van betalingsbewijzen met onkosten geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="56366-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="56366-121">Voer de volgende stappen uit om onkosten te maken of om onkosten te matchen op basis van een betalingsbewijs:</span><span class="sxs-lookup"><span data-stu-id="56366-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="56366-122">Ga in een onkostennota naar het tabblad **Ontvangsten** en koppel een betalingsbewijs door **Ontvangsten toevoegen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="56366-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="56366-123">Onder de geüploade afbeelding van het betalingsbewijs vindt u de opties **Maken** en **Matchen**.</span><span class="sxs-lookup"><span data-stu-id="56366-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="56366-124">Selecteer **Maken** om een handmatig ingevoerde onkostentransactie aan te maken en de waarden in te vullen die uit het betalingsbewijs kunnen worden geëxtraheerd.</span><span class="sxs-lookup"><span data-stu-id="56366-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="56366-125">Als u **Matchen** selecteert, probeert het systeem bestaande onkosten te matchen met het betalingsbewijs.</span><span class="sxs-lookup"><span data-stu-id="56366-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="56366-126">Installatie</span><span class="sxs-lookup"><span data-stu-id="56366-126">Installation</span></span>

<span data-ttu-id="56366-127">Deze functie werkt in combinatie met de functie **Opnieuw ontworpen onkostendeclaraties** om het invoeren van onkosten te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="56366-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="56366-128">Deze functie is alleen beschikbaar voor Tier 2+-omgevingen, namelijk Sandbox en Production.</span><span class="sxs-lookup"><span data-stu-id="56366-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="56366-129">Als u deze geavanceerde mogelijkheden voor onkosten wilt gebruiken, installeert u de invoegtoepassing Expense Management Service voor Microsoft Dynamics 365 Finance en schakelt u de functies in in uw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="56366-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="56366-130">U kunt de invoegtoepassing openen vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="56366-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="56366-131">Meld u aan bij LCS en open de gewenste omgeving.</span><span class="sxs-lookup"><span data-stu-id="56366-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="56366-132">Ga naar **Volledige details**.</span><span class="sxs-lookup"><span data-stu-id="56366-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="56366-133">Selecteer **Onderhouden** of scrol omlaag naar het sneltabblad **Omgevingsinvoegtoepassingen**.</span><span class="sxs-lookup"><span data-stu-id="56366-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="56366-134">Selecteer **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="56366-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="56366-135">Selecteer **Expense Management Service**.</span><span class="sxs-lookup"><span data-stu-id="56366-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="56366-136">Volg de installatiehandleiding en ga akkoord met de algemene voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="56366-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="56366-137">Selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="56366-137">Select **Install**.</span></span>

<span data-ttu-id="56366-138">Schakel in de werkruimte **Functiebeheer** de volgende functies in:</span><span class="sxs-lookup"><span data-stu-id="56366-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="56366-139">Opnieuw ontworpen onkostennota's</span><span class="sxs-lookup"><span data-stu-id="56366-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="56366-140">Automatisch onkosten matchen en maken op basis van een betalingsbewijs</span><span class="sxs-lookup"><span data-stu-id="56366-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="56366-141">Wanneer u deze functies inschakelt, vinden de volgende acties plaats:</span><span class="sxs-lookup"><span data-stu-id="56366-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="56366-142">De bestaande werkruimte **Onkostenbeheer** wordt vervangen door de nieuwe werkruimte.</span><span class="sxs-lookup"><span data-stu-id="56366-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="56366-143">Er wordt een nieuw menu-item voor de zichtbaarheid van onkostenvelden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="56366-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="56366-144">U kunt de voormalige pagina **Onkostennota's** nog steeds openen door naar **Onkostenbeheer > Mijn onkosten > Onkostennota's** te gaan.</span><span class="sxs-lookup"><span data-stu-id="56366-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="56366-145">Via werkstromen en goedkeuringen komt u nog steeds uit bij de bestaande pagina met onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="56366-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="56366-146">Betalingsbewijzen worden verwerkt via Microsoft Azure Cognitive Services en metagegevens worden geëxtraheerd en toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="56366-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="56366-147">Er wordt een optie toegevoegd waarmee u een onkostennota kunt maken die gematchte niet-gekoppelde betalingsbewijzen bevat.</span><span class="sxs-lookup"><span data-stu-id="56366-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="56366-148">Met een optie die aan onkostennota's wordt toegevoegd, kunt u een onkostenregel maken op basis van een betalingsbewijs of wordt geprobeerd een bestaand betalingsbewijs te matchen met een bestaande onkostenregel.</span><span class="sxs-lookup"><span data-stu-id="56366-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="56366-149">Zie [Opnieuw ontworpen onkostendeclaraties](ExpenseWorkspaceNew.md) voor meer informatie over de vernieuwde functie Onkostendeclaraties.</span><span class="sxs-lookup"><span data-stu-id="56366-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="56366-150">Veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="56366-150">Frequently asked questions</span></span>

<span data-ttu-id="56366-151">**Gebruikt Microsoft mijn gegevens voor zijn modellen?**</span><span class="sxs-lookup"><span data-stu-id="56366-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="56366-152">Nee, Microsoft heeft een algemeen Machine Learning-model gebouwd voor zijn service voor de verwerking van betalingsbewijzen.</span><span class="sxs-lookup"><span data-stu-id="56366-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="56366-153">Dit model is niet gebaseerd op de betalingsbewijzen die u uploadt.</span><span class="sxs-lookup"><span data-stu-id="56366-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="56366-154">**Waar is deze functie beschikbaar en waar vindt de gegevensverwerking plaats?**</span><span class="sxs-lookup"><span data-stu-id="56366-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="56366-155">Momenteel worden de Verenigde Staten ondersteund.</span><span class="sxs-lookup"><span data-stu-id="56366-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="56366-156">**Waar gaan mijn betalingsbewijzen naartoe?**</span><span class="sxs-lookup"><span data-stu-id="56366-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="56366-157">Finance neemt contact op met Cognitive Services om de veldgegevens te extraheren.</span><span class="sxs-lookup"><span data-stu-id="56366-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="56366-158">Cognitive Services bewaart gedurende maximaal 24 uur een kopie van uw betalingsbewijs terwijl de verwerking plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="56366-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="56366-159">Nadat de verwerking is voltooid, verwijdert Cognitive Services het betalingsbewijs.</span><span class="sxs-lookup"><span data-stu-id="56366-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="56366-160">Betalingsbewijzen worden nog steeds opgeslagen in Finance.</span><span class="sxs-lookup"><span data-stu-id="56366-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="56366-161">Zie [Het begrijpen van betalingsbewijzen mogelijk maken met de nieuwe mogelijkheid van Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="56366-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
