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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127152"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="90337-103">Waarom kan ik geen records verwijderen uit de entiteit Werkelijke waarden?</span><span class="sxs-lookup"><span data-stu-id="90337-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90337-104">In Project Service Automation (PSA) kunt u geen werkelijke waarden verwijderen omdat deze fungeren als de bron van waarheid voor transacties die financiële gevolgen hebben voor downstream-systemen, zoals het grootboek.</span><span class="sxs-lookup"><span data-stu-id="90337-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="90337-105">Als werkelijke waarden kunnen worden verwijderd, kan de integriteit van de financiële-rapportagetransacties worden betwist.</span><span class="sxs-lookup"><span data-stu-id="90337-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="90337-106">Om een audittrail tot stand te brengen, moeten klanten journalen gebruiken om compenserende transacties te maken.</span><span class="sxs-lookup"><span data-stu-id="90337-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

