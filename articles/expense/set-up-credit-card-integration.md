---
title: Creditcardintegratie instellen
description: In dit onderwerp wordt uitgelegd hoe u onkostengerelateerde creditcardtransacties importeert en onderhoudt.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c7971204b485ee7cb222cd9cffdfdfde93dcf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074527"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="f725d-103">Creditcardintegratie instellen</span><span class="sxs-lookup"><span data-stu-id="f725d-103">Set up credit card integration</span></span>

<span data-ttu-id="f725d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="f725d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f725d-105">Onkostengerelateerde creditcardtransacties kunnen zo worden ingesteld dat ze automatisch volgens een terugkerende planning worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="f725d-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="f725d-106">U kunt de transacties ook handmatig importeren als u ze nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="f725d-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="f725d-107">De creditcardtransacties worden geïmporteerd via de gegevensentiteit Creditcardtransacties.</span><span class="sxs-lookup"><span data-stu-id="f725d-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="f725d-108">Creditcardtransacties importeren</span><span class="sxs-lookup"><span data-stu-id="f725d-108">Import credit card transactions</span></span>

1. <span data-ttu-id="f725d-109">Selecteer op de pagina **Creditcardtransacties** de optie **Transacties importeren**.</span><span class="sxs-lookup"><span data-stu-id="f725d-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="f725d-110">Als u gegevensbeheer voor het eerst opent, moet het systeem de lijst met gegevensentiteiten bijwerken voordat u verder kunt gaan.</span><span class="sxs-lookup"><span data-stu-id="f725d-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="f725d-111">Geef een unieke naam voor de importtaak op in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="f725d-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="f725d-112">Selecteer in het veld **Brongegevensindeling** de indeling van het bestand met de creditcardtransacties die u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="f725d-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="f725d-113">Selecteer **Uploaden** en selecteer het bestand dat u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="f725d-113">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="f725d-114">Nadat het bestand is geüpload, controleert u de toewijzing van het creditcardtransactiebestand en de kolommen van de gegevensentiteit Creditcardtransacties door de koppeling **Toewijzing weergeven** op de tegel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f725d-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="f725d-115">Als er toewijzingsfouten zijn, of als u de toewijzing moet wijzigen, brengt u de wijzigingen in de toewijzing aan op het tabblad **Visualisering van toewijzing** of het tabblad **Toewijzingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="f725d-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="f725d-116">Selecteer **Terugkerende gegevenstaak maken** om de creditcardtransacties te automatiseren.</span><span class="sxs-lookup"><span data-stu-id="f725d-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="f725d-117">U kunt vervolgens het terugkeerpatroon instellen dat bepaalt hoe vaak creditcardtransacties moeten worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="f725d-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="f725d-118">Als u klaar bent, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="f725d-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="f725d-119">Selecteer **Importeren** om het geselecteerde bestand nu te importeren.</span><span class="sxs-lookup"><span data-stu-id="f725d-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="f725d-120">Als er fouten optreden tijdens het importeren, kunt u het uitvoeringslogboek of de faseringsgegevens bekijken om de fouten weer te geven die u moet herstellen om het bestand te kunnen importeren.</span><span class="sxs-lookup"><span data-stu-id="f725d-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="f725d-121">Als u meer dan een bestandsindeling moet importeren, moet u voor elk indelingstype een afzonderlijke importtaak maken.</span><span class="sxs-lookup"><span data-stu-id="f725d-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="f725d-122">De creditcardtransacties opnieuw toewijzen aan werknemers van wie het dienstverband is beëindigd</span><span class="sxs-lookup"><span data-stu-id="f725d-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="f725d-123">Nadat een werknemersrecord is verwijderd, wordt het Active Directory Domain Services-account (AD DS) van de werknemer uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f725d-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="f725d-124">Er kunnen echter actieve creditcardtransacties zijn die alsnog moeten worden afgeschreven en terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="f725d-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="f725d-125">Op de pagina **Creditcardtransacties** kunt u de werknemer opnieuw toewijzen voor elke creditcardtransactie waaruit de gekoppelde werknemer is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="f725d-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="f725d-126">Selecteer een of meer creditcardtransacties en selecteer vervolgens **Transacties opnieuw toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="f725d-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="f725d-127">U kunt vervolgens een andere werknemer selecteren aan wie u de creditcardtransacties wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="f725d-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="f725d-128">Nadat de creditcardtransacties opnieuw zijn toegewezen, kunnen ze worden geselecteerd voor een onkostennota en worden betaald via het gebruikelijke proces voor terugbetaling van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="f725d-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
