---
title: Een schatting importeren in een projectgebaseerde contractregel
description: Dit onderwerp bevat informatie over het importeren van schattingen uit een project naar een contractregel.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d51eb890a4744051ddd7268e1f1f11b15a23b609
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278367"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Een schatting importeren in een projectgebaseerde contractregel

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In Dynamics 365 Project Operations kunt u schattingen uit een project importeren in een projectgebaseerde contractregel.

1. Controleer of het veld **Project** op de projectgebaseerde contractregel is ingevuld.
2. Selecteer op het tabblad **Contractregeldetails** in het subraster **Importeren uit projectschatting**. Er wordt een dialoogvenster met samenvattingsopties geopend. De beschikbare samenvattingsopties zijn **Transactieklasse**, **Categorie**, **Rol** en **Projecttaak**. Op basis van de selecties voor samenvatting wordt de schatting uit het project voor alle transactieklassen op deze contractregel gekopieerd. 
3. Om te controleren welke transactieklassen zijn opgenomen, selecteert u op het tabblad **Algemeen** van de contractregel de waarden in de velden **Tijd opnemen**, **Onkosten opnemen** en **Kosten opnemen**.

Wanneer u schattingen importeert, worden de prijzen standaard ingesteld op basis van de projectprijslijsten die zijn gekoppeld aan het contract en het factureringstype dat is ingesteld op de contractregel. Als een rol of categorie op de contractregel is ingesteld als niet-toerekenbaar, wordt de geïmporteerde schattingsregel voor die rol of categorie als niet-toerekenbaar ingesteld en wordt deze niet opgeteld bij de opgegeven waarde van de contractregel.

Als een contractregel regeldetails bevat, worden de velden **Contractwaarde** en **Geschatte belasting** op de contractregel samengevat en kunnen ze niet worden bewerkt.

Als er meerdere samenvattingsopties zijn geselecteerd, wordt geprobeerd samen te vatten op basis van alle geselecteerde opties. De samenvattingsuitvoer resulteert in meer geïmporteerde contractregels dan wanneer u slechts één samenvattingsoptie selecteert.

Als het project bijvoorbeeld de volgende schattingsregels voor onkosten had:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| Taak B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Taak C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Wanneer de gebruiker ervoor kiest om samen te vatten op **Transactieklasse**, wordt de volgende informatie geïmporteerd:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Wanneer de gebruiker ervoor kiest om samen te vatten op **Transactieklasse** en **Categorie**, wordt de volgende informatie geïmporteerd:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Wanneer de gebruiker ervoor kiest om samen te vatten op **Transactieklasse**, **Categorie** en **Bladknooppunttaak**, wordt de volgende informatie geïmporteerd. Merk op dat dit resultaat hetzelfde is als wat er in het project was:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| Taak B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Taak C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]