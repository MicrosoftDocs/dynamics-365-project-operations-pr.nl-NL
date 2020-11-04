---
title: Project Operations-velden als prijsdimensies
description: Dit onderwerp bevat informatie over het gebruik van velden als prijsdimensies in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074627"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="6fb5f-103">Project Operations-velden als prijsdimensies</span><span class="sxs-lookup"><span data-stu-id="6fb5f-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="6fb5f-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="6fb5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6fb5f-105">De entiteit **Werkelijke waarden** heeft veel velden die kunnen worden gebruikt als prijsdimensies voor prijzen op basis van resources.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="6fb5f-106">Eén algemeen veld is bijvoorbeeld **Boekbare resource**.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="6fb5f-107">Voor kleinere bedrijven met minder dan 20-30 factureerbare resources zijn resourcespecifieke factuur- en kostentarieven mogelijk een eenvoudigere benadering.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="6fb5f-108">Als het aantal factureerbare werknemers echter toeneemt, kan dit echter onrealistisch worden.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="6fb5f-109">De resourcekosten en factuurtarieven variëren naarmate resources worden bevorderd, meer ervaring opdoen of andere vaardigheden verwerven.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="6fb5f-110">Een ander voorbeeld is transactiecategorie.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-110">Another example is that of transaction category.</span></span> <span data-ttu-id="6fb5f-111">Klanten en uitvoerders hebben de transactiecategorie gebruikt voor het classificeren van werk en voor het bepalen van de prijs en kosten op basis van de werkcategorie.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
