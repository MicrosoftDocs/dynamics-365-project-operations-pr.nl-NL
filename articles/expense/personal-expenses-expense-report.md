---
title: Werken met persoonlijke onkosten in een onkostendeclaratie
description: Dit onderwerp biedt informatie over het omgaan met persoonlijke onkosten gemaakt door werknemers tijdens zakelijke reizen.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025678"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="c7272-103">Werken met persoonlijke onkosten in een onkostendeclaratie</span><span class="sxs-lookup"><span data-stu-id="c7272-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="c7272-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="c7272-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7272-105">Tijdens zakenreizen kan een werknemer persoonlijke uitgaven in rekening brengen op zijn zakelijke creditcard.</span><span class="sxs-lookup"><span data-stu-id="c7272-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="c7272-106">Als er geen proces is gedefinieerd voor het afhandelen van persoonlijke onkosten, kan het goedkeuringsproces voor onkostendeclaraties worden verstoord wanneer een werknemer zijn gespecificeerde onkostendeclaratie indient.</span><span class="sxs-lookup"><span data-stu-id="c7272-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="c7272-107">Er zijn twee methoden die u kunt gebruiken om met de persoonlijke onkosten van een werknemer te werken:</span><span class="sxs-lookup"><span data-stu-id="c7272-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="c7272-108">**Betaald door werknemer**: uw organisatie betaalt geen persoonlijke onkosten die op de factuur van de zakelijke creditcard staan.</span><span class="sxs-lookup"><span data-stu-id="c7272-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="c7272-109">In plaats daarvan betaalt de werknemer de onkosten rechtstreeks aan de creditcardverstrekker.</span><span class="sxs-lookup"><span data-stu-id="c7272-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="c7272-110">**Betaald door bedrijf**: uw organisatie betaalt de volledige rekening voor de zakelijke creditcard en incasseert deze vervolgens op de rekening van de werknemer voor persoonlijke onkosten.</span><span class="sxs-lookup"><span data-stu-id="c7272-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="c7272-111">U kunt de methode selecteren die uw organisatie gebruikt op de pagina **Parameters onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="c7272-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="c7272-112">Functie voor gesplitste onkosten inschakelen wanneer het veld voor persoonlijk bedrag een waarde heeft</span><span class="sxs-lookup"><span data-stu-id="c7272-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="c7272-113">De functie **Functie voor gesplitste onkosten inschakelen wanneer het veld voor persoonlijk bedrag een waarde heeft** is alleen van toepassing op onkostendeclaraties die zijn goedgekeurd met een werkstroom op regelniveau.</span><span class="sxs-lookup"><span data-stu-id="c7272-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="c7272-114">Declaraties worden goedgekeurd door naar **Onkostendeclaraties verwerken** > **Onkostendeclaraties aan mij toegewezen** > **Onkostendeclaratie** te gaan.</span><span class="sxs-lookup"><span data-stu-id="c7272-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="c7272-115">Als u deze functie wilt inschakelen, gaat u naar **Werkruimten** > **Functiebeheer**, selecteert u **Functie voor gesplitste onkosten inschakelen wanneer het veld voor persoonlijk bedrag een waarde heeft** en selecteert u vervolgens **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="c7272-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="c7272-116">Wanneer de functie is ingeschakeld, genereren onkostenregels die deze functionaliteit gebruiken twee regels wanneer de declaratie wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="c7272-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="c7272-117">Er worden twee regels gegenereerd zodat de fiatteur elke regel afzonderlijk kan goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="c7272-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
