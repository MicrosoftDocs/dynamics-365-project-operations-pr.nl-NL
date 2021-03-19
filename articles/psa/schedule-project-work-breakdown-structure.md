---
title: Een project inplannen met een structuur voor werkspecificatie
description: Informatie over een project inplannen met een structuur voor werkspecificatie in Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282687"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Een project plannen in een structuur voor werkspecificatie (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Een projectplanning deelt communiceren over het werk dat moet worden geïmplementeerd, welke resources het werken worden uitgevoerd, en een tijdschema waarin die werkt moet worden voltooid. De projectplanning worden alle werk met op tijd de verstrekking van het project is gekoppeld. Een van de eerste stappen in de initiatiefase van het project moet een projectplanning gemaakt op de op. Voor projectplanning een te maken, moet u de structuur voor werkspecificatie maken.  
  
 Maak een projectstructuur met een structuur voor werkspecificatie, die u kunt:  
  
- Werk opsplitsen in overzichtelijke taken  
  
- De tijd inschatten die nodig is om een taak uit te voeren  
  
- Afhankelijkheden en duur voor taken instellen  
  
- Bepalen welke rollen vereist zijn om de taken uit te voeren  
  
  De projectplanning in de structuur voor werkspecificatie heeft een huisvriend hetzelfde uitzien, met een Gantt-diagram interactief voltooien.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Een structuur voor werkspecificatie een project voor  
 Een structuur voor werkspecificatie om de volgorde van taken in een project te geven. De structuur voor werkspecificatie bevat taken, vereisten voor elke taak, en kosteninformatie en omzet. In de structuur voor werkspecificatie, kunt u:  
  
-   De volgorde van taken in een hiërarchie  
  
-   Eventuele andere taken die moeten worden voltooid voordat een taak kan worden gestart  
  
-   De begindatum, betreffende datum, en de duur van een taak is voltooid  
  
-   Het aantal uren dat een taak vereist  
  
-   Vereiste vaardigheden en opleiding van de medewerker  
  
-   De medewerkers die aan een taak zijn toegewezen  
  
-   Geschatte opbrengst en kosten  
  
## <a name="task-types"></a>Opdrachttypen  
U kunt de volgende typen taken bij het maken van de structuur voor werkspecificatie gebruiken:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Project-hoofdknooppunt**. | Hoogste niveau samenvattingstaak voor het project. Alle andere projecttaken worden gemaakt onder worden verwijderd. De naam van de hoofdmaptaak is de projectnaam. De inzet, datums, en wordt de duur in het hoofdknooppunt zijn gebaseerd op de waarden op de hiërarchie die eronder liggen en. U kunt de eigenschappen van het hoofdknooppunt bewerken of het hoofdknooppunt verwijderen. | 
| **Overzicht of containertaken**. | Een samenvattingstaak is een taak die deeltaken onder het heeft. Een samenvattingstaak heeft geen werkinspanning of de kosten van zijn. Zijn de werkinspanning en kosten zijn van een deeltaken zijn. U kunt de naam van een samenvattingstaak wijzigen, maar u kunt de klant, de begin- en einddatum, de duur of wijzigen, omdat met automatisch worden berekend. Het verwijderen van een samenvattingstaak verwijdert de taak- en elk van de deeltaken.|  
| **Bladknooppunttaken**. | Een bladknooppunttaak is het meest gedetailleerde werken aan het project. Het heeft een geschatte inspanning, een geplande aantal resources vereist, een geplande begin- en einddatums, en een duur.|

  
## <a name="task-hierarchy"></a>Taakhiërarchie  
 U hebt de volgende opties wanneer u een taakhiërarchie:  
  
- **Taak toevoegen**.   U kunt een taak- bij een positie toe die u in de taakhiërarchie kiest. Als u niet selecteert positie, drukt u aan het einde wordt de nieuwe taak.  
  
- **Inspringingtaak**.   Spring een taak in om deze een onderliggend element van de taak direct boven het te maken.  
  
- **Inspringing van taak verkleinen**.   Inspringing verklein een taak om deze te maken zodat deze niet langer een deeltaak van de oorspronkelijke itemtaak.  
  
- **Omhoog en omlaag**.   Bewegingstaken boven of beneden in de hiërarchie van de itemtaak. Verplaatsing van een taak bevat naar boven of omlaag geen gevolgen zijn, kosten, inspanning, datums of duur.  
  
## <a name="task-attributes"></a>Taakkenmerken  
 De naam van een taak beschrijft het werk dat moet worden uitgevoerd. U gebruikt verschillende taakkenmerken als u de planning en het personeelsbestand mogelijk vereisten van de taak te geven.  
  
### <a name="schedule-attributes"></a>Planningskenmerken

 - Wijs aan waarden **Inspanningsuren**, **Aantal resources**, **Begindatum**, **Einddatum**, en **Duur** als u de planning voor de taak te bepalen. 
 - **Inspanning** is een schatting van de werkuren het nemen om de taak te voltooien.
 - **Aantal resources** is een schatting van de projectmanager de taak aanbrengt helpen met de best mogelijke planning in de gemaakt zijn. 
 - **Duur** (in dagen) geeft het aantal werkdagen wordt treffen om de taak te voltooien.  
  
### <a name="staffing-attributes"></a>Personeelskenmerken

 - **Rol**, **Resourceorganisatie-eenheid**, **Aantal resources**, **Resources** en worden het personeelsbestand mogelijk de vereisten voor de taak. 
 - **Rol** worden beschreven die het type resource nodig om de taak uit te voeren. 
 - **Resourceorganisatie-eenheid** duidt op de organisatie-eenheid voor de resource voor taken die moeten worden bemand; deze instelling wordt ook de kosten en verkopenschatting van de taak, want dit is opgegeven rekenschap van de configuratie-items bepaalt van de verkoopprijs per eenheid voor de resource. 
 - **Resources** bevat een of algemene resource door een resource wordt gevonden.  
  
## <a name="task-dependencies"></a>Taakafhankelijkheden  
 U kunt activiteitrelaties vorige tussen één of meerdere taken in de structuur voor werkspecificatie maken. U kunt een of meerdere waarden in de vorige activiteitveld op taken instellen om de taken uit te geven er van afhankelijk is. Als u een eerdere activiteit, toewijst aan een taak kan de taak alleen het opstarten van vorige activiteittaken zijn voltooid. Het instellen van dit afhankelijk van een taak wordt weergegeven in recalculation van de geplande begindatum van de taak bij als het einde van zijn vorige activiteiten niet. op de activiteitbetrekking sectie die gevolgen op een planning worden niet door de taakmodus beperkt op de taak wordt gedefinieerd.  
  
## <a name="task-mode"></a>Taakmodus  
 De taak modus is een van de essentiële factoren die het plannen van bladknooppunttaken definiëren. Er zijn twee taakmodussen voor elke taak: auto planning modus en handmatige planningmodus.  
  
-   **Automatisch plannen**   Als u de taakmodus op Automatisch gepland instelt, bepaalt de taakplanningsengine op basis van de planningsregels voor de volgende taakkenmerken de planning voor de taak:  
  
    -   Voorgaande elementen  
  
    -   Inspanning  
  
    -   Aantal resources  
  
    -   Begin- en einddatum  
  
-   **Planningsregels**.   De begindatum van een bladknooppunttaak die geen voorgaande taken heeft, wordt standaard ingesteld op de planningsbegindatum van het project. De duur van een bladknooppunttaak altijd wordt berekend als het werkdagen tussen het begin- en einddatums vereist. Wanneer een taak automatisch wordt geboekt, volgt de planningsengine de volgende regels:  
  
    -   De begin- en einddatums van een taak moeten altijd werkdagen zijn volgens de planningskalender van het project.  
  
    -   De begindatum van een taak die voorgangers heeft, wordt standaard ingesteld op de laatste einddatum van de voorgangers.  
  
    -   Inspanning = Aantal mensen * Duur * uren in een standaardwerkdat van de projectkalender  
  
-   **Handmatige planning**.   In sommige gevallen moet u misschien afwijken van deze regels. In dergelijke gevallen, kunt u de taakmodus voor de taak instellen handmatig plannen. Hierdoor wordt de planningsengine van het berekenen van de waarden voor het plannen andere kenmerken. De instelling op vorige activiteiten taken is altijd de begindatum van de afhankelijke taak.  
  
## <a name="create-a-work-breakdown-structure"></a>Structuur voor werkspecificatie  
  
1.  Ga naar **Project Service > Projecten**.  
  
2.  Klik op het project waaraan u wilt werken.  
  
3.  In de balk die boven aan het scherm wordt weergegeven, selecteert u de pijl-omlaag naast de projectnaam, en klikt u vervolgens op Structuur voor werkspecificatie.  
  
4.  Als u een taak wilt toevoegen, klikt u **Taak toevoegen**. Vul de vereiste velden in en klik vervolgens op **Opslaan**.  
  
5.  Ga verder met het toevoegen van taken aan de structuur voor werkspecificatie is voltooid. Bij het maken van de structuur voor werkspecificatie, kunt u het volgende doen zodat u indelen:  
  
    -   Selecteer een taak en klik **Inspringen** om het onder een andere taak te plaatsen, of klik op Inspringing verkleinen om hem een niveau hoger te zetten.  
  
    -   Selecteer een taak en klik **Omhoog verplaatsen** of **Omlaag verplaatsen** om in de lijst omhoog of omlaag te verplaatsen.  
  
    -   Klik op **Gantt verbergen** om het Gantt-diagram te verbergen en klik op **Gantt weergeven** om het diagram weer zichtbaar te maken.  
  
    -   Selecteer een andere tijdsperiode voor het Gantt-diagram in **Tijdschaal**.  
  
6.  Als u de rollen wilt toevoegen die u in uw structuur voor werkspecificatie hebt opgegeven voor de leden van uw projectteam, klikt u op **Projectteam genereren**.  
  
7.  Klik op de knop **Opslaan** rechtsonder in het scherm wanneer u klaar bent met het aanbrengen van wijzigingen.  
  
### <a name="see-also"></a>Zie ook  
 [Projectmanager-handleiding](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]