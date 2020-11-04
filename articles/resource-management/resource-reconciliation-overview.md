---
title: Overzicht van de afstemming van resources
description: Dit onderwerp bevat informatie over de manier waarop u ervoor kunt zorgen dat de resourceboekingen en toewijzingen aan projecten met elkaar overeenkomen.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074506"
---
# <a name="resource-reconciliation-overview"></a>Overzicht van de afstemming van resources

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Voor teamleden zijn boekingen en toewijzingen op losse wijze gekoppeld. Met andere woorden: resources kunnen toewijzingen hebben, maar geen boekingen of ze kunnen boekingen hebben, maar geen toewijzingen. In het ideale geval overlappen de boekingen en toewijzingen elkaar perfect, zodat resources vastgelegde capaciteit hebben voor het uitvoeren van de taaktoewijzingen. De boekingen kunnen echter zijn gebaseerd op beschikbaarheid en de tijdsplanning van taken kan veranderen naarmate het project vordert. Daarom biedt de losse koppeling van boekingen en toewijzingen flexibiliteit.

Via het tabblad **Afstemming** in het formulier **Projecten** kunnen projectmanagers boekingen van teamleden en hun toewijzingen voor projectteams op elkaar afstemmen.

Op het tabblad **Afstemming** worden ook boekingen en toewijzingen weergegeven tot op het niveau van de afzonderlijke taaktoewijzing voor elk teamlid. Uren worden weergegeven in cellen die tijdsperioden vertegenwoordigen, van maanden tot dagen.

Het tabblad bevat ook een totaal nettobedrag voor het project samen met een kolom **Totaal**.

Voor elke resource wordt op het tabblad het verschil berekend tussen de boekingen van het teamlid en de samengetelde waarde van de taaktoewijzingen van het teamlid. Idealiter zou dit verschil 0 (nul) moeten zijn. Met andere woorden: er zou geen verschil moeten zijn tussen boekingen en toewijzingen. Verschillen hebben een kleur en zijn gearceerd om de aandacht te vestigen op twee toestanden:

- **Te weinig boekingen** – Een tekort aan boekingen treedt op wanneer een resource meer toewijzingen dan boekingen heeft. Omdat deze capaciteit niet is gereserveerd, kan een projectmanager deze toestand corrigeren door de boekingen van de resource uit te breiden om het tekort te dekken.
- **Te veel boekingen** – Een teveel aan boekingen treedt op wanneer een resource is geboekt voor het project, maar er geen taken aan de resource zijn toegewezen. Deze toestand kan acceptabel zijn in die gevallen waarin de resource is geboekt voor het project voordat de taaktoewijzing plaatsvond. In andere gevallen is de resource echter niet gepland om aan taken te worden toegewezen. In dergelijke gevallen moet de projectmanager overwegen de boekingen van de resource te annuleren, zodat de capaciteit voor een ander project kan worden gebruikt.

In sommige gevallen, wanneer u de tijd weergeeft op een hoger niveau dan het dagniveau (bijvoorbeeld op maandniveau), ziet u mogelijk een nettoverschil van nul voor een resource (met andere woorden: boekingen = toewijzingen). Als u echter de tijd op weekniveau weergeeft, ziet u mogelijk toewijzingen van nul uur en boekingen van 40 uur in de eerste week, maar toewijzingen van 40 uur en boekingen van nul uur in de tweede week. Over het algemeen zijn de boekingen en toewijzingen op elkaar afgestemd, maar ze verschillen van week tot week.

Wanneer u tijd op hogere niveaus weergeeft, hebben cellen op het tabblad **Afstemming** een indicator om u erop te wijzen dat er verschillen zijn op lagere niveaus. Door in een cel te dubbelklikken, kunt u inzoomen om het verschil te bekijken. U kunt vervolgens met de rechtermuisknop klikken om uit te zoomen. Door een resource te selecteren en vervolgens op het besturingselement **Volgende verschil** op de rasterwerkbalk te klikken, gaat u naar het volgende verschil tussen boekingen en toewijzingen voor die resource. Vervolgens kunt u het besturingselement **Vorige verschil** gebruiken om terug te gaan. U kunt ook de verschil-indicatoren en het navigatiegedrag uitschakelen onder **Instellingen**.


Als u taaktoewijzingen voor een resource hebt, maar geen boekingen, gaat u naar de pagina **Projecten** en selecteert u op het tabblad **Afstemming** het tekort aan boekingen en selecteert u vervolgens **Boeking uitbreiden**. Het dialoogvenster **Boeking uitbreiden** verschijnt en hierin wordt de boeking weergegeven die nodig is om het tekort van de resource aan te vullen. Ook worden de bestaande boekingen van de resource in alle projecten of andere planbare entiteiten weergegeven. Als u **OK** selecteert om de boeking voor de resource te maken, ongeacht de beschikbaarheid van die resource, kan er overboeking ontstaan.

De projectmanager of resourcemanager kan vervolgens het planbord gebruiken om situaties te beheersen waarin een resource boekingen heeft die zijn of haar capaciteit te boven gaan.

