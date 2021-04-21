---
title: Creditcardintegratie instellen
description: In dit onderwerp wordt uitgelegd hoe u kunt werken met onkostengerelateerde creditcardtransacties.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866677"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="4be7c-103">Creditcardintegratie instellen</span><span class="sxs-lookup"><span data-stu-id="4be7c-103">Set up credit card integration</span></span>

<span data-ttu-id="4be7c-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="4be7c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4be7c-105">Onkostengerelateerde creditcardtransacties kunnen zo worden ingesteld dat ze automatisch volgens een terugkerende planning worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="4be7c-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="4be7c-106">U kunt de transacties ook handmatig importeren als u ze nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="4be7c-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="4be7c-107">De creditcardtransacties worden geïmporteerd via de gegevensentiteit voor creditcardtransacties.</span><span class="sxs-lookup"><span data-stu-id="4be7c-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="4be7c-108">Creditcardtransacties importeren</span><span class="sxs-lookup"><span data-stu-id="4be7c-108">Import credit card transactions</span></span>

<span data-ttu-id="4be7c-109">Volg deze stappen om creditcardtransacties te importeren:</span><span class="sxs-lookup"><span data-stu-id="4be7c-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="4be7c-110">Selecteer op de pagina **Creditcardtransacties** de optie **Transacties importeren**.</span><span class="sxs-lookup"><span data-stu-id="4be7c-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="4be7c-111">Als u gegevensbeheer voor het eerst opent, moet het systeem de lijst met gegevensentiteiten bijwerken voordat u verder kunt gaan.</span><span class="sxs-lookup"><span data-stu-id="4be7c-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="4be7c-112">Voer in het veld **Naam** een unieke beschrijving in voor de importtaak.</span><span class="sxs-lookup"><span data-stu-id="4be7c-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="4be7c-113">Selecteer in het veld **Brongegevensindeling** de indeling van het bestand met de creditcardtransacties die u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="4be7c-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="4be7c-114">Selecteer **Uploaden** en selecteer het bestand dat u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="4be7c-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="4be7c-115">Nadat het bestand is geüpload, controleert u de toewijzing van het creditcardtransactiebestand en de kolommen van de gegevensentiteit voor creditcardtransacties door de koppeling **Toewijzing weergeven** op de tegel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="4be7c-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="4be7c-116">Als er toewijzingsfouten zijn, of als u de toewijzing moet wijzigen, brengt u de wijzigingen in de toewijzing aan op het tabblad **Visualisering van toewijzing** of het tabblad **Toewijzingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="4be7c-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="4be7c-117">Selecteer **Terugkerende gegevenstaak maken** om de creditcardtransacties te automatiseren.</span><span class="sxs-lookup"><span data-stu-id="4be7c-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="4be7c-118">U kunt vervolgens het terugkeerpatroon instellen dat bepaalt hoe vaak creditcardtransacties moeten worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="4be7c-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="4be7c-119">Als u klaar bent, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="4be7c-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="4be7c-120">Selecteer **Importeren** om het geselecteerde bestand nu te importeren.</span><span class="sxs-lookup"><span data-stu-id="4be7c-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="4be7c-121">Als er fouten optreden tijdens het importeren, kunt u het uitvoeringslogboek of de faseringsgegevens bekijken om te zien welke fouten u moet oplossen om een succesvolle import te garanderen.</span><span class="sxs-lookup"><span data-stu-id="4be7c-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="4be7c-122">Als u meer dan één bestandsindeling moet importeren, moet u voor elk indelingstype afzonderlijke importtaken maken.</span><span class="sxs-lookup"><span data-stu-id="4be7c-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="4be7c-123">De creditcardtransacties opnieuw toewijzen aan werknemers van wie het dienstverband is beëindigd</span><span class="sxs-lookup"><span data-stu-id="4be7c-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="4be7c-124">Nadat een werknemersrecord is verwijderd, wordt het Active Directory Domain Services-account (AD DS) van de werknemer uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="4be7c-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="4be7c-125">Er kunnen echter actieve creditcardtransacties zijn die alsnog moeten worden afgeschreven en terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="4be7c-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="4be7c-126">Op de pagina **Creditcardtransacties** kunt u de werknemer opnieuw toewijzen voor elke creditcardtransactie waarbij de gekoppelde werknemer is ontslagen.</span><span class="sxs-lookup"><span data-stu-id="4be7c-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="4be7c-127">Selecteer een of meer creditcardtransacties en selecteer vervolgens **Transacties opnieuw toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="4be7c-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="4be7c-128">U kunt vervolgens een andere werknemer selecteren aan wie u de creditcardtransacties wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="4be7c-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="4be7c-129">Nadat de creditcardtransacties opnieuw zijn toegewezen, kunnen ze worden geselecteerd voor een onkostennota en worden betaald via het gebruikelijke proces voor terugbetaling van onkostennota's.</span><span class="sxs-lookup"><span data-stu-id="4be7c-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="4be7c-130">Creditcardtransacties verwijderen</span><span class="sxs-lookup"><span data-stu-id="4be7c-130">Delete credit card transactions</span></span> 

<span data-ttu-id="4be7c-131">Na het importeren van creditcardtransacties moeten bepaalde transacties mogelijk worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="4be7c-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="4be7c-132">Dit kan bijvoorbeeld zo zijn als de transacties duplicaten zijn of omdat de gegevens mogelijk niet correct zijn.</span><span class="sxs-lookup"><span data-stu-id="4be7c-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="4be7c-133">Beheerders kunnen de functie **Creditcardtransacties verwijderen** gebruiken om creditcardtransacties te selecteren en verwijderen die **niet zijn gekoppeld** aan een onkostennota.</span><span class="sxs-lookup"><span data-stu-id="4be7c-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="4be7c-134">Ga naar **Periodieke taken** > **Creditcardtransacties verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="4be7c-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="4be7c-135">Selecteer **Filter** en geef informatie op om de op te nemen records te identificeren.</span><span class="sxs-lookup"><span data-stu-id="4be7c-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="4be7c-136">Als u de records wilt verwijderen, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="4be7c-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
