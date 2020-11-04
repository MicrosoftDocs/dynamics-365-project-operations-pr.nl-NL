---
title: Wijzigingen op het gebied van resourcebeheer (Project Service Automation 3.x)
description: Dit onderwerp biedt informatie over de wijzigingen op het gebied van resourcebeheer.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074755"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Wijzigingen op het gebied van resourcebeheer (Project Service Automation 3.x)

De secties van dit onderwerp bevatten informatie over de wijzigingen die zijn doorgevoerd in het resourcebeheer-deel van Dynamics 365 Project Service Automation versie 3.x.

## <a name="project-estimates"></a>Projectschattingen

Projectschattingen zijn nu niet meer gebaseerd op de entiteit **msdyn\_projecttask** ( **Projecttaak** ), maar op de entiteit **msdyn\_resourceassignment** ( **Resourcetoewijzing** ). Resourcetoewijzingen zijn de 'bron van waarheid' geworden voor taakplanning en prijzen.

## <a name="line-tasks"></a>Regeltaken

In PSA 3.x zijn lijntaken verouderd (afgeschaft). Toewijzingen verwijzen nu naar de gehele taak in plaats van naar de regeltaken.

In het volgende voorbeeld ziet u hoe een taak met de naam Testtaak wordt toegewezen aan de teamleden A en B in eerdere versies van PSA en in PSA 3.x.

- **Vóór PSA 3.x:**

    - Testtaak

        - Testtaak – regeltaak 1

            - Toewijzing aan A

        - Testtaak – regeltaak 2

            - Toewijzing aan B

- **PSA 3.x:**

    - Testtaak

        - Toewijzing aan A
        - Toewijzing aan B

## <a name="unassigned-assignment"></a>Niet-toegewezen toewijzing

In PSA 3.x is een niet-toegewezen toewijzing een toewijzing die is toegewezen aan een **NULL** -teamlid en een **NULL** -resource. Niet-toegewezen toewijzingen kunnen in een aantal scenario's optreden:

- Als een taak is gemaakt maar nog niet is toegewezen aan een teamlid, wordt altijd een niet-toegewezen toewijzing gemaakt. 
- Als alle toegewezen gebruikers van een taak worden verwijderd, wordt een niet-toegewezen toewijzing voor die taak opnieuw gemaakt.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Planningsvelden in de entiteit Projecttaak

De velden in de entiteit **msdyn\_projecttask** zijn afgeschaft of verplaatst naar de entiteit **msdyn\_resourceassignment** , of er wordt nu naar verwezen vanuit de entiteit **msdyn\_projectteam** ( **Projectteamlid** ).

| Afgeschaft veld op msdyn\_projecttask (Projecttaak) | Nieuw veld op msdyn\_resourceassignment (Resourcetoewijzing) | Opmerking |
|---|---|---|
| msdyn\_assignedresources | Geen | |
| msdyn\_assignedteammembers | Geen | |
| msdyn\_numberofresources | Geen | |
| msdyn\_scheduledhours | Geen | |
| msdyn\_effortcontour | msdyn\_plannedwork | De indeling van de gegevensstructuur JavaScript Object Notation (JSON) die is opgeslagen in het veld, is gewijzigd. |

## <a name="schedule-contour"></a>Planningscontour

De planningscontour is opgeslagen in het veld **Gepland werk** ( **\_msdyn plannedwork** ) van elke entiteit van het type **Resourcetoewijzing** ( **\_msdyn ResourceAssignment** ).

### <a name="structure"></a>Structuur

De nieuwe structuur van de planningscontour bestaat uit flexibele tijdsegmenten die voor elke dag van de planning zijn gedefinieerd. Elke tijdsectie heeft de volgende eigenschappen:

- **Begin** : het begin van de werkuren voor de dag, volgens de projectagenda.
- **Eind** : het einde van de werkuren voor de dag, volgens de projectagenda.
- **Uren** : het aantal uren dat is toegewezen op de dag.

**Voorbeeld**

In dit voorbeeld wordt een projectagenda gebruikt waarin de werkdag loopt van 9 uur tot 17 uur in de tijdzone UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatisch plannen en handmatig plannen

Als een taak automatisch wordt gepland, worden de uren vooraf geladen en kan de duur van de taak worden verminderd.

**Voorbeeld**

De volgende taak wordt automatisch gepland voor 18 uur gedurende drie dagen (3 december 2018 tot en met 5 december 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Als een taak handmatig wordt gepland, worden de uren gelijkmatig verdeeld over alle datums.

**Voorbeeld**

De volgende taak wordt handmatig gepland voor 18 uur gedurende drie dagen (3 december 2018 tot en met 5 december 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Toewijzingseenheid

De toewijzingseenheid is afgeschaft in PSA 3.x. De inspanningsuren van een taak worden nu gelijkelijk verdeeld, per dag, tussen alle toegewezen resources.

**Voorbeeld**

In dit voorbeeld wordt de taak toegewezen aan twee resources en automatisch gepland voor 36 uur gedurende drie dagen (3 december 2018 tot en met 5 december 2018).

- Toewijzing 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Toewijzing 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Prijsdimensies

In PSA 3.x zijn resourcespecifieke dimensievelden voor prijzen (zoals **Rol** en **Organisatie-eenheid** ) verwijderd uit de entiteit **msdyn\_projecttask**. Deze velden kunnen nu worden opgehaald uit het bijbehorende projectteamlid ( **msdyn\_projectteam** ) van de resourcetoewijzing ( **msdyn\_resourceassignment** ) wanneer projectschattingen worden gegenereerd. Er is een nieuw veld, **msdyn\_organizationalunit** , toegevoegd aan de entiteit **msdyn\_projectteam**.

| Afgeschaft veld op msdyn\_projecttask (Projecttaak) | Veld van msdyn\_projectteam (Projectteamlid) dat in plaats daarvan wordt gebruikt |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Contouren

De contourvelden voor prijzen en schattingen zijn afgeschaft voor de entiteit **msdyn\_projecttask**. Ze zijn verplaatst naar de entiteit **msdyn\_resourceassignment**.

| Afgeschaft veld op msdyn\_projecttask (Projecttaak) | Nieuw veld op msdyn\_resourceassignment (Resourcetoewijzing) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

De volgende velden zijn toegevoegd aan de entiteit **msdyn\_resourceassignment** :

* msdyn\_plannedcost
* msdyn\_plannedsales

De volgende velden voor geplande, werkelijke en resterende kosten en verkopen zijn niet veranderd voor de entiteit **msdyn\_projecttask** :

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
