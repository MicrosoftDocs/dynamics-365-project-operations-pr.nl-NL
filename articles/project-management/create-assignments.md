---
title: Resourcetoewijzingen maken
description: Dit artikel bevat informatie over het maken van generieke en benoemde resourcetoewijzingen.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811987"
---
# <a name="create-resource-assignments"></a>Resourcetoewijzingen maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


Een resourcetoewijzing is de directe koppeling van een projectteamlid aan een bladknooppunttaak. Dit artikel bevat informatie over de verschillende manieren waarop u resources kunt toewijzen.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Een algemeen teamlid maken door taken toe te wijzen


Wanneer u een algemeen teamlid maakt via taaktoewijzing, maakt u een tijdelijke aanduiding of algemene resource. In deze algemene resource worden de kenmerken van de benoemde resource beschreven die uiteindelijk aan de taken moet werken. Vervolgens genereert u een vereiste of dient u een verzoek in op basis van de vereiste die gebruikt wordt om de benoemde resource te zoeken en te boeken.

1. Selecteer in het raster Planning voor een taak het pictogram Resource in de cel **Resource**.
2. Typ een naam als tijdelijke aanduiding voor de naam van de resource. bijvoorbeeld Programmanager.
3. Selecteer **Maken** en stel in het veld **Snelle invoer: Projectteamlid** de rol voor de algemene resource in.
4. Wijs naar wens taken aan deze tijdelijke resourceaanduiding toe door de resource voor de taak te selecteren in de **resourceselectie**. De resources worden weergegeven onder **Teamleden**.
5. Als u klaar bent met het toewijzen van de algemene resource, selecteert u de algemene resource op het tabblad **Team** en selecteert u **Vereiste genereren** om een resourcevereiste te maken voor de algemene resource.
6. Selecteer **Boeken** voor de algemene resource en gebruik het planbord om een echte resource te zoeken en te boeken. U kunt de vereiste ook indienen voor afhandeling door een resourcemanager.
7. Wanneer de algemene resource volledig is uitgevoerd met een benoemde resource, wordt de algemene resource uit het team verwijderd. (Gedeeltelijke uitvoering van een resourcevereiste leidt niet tot een resourcetoewijzing.) De taaktoewijzingen voor de algemene resource worden toegewezen aan de benoemde resource die de resourcevereiste van de algemene resource uitvoert.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Een benoemde resource toewijzen vanuit de lijst met alle boekbare resources

U kunt het zoekvak in de **resourcekiezer** gebruiken om alle boekbare resources te doorzoeken en deze toe te wijzen aan een bladknooppunttaak. Resources die op deze manier worden toegewezen, worden zonder boekingen aan het team toegevoegd. Dit is vergelijkbaar met het toevoegen van een teamlid en het selecteren van **Geen** als de toewijzingsmethode. De resource wordt op de tabbladen **Team**, **Resourcetoewijzing** en **Afstemming** weergegeven als resources met alleen toewijzingen en een boekingstekort. Boek deze resources als u hun beschikbaarheid wilt gebruiken.

1. Navigeer vanuit het taakraster, het planbord of de tijdlijn naar de cel **Toegewezen aan**.
2. Begin met het typen van een naam in het zoekvak. De zoekresultaten voor de naam worden weergegeven in de **resourceselectie** onder **Overige resources**.
3. Selecteer de resource die u aan de taak wilt toewijzen of selecteer de naam van de resource onder **Andere teamresources**.

## <a name="editing-resource-assignment-contours"></a>Contouren voor resourcetoewijzing bewerken

Wanneer resources worden toegewezen aan een taak in de planning, wordt hun inspanning op basis van de werkuren van die resource en de planningsmodus van het project standaard lineair verdeeld over elke resource. Een projectmanager kan het resourcetoewijzingsraster gebruiken om de inspanningsschattingen te verfijnen van elke resource die is toegewezen aan een of meer taken over de verschillende tijdschalen. Deze functie helpt projectmanagers nauwkeurigere kosten- en verkoopramingen te maken, die worden aangestuurd door de resourcetoewijzingscontouren die worden gegenereerd wanneer een resource aan een taak wordt toegewezen. Bovendien kunnen projectmanagers gemakkelijker de resourcevraag weergeven die nodig is om de vraag in een resourcevereiste in te bouwen.

### <a name="navigation"></a>Navigatie

Om toegang te krijgen tot het contourbewerkingsraster, selecteert de projectmanager eerst het tabblad **Taken** op de hoofdpagina van het project en selecteert deze vervolgens het tabblad **Toewijzingen**.

![Tabblad Toewijzingen op het tabblad Taken van de hoofdpagina van het project.](media/AssignmentGrid.png)

Het raster ondersteunt twee methoden voor groeperen: **groeperen op resource** en **groeperen op taak**. In tegenstelling tot de rasterweergave kunnen kolommen niet worden geconfigureerd. De enige zichtbare kolommen zijn **Toegewezen aan**, **Taaknaam**, **Toewijzing starten**, **Toewijzing voltooid** en **Toewijzingsinspanning**.

Wanneer het raster voor het eerst wordt weergegeven, begint het bij de vroegste toewijzingscontour. Als uw schema geen toewijzingen bevat waarvoor inspanningen gedaan moeten worden, is het raster leeg en wordt er niets weergegeven.

![Leeg toewijzingsraster.](media/emptyassignmentgrid.png)

Als u uw contouren en verschillende tijdschalen wilt bekijken, zijn ook het alleen-lezen resourcetoewijzingsraster en resource-reconciliatieraster beschikbaar.

### <a name="resource-calendars"></a>Resourceagenda´s

De mogelijkheid om een contour voor een specifieke dag te bewerken, wordt bepaald door de werkdagen van de resource, zoals weerspiegeld in hun kalender. Als een cel is uitgeschakeld voor een bepaalde resource, heeft die resource gedurende die periode geen werkdagen.

De contouren van een resource kunnen verder reiken dan de huidige start- en einddatums van de toegewezen taak. Als een contour wordt bijgewerkt zodat deze na de laatste einddatum of de vroegste startdatum van een taak valt, wordt de einddatum of startdatum van de taak waar nodig gewijzigd. Als een contour echter wordt bijgewerkt zodat deze eerder valt dan de startdatum van een taak die is gekoppeld aan een voorganger, mislukt de update omdat de toewijzing de taak activeert om te starten voordat de voorganger is voltooid, en dat gedrag wordt momenteel niet ondersteund.

### <a name="co-authoring"></a>Gezamenlijke creatie

Wijzigingen in het resourcetoewijzingsraster worden automatisch weerspiegeld in alle bijbehorende weergaven, inclusief de diagram-, tijdlijn-, bord- en rasterweergaven. Als meerdere gebruikers het project tegelijkertijd beoordelen, worden alle wijzigingen die een gebruiker aanbrengt, weergegeven in het raster. Omgekeerd worden alle wijzigingen die worden aangebracht in het resourcetoewijzingsraster weergegeven aan alle andere gebruikers die het project in dezelfde sessie bekijken.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
