---
title: Integratie van twee keer wegschrijven in Project Operations
description: Dit onderwerp geeft een overzicht van integratie van twee keer wegschrijven in Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998675"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="18900-103">Overzicht van integratie van twee keer wegschrijven in Project Operations</span><span class="sxs-lookup"><span data-stu-id="18900-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="18900-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="18900-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="18900-105">Project Operations gebruikt [mogelijkheden voor twee keer wegschrijven](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) om gegevens te synchroniseren tussen Microsoft Dataverse en Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="18900-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="18900-106">De volgende afbeelding laat zien hoe gegevens worden gesynchroniseerd als onderdeel van deze integratie tussen Dataverse en Finance.</span><span class="sxs-lookup"><span data-stu-id="18900-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Overzicht van gegevensstromen in Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="18900-108">Project Operations in Dataverse biedt een moderne gebruikersinterface (UI) en eenvoudige uitbreidbaarheid zonder code/met weinig code met behulp van Power Platform-mogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="18900-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="18900-109">Projectmanagers, resourcemanagers, projectteamleden en andere frontoffice-persona's voeren hun activiteiten uit in Project Operations op Dataverse.</span><span class="sxs-lookup"><span data-stu-id="18900-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="18900-110">Project Operations in Finance biedt ondersteuning voor projectadministratie en opbrengstentoerekening.</span><span class="sxs-lookup"><span data-stu-id="18900-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="18900-111">Project Operations wordt aangesloten op het financiële raamwerk in Finance voor het berekenen van omzetbelasting, valutakoersen, rapportage van financiële dimensies en meer.</span><span class="sxs-lookup"><span data-stu-id="18900-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="18900-112">De ervaringen van de projectaccountant zijn voornamelijk gebaseerd op Finance.</span><span class="sxs-lookup"><span data-stu-id="18900-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="18900-113">Project Operations-integratie bestaat uit de volgende onderdeelintegratie:</span><span class="sxs-lookup"><span data-stu-id="18900-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="18900-114">Integratie van instellings- en configuratiegegevens in Project Operations</span><span class="sxs-lookup"><span data-stu-id="18900-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="18900-115">Projectschattingen en werkelijke waarden</span><span class="sxs-lookup"><span data-stu-id="18900-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="18900-116">Projectfacturen</span><span class="sxs-lookup"><span data-stu-id="18900-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="18900-117">Onkostenbeheer</span><span class="sxs-lookup"><span data-stu-id="18900-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="18900-118">Leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="18900-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
