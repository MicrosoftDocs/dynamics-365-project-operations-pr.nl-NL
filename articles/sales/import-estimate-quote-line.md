---
title: Projectschattingen importeren in projectgebaseerde prijsopgaveregel
description: Dit onderwerp bevat informatie over het importeren van schattingen uit een project naar een prijsopgaveregel.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c0fe18b33207f73848709b99334f64aadc7867a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074480"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Projectschattingen importeren in projectgebaseerde prijsopgaveregel

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_


Als een project wordt aangemaakt tijdens de voor-verkoopfase, kunt u ervoor kiezen om de financiële schatting van het project in de projectgebaseerde prijsopgaveregel te importeren.

1. Zorg ervoor dat de projectgebaseerde prijsopgaveregel de projectinformatie bevat in het veld **Project**.
2. Selecteer op het tabblad **Prijsopgaveregeldetails** de optie **Importeren uit projectschatting**.
3. Selecteer op de dialoogvensterpagina die wordt geopend een van de volgende overzichtsopties:

  - **Transactieklasse**
  - **Categorie**
  - **- Rol** 
  - **Projecttaak**

Op basis van uw selectie wordt de schatting uit het project voor alle transactieklassen op deze prijsopgaveregel gekopieerd. Om te controleren welke transactieklassen zijn inbegrepen, selecteert u het tabblad **Algemeen** op de projectgebaseerde prijsopgaveregel en controleert u de waarden voor **Inclusief tijd** , **Inclusief kosten** en **Inclusief kosten**.

Wanneer u schattingen importeert, worden standaard de prijzen gebruiken uit de projectprijslijsten die aan de prijsopgave zijn gekoppeld en het factureringstype dat is ingesteld op de projectgebaseerde prijsopgaveregel. Als een rol of categorie op de projectgebaseerde prijsopgaveregel is ingesteld als niet-toerekenbaar, wordt de geïmporteerde schattingsregel ingesteld als niet-toerekenbaar en wordt deze niet opgeteld bij de opgegeven waarde van de prijsopgaveregel.

Als een prijsopgaveregel regeldetails bevat, worden de velden **Waarde prijsopgave** en **Geschatte belasting** op de prijsopgaveregel samengevat en kunnen ze niet worden bewerkt.

Als er meerdere samenvattingsopties zijn geselecteerd, wordt geprobeerd samen te vatten op basis van alle geselecteerde opties. Het resultaat is dat de uitvoer van geïmporteerde prijsopgaveregels meer zal zijn dan wanneer u slechts één samenvattingsoptie hebt geselecteerd.

Als het project bijvoorbeeld de volgende schattingsregels voor onkosten heeft.

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| Taak B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Taak C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Wanneer de gebruiker ervoor kiest om samen te vatten op transactieklasse, wordt de volgende informatie geïmporteerd.

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

Wanneer de gebruiker ervoor kiest om samen te vatten op transactieklasse en categorie, wordt de volgende informatie geïmporteerd.

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Wanneer de gebruiker ervoor kiest om samen te vatten op transactieklasse, categorie en bladknooppunttaak, wordt de volgende informatie geïmporteerd. Merk op dat dit resultaat hetzelfde is als wat er op het project was.

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| Taak B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Taak C | Hotel | 11/1/2020 | 2 | 200 | 400 |