---
title: Creditcardtransacties importeren en onderhouden
description: In dit onderwerp wordt uitgelegd hoe u onkostengerelateerde creditcardtransacties importeert en onderhoudt. Deze transacties kunnen zo worden ingesteld dat ze automatisch worden geïmporteerd volgens een periodiek schema, of ze kunnen handmatig worden geïmporteerd als ze nodig zijn.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951068"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="92793-104">Creditcardtransacties importeren en onderhouden</span><span class="sxs-lookup"><span data-stu-id="92793-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="92793-105">Onkostengerelateerde creditcardtransacties kunnen zo worden ingesteld dat ze automatisch volgens een terugkerende planning worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="92793-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="92793-106">U kunt de transacties ook handmatig importeren als u ze nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="92793-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="92793-107">De creditcardtransacties worden geïmporteerd via de gegevensentiteit Creditcardtransacties.</span><span class="sxs-lookup"><span data-stu-id="92793-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="92793-108">Zie [Gegevensentiteiten](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities) voor meer informatie over gegevensentiteiten.</span><span class="sxs-lookup"><span data-stu-id="92793-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="92793-109">Creditcardtransacties importeren</span><span class="sxs-lookup"><span data-stu-id="92793-109">Import credit card transactions</span></span>

1. <span data-ttu-id="92793-110">Selecteer op de pagina **Creditcardtransacties** de optie **Transacties importeren**.</span><span class="sxs-lookup"><span data-stu-id="92793-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="92793-111">Als u gegevensbeheer voor het eerst opent, moet het systeem de lijst met gegevensentiteiten bijwerken voordat u verder kunt gaan.</span><span class="sxs-lookup"><span data-stu-id="92793-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="92793-112">Geef een unieke naam voor de importtaak op in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="92793-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="92793-113">Selecteer in het veld **Brongegevensindeling** de indeling van het bestand met de creditcardtransacties die u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="92793-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="92793-114">Selecteer **Uploaden** en selecteer het bestand dat u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="92793-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="92793-115">Nadat het bestand is geüpload, controleert u de toewijzing van het creditcardtransactiebestand en de kolommen van de gegevensentiteit Creditcardtransacties door de koppeling **Toewijzing weergeven** op de tegel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="92793-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="92793-116">Als er toewijzingsfouten zijn, of als u de toewijzing moet wijzigen, brengt u de wijzigingen in de toewijzing aan op het tabblad **Visualisering van toewijzing** of het tabblad **Toewijzingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="92793-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="92793-117">Selecteer **Terugkerende gegevenstaak maken** om de creditcardtransacties te automatiseren.</span><span class="sxs-lookup"><span data-stu-id="92793-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="92793-118">U kunt vervolgens het terugkeerpatroon instellen dat bepaalt hoe vaak creditcardtransacties moeten worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="92793-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="92793-119">Als u klaar bent, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="92793-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="92793-120">Selecteer **Importeren** om het geselecteerde bestand nu te importeren.</span><span class="sxs-lookup"><span data-stu-id="92793-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="92793-121">Als er fouten optreden tijdens het importeren, kunt u het uitvoeringslogboek of de faseringsgegevens bekijken om de fouten weer te geven die u moet herstellen om het bestand te kunnen importeren.</span><span class="sxs-lookup"><span data-stu-id="92793-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="92793-122">Als u meer dan een bestandsindeling moet importeren, moet u voor elk indelingstype een afzonderlijke importtaak maken.</span><span class="sxs-lookup"><span data-stu-id="92793-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="92793-123">De creditcardtransacties opnieuw toewijzen aan werknemers van wie het dienstverband is beëindigd</span><span class="sxs-lookup"><span data-stu-id="92793-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="92793-124">Nadat een werknemersrecord is verwijderd, wordt het Active Directory Domain Services-account (AD DS) van de werknemer uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="92793-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="92793-125">Er kunnen echter actieve creditcardtransacties zijn die alsnog moeten worden afgeschreven en terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="92793-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="92793-126">Op de pagina **Creditcardtransacties** kunt u de werknemer opnieuw toewijzen voor elke creditcardtransactie waaruit de gekoppelde werknemer is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="92793-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="92793-127">Selecteer een of meer creditcardtransacties en selecteer vervolgens **Transacties opnieuw toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="92793-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="92793-128">U kunt vervolgens een andere werknemer selecteren aan wie u de creditcardtransacties wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="92793-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="92793-129">Nadat de creditcardtransacties opnieuw zijn toegewezen, kunnen ze worden geselecteerd voor een onkostennota en worden betaald via het gebruikelijke proces voor terugbetaling van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="92793-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]