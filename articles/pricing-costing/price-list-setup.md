---
title: Prijslijsten instellen
description: Dit onderwerp bevat informatie over het instellen van kostprijs- en verkoopprijslijsten.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 000c22944b187b6250f2e982d73020028093fde6
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180186"
---
# <a name="set-up-price-lists"></a>Prijslijsten instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Prijslijsten in Dynamics 365 Project Operations vertegenwoordigen een catalogus met tarieven. In de tarieven worden kosten-, verkoop- en factureringstarieven uitgedrukt. Afhankelijk van of de prijslijst kostentarieven of verkoop- en factuurtarieven uitdrukt, is de context van de prijslijst **Verkoop** of **Kosten**.

De volgende uitbreidingen zijn specifiek voor Project Operations en worden toegepast op prijslijsten vanuit Dynamics 365 Sales.

- **Context**: dit veld heeft de ondersteunde waarden **Kosten** en **Verkoop**. De waarde **Inkoop** wordt niet ondersteund. Stel de context in op **Kosten** om een kostprijslijst te maken of op **Verkoop** voor een verkoopprijslijst. Kostprijslijsten zetten de prijs voor de kostensoort om in schattingen en werkelijke gegevens. Verkoopprijslijsten zetten de prijs voor geschatte en werkelijke records om van niet-gefactureerde en gefactureerde verkoopsoorten.
- **Tijdseenheid**: dit is de standaard tijdseenheid waarvoor de prijs is ingesteld in de gerelateerde tabel **Rolprijs** voor deze prijslijst.
- **Entiteit prijslijst**: dit verborgen veld wordt door Project Operations gebruikt om prijslijsten te onderscheiden die prijsopgave- of contractspecifiek zijn en die standaard en algemeen toepasbaar zijn.

## <a name="price-list-header"></a>Prijslijstkop

De volgende tabel bevat de velden op het tabblad **Algemeen** van een prijslijst die uniek zijn voor Project Operations of zich significant anders gedragen dan prijslijsten in Verkoop.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| Meetcriterium | Tabblad **Algemeen** en formulieren **Snelle invoer** | De identiteit van de prijslijst. | De prijslijst wordt weergegeven met deze waarde op alle lijstpagina's en opties van vervolgkeuzelijsten.|
| Context | Tabblad **Algemeen** en formulieren **Snelle invoer** | Dit veld kan worden ingesteld op **Kosten** of **Verkoop**. | Een prijslijst die is ingesteld op **Kosten**, wordt gebruikt om de prijs op te zoeken voor kostenramingen en werkelijke kosten. Een prijslijst die is ingesteld op **Verkoop**, wordt gebruikt om de prijs op te zoeken voor verkoopramingen en werkelijke verkoopkosten. Alleen prijslijsten waarvoor de context is ingesteld op **Verkoop**, kunnen worden toegevoegd aan projectprijslijsten voor klanten, projectprijsopgaven of projectcontracten. |
| Begindatum | Tabblad **Algemeen** en formulieren **Snelle invoer** | De startdatum van de periode waarin de prijslijst van kracht is. | Samen met het veld **Einddatum** wordt dit veld gebruikt om te bepalen welke prijslijst van toepassing is op een bepaalde schatting of werkelijke regel. |
| Einddatum | Tabblad **Algemeen** en formulieren **Snelle invoer** | De einddatum van de periode waarin de prijslijst van kracht is. | Samen met het veld **Begindatum** wordt dit veld gebruikt om te bepalen welke prijslijst van toepassing is op een bepaalde schatting of werkelijke regel. |
| Valuta | Tabblad **Algemeen** en formulieren **Snelle invoer** | Dit veld wordt gebruikt voor de standaardvaluta van elke rol, categorie of prijslijstartikelregel die samenhangt met deze prijslijst. | Voor **Verkoop** kunnen prijslijsten, rollen, categorieën of prijslijstartikelregels niet in een andere valuta dan deze valuta worden gemaakt. Voor **Kost** prijslijsten kunt u een rolprijsregel in elke valuta aanmaken. De valuta die hier wordt gedefinieerd, wordt als standaard gebruikt. De gebruikersinstellingen voor gerelateerde rolprijzen kunnen deze waarde overschrijven om het instellen van loonkosten in elke valuta mogelijk te maken. Categoriekostentarieven en prijslijstartikelkosten kunnen alleen worden ingesteld in de hier gedefinieerde valuta. |
| Tijdseenheid | Tabblad **Algemeen** en formulieren **Snelle invoer** | Dit veld wordt gebruikt voor de standaard tijdseenheid van elke rolregel die samenhangt met deze prijslijst. | Deze veldwaarde wordt alleen gebruikt bij het instellen van de gerelateerde rolprijs. In prijslijsten voor **Kosten** en **Verkoop** kunt u een rolprijsregel in elke tijdseenheid aanmaken. De tijdseenheid die hier wordt gedefinieerd, wordt als standaard gebruikt. De gebruikersinstellingen voor gerelateerde rolprijzen kunnen deze waarde overschrijven om het instellen van loonkosten en factuurtarieven in elke tijdseenheid mogelijk te maken. |
| Beschrijving | Tabblad **Algemeen** en formulieren **Snelle invoer** | Dit is een tekstveld waarmee u een beschrijving van meerdere regels kunt opgeven voor de prijslijst. | Dit veld wordt weergegeven in de **Gekoppelde** weergaven van de prijslijst in verschillende entiteiten die gerelateerde prijslijsten hebben. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]