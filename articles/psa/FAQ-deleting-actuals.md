---
title: Waarom kan ik geen records verwijderen uit de entiteit Werkelijke waarden?
description: In dit onderwerp wordt beschreven waarom u geen records uit de entiteit Werkelijke waarden kunt verwijderen.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074690"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="6b8ea-103">Waarom kan ik geen records verwijderen uit de entiteit Werkelijke waarden?</span><span class="sxs-lookup"><span data-stu-id="6b8ea-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6b8ea-104">In Project Service Automation (PSA) kunt u geen werkelijke waarden verwijderen omdat deze fungeren als de bron van waarheid voor transacties die financiële gevolgen hebben voor downstream-systemen, zoals het grootboek.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="6b8ea-105">Als werkelijke waarden kunnen worden verwijderd, kan de integriteit van de financiële-rapportagetransacties worden betwist.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="6b8ea-106">Om een audittrail tot stand te brengen, moeten klanten journalen gebruiken om compenserende transacties te maken.</span><span class="sxs-lookup"><span data-stu-id="6b8ea-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

