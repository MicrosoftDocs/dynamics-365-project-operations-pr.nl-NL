---
title: Projectkosten en -opbrengsten
description: Dit onderwerp bevat informatie over het schatten van de projectkosten en -opbrengsten.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: fe51af8adb7c3831a57494b8359def2a0176b552efe16feb53a2a265f5ffcb0c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002550"
---
# <a name="project-costs-and-revenue"></a>Projectkosten en -opbrengsten

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projectschattingen bieden de financiële weergave voor werk dat wordt geschat en gepland in de projectplanning. Op het tabblad **Schattingen** op de pagina **Projecten** ziet u welke impact het door u geplande werk heeft op de kosten en de omzet. Het tabblad biedt ook informatie over vele vooraf gedefinieerde dimensies. 

> ![Tabblad Schattingen.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Kosten en verkoopwaarden van het project

Prijslijsten bepalen de kosten en factuurtarieven voor de rollen in een project. U kunt de impact van het werk op de kosten en de omzet bepalen op basis van de rollen die zijn gekoppeld aan de naam van de positie en de benoemde resource die aan een taak is toegewezen. Als er taken zijn die geen toewijzingen hebben (algemeen of benoemd), kunt u geen kosten- of verkoopschattingen ophalen. Bij kosten- en verkoopwaarden wordt rekening gehouden met de datum die is gedefinieerd in de prijslijsten.

### <a name="default-cost-price"></a>Standaardkostprijs  

Elk project behoort tot een organisatie. Deze organisatie wordt weergegeven in het veld **Contracterende eenheid** in het project. De prijslijst die aan de contracterende eenheid is gekoppeld, wordt gebruikt om de kostprijs per eenheid te bepalen. Als u de juiste kostprijzen wilt bepalen voor rollen voor de datum die is gedefinieerd op schattingsregels, zoekt u naar de combinatie van rol, eenheid en organisatie-eenheid in de kostprijslijst. 

Alle taken moeten aan een resource worden toegewezen, zodat hun kostprijzen kunnen worden berekend. Alle niet-toegewezen taken hebben een kostprijs van 0,00.

Als de combinatie van rol, eenheid en organisatie-eenheid geen kostprijs uit de prijslijst van de contracterende eenheid retourneert, wordt de eenheid genegeerd door het systeem. In plaats daarvan wordt gezocht naar de combinatie van alleen rol en organisatie-eenheid. Als er een kostprijs wordt gevonden, worden conversiefactoren gebruikt om deze te converteren naar de eenheid die u op de schattingsregel hebt geselecteerd.

Als de combinatie van rol en organisatie-eenheid geen kostprijs retourneert, wordt de organisatie-eenheid genegeerd door het systeem. In plaats daarvan wordt gezocht naar de combinatie van rol en eenheid om de standaardprijs in te stellen (nadat een conversie is toegepast).

Als het systeem geen prijs voor de rol vindt, wordt de kostprijs op de schattingsregel ingesteld op de standaardwaarde **0,00**. Alle kostenbedragen op de schattingsregels voor projectkosten worden vastgelegd in de valuta van de contracterende eenheid.

> [!NOTE]
> Standaard worden in Microsoft Dynamics 365 kostenbedragen in uw basisvaluta opgeslagen. De kostenbedragen op het tabblad **Schattingen** worden echter weergegeven in de valuta van de contracterende eenheid.  

### <a name="default-sales-price"></a>Standaardverkoopprijs 

De verkoopprijslijst wordt bepaald door ofwel de verkoopentiteit waaraan het project is gekoppeld of de projectklant. Wanneer een verkoopentiteit, zoals verkoopkans, prijsopgave of contract, aan het project is gekoppeld, wordt de verkoopprijs van de verkoopentiteit bepaald door de prijslijst die aan de prijsopgave of het contract is gekoppeld. Als de prijsopgave of het contract een aangepaste prijslijst bevat, wordt die prijslijst gebruikt als de standaardverkoopprijslijst voor projectschattingen. Als er geen koppeling is met verkoopentiteiten, wordt de standaardverkoopprijslijst van de parameters gebruikt als de standaardverkoopprijslijst van het project en wordt de valuta van de klant gebruikt die voor het project is gedefinieerd.

Aan elke schattingsregel is een resource-eenheid gekoppeld. De resource-eenheid geeft de organisatie-eenheid aan waaruit de resources worden geboekt om de taak te voltooien. Als u de verkoopprijs voor de gekoppelde rollen wilt bepalen, zoekt u naar de combinatie van rol, eenheid en resource-eenheid in de verkoopprijslijst. Als er geen toewijzingen voor de taak zijn, is de verkoopprijs voor de taak 0,00.

Als de combinatie van rol, eenheid en resource-eenheid geen verkoopprijs uit de verkoopprijslijst retourneert, wordt de eenheid genegeerd door het systeem. In plaats daarvan wordt gezocht naar de combinatie van alleen rol en resource-eenheid. Als er een verkoopprijs wordt gevonden, worden conversiefactoren gebruikt om deze te converteren naar de eenheid die u op de verkoopschattingsregel hebt geselecteerd. 

Als de combinatie van rol en resource-eenheid geen verkoopprijs uit de verkoopprijslijst retourneert, wordt de resource-eenheid genegeerd door het systeem. In plaats daarvan wordt gezocht naar de combinatie van rol en eenheid om de standaardprijs in te stellen (nadat een conversie is toegepast).

Als het systeem geen prijs voor de rol vindt, wordt de verkoopprijs op de schattingsregel ingesteld op de standaardwaarde **0,00**.

Het tabblad **Schattingen** heeft een rasterweergave waarin schattingsregels worden weergegeven. Het raster bevat kolommen voor de eenheid, de totale kostprijs en de totale verkoopprijs, zoals in de volgende afbeelding wordt weergegeven. 

> ![Rasterweergave op het tabblad Schattingen.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Weergave van projectschattingen tijdgebonden

De tijdgebonden weergave van projectschattingen toont de schattingsgegevens uit de rasterweergave op de tijdlijn, in een tijdschaal die u selecteert. Standaard worden de schattingsgegevens rond de dimensie **Rol** gedraaid.

> ![Tijdgebonden weergave voor projectschattingen.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Geschatte inspanning toewijzen op basis van de taakmodus

In de tijdgebonden weergave verdeelt u de totale inspanning die wordt geschat voor de taak, door inspanningsuren toe te wijzen per eenheidstijdsperiode op de gekozen tijdschaal. De taakmodus bepaalt hoe de inspanning wordt toegewezen voor de duur van de taak. De twee soorten toewijzing zijn: **Even** (gelijkmatig) en **Gebaseerd op werkuren**.

### <a name="work-hours-based-allocation"></a>Toewijzing op basis van werkuren
 
In de taakmodus voor automatisch plannen worden de dagelijkse standaarduren voor taakresources ingesteld op het volledige werkuurtarief. Dit gedrag treedt op wanneer inspanning wordt toegewezen door deze op te splitsen voor de duur van de taak in de tijdgebonden weergave. Als u bijvoorbeeld schat dat een taak door één resource kan worden voltooid in de tijdschaal **Dag**, zal de inspanning die wordt toegewezen per dag, het aantal werkuren per dag dat is gedefinieerd in de projectagenda, niet overschrijden. Daarom wordt er bij de toewijzing van inspanning altijd voor gezorgd dat er bij de schatting van wordt uitgegaan dat de resources de hele dag worden gebruikt.

### <a name="even-allocation"></a>Gelijkmatige toewijzing

In de taakmodus voor handmatig plannen worden de werkuren van de projectagenda niet gebruikt. In plaats daarvan is de taakplanning gebaseerd op invoer van de gebruiker. Voor deze taken heeft de toewijzing van inspanning per eenheidstijdsperiode in de geselecteerde tijdschaal geen beperkende factor. De totale inspanning voor de taak wordt in gelijke delen opgesplitst voor elke eenheidstijdsperiode in de geselecteerde tijdschaal. Daarom bepaalt de taakmodus die is gedefinieerd voor de taak, de verdeling van de inspanning of de toewijzing van inspanning per eenheidstijdsperiode in tijdgebonden schattingen.

## <a name="grouping-and-time-phasing-options"></a>Groepering en time-phasing opties

In de tijdgebonden weergave worden de verdeling van de inspanning, de kosten en de verkoopschattingen per dag, week, maand of jaar weergegeven. Standaard worden de schattingsgegevens rond de dimensie **Rol** gedraaid. U kunt echter de optie **Groeperen op** gebruiken om twee andere dimensies als draaipunt te gebruiken: **Categorie** en **Resource**.

In zowel de rasterweergave als de tijdgebonden weergave kunt u de velden selecteren die moeten worden weergegeven. De totalen voor elk tijdsblok worden onder aan het project weergegeven. Ze geven de totale geschatte inspanning, kosten en verkoop voor een dag, week, maand of jaar weer. De standaardkostprijs en verkoopprijs zijn datumafhankelijk. Met andere woorden: ze veranderen voor elke resource op basis van de tijdgebonden weergave die u selecteert.

## <a name="expense-estimates"></a>Onkostenschattingen

Met de knop **Een nieuwe onkostenschatting toevoegen** in de rasterweergave kunt u onkosten vastleggen die het project met zich meebrengt, maar die niet direct gerelateerd zijn aan arbeid. U kunt de onkostenschattingen voor een specifieke taak of voor het hele project vastleggen. Selecteer onkostencategorieën en de voorlopige datum waarop u verwacht de onkosten te betalen. Als de gekoppelde kostprijslijst en verkoopprijslijst standaardprijzen hebben (of als er opslagpercentages zijn gedefinieerd voor onkostencategorieën), worden deze automatisch ingevoerd op de schattingsregel wanneer de koppeling optreedt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]