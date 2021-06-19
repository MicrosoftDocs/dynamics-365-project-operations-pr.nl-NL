---
title: Een bestaand veld in Project Service gebruiken als een prijsdimensie
description: Dit onderwerp bevat informatie over het gebruik van bestaande Project Service-velden als prijsdimensies.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008080"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="dec3e-103">Een bestaand veld in Project Service gebruiken als een prijsdimensie</span><span class="sxs-lookup"><span data-stu-id="dec3e-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dec3e-104">Project Service Automation (PSA) heeft veel velden in de entiteit **Werkelijke waarden** die kunnen worden gebruikt als prijsdimensies voor op resources gebaseerde prijzen in projectorganisaties.</span><span class="sxs-lookup"><span data-stu-id="dec3e-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="dec3e-105">Eén algemeen veld is bijvoorbeeld **Boekbare resource**.</span><span class="sxs-lookup"><span data-stu-id="dec3e-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="dec3e-106">Voor kleinere bedrijven met minder dan 20-30 factureerbare resources zijn resourcespecifieke factuur- en kostentarieven mogelijk een eenvoudigere benadering.</span><span class="sxs-lookup"><span data-stu-id="dec3e-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="dec3e-107">Als het aantal factureerbare werknemers toeneemt, kunnen specifieke tarieven onrealistisch worden omdat resourcekosten en factuurtarieven variëren naarmate resources worden bevorderd, meer ervaring opdoen of een andere set vaardigheden verwerven.</span><span class="sxs-lookup"><span data-stu-id="dec3e-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="dec3e-108">Omdat deze benadering nog steeds werkt voor bedrijven met een bepaalde grootte, raadpleegt u [Een boekbare resource gebruiken als een prijsdimensie](bookable-resource-pricing-dimension.md) om te begrijpen hoe een bestaand Project Service-veld kan worden gebruikt als een prijsdimensie.</span><span class="sxs-lookup"><span data-stu-id="dec3e-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="dec3e-109">Een ander voorbeeld is transactiecategorie.</span><span class="sxs-lookup"><span data-stu-id="dec3e-109">Another example is that of transaction category.</span></span> <span data-ttu-id="dec3e-110">Klanten en implementeerders hebben de transactiecategorie in PSA gebruikt voor het classificeren van werk en voor het bepalen van de prijs en kosten op basis van de werkcategorie.</span><span class="sxs-lookup"><span data-stu-id="dec3e-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="dec3e-111">Zie voor meer informatie [Transactiecategorie gebruiken als een prijsdimensie](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="dec3e-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]