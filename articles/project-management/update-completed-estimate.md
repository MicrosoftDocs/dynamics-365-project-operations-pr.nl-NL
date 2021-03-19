---
title: Schatting bij voltooiing bijwerken
description: Dit onderwerp bevat informatie over het bijwerken van de prognose van inspanning voor project.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286422"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="4ed6e-103">Schatting bij voltooiing bijwerken</span><span class="sxs-lookup"><span data-stu-id="4ed6e-103">Update estimate at completion</span></span>

<span data-ttu-id="4ed6e-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="4ed6e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ed6e-105">Het is gebruikelijk voor een projectbeheerder om de oorspronkelijke schattingen voor een taak te herzien.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="4ed6e-106">Herziene prognoses vormen de perceptie van een projectmanager van de schattingen op basis van de huidige status van een project.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="4ed6e-107">We raden projectbeheerders echter niet aan om de baseline-cijfers aan te passen, omdat de project-baseline de vastgestelde 'bron van waarheid' vertegenwoordigt voor de planning en kostenraming voor het project die door alle belanghebbenden van het project is geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="4ed6e-108">Er zijn twee manieren waarop een projectmanager een nieuwe prognose van de inspanning voor taken kan maken:</span><span class="sxs-lookup"><span data-stu-id="4ed6e-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="4ed6e-109">De projectbeheerder kan de standaard-ETC (Estimate To Complete, geschatte voltooiingstijd) vervangen door een nieuwe schatting van de werkelijke resterende inspanning voor de taak.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="4ed6e-110">De projectbeheerder kan het standaardvoortgangspercentage vervangen door een nieuwe schatting van de werkelijke voortgang voor de taak.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="4ed6e-111">Bij elk van deze benaderingen worden de ETC, de EAC, het voortgangspercentage en de verwachte inspanningsafwijking voor een taak opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="4ed6e-112">De EAC, ETC en het voortgangspercentage voor de overzichtstaken worden opnieuw berekend en leveren een nieuwe prognose van de inspanningsafwijking op.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]