---
title: Een ad-hocvoorschot maken voor een contract
description: Dit onderwerp bevat informatie over het maken van een voorschot op een contract als dat nodig is.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 51e3b0ac8e111be70fe6ad0f9c162dfaec3339ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003490"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Een ad-hocvoorschot maken voor een contract

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Microsoft Dynamics 365 Project Operations ondersteunt factureringsscenario's met vooruitbetalingen en voorschotten. Het proces voor het gebruik van **Vooruitbetalingen** in **Project Operations** is vergelijkbaar met contracten met **Voorschotten**. 

Voer de volgende stappen uit om een voorschot aan de klant te factureren.

1. Ga naar de pagina **Projectcontract** en selecteer vervolgens het tabblad **Vooruitbetalingen en voorschotten**.
2. Selecteer in het subraster met alle eerder geboekte voorschotten en vooruitbetalingen **+ Nieuw voorschot voor projectcontract**. 

    het formulier **Snelle invoer** wordt geopend voor het vastleggen van een vooruitbetaling of voorschot.
    
3. In de onderstaande tabel staan de velden voor het vastleggen van een voorschot en de overwegingen bij het maken van nieuwe:

    | Veld | Beschrijving | Downstreamimpact |
    | --- | --- | --- |
    | **Projectcontractklant** | Dit veld geeft aan welke klant op het contract dit voorschot in rekening zal worden gebracht. | Als er meerdere klanten in het contract staan en u aan elk van hen een specifiek vooruitbetaling of voorschotbedrag wilt factureren, maakt u voor elke klant afzonderlijk een voorschot. |
    | **Beschrijving** | De beschrijving van het doel of de timing van het voorschot om dit voorschot te helpen identificeren. | Deze omschrijving wordt weergegeven op de factuurregel voor dit voorschot. |
    | **Bedrag** | Het bedrag voor de vooruitbetaling of het voorschot. | Dit bedrag wordt weergegeven op de factuurregel voor dit voorschot. |
    | **Factuurdatum** | De datum waarop dit voorschot aan de klant wordt gefactureerd. | Dit is de datum voor het automatische aanmaakproces van facturen om een factuurregel voor dit voorschot te creëren. |
    | **Factuurstatus** | Dit is een optie-instelling die aangeeft of dit voorschot wordt toegevoegd aan een conceptfactuur voor deze klant. De mogelijke waarden zijn:</br>- **Niet gereed voor facturering**</br>- **Gereed voor facturering** | Wanneer een voorschot of vooruitbetaling is gemarkeerd als **Gereed voor facturering**, wordt het toegevoegd als een regeltijd in een conceptfactuur. Alleen een volledig gefactureerd voorschot kan worden gebruikt om af te stemmen met projectkosten voor de volgende factuurperiode. |

4. Selecteer **Opslaan en sluiten** in het dialoogvenster Snelle invoer om het voorschot of de vooruitbetaling te registreren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]