---
title: Een project maken en bijwerken
description: In dit onderwerp krijgt u informatie over het bijwerken van projecten in Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 07f96973a1341e65e648f126a931d72454334e9c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592502"
---
# <a name="create-and-update-a-project"></a>Een project maken en bijwerken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Hier volgt een samenvatting van de velden die kunnen worden bijgewerkt voor een project nadat dit is gemaakt. Dit omvat ook eventuele toepasselijke implicaties op basis van deze updates.

## <a name="project-detail-fields"></a>Projectdetailvelden

- **Naam**: de naam van het project.
- **Beschrijving**: een overzicht van het project.
- **Klant**: het bedrijf waaraan het project zal worden opgeleverd.
- **Kalendersjabloon**: de werktijden van het project. Wanneer het veld wordt gewijzigd, wordt het volledige schema opnieuw berekend.
- **Valuta**: de valuta voor het project. De standaardwaarde voor dit veld is gebaseerd op de valuta die is gedefinieerd in de contracterende eenheid. Wanneer de contracterende eenheid wordt bijgewerkt, wordt het veld ook bijgewerkt.
- **Contracterende eenheid**: de organisatie-eenheid die de bedrijfsgroep of divisie vertegenwoordigt die primair verantwoordelijk is voor het sluiten van de verkoop en het beheren van de levering van arbeid en diensten aan de klant.  Als de organisatie-eenheid van de projectmanager niet is gedefinieerd, wordt dit veld standaard ingesteld op de waarde die is gedefinieerd in de projectparameters.
- **Projectmanager**: het projectteamlid dat de bevoegdheid heeft om tijdinvoer en onkosten te beoordelen en goed te keuren.

## <a name="estimate-fields"></a>Velden met schattingen

- **Geschatte startdatum**: de datum waarop het project begint. Wanneer dit veld wordt bijgewerkt, worden alle taken in het project proportioneel verplaatst met de nieuwe startdatum.
- **Einddatum**: de datum waarop het project moet eindigen.
- **Inspanning**: de geschatte inspanning voor het project. Wanneer taken aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.
- **Geschatte arbeidskosten**: de geschatte arbeidskosten van het project. Wanneer arbeidskosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.
- **Geschatte onkosten**: de geschatte onkosten van het project. Wanneer onkosten aan het project worden toegevoegd, kan dit veld niet langer worden bewerkt.

## <a name="project-actual-fields"></a>Velden met werkelijke projectgegevens
- **Werkelijke start**: de datum waarop het project is gestart.
- **Werkelijk einde**: wordt bijgewerkt wanneer een project is voltooid.

## <a name="project-status-fields"></a>Velden voor projectstatus

- **Algemene projectstatus**: de algehele status van het project die wordt geleverd door de projectmanager.
- **Opmerkingen**: een beschrijving van de huidige status van het project, geleverd door de projectmanager.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
