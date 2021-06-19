---
title: Een projectteam maken
description: Dit onderwerp bevat informatie over het maken en beheren van projectteams.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d3d39aa28565692bf894ff8d4fc8f8c3c5542d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006190"
---
# <a name="create-a-project-team"></a>Een projectteam maken

[!include [banner](../includes/banner.md)]

Als u de rollen wilt gebruiken die eerder in een project zijn ingesteld, moet een projectmanager de rollen aan het project koppelen. Er kunnen meerdere rollen worden toegewezen voor een project. Om verwarring te voorkomen worden deze rollen automatisch gelabeld tijdens het reserveren. Als de projectmanager bijvoorbeeld drie software-engineers nodig heeft, worden automatisch drie software-engineerrollen gegenereerd met **software-engineer 1**, **software-engineer 2** en **software-engineer 3** als label. Als er eerder rolkenmerken voor de rol waren ingesteld, worden deze als filter toegepast tijdens het zoeken naar een resource. Er kunnen naar behoefte extra kenmerken worden toegevoegd om de zoekopdracht verder te verfijnen.

De weergave-instellingen kunnen eveneens worden aangepast om een beter beeld te krijgen van de beschikbaarheid van resources. Er zijn opties om de beschikbaarheid per uur, dag, week, maand, kwartaal en jaar weer te geven. Er is ook een optie om beschikbare en resterende capaciteit voor resources weer te geven. Deze optie is handig voor tijdbeheer, wanneer u de beschikbare tijd voor activiteiten of de beschikbaarheid van resources wilt inschatten.

De projectmanager kan een rol op de pagina selecteren en vervolgens, als er een beschikbare resource is die aan de vereiste voldoet, een resource reserveren voor het vervullen van de rol. Houd er rekening mee dat de resources op dit punt in de planningsfase niet hoeven te worden gereserveerd. Wanneer u een WBS maakt, kunt u rollen vervangen door bemande resources voor het project. Als rollen worden vervangen door bemande resources in de WBS, werkt de resource-instelling automatisch de projectteamlijst en -planning bij.

[![Projectteamlijst met zowel rollen als daadwerkelijke resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

De projectmanager heeft verschillende mogelijkheden om een resource voor een project te boeken, zoals **Resterende capaciteit**, **Volledige capaciteit**, **Capaciteitspercentage** en **Uren opgeven**. Deze boekingsopties kunnen op elk moment worden geannuleerd als de resourcetoewijzingen veranderen. Er worden twee typen boekingen ondersteund:

- **Hard boeken** - De resourcereservering is goedgekeurd en bevestigd om voor de opgegeven duur aan de opdracht te werken.
- **Zachgt boeken** - De resourcereservering is voorlopig ingesteld om voor de opgegeven duur aan de opdracht te werken.

In de volgende procedure wordt uitgelegd hoe u een projectteam maakt.

## <a name="create-a-project-team"></a>Een projectteam maken

1. Selecteer op de pagina **Alle projecten** een project en selecteer vervolgens **Bewerken**.
2. Voer op het tabblad **Projectteam en planning**, in het veld **Einddatum planning** de begindatum van de planning plus een maand in. Als de begindatum van de planning bijvoorbeeld 24 juni 2017 (24-06-2017) is, voert u **24-07-2017** in.
3. Selecteer **Toevoegen**.
4. Selecteer in het deelvenster **Rollen toevoegen aan het project**, in het veld **Rol**, de optie **Senior projectmanager**.
5. Selecteer **Vereiste competenties**.
6. Op de pagina **Kenmerken kiezen** zijn standaard de kenmerken geselecteerd die u eerder hebt ingesteld voor de rol Senior projectmanager. Selecteer **OK**.
7. Voer op de pagina **Rollen toevoegen aan project**, in het veld **Aantal resources** de waarde **1** in.
8. In het veld **Resource** geeft de zoekopdracht alle resources weer die de vereiste competenties hebben. Selecteer **Daniel Goldschmidt** en selecteer vervolgens **Maken**.
9. Selecteer op de pagina **Project** de optie **Toevoegen**.
10. Selecteer in het deelvenster **Rollen toevoegen aan het project**, in het veld **Rol**, de optie **Teamlid**. Voer in het veld **Aantal resources** de waarde **5** in.
11. Selecteer **Maken**.
12. Selecteer op de pagina **Projecten** de optie **Resource vervullen**.

## <a name="monitor-project-teams"></a>Projectteams bewaken
1. Selecteer op de pagina **Alle projecten** de koppeling **Project-id** voor het project **XYZ-upgrade fase 2**.
2. Controleer op het sneltabblad **Projectteam en planning** of de vermelde projectresources correct zijn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]