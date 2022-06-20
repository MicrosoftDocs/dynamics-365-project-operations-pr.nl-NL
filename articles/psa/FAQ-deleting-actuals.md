---
title: Waarom kan ik geen records verwijderen uit de entiteit Werkelijke waarden?
description: In dit artikel wordt beschreven waarom u geen records uit de entiteit Werkelijke waarden kunt verwijderen.
author: JPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925574"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Waarom kan ik geen records verwijderen uit de entiteit Werkelijke waarden?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Project Service Automation (PSA) kunt u geen werkelijke waarden verwijderen omdat deze fungeren als de bron van waarheid voor transacties die financiële gevolgen hebben voor downstream-systemen, zoals het grootboek. Als werkelijke waarden kunnen worden verwijderd, kan de integriteit van de financiële-rapportagetransacties worden betwist. Om een audittrail tot stand te brengen, moeten klanten journalen gebruiken om compenserende transacties te maken.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
