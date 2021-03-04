---
title: Onkostenoverzicht
description: Dit onderwerp biedt informatie over de functionaliteit voor onkosten in Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764903"
---
# <a name="expense-home-page"></a><span data-ttu-id="e72c4-103">Startpagina voor onkosten</span><span class="sxs-lookup"><span data-stu-id="e72c4-103">Expense home page</span></span>

<span data-ttu-id="e72c4-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="e72c4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e72c4-105">Dynamics 365 Project Operations ondersteunt de mogelijkheid om onkosten te verwerken.</span><span class="sxs-lookup"><span data-stu-id="e72c4-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="e72c4-106">Onkostenverwerking vindt plaats met of zonder projecten door gebruik te maken van een aanpasbare werkstroom van beleidsregels, transactiecategorieën en goedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="e72c4-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="e72c4-107">In Project Operations zijn er twee ondersteunde implementatiemodellen voor onkosten:</span><span class="sxs-lookup"><span data-stu-id="e72c4-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="e72c4-108">**Volledig**: een volledige implementatie is beschikbaar voor **Project Operations voor scenario's op basis van resources/niet-voorradige artikelen** of **Project Operations voor scenario's op basis van productieorders**.</span><span class="sxs-lookup"><span data-stu-id="e72c4-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="e72c4-109">**Basis**: een basisimplementatie is beschikbaar voor **Project Operations voor scenario's op basis van resources/niet-voorradige artikelen** en **Lite-implementatie – van deal tot pro-formafacturering**.</span><span class="sxs-lookup"><span data-stu-id="e72c4-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="e72c4-110">Volledig</span><span class="sxs-lookup"><span data-stu-id="e72c4-110">Full</span></span> 
<span data-ttu-id="e72c4-111">Volledige implementatie van onkosten biedt een volledige handhaving van beleid, inclusief de mogelijkheid om beleid te maken, zoals:</span><span class="sxs-lookup"><span data-stu-id="e72c4-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="e72c4-112">Onkostencategorielimieten</span><span class="sxs-lookup"><span data-stu-id="e72c4-112">Expense category limits</span></span>
  - <span data-ttu-id="e72c4-113">Op reis</span><span class="sxs-lookup"><span data-stu-id="e72c4-113">Travel</span></span>
  - <span data-ttu-id="e72c4-114">Per diem</span><span class="sxs-lookup"><span data-stu-id="e72c4-114">Per diem</span></span>
  - <span data-ttu-id="e72c4-115">Imports van creditcards</span><span class="sxs-lookup"><span data-stu-id="e72c4-115">Credit card imports</span></span>
  - <span data-ttu-id="e72c4-116">Optische tekenherkenning (OCR) voor betalingsbewijzen</span><span class="sxs-lookup"><span data-stu-id="e72c4-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="e72c4-117">Basis</span><span class="sxs-lookup"><span data-stu-id="e72c4-117">Basic</span></span> 
<span data-ttu-id="e72c4-118">Met het implementatiescenario Basisonkosten kunt u alleen basisonkosten voor een project registreren.</span><span class="sxs-lookup"><span data-stu-id="e72c4-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="e72c4-119">Zie voor meer informatie [Onkostenpost (Lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="e72c4-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="e72c4-120">Uw type implementatie van Onkosten bepalen</span><span class="sxs-lookup"><span data-stu-id="e72c4-120">Determine your Expense deployment</span></span>
<span data-ttu-id="e72c4-121">Om te bepalen of u de beheerimplementatie Basisonkosten uitvoert, controleert u of de adres-URL eindigt op **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="e72c4-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
