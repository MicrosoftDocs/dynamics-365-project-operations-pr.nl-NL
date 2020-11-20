---
title: Verkoopprijslijsten voor project overschrijven
description: Dit onderwerp bevat informatie over het maken van aangepaste verkoopprijslijsten.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130842"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="17120-103">Verkoopprijslijsten voor project overschrijven</span><span class="sxs-lookup"><span data-stu-id="17120-103">Override project sales price lists</span></span>

<span data-ttu-id="17120-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="17120-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="17120-105">Klantspecifieke projectprijslijsten</span><span class="sxs-lookup"><span data-stu-id="17120-105">Customer-specific project price lists</span></span>

<span data-ttu-id="17120-106">Klantspecifieke prijsafspraken kunnen worden ingesteld als projectprijslijsten op een accountrecord in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="17120-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="17120-107">Als u een klantspecifieke projectprijslijst wilt instellen, gaat u in het gebied **Verkoop** naar de accountrecord.</span><span class="sxs-lookup"><span data-stu-id="17120-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="17120-108">Open de lijstpagina **Accounts**.</span><span class="sxs-lookup"><span data-stu-id="17120-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="17120-109">Zoek en dubbelklik op een klantrecord om de detailpagina **Account** te openen.</span><span class="sxs-lookup"><span data-stu-id="17120-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="17120-110">Selecteer op het tabblad **Projectprijslijsten** \*\*+ Nieuwe projectprijslijst^^.</span><span class="sxs-lookup"><span data-stu-id="17120-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="17120-111">Op de pagina **Nieuwe projectprijslijst** selecteert u een prijslijst in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="17120-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="17120-112">Alleen prijslijsten waarvoor de context is ingesteld op **Verkoop** en waarvan de valuta overeenkomt met de accountvaluta zijn inbegrepen.</span><span class="sxs-lookup"><span data-stu-id="17120-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="17120-113">Geef de koppeling een naam en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="17120-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="17120-114">Er wordt een klantspecifieke projectprijslijst gemaakt.</span><span class="sxs-lookup"><span data-stu-id="17120-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="17120-115">Deze prijslijst wordt gebruikt om de standaardprojectprijzen te gebruiken voor projectoffertes of contracten die voor deze klant zijn gemaakt, waarbij de aanmaakdatum van de offerte of het projectcontract binnen de geldigheidsperiode van de prijslijst valt.</span><span class="sxs-lookup"><span data-stu-id="17120-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="17120-116">Aangepaste prijzen voor projectoffertes</span><span class="sxs-lookup"><span data-stu-id="17120-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="17120-117">Voor projectoffertes kunt u projectprijzen gebruiken die beginnen met een standaardprijslijst van de klant of de projectparameters.</span><span class="sxs-lookup"><span data-stu-id="17120-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="17120-118">Als u aangepaste prijzen nodig hebt voor projectgerelateerd werk aan een bepaalde offerte, kunt u deze vinden in de projectprijslijsten van de bijbehorende entiteit.</span><span class="sxs-lookup"><span data-stu-id="17120-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="17120-119">Voer de volgende stappen uit om offertespecifieke projectprijzen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="17120-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="17120-120">Open de projectofferte en selecteer het tabblad **Projectprijslijsten**.</span><span class="sxs-lookup"><span data-stu-id="17120-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="17120-121">Selecteer **Aangepaste prijzen maken** in het subraster.</span><span class="sxs-lookup"><span data-stu-id="17120-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="17120-122">Alle projectprijslijsten die bij de offerte zijn gevoegd, worden gekopieerd naar nieuwe prijslijsten.</span><span class="sxs-lookup"><span data-stu-id="17120-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="17120-123">De namen van de nieuwe prijslijsten weerspiegelen de naam van de offerte met een datum-tijdstempel voor wanneer deze prijslijsten zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="17120-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="17120-124">U kunt elk van deze prijslijsten gebruiken en de prijzen voor arbeid (rolprijs) en onkosten (categorieprijs) bijwerken.</span><span class="sxs-lookup"><span data-stu-id="17120-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="17120-125">Deze gewijzigde prijzen zijn alleen van toepassing op deze projectofferte.</span><span class="sxs-lookup"><span data-stu-id="17120-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="17120-126">Prijslijsten voor een projectcontract</span><span class="sxs-lookup"><span data-stu-id="17120-126">Price lists on a project contract</span></span>

<span data-ttu-id="17120-127">Bij een projectcontract wordt de projectprijs altijd standaard ingesteld als een aangepaste prijslijst met de naam van het contract en de aangemaakte datum-tijdstempel toegevoegd aan de naam.</span><span class="sxs-lookup"><span data-stu-id="17120-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="17120-128">Dit geldt ongeacht of het contract is gemaakt toen de offerte werd gewonnen of dat het contract helemaal opnieuw is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="17120-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="17120-129">Indien nodig kunt u deze koppeling met de aangepaste prijslijst verwijderen en in plaats daarvan een standaardprijslijst aan het projectcontract koppelen.</span><span class="sxs-lookup"><span data-stu-id="17120-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="17120-130">Wanneer u een standaardprijslijst koppelt aan de projectprijslijsten in de offerte of het contract, hebben eventuele wijzigingen in de prijzen in de prijslijst invloed op alle offertes en contracten die de prijslijst gebruiken.</span><span class="sxs-lookup"><span data-stu-id="17120-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
