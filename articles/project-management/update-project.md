---
title: Een project bijwerken
description: In dit onderwerp krijgt u informatie over het bijwerken van projecten in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074419"
---
# <a name="update-a-project"></a>Een project bijwerken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Hieronder vindt u een overzicht van de velden die kunnen worden bijgewerkt voor een project nadat het is gemaakt en alle toepasselijke implicaties van de updates.

## <a name="project-detail-fields"></a>Projectdetailvelden

- **Naam** : de naam van het project.
- **Beschrijving** : een overzicht van het project.
- **Klant** : het bedrijf waaraan het project zal worden opgeleverd.
- **Kalendersjabloon** : de werktijden van het project. Wanneer het veld wordt gewijzigd, wordt het volledige schema opnieuw berekend.
- **Valuta** : de valuta voor het project. Dit veld wordt standaard ingesteld op basis van de valuta die is gedefinieerd in de contracterende eenheid. Wanneer de contracterende eenheid wordt bijgewerkt, wordt het veld ook bijgewerkt.
- **Contracterende eenheid** : de organisatie-eenheid die de bedrijfsgroep of divisie vertegenwoordigt die primair verantwoordelijk is voor het sluiten van de verkoop en het beheren van de levering van arbeid en diensten aan de klant. 
- **Projectmanager** : het projectteamlid dat de bevoegdheid heeft om tijdinvoer en onkosten te beoordelen en goed te keuren.

## <a name="estimate-fields"></a>Velden met schattingen

- **Geschatte startdatum** : de datum waarop het project begint. Wanneer dit veld wordt bijgewerkt, worden alle taken in het project proportioneel verplaatst met de nieuwe startdatum.
- **Einddatum** : de datum waarop het project moet eindigen.
- **Inspanning** : de geschatte inspanning voor het project. Wanneer taken aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.
- **Geschatte arbeidskosten** : de geschatte arbeidskosten van het project. Wanneer arbeidskosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.
- **Geschatte onkosten** : de geschatte onkosten van het project. Wanneer onkosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.

## <a name="project-actual-fields"></a>Velden met werkelijke projectgegevens
- **Werkelijke start** : de datum waarop het project is gestart.
- **Werkelijk einde** : wordt bijgewerkt wanneer een project is voltooid.

## <a name="project-status-fields"></a>Velden voor projectstatus

- **Algemene projectstatus** : de algehele status van het project die wordt geleverd door de projectmanager.
- **Opmerkingen** : een beschrijving van de huidige status van het project, geleverd door de projectmanager.

