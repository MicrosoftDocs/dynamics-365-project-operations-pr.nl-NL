---
title: Impact van werkelijke waarden in een opdracht met een vaste prijs
description: Dit artikel biedt informatie over de impact op de tabel Werkelijke waarden bij verschillende gebeurtenissen tijdens de levenscyclus van een opdracht met een vaste prijs in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918122"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Impact van werkelijke waarden in een opdracht met een vaste prijs

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

De volgende tabel biedt een overzicht van de werkelijke waarden van verschillende transactietypen die zijn gemaakt tijdens verschillende gebeurtenissen in een opdracht met een vaste prijs.

| Gebeurtenis | Werkelijke waarde voor kosten | Niet-gefactureerde werkelijke waarde voor verkoop | Gefactureerde werkelijke waarde voor verkoop | Voorbeeld |
|---|---|---|---|---|
| Tijd wordt gemaakt. | Niet van toepassing | Niet van toepassing | Niet van toepassing | <p>Bob Kozack, van de Amerikaanse organisatie-eenheid Fabrikam met een kostentarief van 100 Amerikaanse dollar (USD 100) per uur, werkt aan een project met de naam 'Installatie van arm bij Adatum'. Dit project is toegewezen aan een factureringsmethode met vaste prijs op de contractregel. Hier is een voorbeeld van een tijdsvermelding van Bob Kozak:</p><p>Bob Kozack - 8 uur</p> |
| Tijd wordt ingediend. | Niet van toepassing | Niet van toepassing | Niet van toepassing | Er wordt een kostendagboekregel gemaakt voor de tijdsvermelding. Het standaardkostentarief worden in de journaalpost ingevoerd. |
| De tijdsvermelding wordt ingetrokken voordat deze wordt goedgekeurd. | Niet van toepassing | Niet van toepassing | Niet van toepassing | |
| Tijd wordt goedgekeurd. | Er wordt een werkelijke kostprijs gemaakt. | Niet van toepassing | Niet van toepassing | <p>Er wordt een nieuwe werkelijke waarde gemaakt:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800</li></ul> |
| Goedkeuring van de tijdsvermelding wordt geannuleerd. | <p>De aanpassingsstatus van de oorspronkelijke werkelijke kostenwaarde wordt bijgewerkt naar **Aangepast**.</p><p>Er wordt een terugboeking van een werkelijke kostenwaarde gemaakt met een aanpassingsstatus **Niet-aanpasbaar**.</p> | Niet van toepassing | Niet van toepassing | <p>Bestaande werkelijke waarde die wordt bijgewerkt:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800, *Aangepast*</li></ul><p>Nieuwe werkelijke waarde die wordt gemaakt om de vorige financiële impact ongedaan te maken:</p><ul><li>**Werkelijke kosten:** Bob Kozack (8 uur), (USD 800), *Niet-aanpasbaar*</li></ul> |
| De tijdsvermelding wordt ingetrokken nadat deze wordt goedgekeurd. | <p>De aanpassingsstatus van de oorspronkelijke werkelijke kostenwaarde wordt bijgewerkt naar **Aangepast**.</p><p>Er wordt een terugboeking van een werkelijke kostenwaarde gemaakt met een aanpassingsstatus **Niet-aanpasbaar**.</p> | Niet van toepassing | Niet van toepassing | <p>Bestaande werkelijke waarde die wordt bijgewerkt:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800, *Aangepast*</li></ul><p>Nieuwe werkelijke waarde die wordt gemaakt om de vorige financiële impact ongedaan te maken:</p><ul><li>**Werkelijke kosten:** Bob Kozack (8 uur), (USD 800), *Niet-aanpasbaar*</li></ul> |
| Het contract wordt bevestigd. | <p>De aanpassingsstatus van de oude werkelijke kosten wordt bijgewerkt naar **Aangepast**.</p><p>Er wordt terugboekingen van werkelijke kostenwaarden gemaakt met een aanpassingsstatus **Niet-aanpasbaar**.</p><p>Er worden nieuwe werkelijke kostenwaarden gemaakt nadat de contractuele regels opnieuw zijn geëvalueerd.</p> | Niet van toepassing | Niet van toepassing | <p>Bestaande werkelijke waarde die wordt bijgewerkt:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800, *Aangepast*</li></ul><p>Nieuwe werkelijke waarde die wordt gemaakt om de vorige financiële impact ongedaan te maken:</p><ul><li>**Werkelijke kosten:** Bob Kozack (8 uur), (USD 800), *Niet-aanpasbaar*</li></ul><p>Er wordt een nieuwe werkelijke waarde gemaakt voor de opnieuw geëvalueerde financiële impact:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800</li></ul> |
| Er wordt een factuur gemaakt. | Niet van toepassing | Niet van toepassing | Niet van toepassing | |
| De factuur wordt bevestigd met een mijlpaal. | Niet van toepassing | Niet van toepassing | Er worden nieuwe op mijlpalen gebaseerde gefactureerde verkoopwaarden gemaakt. | <p>Bestaande werkelijke waarde die ongewijzigd blijft:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800</li></ul><p>Nieuwe werkelijke waarde die is gemaakt om de gefactureerde verkoopwaarden vast te leggen:</p><ul><li>**Gefactureerde werkelijke verkoopwaarde** Mijlpaal, USD 5000</li></ul> |
| De factuur wordt gecorrigeerd om de mijlpaal te crediteren. | Niet van toepassing | Niet van toepassing | Er worden terugboekingen voor twee gefactureerde werkelijke verkoopwaarden gemaakt. | <p>Bestaande werkelijke waarde die ongewijzigd blijft:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, 800 USD</li></ul><p>Bestaande werkelijke waarde die wordt bijgewerkt:</p><ul><li>**Gefactureerde werkelijke verkoopwaarde:** Mijlpaal, USD 5000, *Aangepast*</li></ul><p>Nieuwe werkelijke waarde die is gemaakt om de vorige gefactureerde verkoopwaarden terug te boeken:</p><ul><li>**Gefactureerde werkelijke verkoopwaarde:** Mijlpaal, (USD 5000), *Niet-aanpasbaar*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
