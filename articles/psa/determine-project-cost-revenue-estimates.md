---
title: Schattingen voor projectkosten en -opbrengst bepalen
description: Informatie over schattingen voor projectkosten en -opbrengst bepalen in Project Service
author: ruhercul
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148817"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Schattingen voor projectkosten en -opbrengst bepalen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Project-de financiële ramingen verschaffen de weergave voor het werken met en de geschatte omzet in de structuur voor werkspecificatie van het project te kunnen worden ingepland. De schattingenweergave informeert u over - kosten en omzetgevolg van de geplande werken. De schattingenweergave is een hulpprogramma dat de klantgegevens altijd wilt zien over een aantal vooraf gedefinieerde dimensies u over de financiële gevolgen van het project de record misschien aanbevolen vertellen.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Kosten en verkopenwaarde van het project  
De prijslijsten in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bepalen de kosten en factuurtarieven voor de rollen waarvan projecten gebruik maken. Afhankelijk van de rollen met de taken in de structuur voor werkspecificatie van het project zijn gekoppeld, kunt u de kosten en omzetgevolg van werk in kwestie definiëren.  
  
## <a name="cost-price-defaulting"></a>Standaardwaarde kostprijs  
Elk project is het eigendom van een organisatie (in **Bezittend Unit** in het project weergegeven). De prijslijst aan de bezittende organisatie-eenheid bepaalt de unitkostprijs is gekoppeld. De [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]-mogelijkheden bepalen kostprijzen voor rollen door te zoeken naar de combinatie van rol, eenheid, en organisatie-eenheid in de kostprijslijst en zo de juiste kostprijs voor de betreffende datum te vinden in schattingregels.  
  
Als de combinatie van rol, eenheid en organisatie-eenheid niet resulteert in een kostprijs uit de prijslijst van de eenheid die eigenaar is, wordt de eenheid genegeerd ten gunste van de combinatie van rol en organisatie-eenheid. Als er een kostprijs is, wordt deze prijs wordt geconverteerd naar de eenheid weergegeven die u op de schattingregel hebt gekozen.  
  
Als de combinatie van rol en organisatie-eenheid niet resulteert in een kostprijs, wordt de organisatie-eenheid genegeerd ten gunste van de combinatie van rol en eenheid, en wordt de prijs de standaardwaarde na het toepassen van enige conversie, indien nodig.  
  
 Als er geen is de prijs voor rol, moet de kostprijs blijft met 0,00 op de schattingregel in als standaardwaarde.  
  
 Alle kostenbedragen op de regels van de projectkostenraming worden valuta's van de bezittende organisatie-eenheid.  
  
## <a name="sales-price-defaulting"></a>Standaardwaarde verkoopprijs  
De verkoopprijslijst is gebaseerd op de verkoopmaatschappij het project waarvoor is toegevoegd. De verkoopprijslijst aan de offerte of het contract is gekoppeld bepaalt de verkoopprijs per eenheid. Als de prijsopgave of het contract een aangepaste prijslijst bevat, is dit de standaardverkoopprijs voor projectschattingen. Als er niet aan verkoopentiteiten de koppeling is, wordt de lijst met de standaardverkoopprijs parametersinstellingen is geconfigureerd in het overzicht van de standaardverkoopprijs voor het project. Elke campaign schattingregel heeft een resourceorganisatie-eenheid is gekoppeld om de organisatie-eenheid te geven waarop resources voor het voltooien van de taak wordt geboekt. De verkoopprijzen voor gekoppelde rollen worden bepaald door te zoeken naar de combinatie van de rol, eenheid en resourceorganisatie-eenheid in de verkoopprijslijst om de juiste verkoopprijs voor de datum te vinden op schattingregels.  
  
Als de gewenste combinatie van rol, eenheid, en resourceorganisatie-eenheid niet in een van de verkoopprijs verkoopprijslijst optreedt, stuurt het systeem unit en zoek de gewenste combinatie van resourceorganisatie-eenheid negeren en rol. Als er een verkoopprijs is, wordt deze geconverteerd naar de eenheid die u op de verkoopramingsregel hebt gekozen.  
  
Als het systeem niet prijs voor de functie zoeken, moet de verkoopprijs standaardwaarde is 0,00 op de schattingregel.  
  
De schattingenweergave heeft een rasterweergave voor een kort raster van schattingregels met unit en de totale kosten en verkoopprijs worden weergegeven.  
  
## <a name="time-phased-view-of-project-estimates"></a>Weergave van projectschattingen tijdgebonden  
In de weergave voor projectschattingen tijdgebonden, worden de schattingengegevens van de rasterweergave gedraaid standaard op rol, en ziet u een van schattinggegevens verspreiding over de tijdlijn in de gekozen tijdschaal.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>De toewijzing van inspanningsschatting op basis van die taakmodus  
Tijdgebonden in de weergave, wordt de totale geschatte inzet voor de taak wordt gedistribueerd op een bepaald aantal inspanningsuren per unittijdspanne van de gekozen tijdschaal toe te wijzen. In Project Service bepaalt de taakmodus hoe de inzet wordt toegewezen over de duur van de taak. De twee soorten toewijzing zijn gelijkmatige toewijzing en toewijzing op basis van werkuren. 
  
## <a name="work-hours-based-allocation"></a>Toewijzing op basis van werkuren  
De automatische planning taakmodus voor een taak regeert voor het aantal resources de geschatte omzet voor de taak, worden ze de geschatte omzet voor de gehele dag werkuren worden gebruikt. Dit geldt bij het toewijzen van de klant voor het bevolkingssegment van door de duur van taken op de tijd gefaseerde weergave ook te splitsen. Zo mag op een tijdschaal van Dag voor een taak die naar schatting door één resource wordt voltooid, de toegewezen inspanning per dag de in de kalender van het project gedefinieerde werkuren per dag niet overschrijden. Daarom kan de inspanningstoewijzing altijd voor dat er resources voor de gehele dag worden geschatte worden gebruikt.  
  
## <a name="even-distribution"></a>Zelfs distributie  
De eert handmatig die niet de taakmodus geplande de werkuren, projectkalender, of het aantal resources voor de taak wordt gedefinieerd. De taakplanning is gebaseerd op gebruikerinvoer. Voor deze taken, heeft de inspanningstoewijzing per unittijdspanne van de gekozen tijdschaal geen beperkende factoren. De totale inzet voor de taak in op is gelijk splitsen en toegewezen voor elke unittijdspanne op de tijdschaal gekozen.  
  
Op deze manier, wordt de taakmodus op de taak wordt bepaald of de inspanningsdistributie de toewijzing van klant per unittijdspanne tijdgebonden schattingen in.  
  
## <a name="grouping-and-time-phasing-options"></a>Groepering en time-phasing opties  
In deze weergave kunt u de verdeling van de klant, de kosten en de verkoop-, schattingen op een dag, week, maand, of jaarbasis kennen. Groeperen op de optie hiermee kunt draaiend de schattingengegevens op twee andere dimensies: categorie en resource. Zowel op de rasterweergave tijdgebonden als de weergave kunt u de velden weer te kiezen. De totalen voor elk van de tijdsblokken worden onderaan weergegeven en geven de totale geschatte inspanning, kosten en verkoop weer voor de dag, week, maand of het jaar.  
  
De standaardkostprijs en verkoopprijs zijn datumafhankelijk. Wanneer de tarieven voor de rollen wijzigen, is het transparanter in de tijdgebonden weergave wanneer u schattingsgegevens bekijkt rond 'Resource' en tijdgebonden per week.  
  
## <a name="expense-estimates"></a>Onkostenschattingen  
Eventuele onkosten die in het project worden gemaakt die niet rechtstreeks verband houden met arbeid, kunnen in de projectschattingen in de rasterweergave worden geregistreerd. Met de optie **Toevoegen-onkostenschatting** in de rasterweergave, kunt u dit te bereiken. De onkostenschattingen kunnen worden geregistreerd voor een specifieke taak of voor het hele project. U kunt op deze regels onkostencategorieën kiezen en een voorlopige datum kiezen waarop de onkosten naar verwachting zullen worden gemaakt. Als de gekoppelde verkoopprijslijst standaardprijzen overschrijven met kosten en, of verhogingpercentages heeft voor onkostencategorieën worden bepaald, stopt setup op de schattingregel op de koppeling in de standaardinstelling.  
  
### <a name="see-also"></a>Zie ook  
 [Projectmanager-handleiding](../psa/project-manager-guide.md)
