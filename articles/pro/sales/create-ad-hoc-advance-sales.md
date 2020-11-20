---
title: Een ad-hocvoorschot maken voor een contract - lite
description: Dit onderwerp bevat informatie over het maken van een voorschot op een contract als dat nodig is.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181356"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Een ad-hocvoorschot maken voor een contract - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

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
