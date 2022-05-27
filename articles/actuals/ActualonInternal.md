---
title: Impact van werkelijke waarden voor een intern project
description: Dit onderwerp biedt informatie over de impact op de tabel Werkelijke waarden bij verschillende gebeurtenissen voor een intern project in Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579760"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impact van werkelijke waarden voor een intern project

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

De volgende tabel biedt een overzicht van de werkelijke waarden van verschillende transactietypen die zijn gemaakt tijdens verschillende gebeurtenissen in een interne projectopdracht.

| Gebeurtenis | Werkelijke waarde voor kosten | Voorbeeld |
|---|---|---|
| Tijd wordt gemaakt. | Niet van toepassing | <p>Bob Kozack, van de Amerikaanse organisatie-eenheid Fabrikam met een kostentarief van 100 Amerikaanse dollar (USD 100) per uur, werkt aan een project met de naam 'Installatie van arm bij Adatum'. Dit project is toegewezen aan een factureringsmethode met vaste prijs op de contractregel. Hier is een voorbeeld van een tijdsvermelding van Bob Kozak:</p><p>Bob Kozack - 8 uur</p> |
| Tijd wordt ingediend. | Niet van toepassing | Er wordt een kostendagboekregel gemaakt voor de tijdsvermelding. Het standaardkostentarief worden in de journaalpost ingevoerd. |
| De tijdsvermelding wordt ingetrokken voordat deze wordt goedgekeurd. | Niet van toepassing | |
| Tijd wordt goedgekeurd. | Er wordt een werkelijke kostprijs gemaakt. | <p>Er wordt een nieuwe werkelijke waarde gemaakt:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800</li></ul> |
| De goedkeuring van de tijdsvermelding wordt geannuleerd. | <p>De aanpassingsstatus van de oorspronkelijke werkelijke kostenwaarde wordt bijgewerkt naar **Aangepast**.</p><p>Er wordt een terugboeking van een werkelijke kostenwaarde gemaakt met een aanpassingsstatus **Niet-aanpasbaar**.</p> | <p>Bestaande werkelijke waarde die wordt bijgewerkt:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800, *Aangepast*</li></ul><p>Nieuwe werkelijke waarde die wordt gemaakt om de vorige financiële impact ongedaan te maken:</p><ul><li>**Werkelijke kosten:** Bob Kozack (8 uur), (USD 800), *Niet-aanpasbaar*</li></ul> |
| De tijdsvermelding wordt ingetrokken nadat deze wordt goedgekeurd. | <p>De aanpassingsstatus van de oorspronkelijke werkelijke kostenwaarde wordt bijgewerkt naar **Aangepast**.</p><p>Er wordt een terugboeking van een werkelijke kostenwaarde gemaakt met een aanpassingsstatus **Niet-aanpasbaar**.</p> | <p>Bestaande werkelijke waarde die wordt bijgewerkt:</p><ul><li>**Werkelijke kosten:** Bob Kozack, 8 uur, USD 800, *Aangepast*</li></ul><p>Nieuwe werkelijke waarde die wordt gemaakt om de vorige financiële impact ongedaan te maken:</p><ul><li>**Werkelijke kosten:** Bob Kozack (8 uur), (USD 800), *Niet-aanpasbaar*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
