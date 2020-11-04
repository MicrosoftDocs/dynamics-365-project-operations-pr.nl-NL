---
title: Een voorschot of een vooruitbetaling factureren
description: Dit onderwerp bevat informatie over hoe u een voorschot of een vooruitbetaling factureert in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ed3b71d5f0ac035403de9fa213f3f45d14038e0
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087874"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Een voorschot of een vooruitbetaling factureren

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations ondersteunt contracten op basis van voorschotten en eenmalige vooruitbetalingen. In een projectcontract kunt u een schema van voorschotten of een eenmalige vooruitbetaling registreren. Registratie op projectcontractniveau maakt een voorschot of een vooruitbetaling echter niet direct beschikbaar voor gebruik. Als u een voorschot of een vooruitbetaling wilt gebruiken voor een factuur die daadwerkelijk bij de klant in rekening wordt gebracht, moet het voorschot of de vooruitbetaling eerst worden gefactureerd.

Voer de volgende stappen uit om een voorschot of een vooruitbetaling te factureren.

1. Selecteer **Verkoop** > **Facturering** > **Voorschotten en vooruitbetalingen**. 
2. Gebruik op de pagina **Vooruitbetalingen en voorschotten** het filter om het specifieke voorschot of de specifieke vooruitbetaling te selecteren dat/die u wilt factureren en markeer dit als **Gereed voor facturering**.
3. Maak handmatig een factuur via de lijstpagina of detailpagina **Projectcontract**. Het voorschot of de vooruitbetaling wordt weergegeven op de conceptfactuur in de sectie **Vooruitbetalingen en voorschotten** op de pagina **Factuur**.
4. Bevestig de factuur. Dit maakt het voorschot of de vooruitbetaling beschikbaar voor gebruik. U kunt de factuur verifiëren op de lijstpagina **Voorschotten en vooruitbetalingen**. Voor een gefactureerd voorschot of een gefactureerde vooruitbetaling wordt het beschikbare bedrag in het raster weergegeven.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Een voorschot of vooruitbetaling via het factuurraster maken

U kunt een voorschot of een vooruitbetaling rechtstreeks op een factuur maken.

1. Selecteer op een conceptfactuur in het subraster **Voorschotten en vooruitbetalingen** **Nieuw** om een nieuw voorschot of een nieuwe vooruitbetaling te maken. 
2. Op de pagina **Snel maken** voegt u de benodigde informatie toe en selecteert u vervolgens **Opslaan**. Het voorschot of de vooruitbetaling wordt op het projectcontract gemaakt dat aan de factuur is gerelateerd. Het voorschot of de vooruitbetaling wordt automatisch gemarkeerd als **Gereed voor facturering** en vervolgens toegevoegd aan het subraster **Vooruitbetalingen en voorschotten** op de pagina **Factuur**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Een gefactureerd voorschot of een gefactureerde vooruitbetaling afstemmen

Nadat een voorschot of vooruitbetaling is gefactureerd, kunnen deze worden gebruikt of afgestemd op een factuur met tijd, onkosten, mijlpalen of andere projectgebaseerde kosten. Klanten zien hun factuurbedrag verminderd met het voorschot- of vooruitbetalingsbedrag dat op deze factuur is gebruikt.

Op elke factuur die wordt gegenereerd voor een projectcontract dat gefactureerde voorschotten of vooruitbetalingen heeft, past Project Operations automatisch het voorschot of de vooruitbetaling op de factuur toe.

Dit is te zien in het raster **Toegepaste voorschotten en vooruitbetalingen** op de pagina **Factuur**. De volgende tabel bevat informatie over de velden in het raster **Toegepaste voorschotten en vooruitbetalingen** van de pagina **Projectfactuur**.

| Veld | Locatie | Relevantie, doel en richtlijnen | Downstreamimpact |
| --- | --- | --- | --- |
| Beschrijving | Dit is te zien in het raster **Toegepaste voorschotten en vooruitbetalingen** op de pagina **Projectfactuur**. |Dit alleen-lezen veld geeft een beschrijving van het voorschot dat of de vooruitbetaling die op deze factuur wordt gebruikt. Deze waarde kan niet worden gewijzigd op de factuur. Deze waarde kan worden bijgewerkt in het subraster op de pagina **Projectcontract**. | Dit veld kan aan de klant op de afgedrukte factuur worden weergegeven om aan te geven welk voorschot of welke vooruitbetaling op de factuur wordt toegepast. |
| Afgeleverd op | Dit is te zien in het raster **Toegepaste voorschotten en vooruitbetalingen** op de pagina **Projectfactuur**.  | Dit alleen-lezen veld bevat de factuurdatum van het voorschot dat of de vooruitbetaling die op deze factuur wordt gebruikt. Deze waarde kan niet worden gewijzigd op de factuur. Deze waarde kan worden bijgewerkt in het subraster op de pagina **Projectcontract**. | Dit veld kan aan de klant op de afgedrukte factuur worden weergegeven om de datum aan te geven waarop het voorschot of de vooruitbetaling voor het eerst aan de klant is gefactureerd. |
| Bedrag | Dit is te zien in het raster **Toegepaste voorschotten en vooruitbetalingen** op de pagina **Projectfactuur**.  | Dit alleen-lezen veld bevat het bedrag van het voorschot dat of de vooruitbetaling die op deze factuur wordt gebruikt. Deze waarde kan niet worden gewijzigd op de factuur. Deze waarde kan worden bijgewerkt in het subraster op de pagina **Projectcontract**. | Dit veld kan aan de klant op de afgedrukte factuur worden weergegeven om het oorspronkelijke bedrag aan te geven van het voorschot dat of de vooruitbetaling die door de klant is betaald. |
| Gebruikt bedrag | Dit is te zien in het raster **Toegepaste voorschotten en vooruitbetalingen** op de pagina **Projectfactuur**.  | Dit alleen-lezen veld bevat de berekende waarde die samenvat hoeveel van het voorschot of de vooruitbetaling is gebruikt. | Dit veld kan aan de klant op de afgedrukte factuur worden weergegeven om het reeds gebruikte bedrag van het voorschot of de vooruitbetaling aan te geven. |
| Berekend bedrag | Dit is te zien in het raster **Toegepaste voorschotten en vooruitbetalingen** op de pagina **Projectfactuur**.  | Dit bewerkbare veld bevat het bedrag van het voorschot dat of de vooruitbetaling die op deze projectfactuur wordt gebruikt. Dit bedrag kan niet hoger zijn dan het bedrag dat beschikbaar is in de vooruitbetaling. Dit wordt automatisch berekend als het verschil tussen de velden **Bedrag** en **Gebruikt bedrag** in het raster. U kunt deze hoeveelheid verlagen om minder te gebruiken dan wat beschikbaar is, maar u kunt de hoeveelheid niet verhogen om meer te gebruiken dan wat beschikbaar is. | Dit veld kan aan de klant op de afgedrukte factuur worden weergegeven om het op de factuur gebruikte bedrag van het voorschot of de vooruitbetaling aan te geven. |
| Saldobedrag van voorschot. | Dit is te zien in het raster **Toegepaste voorschotten en vooruitbetalingen** op de pagina **Projectfactuur**.  | Dit alleen-lezen veld geeft de waarde aan van hoeveel van het voorschot of de vooruitbetaling er overblijft nadat de factuur is bevestigd. | Dit veld kan aan de klant op de afgedrukte factuur worden weergegeven om het bedrag aan te geven dat overblijft van dit voorschot of deze vooruitbetaling nadat de factuur is bevestigd en betaald. |
