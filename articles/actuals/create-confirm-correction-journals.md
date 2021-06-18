---
title: Correctiejournalen maken en bevestigen
description: Dit onderwerp bevat informatie over het maken en bevestigen van een correctiejournaal.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d242741b2070f086bf8d3f1d40a5380c2a0f518
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996650"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="70bee-103">Correctiejournalen maken en bevestigen</span><span class="sxs-lookup"><span data-stu-id="70bee-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="70bee-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="70bee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70bee-105">Af en toe worden tijds- en onkostenvermeldingen onjuist ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="70bee-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="70bee-106">Een consultant kan bijvoorbeeld de verkeerde datum selecteren bij het invoeren van tijdgegevens of ze kunnen de cijfers transponeren bij het invoeren van onkosten.</span><span class="sxs-lookup"><span data-stu-id="70bee-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="70bee-107">Als een consultant de ingediende items niet kan bijwerken, kan een beheerder de invoer voor een project rechtstreeks corrigeren.</span><span class="sxs-lookup"><span data-stu-id="70bee-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="70bee-108">U hebt beheerdersmachtigingen nodig om de procedures in dit onderwerp te voltooien.</span><span class="sxs-lookup"><span data-stu-id="70bee-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="70bee-109">Correcte goedgekeurde tijdsvermeldingen</span><span class="sxs-lookup"><span data-stu-id="70bee-109">Correct approved time entries</span></span>     

<span data-ttu-id="70bee-110">Voer de volgende stappen uit om enkele of meerdere tijdsvermeldingen voor een project te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="70bee-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="70bee-111">Selecteer in het gebied **Verkoop** de optie **Transacties** en selecteer vervolgens **Goedgekeurde tijd**.</span><span class="sxs-lookup"><span data-stu-id="70bee-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="70bee-112">Zoek en selecteer in de lijst **Goedgekeurde tijd** een of meer goedgekeurde tijdsvermeldingen om te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="70bee-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="70bee-113">U kunt het filter gebruiken om gerelateerde items te lokaliseren.</span><span class="sxs-lookup"><span data-stu-id="70bee-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="70bee-114">U kunt bijvoorbeeld filteren op een project-id en alle goedgekeurde tijdsvermeldingen met die project-id selecteren.</span><span class="sxs-lookup"><span data-stu-id="70bee-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="70bee-115">Selecteer **Posten corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="70bee-115">Select **Correct entries**.</span></span> <span data-ttu-id="70bee-116">Er wordt automatisch een nieuw correctiejournaal gemaakt met het toegewezen type **Correctie van tijd**.</span><span class="sxs-lookup"><span data-stu-id="70bee-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="70bee-117">De geselecteerde items worden toegevoegd aan het journaal.</span><span class="sxs-lookup"><span data-stu-id="70bee-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="70bee-118">Voer op de pagina **Nieuw journaal** een **Beschrijving** voor uw correctiejournaal in en selecteer vervolgens het tabblad **Correcties van tijdsvermeldingen**.</span><span class="sxs-lookup"><span data-stu-id="70bee-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="70bee-119">Werk in de sectie **Nieuwe waarden voor tijdsvermeldingen** de velden indien nodig bij met de juiste informatie.</span><span class="sxs-lookup"><span data-stu-id="70bee-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="70bee-120">U kunt bijvoorbeeld het toegewezen project of de boekbare resource wijzigen.</span><span class="sxs-lookup"><span data-stu-id="70bee-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="70bee-121">Selecteer **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="70bee-121">Select **Preview**.</span></span> <span data-ttu-id="70bee-122">Selecteer **OK** in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="70bee-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="70bee-123">Op het tabblad **Journaalregels** kunt u een lijst bekijken van de originele werkelijke waarden die betrekking hebben op de geselecteerde tijdsvermeldingen die zijn teruggedraaid en de gecorrigeerde overeenkomstige regels die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="70bee-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="70bee-124">Herhaal stap 5 en 6 als er aanvullende correcties nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="70bee-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="70bee-125">Alle gecorrigeerde werkelijke waarden hebben dezelfde waarden die u in de sectie **Nieuwe waarden voor tijdsvermeldingen** hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="70bee-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="70bee-126">Selecteer **Bevestigen** als de correcties verschijnen zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="70bee-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="70bee-127">Selecteer **OK** in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="70bee-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="70bee-128">Ga terug naar het gebied **Verkoop**, selecteer **Projecten** en open vervolgens het project waarvoor u zojuist de tijdsvermeldingen hebt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="70bee-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="70bee-129">Bekijk op de pagina **Projecten**, op het tabblad **Werkelijke waarden** de wijzigingen die u hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="70bee-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="70bee-130">Als het tabblad **Werkelijke waarden** niet zichtbaar is, selecteert u **Gerelateerd** > **Werkelijke waarden**.</span><span class="sxs-lookup"><span data-stu-id="70bee-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="70bee-131">In de lijst **Gekoppelde weergave van werkelijke waarden** kunt u zien dat de oorspronkelijke tijdsvermeldingen die zijn teruggedraaid, nog steeds worden vermeld evenals de corresponderende gecorrigeerde tijdsvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="70bee-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="70bee-132">In de volgende afbeelding zijn er bijvoorbeeld twee regelitems met een hoeveelheid van 8,00 waarvoor afschrijvingen worden vermeld in de kolom Bedrag.</span><span class="sxs-lookup"><span data-stu-id="70bee-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="70bee-133">Daarnaast zijn er twee regelitems met een hoeveelheid van -8,00 die gecrediteerde bedragen weergeven in de kolom Bedrag.</span><span class="sxs-lookup"><span data-stu-id="70bee-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="70bee-134">Deze correcties resulteren in de hoeveelheid nul.</span><span class="sxs-lookup"><span data-stu-id="70bee-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="70bee-135">Correcte goedgekeurde onkostenvermeldingen</span><span class="sxs-lookup"><span data-stu-id="70bee-135">Correct approved expense entries</span></span>

<span data-ttu-id="70bee-136">Voer de volgende stappen uit om een of meer onkostenvermeldingen te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="70bee-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="70bee-137">Selecteer in het gebied **Verkoop** in het linkernavigatievenster onder **Transacties** de optie **Goedgekeurde onkosten**.</span><span class="sxs-lookup"><span data-stu-id="70bee-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="70bee-138">Selecteer in de lijst **Goedgekeurde onkosten** het project dat u wilt corrigeren en selecteer vervolgens **Correcte vermeldingen**.</span><span class="sxs-lookup"><span data-stu-id="70bee-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="70bee-139">Er wordt automatisch een nieuw correctiejournaal gemaakt met het toegewezen type **Correctie van onkosten**.</span><span class="sxs-lookup"><span data-stu-id="70bee-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="70bee-140">Voer op de pagina **Nieuw journaal** een **Beschrijving** voor de correctie in, en selecteer op het tabblad **Onkostencorrectie**, in de sectie **Nieuwe waarden voor onkosten** de gegevensvelden die u wilt corrigeren voor de geselecteerde onkostenregels.</span><span class="sxs-lookup"><span data-stu-id="70bee-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="70bee-141">U kunt de uitgave bijvoorbeeld toewijzen aan een ander **Project** of de **Onkostencategorie**, **Onkostendatum** of **Boekbare resource** corrigeren.</span><span class="sxs-lookup"><span data-stu-id="70bee-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="70bee-142">Selecteer **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="70bee-142">Select **Preview**.</span></span> <span data-ttu-id="70bee-143">Selecteer **OK** in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="70bee-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="70bee-144">Controleer de correcties op het tabblad **Journaalregels**. U kunt u een lijst bekijken van de originele werkelijke waarden die betrekking hebben op de geselecteerde onkostenvermeldingen die zijn teruggedraaid en de gecorrigeerde overeenkomstige regels die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="70bee-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="70bee-145">Selecteer **Bevestigen** als de gecorrigeerde waarden voldoen aan de verwachting.</span><span class="sxs-lookup"><span data-stu-id="70bee-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="70bee-146">Selecteer **OK** in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="70bee-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="70bee-147">Als de waarden niet worden weergegeven zoals verwacht, selecteert u **Annuleren** om terug te keren naar de lijst **Goedgekeurde onkosten**.</span><span class="sxs-lookup"><span data-stu-id="70bee-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="70bee-148">Herhaal de stappen 2 tot en met 5.</span><span class="sxs-lookup"><span data-stu-id="70bee-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="70bee-149">De gecorrigeerde werkelijke waarden hebben dezelfde waarden die u in de sectie **Nieuwe waarden voor onkosten** hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="70bee-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="70bee-150">Nadat u het correctiejournaal hebt bevestigd, navigeert u terug naar het project of de projecten die u hebt bijgewerkt om uw wijzigingen te bekijken.</span><span class="sxs-lookup"><span data-stu-id="70bee-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="70bee-151">Controleer op het tabblad **Werkelijke waarden** op de projectpagina de **Gekoppelde weergave van werkelijke waarden**.</span><span class="sxs-lookup"><span data-stu-id="70bee-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="70bee-152">De oorspronkelijke vermeldingen en de gecorrigeerde vermeldingen worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="70bee-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="70bee-153">In de volgende afbeelding ziet u de oorspronkelijke bedragen voor onkostenvermeldingen en de overeenkomstige gecorrigeerde bedragen voor onkostenvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="70bee-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]