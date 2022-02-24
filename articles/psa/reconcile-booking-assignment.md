---
title: Boekingen en toewijzingen afstemmen
description: In dit onderwerp krijgt u informatie over werkelijke waarden.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147917"
---
# <a name="reconcile-bookings-and-assignments"></a>Boekingen en toewijzingen afstemmen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

De projectboekingen en projecttaaktoewijzingen van een projectteamlid zijn op losse wijze gekoppeld. Daarom kan een resource taaktoewijzingen hebben die niet overeenkomen met boekingen en boekingen die niet overeenkomen met taaktoewijzingen. In het ideale geval overlappen de projectboekingen en toewijzingen elkaar perfect, zodat resources vastgelegde capaciteit hebben voor het uitvoeren van hun taaktoewijzingen. De realiteit is echter dat er sprake is van boekingen op basis van beschikbaarheid en dat de tijdsplanning van taken kan veranderen naarmate het project vordert. Daarom zorgt de losse koppeling voor flexibiliteit.

Vanwege de losse koppeling van projectboekingen en taaktoewijzingen, is er een tabblad **Afstemming** voor de entiteit Project opgenomen. Op dit tabblad kunnen projectmanagers boekingen van teamleden en hun toewijzingen voor hun projectteam afstemmen.

Voor elk benoemde teamlid worden op het tabblad **Afstemming** de boekingen en toewijzingen weergegeven tot op het niveau van de afzonderlijke taaktoewijzing. Er worden uren weergegeven die tijdsperioden vertegenwoordigen van maanden tot dagen.

In het veld **Tijdschaal** kunt u **Maand**, **Week** of **Dag** selecteren. Standaard is **Week** geselecteerd. U kunt de standaardwaarde echter wijzigen door de knop **Instellingen** te selecteren. Wanneer het tabblad **Afstemming** wordt geopend, wordt de huidige datum weergegeven, maar u kunt het agendabesturingselement gebruiken om vooruit of achteruit te gaan in de tijd. Wanneer een project een begindatum heeft die in de toekomst ligt, wordt op het tabblad die datum weergegeven wanneer het tabblad wordt geopend. Het agendabesturingselement bevat ook opties waarmee u naar de begin- en einddatums van het project kunt gaan.

U kunt de uitvouwbesturingselementen voor elke resource gebruiken om de details van de boekingen van die resource weer te geven. U ook de toewijzingen van elke resource uitvouwen tot op het niveau van de afzonderlijke taak.

Onderaan op het tabblad **Afstemming** wordt een totaal nettobedrag voor het project weergegeven en het tabblad bevat ook een kolom voor totalen. Voor elke resource wordt op het tabblad het verschil genomen tussen de boekingen van een teamlid voor het project en de samengetelde waarde van de taaktoewijzingen van dat teamlid. Idealiter zou dit verschil 0 (nul) moeten zijn. Met andere woorden: er zou geen verschil moeten zijn tussen boekingen en de toewijzingen van de resource. Eventuele verschillen worden aangegeven door kleur en arcering om de aandacht te vestigen op twee toestanden:

- **Te weinig boekingen** – Een tekort aan boekingen treedt op wanneer een resource meer toewijzingen dan boekingen heeft. Omdat deze capaciteit niet is gereserveerd, kan een projectmanager deze toestand corrigeren door de boekingen van de resource uit te breiden om het tekort te dekken.
- **Te veel boekingen** – Een teveel aan boekingen treedt op wanneer een resource is geboekt voor het project, maar er geen taken aan de resource zijn toegewezen. Deze toestand kan acceptabel zijn als de resource bijvoorbeeld is geboekt voordat er taaktoewijzing plaatsvond. In andere gevallen is de resource mogelijk niet gepland om aan taken te worden toegewezen. In dergelijke gevallen moet de projectmanager overwegen de boekingen van de resource te annuleren, zodat de capaciteit voor een ander project kan worden gebruikt.

> [!NOTE]
> De legenda voor deze toestanden is mogelijk verborgen om meer ruimte te maken voor het raster. In dit geval kunt u de legenda zichtbaar maken door de knop **Instellingen** te selecteren.

In sommige gevallen, wanneer het veld **Tijdschaal** is ingesteld op een niveau dat hoger is dan **Dag**, kunnen verschillen worden berekend als 0 (nul). Op het niveau van de **Maand** kan het nettoverschil voor een resource bijvoorbeeld 0 (nul) zijn om aan te geven dat de boekingen gelijk zijn aan de toewijzingen. Als u echter naar het niveau **Week** kijkt, ziet u mogelijk toewijzingen van 0 (nul) uur en boekingen van 40 uur in de eerste week van de maand en toewijzingen van 40 uur en boekingen van 0 (nul) uur in de tweede week van de maand. Hoewel het totale aantal boekingen en toewijzingen voor de maand gelijk zijn, verschillen ze per week.

Wanneer u tijd op hogere niveaus weergeeft, wordt op het tabblad **Afstemming** een celindicator weergegeven om u erop te wijzen dat er verschillen zijn op lagere tijdniveaus. In de volgende afbeelding wordt bijvoorbeeld een celindicator weergegeven in de cel voor de maand oktober 2018 voor de resource met de naam Josephine Beukema. Daarom kunt u zien dat, zelfs als de resourceboekingen en toewijzingen gelijk zijn wanneer ze worden samengevoegd op het niveau van **Maand**, ze niet overeenkomen op lagere niveaus.

![Niet-overeenkomende boekingen en toewijzingen op maandelijks niveau](media/reconcile-assignments-01.JPG)

Dubbelklik op een cel om in te zoomen op het volgende lagere niveau en het verschil te bekijken. Als u bijvoorbeeld dubbelklikt op het verschil in oktober 2018 voor Josephine Beukema, geeft u de details weer op het niveau **Week**. Vervolgens ziet u dat de resource boekingen van 16 uur heeft, maar geen toewijzingen in de eerste twee weken van oktober en toewijzingen van 16 uur, maar geen boekingen in de derde week van oktober.

![Niet-overeenkomende boekingen en toewijzingen op wekelijks niveau](media/reconcile-assignments-02.JPG)

U kunt met de rechtermuisknop op een cel klikken om naar het volgende hogere niveau uit te zoomen. U kunt de celindicator ook uitschakelen door de knop **Instellingen** te selecteren. 

U kunt ook de knoppen **Vorige** en **Volgende** boven het raster gebruiken om door eventuele verschillen in uw project te navigeren. Als u deze knoppen wilt gebruiken, moet u eerst een resource selecteren. Selecteer **Volgende** om naar het volgende verschil tussen boekingen en toewijzingen voor die resource te gaan. Selecteer **Vorige** om naar het vorige verschil te gaan.

Als u taaktoewijzingen voor een resource hebt, maar geen boekingen, kunt u het tekort aan boekingen selecteren en vervolgens **Boeking uitbreiden** selecteren. U ziet nu de boeking die nodig is om het tekort van de resource aan te pakken. U ook de boekingen van de resource bekijken voor het huidige project en andere projecten. Selecteer **OK** om de boeking voor de resource te maken zonder rekening te houden met de huidige beschikbaarheid. De projectmanager of resourcemanager kan vervolgens het planbord gebruiken om situaties te beheersen waarin een resource boekingen heeft die zijn of haar capaciteit te boven gaan omdat de boekingen zijn uitgebreid.

## <a name="managing-with-time-zones"></a>Beheer met tijdzones
Om te zorgen voor nauwkeurige en voorspelbare resultaten bij gebruik van Boeking uitbreiden, zijn er twee belangrijke voorwaarden waaraan moet worden voldaan:  

- De gebruiker moet de tijdzone van zijn apparaat instellen op de tijdzone die is gedefinieerd in de Persoonlijke instellingen van uw systeem.
 
  ![Tijdzone-instellingen in Windows 10](media/reconcile-assignments-03.png)

  ![Tijdzone-instellingen in Persoonlijke instellingen](media/reconcile-assignments-04.png)
 
- De boekbare resource moet ten minste één minuut werktijd hebben die overlapt met de contouren waarmee de aangevraagde uitbreiding wordt gedefinieerd. In het volgende voorbeeld ziet u bijvoorbeeld beoordelingsresources met werkuren die vallen tussen 09:00 en 19:00 uur. 

  ![Vergelijking van resourcecontouren](media/reconcile-assignments-05.png)

In de onderstaande tabel ziet u het volgende:

- Een sjabloon van een projectagenda.
- Resource A: Deze resource heeft dezelfde agenda en bevindt zich in dezelfde tijdzone als het project. De starttijd van de boekingen is 09.00 uur.
- Resource B: Deze resource bevindt zich in een andere tijdzone dan het project en begint daarom om 07:00 uur in de eigen tijdzone. De boekingen beginnen echter om 09:00 uur, omdat dit de vroegste starttijd van de toewijzingscontour is.
- Resources C en D: De resources bevinden zich ook ieder in een andere tijdzone, en hun tijdzones verschillen ook van het project. Hun boekingen beginnen niet eerder dan hun respectieve beschikbare starttijden.

|Entiteit  |Agenda  |
|-|-|
|Sjabloon van projectagenda   | ![projectagenda](media/reconcile-assignments-06.png) |
|Resource A  | ![Agenda van resource A](media/reconcile-assignments-06.png) |
|Resource B  |  ![Agenda van resource B](media/reconcile-assignments-07.png) |
|Resource C  |  ![Agenda van resource C](media/reconcile-assignments-08.png) |
|Resource D  | ![Agenda van resource D](media/reconcile-assignments-09.png)  |
 
Wanneer u naar de afstemmingsweergave navigeert, worden de resourcetoewijzingen en de bijbehorende boekingstekorten weergegeven.
 ![Afstemmingsweergave vóór uitbreiding](media/reconcile-assignments-10.png)

De functionaliteit Boeking uitbreiden wordt uitgevoerd op elke resource en de boekingen worden daadwerkelijk uitgebreid voor elke resource. Dit komt omdat de werkuren van elke resource overlappen met de contouren van het tekort.
 ![Afstemmingsweergave na uitbreiding van de boeking](media/reconcile-assignments-11.png) 

Als we de details van de boekingen echter nader bekijken, zien we verschillen in de starttijd van de boekingen. De boekingen starten niet eerder dan de starttijd van de toewijzingscontour en niet eerder dan de beschikbare starttijd van de resource.
 ![Nieuwe boekingen van de resources in het planbord](media/reconcile-assignments-12.png)
