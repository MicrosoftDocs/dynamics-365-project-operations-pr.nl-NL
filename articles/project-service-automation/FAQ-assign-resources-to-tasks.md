---
title: Een resource toewijzen aan een taak
description: Dit onderwerp biedt informatie over hoe u resources toewijst aan taken.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: Project Service
ms.technology: Dynamics 365 Project Service Automation 3.x
ms.assetid: 3ea9516c-0276-4e30-b308-f792f64d608b
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 509f7a4464b2e810900b31a78219ba696192a18b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750856"
---
# <a name="assign-a-resource-to-a-task"></a>Een resource toewijzen aan een taak

Er zijn drie manieren om een resource aan een taak toe te wijzen in Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Een resource als teamlid boeken en de resource vervolgens toewijzen aan een taak

U kunt een resource aan het projectteam toewijzen en deze resource vervolgens aan taken in de projectplanning toewijzen.

1. Voeg op het tabblad **Teamlid** een nieuw teamlid toe door **Nieuw** te selecteren. 

2. Het deelvenster **Snelle invoer voor teamleden** wordt geopend waarin u de te boeken resourcenaam kunt selecteren en een rol kunt instellen. 

    Selecteer een van de volgende toewijzingsmethoden voor de boeking van de resource:

    - Met **Volledige capaciteit** boekt u de volledige capaciteit van de resource voor de opgegeven periode.
    - Met **Percentagecapaciteit** boekt u een percentage van de capaciteit van de resource voor de opgegeven periode.
    - Met **Uren gelijkmatig verdelen** wordt de resource voor een bepaald aantal uren geboekt en worden deze gelijkmatig verdeeld over de periode tussen de opgegeven begin- en einddatum.
    - Met **Uren vooraf laden** wordt de resource voor een bepaald aantal uren geboekt en worden de uren zoveel mogelijk in het begin van de periode tussen de opgegeven begin- en einddatum geboekt.
    - Met **Geen** wordt de resource aan het team toegevoegd, maar worden er geen boekingen gemaakt die capaciteit van de resource verbruiken.

3. Selecteer in het raster **Planning** voor een taak het pictogram **Resource** in de resourcecel en selecteer vervolgens onder **Teamleden** het teamlid dat u zojuist hebt toegevoegd. 

> [!NOTE]
> Zowel op het tabblad **Teamlid** als op het tabblad **Vereffening** worden voor de resource geboekte en toegewezen uren weergegeven. Doorgaans komen deze aantallen overeen, maar dit hoeft niet, aangezien boekingen en toewijzingen niet nauw gekoppeld zijn. Het tabblad **Vereffening** biedt meer informatie wanneer deze aantallen niet overeenkomen, bijvoorbeeld wanneer u een resource meer uren hebt toegewezen dan u hebt geboekt. Indien nodig kunt u de gegevens corrigeren door de boekingen van de resource uit te breiden of de toewijzing te wijzigen.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Een algemeen teamlid maken door taken toe te wijzen

Wanneer u een algemeen teamlid wilt maken door een taak toe te wijzen, maakt u een tijdelijk aanduiding of een algemene resource waarin de kenmerken van de benoemde resource worden beschreven die uiteindelijk aan de taken moeten werken. Vervolgens genereert u een vereiste (of dient u een verzoek in op basis van de vereiste) om de benoemde resource te zoeken en te boeken.

1. Selecteer in het raster **Planning** voor een taak het pictogram **Resource** in de resourcecel.

2. Typ een naam als tijdelijke aanduiding voor de resourcenaam, bijvoorbeeld Programmanager.

3. Selecteer **Maken** en stel in het veld **Snelle invoer: Projectteamlid** de rol voor de algemene resource in.

4. U kunt doorgaan met het toewijzen van taken aan deze tijdelijke resourceaanduiding door de resource voor de taak te selecteren in de **resourceselectie**. Deze worden weergegeven onder **Teamleden**.

5. Als u klaar bent met het toewijzen van de algemene resource, selecteert u de algemene resource op het tabblad **Team** en selecteert u **Vereiste genereren** om een resourcevereiste te maken voor de algemene resource.

6. Selecteer **Boeken** voor de algemene resource. Vervolgens kunt u het planbord gebruiken om een echte resource te zoeken en te boeken. U kunt de vereiste ook indienen voor afhandeling door een resourcemanager.

7. Als de algemene resource door een benoemde resource wordt vervangen, wordt de algemene resource uit het team verwijderd en worden de taaktoewijzingen voor de algemene resource toegewezen aan de benoemde resource waarmee aan de resourcevereiste van de algemene resource werd voldaan.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Een benoemde resource toewijzen vanuit de lijst met alle boekbare resources

U kunt het zoekvak in de **resourceselectie** gebruiken om alle boekbare resources te doorzoeken en deze toe te wijzen aan een taak.

Resources die op deze manier worden toegewezen, worden zonder boekingen aan het team toegevoegd. Dit is vergelijkbaar met het toevoegen van een teamlid en het selecteren van Geen als de toewijzingsmethode. De resource wordt op de tabbladen **Team** en **Vereffening** als resources met alleen toewijzingen en een boekingstekort weergegeven. Boek deze resources als u hun beschikbaarheid wilt gebruiken.

1. Selecteer in het raster **Planning** voor een taak het pictogram **Resource** in de resourcecel.

2. Typ een naam. De zoekresultaten voor de naam worden weergegeven in de **resourceselectie** onder **Overige resources**.

3. Selecteer de resource die u aan de taak wilt toewijzen.

