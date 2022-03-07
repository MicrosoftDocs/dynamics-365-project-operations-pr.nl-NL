---
title: Hoe wijs ik een boekbare resource toe aan een taak in de webapp
description: Een overzicht van de manieren waarop u boekbare resources kunt toewijzen.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25cf017c53d7db23e467b3b610e2990e56e95cb56bdf9820e427dfeeeb979637
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987700"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Hoe wijs ik een boekbare resource toe aan een taak in de webapp (Project Service-app v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Er zijn twee manieren om een resource aan een taak toe te wijzen in Project Service. U kunt een resource als teamlid boeken en deze toewijzen aan een taak. U kunt ook een algemeen teamlid maken door rollen toe te wijzen voor taken, een team te genereren en aan de ondersteunende vereisten te voldoen met een benoemde resource.

Als u een boekbare resource aan een taak wilt toewijzen, moet het boekbare lid van het resourceteam voldoende beschikbare boekingen hebben. De boeking moet de status Hard geboekt en het toewijzingstype Vastgelegd hebben. Als er niet voldoende boekingen voor de resource zijn, wordt de toewijzing verwijderd en wordt het volgende foutbericht weergegeven:

*Kan resource niet aan taak toewijzen - De volgende resource(s) heeft/hebben niet voldoende uren geboekt voor dit project*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Een resource als teamlid boeken en de resource vervolgens toewijzen aan een taak

Met deze methode voegt u een resource aan het projectteam toe en wijst u vervolgens taken aan de resource toe in de projectplanning. Ga als volgt te werk:
1.  Voeg in het raster voor teamleden een nieuw teamlid toe door **Nieuw** te selecteren.
2.  Selecteer de boekbare resource in het scherm Snelle invoer en stel een rol in.
3.  Selecteer de datums bij **Van** en **Tot**.

    > [!div class="mx-imgBorder"] 
    > ![Schermopname van het toevoegen van een teamlid.](media/FAQ-Resources-to-Tasks2-1.png "Schermopname van het toevoegen van een teamlid")
 
4.  Selecteer een van de volgende toewijzingsmethoden om de resource te boeken:
    - Met **Volledige capaciteit** boekt u de volledige capaciteit van de resource voor de opgegeven periode.
    - Met **Percentagecapaciteit** boekt u een percentage van de capaciteit van de resource voor de opgegeven periode.
    - Met **Uren gelijkmatig verdelen** wordt de resource voor een bepaald aantal uren geboekt en worden de uren gelijkmatig verdeeld over de periode tussen de opgegeven begin- en einddatum.
    - Met **Uren vooraf laden** wordt de resource voor een bepaald aantal uren geboekt en worden de uren zoveel mogelijk in het begin van de periode tussen de opgegeven begin- en einddatum geboekt.

    Selecteer **Geen** niet omdat de resource hiermee aan het teamlid wordt toegevoegd, maar er geen boekingen worden gemaakt die capaciteit van de resource verbruiken.
5.  Selecteer **Opslaan**.

    De uren van de boeking moeten voldoende zijn om de inspanningsuren en datumbereiken te dekken van de taken waaraan u deze resource toewijst. Als dit niet het geval is, kunt u de resource niet aan de taak toewijzen.

6.  In de structuur voor werkspecificatie voor de taak klikt u op de vervolgkeuzelijst in de resourcecel. Ga vervolgens als volgt te werk: 

    1. Selecteer **Toevoegen**.
    2. Selecteer de vervolgkeuzelijst onder **Resources** en selecteer het teamlid dat u eerder hebt toegevoegd.
    3. Selecteer **OK**. Het teamlid wordt nu toegewezen aan de taak.

    > [!div class="mx-imgBorder"] 
    > ![Schermopname van het toevoegen van resources met WBS.](media/FAQ-Resources-to-Tasks2-2.png "Schermopname van het toevoegen van resources met WBS")
 
In het raster van het teamlid wordt het totaal van de toegewezen uren voor de resource weergegeven onder Toegewezen uren. Dit is minder dan of gelijk aan de geboekte uren voor de resource. 

> [!div class="mx-imgBorder"] 
> ![Schermopname van toegewezen uren voor een resource.](media/FAQ-Resources-to-Tasks2-3.png "Schermopname van toegewezen uren voor een resource")
 
Als de taak die u probeert toe te wijzen aan de resource na de einddatum van de resourceboekingen begint, wordt de resource niet in de vervolgkeuzelijst weergegeven.

U kunt een resource aan meer uren dan de geboekte uren toewijzen als de resource nog resterende niet-toegewezen capaciteit heeft. In dit geval wordt de resource slechts gedeeltelijk toegewezen aan de boekingen. U kunt de resterende, niet-toegewezen taakuren bekijken door de kolom Onbemande uren toe te voegen aan de structuur voor werkspecificatie.

Als resources aan hun geboekte uren zijn toegewezen (hun geboekte uren zijn gelijk aan hun toegewezen uren), kunt u het volgende foutbericht verwachten wanneer u probeert nog meer taken toe te wijzen:

*Kan resource niet aan taak toewijzen - De volgende resource(s) heeft/hebben niet voldoende uren geboekt voor dit project.*

Daarnaast wordt de standaardprojectmanager die aan het team wordt toegevoegd wanneer u het project maakt, toegevoegd zonder boekingen en kan deze niet aan taken worden toegewezen. De standaardprojectmanager wordt niet weergegeven in de vervolgkeuzelijst met resources voor taken.

Als u deze resource wilt toewijzen, moet u deze uit het team verwijderen en vervolgens opnieuw toevoegen met een andere toewijzingmethode dan Geen. Deze standaardprojectmanager wordt bij het maken van een project aan het team toegevoegd om ervoor te zorgen dat een project standaard minstens één projectfiatteur heeft.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Een algemeen teamlid maken door rollen toe te wijzen voor taken

Met deze methode weet u zeker dat resources voldoende boekingen hebben voor taken. Eerst maakt u een tijdelijk aanduiding of een algemene resource waarin de kenmerken van de benoemde resource worden beschreven die uiteindelijk aan de taken moeten werken. Ga als volgt te werk:

1. Selecteer een taak in de structuur voor werkspecificatie.
2. Selecteer het vervolgkeuzelijstpictogram **Toegewezen rol** in de resourcecel.
3. Selecteer de vervolgkeuzelijst **Rol** en selecteer de rol voor de algemene resource.
4. Selecteer **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Schermopname van het gebruik van WBS om een resource toe te voegen.](media/FAQ-Resources-to-Tasks2-4.png "Schermopname van het gebruik van WBS om een resource toe te voegen")
 
Wanneer u klaar bent met het toewijzen van rollen aan de taken in de structuur voor werkspecificatie, selecteert u **Projectteam genereren**. In Project Service wordt het minimum aantal algemene teamleden op basis van de rollen, resource-eenheden en projectagenda gemaakt door de taaktoewijzingen op te tellen.

> [!div class="mx-imgBorder"] 
> ![Schermopname van het genereren van het projectteam.](media/FAQ-Resources-to-Tasks2-5.png "Schermopname van het genereren van het projectteam")
 
In het raster voor teamleden worden resources van het type Algemene resource met de rol en positienaam weergegeven. Als twee resources voor een rol nodig zijn om het werk af te maken, maakt u met de functie Team genereren twee teamleden en kunnen deze twee op basis van de positienaam worden onderscheiden.

> [!div class="mx-imgBorder"] 
> ![Schermopname van het toevoegen van twee algemene resources.](media/FAQ-Resources-to-Tasks2-6.png "Schermopname van het toevoegen van twee algemene resources")
 
U kunt de ondersteunende resourcevereiste voor het algemene teamlid openen door de koppeling onder Resourcevereiste te selecteren.

> [!div class="mx-imgBorder"] 
> ![Schermopname van het openen van de vereiste voor ondersteunende resource.](media/FAQ-Resources-to-Tasks2-7.png "Schermopname van het openen van de vereiste voor ondersteunende resource")

Selecteer **Boeken** voor de algemene resource en gebruik het planbord om een echte resource te zoeken en te boeken. U kunt de vereiste voor afhandeling door een resourcemanager ook verzenden door **Aanvraag verzenden** te selecteren.

Als de algemene resource door een benoemde resource wordt vervangen, wordt de algemene resource uit het team verwijderd en worden de taaktoewijzingen voor de algemene resource toegewezen aan de benoemde resource waarmee aan de resourcevereiste van de algemene resource werd voldaan.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]