---
title: Veelgestelde vragen over resourcebeheer
description: Dit artikel biedt antwoorden op veelgestelde vragen over resourcebeheer.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 6610098737b79d76b38c3d467135b9118c2a8ec7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913338"
---
# <a name="resource-management-faq"></a>Veelgestelde vragen over resourcebeheer

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Wat is het verschil tussen een teamlid en een resourcevereiste?

Een projectteamlid kan worden toegewezen aan taken, geboekt of overboekt, en ingesteld als een fiatteur. Een resourcevereiste kan bestaan zonder een projectteamlid, als conceptnotitie van de vraag. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Wat is het verschil tussen voorgestelde uren en zacht geboekte uren?

Voorgestelde uren en zacht geboekte uren verschillen in zichtbaarheid. Voorgestelde uren zijn alleen zichtbaar voor resourcemanagers en de projectmanager die de vraag heeft geïnitieerd door middel van een resourceaanvraag. Zacht geboekte uren zijn zichtbaar voor iedereen die toegang heeft tot het planbord.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Hoe kan ik de zacht geboekte uren voor resources in een team bekijken?

Zachte boekingen kunnen worden gemaakt wanneer u een resourcevereiste boekt. Resources die zacht zijn geboekt in een projectteam, worden weergegeven als teamleden met zacht geboekte uren. Ze worden ook weergegeven op het planbord.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Hoe wijzig ik de vereiste uren en de begin- en einddatums voor een resource (algemeen of benoemd) die ik heb geboekt?

Nadat de resources zijn geboekt, selecteert u **Boekingen bijhouden** om de vereiste wijzigingen aan te brengen.

## <a name="what-resources-types-does-project-service-automation-support"></a>Welke resourcetypen ondersteunt Project Service Automation?

**Gebruiker** en **Contactpersoon** zijn de enige resourcetypen die worden ondersteund in Dynamics 365 Project Service Automation. Hoewel u andere typen resources kunt maken (bijvoorbeeld **Apparatuur** en **Groep**), worden er geen end-to-end gebruiksscenario's voor ondersteund.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Wat is het verschil tussen een toewijzing en een boeking?

Toewijzingen zijn de toewijzing van resources aan projecttaken in de projectplanning. De resources kunnen echte resources zijn of algemene resources. Boekingen zijn de harde of zachte toewijzing van resources aan een project. Een harde boeking verbruikt de capaciteit van een resource. In het ideale geval moeten voor echte resources de boekingen en toewijzingen overeenkomen, omdat ze niet verschillen. PSA dwingt deze overeenkomst echter niet af. In de weergave Vereffening wordt aan een projectmanager getoond waar boekingen en toewijzingen van een resource niet overeenkomen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
