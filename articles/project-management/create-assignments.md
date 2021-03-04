---
title: Resourcetoewijzingen maken
description: Dit onderwerp biedt informatie over het maken van algemene en benoemde resourcetoewijzingen.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 829c1d1de7270e7cafbb98ef80235ae6404f77f7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131742"
---
# <a name="create-resource-assignments"></a>Resourcetoewijzingen maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


Een resourcetoewijzing is de directe koppeling van een projectteamlid aan een bladknooppunttaak. Dit onderwerp biedt informatie over de verschillende manieren om resources toe te wijzen.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Een algemeen teamlid maken door taken toe te wijzen


Wanneer u een algemeen teamlid maakt via taaktoewijzing, maakt u een tijdelijke aanduiding of algemene resource. In deze algemene resource worden de kenmerken van de benoemde resource beschreven die uiteindelijk aan de taken moet werken. Vervolgens genereert u een vereiste (of dient u een verzoek in op basis van de vereiste) om de benoemde resource te zoeken en te boeken.

1. Selecteer in het raster Planning voor een taak het pictogram Resource in de cel **Resource**.
2. Typ een naam als tijdelijke aanduiding voor de resourcenaam, bijvoorbeeld Programmanager.
3. Selecteer **Maken** en stel in het veld **Snelle invoer: Projectteamlid** de rol voor de algemene resource in.
4. Wijs naar wens taken aan deze tijdelijke resourceaanduiding toe door de resource voor de taak te selecteren in de **resourceselectie**. De resources worden weergegeven onder **Teamleden**.
5. Als u klaar bent met het toewijzen van de algemene resource, selecteert u de algemene resource op het tabblad **Team** en selecteert u **Vereiste genereren** om een resourcevereiste te maken voor de algemene resource.
6. Selecteer **Boeken** voor de algemene resource en gebruik het planbord om een echte resource te zoeken en te boeken. U kunt de vereiste ook indienen voor afhandeling door een resourcemanager.
7. Wanneer de algemene resource volledig is uitgevoerd (gedeeltelijke uitvoering van een resourcevereiste leidt niet tot een resourcetoewijzing) met een benoemde resource, wordt de algemene resource uit het team verwijderd. De taaktoewijzingen voor de algemene resource worden toegewezen aan de benoemde resource die voldeed aan de resourcevereiste van de algemene resource.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Een benoemde resource toewijzen vanuit de lijst met alle boekbare resources

U kunt het zoekvak in de **resourcekiezer** gebruiken om alle boekbare resources te doorzoeken en deze toe te wijzen aan een bladknooppunttaak. Resources die op deze manier worden toegewezen, worden zonder boekingen aan het team toegevoegd. Dit is vergelijkbaar met het toevoegen van een teamlid en het selecteren van **Geen** als de toewijzingsmethode. De resource wordt op de tabbladen **Team**, **Resourcetoewijzing** en **Afstemming** weergegeven als resources met alleen toewijzingen en een boekingstekort. Boek deze resources als u hun beschikbaarheid wilt gebruiken.

1. Navigeer vanuit het taakraster, het planbord of de tijdlijn naar de cel **Toegewezen aan**.
2. Begin met het typen van een naam in het zoekvak. De zoekresultaten voor de naam worden weergegeven in de **resourceselectie** onder **Overige resources**.
3. Selecteer de resource die u aan de taak wilt toewijzen of selecteer de naam van de resource onder **Andere teamresources**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]