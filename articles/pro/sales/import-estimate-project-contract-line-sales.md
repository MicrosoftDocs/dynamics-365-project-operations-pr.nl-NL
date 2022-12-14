---
title: Schattingen importeren vanuit een projectcontractregel
description: Dit artikel bevat informatie over het importeren van financiële ramingen vanuit een project naar een contractregel.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824668"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Schattingen importeren vanuit een projectcontractregel

_**Van toepassing op:** Vereenvoudigde implementatie - van deal tot pro-formafacturering en Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_ _

In Dynamics 365 Project Operations kunt u schattingen uit een project importeren in een projectgebaseerde contractregel.

1. Controleer of het veld **Project** op de projectgebaseerde contractregel is ingevuld.
2. Selecteer op het tabblad **Contractregeldetails** in het subraster **Importeren uit projectschatting**. Er wordt een dialoogvenster met samenvattingsopties geopend. De beschikbare samenvattingsopties zijn **Transactieklasse**, **Categorie**, **Rol** en **Projecttaak**.
3. Op basis van de selecties voor samenvatting wordt de schatting uit het project voor alle transactieklassen en taken op deze contractregel gekopieerd. Om te controleren welke transactieklassen zijn opgenomen, selecteert u op het tabblad **Algemeen** op de projectgebaseerde contractregel de waarden in de velden **Tijd opnemen**, **Onkosten opnemen** en **Kosten opnemen**. 
4. Om te zien welke taken zijn opgenomen, selecteert u het tabblad **Toerekenbare taken** op de contractregel. Op basis van de gekoppelde taken waarvan het veld **Opgenomen transactieklassen** is ingesteld op **Ja**, worden alle schattingen voor deze taak- en transactieklassecombinaties geïmporteerd in de contractregel.

Wanneer u schattingen importeert, worden de prijzen standaard ingesteld op basis van de projectprijslijsten die zijn gekoppeld aan het contract en het factureringstype dat is ingesteld op de contractregel. Als een taak, rol of categorie op de contractregel is ingesteld als niet-toerekenbaar, wordt de geïmporteerde schattingsregel niet-toerekenbaar en wordt deze niet opgeteld bij de opgegeven waarde van de contractregel.

Als een contractregel regeldetails bevat, worden de velden **Contractwaarde** en **Geschatte belasting** op de contractregel samengevat en kunnen ze niet worden bewerkt.

Als er meerdere samenvattingsopties zijn geselecteerd, wordt geprobeerd samen te vatten op basis van alle geselecteerde opties. De samenvattingsuitvoer resulteert in meer geïmporteerde contractregels dan wanneer u slechts één samenvattingsoptie selecteert.

Als het project bijvoorbeeld de volgende schattingsregels voor onkosten heeft:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| Taak B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Taak C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Wanneer de gebruiker ervoor kiest om samen te vatten op **Transactieklasse**, wordt de volgende informatie geïmporteerd:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Wanneer de gebruiker ervoor kiest om samen te vatten op **Transactieklasse** en **Categorie**, wordt de volgende informatie geïmporteerd:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Wanneer de gebruiker ervoor kiest om samen te vatten op **Transactieklasse**, **Categorie** en **Bladknooppunttaak**, wordt de volgende informatie geïmporteerd. Merk op dat dit resultaat hetzelfde is als wat er in het project is:

| Opdracht | Categorie | Datum | Aantal | Prijs per eenheid | Bedrag |
| --- | --- | --- | --- | --- | --- |
| Taak A | Vliegticket | 10/1/2020 | 4 | 400 | 1600 |
| Taak B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Taak C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
