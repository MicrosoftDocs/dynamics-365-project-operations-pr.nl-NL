---
title: Een nieuw project maken
description: Dit onderwerp bevat informatie over het maken van een nieuw project.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074699"
---
# <a name="create-a-new-project"></a>Een nieuw project maken

[!include [banner](../includes/banner.md)]

Voer de volgende stappen uit om een nieuw project te maken.

1. Selecteer op de pagina **Projectmanagement** de optie **Nieuw project** en voer de volgende waarden in:

    - **Projecttype:** Tijd en materiaal
    - **Naam van project:** XYZ-upgrade fase 2
    - **Projectgroep:** TM\_WIP
    - **Projectcontract-id:** 00000002

2. Selecteer **Project maken**.

## <a name="assign-a-resource-to-a-project"></a>Een resource toewijzen aan een project

1. Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de record voor de werknemer voor wie u eerder competenties hebt ingesteld en open de werknemerrecord.
2. Ga naar het actievenster op het tabblad **Project** en selecteer in de groep **Instelling** de optie **Projecten toewijzen**.
3. Filter op de pagina **Projectopdrachten voor resourcevalidatie** , op het tabblad **Projecten** , in het veld **Het project toevoegen aan geselecteerde projecten** , op het project **XYZ-upgrade fase 2**.
4. Selecteer in het deelvenster **Resterende projecten** een project en selecteer vervolgens de pijlknop om het toe te voegen aan het deelvenster **Geselecteerde projecten**.

U kunt desgewenst ook categorieën aan een resource toewijzen. Het categorietype is **Kosten** of **Omzet**. Het categorietype wordt bepaald door uw organisatie. Als er geen categorieën zijn toegewezen aan een resource, zoekt Finance de standaardcategorie voor uurprijzen voor kosten en omzet.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projectresource- en rolkenmerken instellen

Een projectmanager kan de functionaliteit voor het toewijzen van resources aan projecten gebruiken om de rollen te creëren die nodig zijn voor het project. Rollen kunnen worden gebruikt als bevestigde resources nog onbekend zijn bij het reserveren van resources. Rollen kunnen tijdelijk worden gereserveerd als geplande resources, zodat u kunt doorgaan met de projectplanningsfasen.

[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso is ingehuurd om een tijd- en materiaalproject uit te voeren met een goedgekeurd projectcharter. De junior projectmanager is nog bezig met het afronden van het bereik van het project. De resourcemanager identificeert momenteel specifieke resources die zullen worden gereserveerd om aan het nieuwe project te werken. Vanwege de cruciale aard van het project heeft de projectsponsor de senior projectmanager gevraagd een van de rollen op zich te nemen. De resourcemanager moet de nieuwe resource verwerven en de rol in het systeem definiëren voor het geval de junior projectmanager de resourcegegevens nodig heeft tijdens de projectplanning.

De volgende stappen laten zien hoe de resourcemanager de rol van senior projectmanager kan instellen en hieraan resourcekenmerken kan koppelen. Later kan de rol worden gebruikt om te zoeken naar beschikbare resources die passen bij de vereiste resourcecompetenties.

1. Selecteer op de pagina **Rollen instellen** de optie **Nieuw** en voer de volgende waarden in:

    - **Rol-id:** Senior projectmanager
    - **Beschrijving:** Senior projectmanager

2. Selecteer **Maken**.
3. Selecteer de rol **Senior projectmanager** en selecteer vervolgens **Kenmerken configureren**.
4. Selecteer in het veld **Kenmerktype** de optie **Vaardigheid**.
5. Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u wilt zoeken.
6. Selecteer in het veld **Kenmerktype** de optie **Certificaat**.
7. Voer in het veld **Beschikbare kenmerken** het certificaattype in waarnaar u wilt zoeken.

## <a name="assign-a-project-resource-to-a-project"></a>Een projectresource toewijzen aan een project

1. Selecteer op de pagina **Alle projecten** het project **XYZ-upgrade fase 2**.
2. Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.
3. Selecteer in het veld **Rol** de optie **Teamlid**.
4. Selecteer **Boeken vanuiit agenda**.
5. Selecteer op de pagina **Beschikbaarheid van resources** de optie **Instellingen weergeven**.
6. Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:

    - **Indeling voor datumbereikweergave:** Dag
    - **Beschrijvingen van beschikbaarheid weergeven:** Ja
    - **Resterende capaciteit weergeven:** Ja

7. Selecteer een resource in de lijst met resources.
8. Selecteer **Hard boeken** en **Volledige capaciteit**.

## <a name="assign-a-resource-to-a-default-role"></a>Een standaardrol aan een resource toewijzen

Als hulpmiddel voor project- of resourcemanagers kan verder worden ingezoomd op de resources die kunnen worden gereserveerd voor een project. U kunt een standaardrol koppelen aan een bestaande resource of een nieuw verworven resource. Toen Daniel bijvoorbeeld werd aangenomen, had hij de ervaring en vaardigheden om de rol van bedrijfsanalist te vervullen. De resourcemanager heeft deze rol als standaardrol toegewezen aan Daniel. Daarom heeft de resourcemanager Daniel toegevoegd aan een pool van bedrijfsanalisten die beschikbaar zijn om aan projecten te werken.

Tijdens het reserveren van resources kunnen projectmanagers de rolresources filteren die beschikbaar zijn om aan projecten te werken. Ze kunnen deze informatie als één criterium gebruiken wanneer ze besluitvormingsanalyses op meerdere criteria uitvoeren tijdens het vervullen van resources. Zij kunnen ook andere resourcekenmerken aan het filter toevoegen om te zoeken naar resources met specifieke vaardigheden, opleiding en ervaring voor een bepaald project.

**Scenario:** Er is een goedgekeurd project gestart en de rol van senior projectmanager is tijdens de projectplanningsfase gereserveerd als een geplande resource. De resourcemanager heeft nu een resource verworven om de rol van senior projectmanager te vervullen.

1. Selecteer op de pagina **Resourcelijst** de naam **Daniel Goldschmidt**.
2. Selecteer op de pagina **Resourcerol** de optie **Nieuw** en voer de volgende waarden in:

    - **Ingangsdaum:** Voer de huidige datum in.
    - **Vervaldatum:** Voer **Nooit** in.
    - **Rol:** Voer **Senior projectmanager** in.

3. Selecteer **Opslaan** en sluit vervolgens de pagina.
4. Voeg op het tabblad **Competenties** de vaardigheid **ProjectMgmt** en het certificaat **PMP** in.


[!INCLUDE[footer-include](../includes/footer-banner.md)]