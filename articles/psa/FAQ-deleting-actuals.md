---
title: Waarom kan ik geen records verwijderen uit de entiteit Werkelijke waarden?
description: In dit onderwerp wordt beschreven waarom u geen records uit de entiteit Werkelijke waarden kunt verwijderen.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286062"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="b6678-103">Waarom kan ik geen records verwijderen uit de entiteit Werkelijke waarden?</span><span class="sxs-lookup"><span data-stu-id="b6678-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b6678-104">In Project Service Automation (PSA) kunt u geen werkelijke waarden verwijderen omdat deze fungeren als de bron van waarheid voor transacties die financiële gevolgen hebben voor downstream-systemen, zoals het grootboek.</span><span class="sxs-lookup"><span data-stu-id="b6678-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="b6678-105">Als werkelijke waarden kunnen worden verwijderd, kan de integriteit van de financiële-rapportagetransacties worden betwist.</span><span class="sxs-lookup"><span data-stu-id="b6678-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="b6678-106">Om een audittrail tot stand te brengen, moeten klanten journalen gebruiken om compenserende transacties te maken.</span><span class="sxs-lookup"><span data-stu-id="b6678-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]