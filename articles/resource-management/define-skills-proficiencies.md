---
title: Vaardigheden en deskundigheden definiëren
description: Dit onderwerp bevat informatie over het instellen van deskundigheidsmodellen om resources te beoordelen.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279672"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="b13b6-103">Vaardigheden en deskundigheden definiëren</span><span class="sxs-lookup"><span data-stu-id="b13b6-103">Define skills and proficiencies</span></span>

<span data-ttu-id="b13b6-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="b13b6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b13b6-105">Vaardigheden zijn resourcekenmerken die worden gedeeld tussen Dynamics 365 Project Operations en Dynamics 365 Field Service (indien aanwezig).</span><span class="sxs-lookup"><span data-stu-id="b13b6-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="b13b6-106">Voor onderhoud van de opslagplaats van vaardigheden in Project Operations gaat u naar **Resources** \> **Resourcevaardigheden**.</span><span class="sxs-lookup"><span data-stu-id="b13b6-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="b13b6-107">Resources beoordelen met deskundigheidsmodellen</span><span class="sxs-lookup"><span data-stu-id="b13b6-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="b13b6-108">Vaardigheden voor resources worden beoordeeld door middel van deskundigheidsmodellen.</span><span class="sxs-lookup"><span data-stu-id="b13b6-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="b13b6-109">De individuele beoordelingen zijn in een deskundigheidsmodel.</span><span class="sxs-lookup"><span data-stu-id="b13b6-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="b13b6-110">Als u een deskundigheidsmodel wilt maken, gaat u naar **Resources** \> **Deskundigheidsmodellen** en selecteert u hier **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="b13b6-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="b13b6-111">Geef in het nieuwe beoordelingsmodel de minimale beoordelingswaarde, de maximale beoordelingswaarde en de entiteit op die wordt beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="b13b6-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="b13b6-112">In het subraster **Beoordelingswaarden** kunt u de verschillende beoordelingswaarden definiëren, van het minimum tot het maximum.</span><span class="sxs-lookup"><span data-stu-id="b13b6-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="b13b6-113">Deze beoordelingswaarden worden weergegeven in de filters **Resourcevereisten**, **Planbord** en **Planningsassistent**.</span><span class="sxs-lookup"><span data-stu-id="b13b6-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]