---
title: Overzicht van goedkeuringen
description: Dit onderwerp biedt informatie over het werken met goedkeuringen in Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074424"
---
# <a name="approvals-overview"></a>Overzicht van goedkeuringen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Indieningen van tijd en onkosten doorlopen een goedkeuringswerkstroom. Nadat de boekingen zijn goedgekeurd, worden transacties geregistreerd in werkelijke waarden of wordt tijd geboekt in de planning.

## <a name="approvals-workflow"></a>Werkstroom voor goedkeuringen
Wanneer u een tijdsvermelding of onkostenpost maakt en indient, wordt een goedkeuringsboeking gemaakt. De projectfiatteur of uw manager beoordeelt uw inzending en keurt deze goed. Als de inzending betrekking heeft op een project, worden de werkelijke waarden bij goedkeuring aangemaakt. Hierdoor kunnen de kosten en facturering worden gevolgd. 

## <a name="approve-an-entry"></a>Een inzending goedkeuren
Via het formulier **Goedkeuringen** kunt u schakelen tussen verschillende weergaven, zodat u de verschillende soorten goedkeuringen kunt bekijken.
  
1. Ga naar het formulier **Goedkeuringen** en selecteer **Onkosten** , **Tijd** of **Intrekkingen**.
2. Bekijk elke goedkeuring en selecteer de goedkeuringen die u wilt goedkeuren.
3. Selecteer **Goedkeuren** om de geselecteerde items goed te keuren.
Deze items worden verwerkt en er worden werkelijke waarden of een boeking gemaakt.

## <a name="reject-an-entry"></a>Een item afwijzen
Als de projectfiatteur moet u mogelijk een item ter correctie terugsturen naar een gebruiker.
  
1. Ga naar het formulier **Goedkeuringen** en selecteer het item dat u wilt afwijzen. 
2. Selecteer **Afwijzen**.
3. Optioneel - Voeg een opmerking toe in het dialoogvenster **Opmerkingen bij weigering** om de gebruiker te informeren waarom het item wordt afgewezen.
4. Selecteer **OK**. Het item wordt teruggestuurd naar de gebruiker.
  
## <a name="recall-entries"></a>Items intrekken
Op een gegeven moment moet u mogelijk een ingediend item intrekken. Als het item niet is goedgekeurd, wordt het onmiddellijk geretourneerd. Een goedgekeurd item kan echter een materiële impact hebben. De projectfiatteur moet de intrekking goedkeuren om de transactie in Werkelijke waarden terug te draaien.

## <a name="specify-project-approvers"></a>Projectfiatteurs opgeven
Elk project heeft een aantal projectteamleden. U kunt opgeven welke teamleden ook projectfiatteurs zijn.

1. Ga naar het formulier **Projecten** en open het project vanuit de lijst.
2. Op het tabblad **Team** selecteert u het teamlid dat een projectfiatteur moet zijn en vervolgens selecteert u **Bewerken**.
3. Stel het veld **Projectfiatteur** in op **Ja**.
4. Selecteer **Opslaan**.
5. Herhaal stap 2 tot en met 4 om extra projectfiatteurs toe te voegen.

## <a name="configure-the-users-manager"></a>De manager van een gebruiker configureren

1. Ga naar **Instellingen** > **Beveiliging** > **Gebruikers**.
2. Selecteer de gebruiker aan wie u een manager toewijst en selecteer in het gebied **Organisatie-informatie** de manager in de lijst. 
3. Selecteer **Opslaan**.


