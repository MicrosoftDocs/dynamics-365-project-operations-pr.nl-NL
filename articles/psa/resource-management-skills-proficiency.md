---
title: Vaardigheids- en deskundigheidsmodellen
description: Dit onderwerp biedt informatie over het gebruik van de modellen voor vaardigheden en deskundigheid.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 82eeab4c9682e5b777da4e66f6c4f3f1afb3c19b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282957"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="9a080-103">Vaardigheids- en deskundigheidsmodellen</span><span class="sxs-lookup"><span data-stu-id="9a080-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9a080-104">Vaardigheden zijn resourcekenmerken die worden gedeeld tussen Dynamics 365 Project Service Automation en Dynamics 365 Field Service (indien aanwezig).</span><span class="sxs-lookup"><span data-stu-id="9a080-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="9a080-105">Voor onderhoud van de opslagplaats van vaardigheden in Project Service Automation gaat u naar **Resources** \> **Resourcevaardigheden**.</span><span class="sxs-lookup"><span data-stu-id="9a080-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Resourcevaardigheden](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="9a080-107">Resources beoordelen met deskundigheidsmodellen</span><span class="sxs-lookup"><span data-stu-id="9a080-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="9a080-108">Vaardigheden voor resources worden beoordeeld door middel van deskundigheidsmodellen.</span><span class="sxs-lookup"><span data-stu-id="9a080-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="9a080-109">De individuele beoordelingen zijn in een deskundigheidsmodel.</span><span class="sxs-lookup"><span data-stu-id="9a080-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="9a080-110">Als u een deskundigheidsmodel wilt maken, gaat u naar **Resources** \> **Deskundigheidsmodellen** en selecteert u hier **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9a080-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="9a080-111">Geef in het nieuwe beoordelingsmodel de minimale beoordelingswaarde, de maximale beoordelingswaarde en de entiteit op die wordt beoordeeld.</span><span class="sxs-lookup"><span data-stu-id="9a080-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="9a080-112">In het subraster **Beoordelingswaarden** kunt u de verschillende beoordelingswaarden definiëren, van het minimum tot het maximum.</span><span class="sxs-lookup"><span data-stu-id="9a080-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Minimale en maximale beoordelingen gedefinieerd](media/Resource-Management-image85.png)

<span data-ttu-id="9a080-114">Deze beoordelingswaarden worden weergegeven in de filters **Resourcevereisten**, **Planbord** en **Planningsassistent**.</span><span class="sxs-lookup"><span data-stu-id="9a080-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]