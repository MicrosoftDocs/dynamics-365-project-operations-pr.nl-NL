---
title: Vaardigheids- en deskundigheidsmodellen
description: Dit onderwerp biedt informatie over het gebruik van de modellen voor vaardigheden en deskundigheid.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074784"
---
# <a name="skills-and-proficiency-models"></a>Vaardigheids- en deskundigheidsmodellen

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vaardigheden zijn resourcekenmerken die worden gedeeld tussen Dynamics 365 Project Service Automation en Dynamics 365 Field Service (indien aanwezig). 

Voor onderhoud van de opslagplaats van vaardigheden in Project Service Automation gaat u naar **Resources** \> **Resourcevaardigheden**. 

> ![Resourcevaardigheden](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Resources beoordelen met deskundigheidsmodellen

Vaardigheden voor resources worden beoordeeld door middel van deskundigheidsmodellen. De individuele beoordelingen zijn in een deskundigheidsmodel. 

1. Als u een deskundigheidsmodel wilt maken, gaat u naar **Resources** \> **Deskundigheidsmodellen** en selecteert u hier **Nieuw**.
2. Geef in het nieuwe beoordelingsmodel de minimale beoordelingswaarde, de maximale beoordelingswaarde en de entiteit op die wordt beoordeeld.
3. In het subraster **Beoordelingswaarden** kunt u de verschillende beoordelingswaarden definiëren, van het minimum tot het maximum.

> ![Minimale en maximale beoordelingen gedefinieerd](media/Resource-Management-image85.png)

Deze beoordelingswaarden worden weergegeven in de filters **Resourcevereisten** , **Planbord** en **Planningsassistent**.