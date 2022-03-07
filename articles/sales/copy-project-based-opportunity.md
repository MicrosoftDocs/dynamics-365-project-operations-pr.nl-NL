---
title: Projectgebaseerde verkoopkansen kopiëren
description: Dit onderwerp bevat informatie over het kopiëren van projectgebaseerde verkoopkansen in Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 83fe41cb16be6bdd91219fc59e517ae0e5848afec5f771edde575bb5c24f9865
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999715"
---
# <a name="copy-project-based-opportunities"></a>Projectgebaseerde verkoopkansen kopiëren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


Projectgebaseerde verkoopkansen kunnen eenvoudig worden gekopieerd om nieuwe projectkansen te maken. 

1. Ga naar de lijstpagina **Projectgebaseerde verkoopkansen** en selecteer een verkoopkans in de lijst. U kunt ook de detailpagina van een specifieke verkoopkans openen. 
2. Selecteer op een van beide pagina's **Kopiëren**. Er wordt een dialoogvensterpagina geopend met de volgende veldinformatie. Afhankelijk van de waarden die u in dit dialoogvenster selecteert, kan het kopieerproces veranderen.

    | **Veld** | **Beschrijving** | **Downstreamimpact** |
    | --- | --- | --- |
    | Onderwerp | Voer het relevante onderwerp van de doelverkoopkans in. Wanneer het dialoogvenster wordt geopend, wordt het ingesteld op het onderwerp van de bronverkoopkans met **-kopie** eraan toegevoegd. | Er is geen impact op dit veld. |
    | Account | Verwijzingen naar de bedrijfs- of accountrecord van de klant. Wanneer het dialoogvenster wordt geopend, wordt deze ingesteld op de account in de bronverkoopkans. | Dit veld is de primaire klant in de verkoopkans. |
    | Contracterende eenheid | De organisatie-eenheid die verantwoordelijk is voor de oplevering van de projecten die bij deze deal horen. Wanneer het dialoogvenster wordt geopend, wordt deze ingesteld op de contracterende eenheid van de bronverkoopkans. | De contracterende eenheid is de bedrijfsdivisie die de projecten zal uitvoeren nadat de deal is gesloten. Elke contracterende eenheid heeft een valuta en deze valuta wordt gebruikt om de geschatte en werkelijke kosten te rapporteren die tijdens het project zijn gemaakt. |
    | Valuta | De valuta waarin de transacties voor de deal worden berekend. Wanneer de dialoogvensterpagina wordt geopend, wordt deze ingesteld op de valuta van de bronverkoopkans. | Valuta wordt gebruikt om een standaardprijslijst in te stellen en financiële schattingen voor de prijsopgave te maken. Uiteindelijk wordt de valuta gebruikt om de klant te factureren wanneer de deal is gewonnen. |
    | Prijzen kopiëren | Een Ja-/Nee-waarde waarmee wordt aangegeven of de prijzen van de verkoopkans moeten worden gekopieerd vanuit de bronverkoopkans. | Als **Ja** wordt geselecteerd, worden prijslijsten gekopieerd van de bron- naar de doelverkoopkans. Als **Nee** wordt geselecteerd, worden prijslijsten standaard ingesteld op basis van de laatste ingestelde prijslijsten. |

3. Selecteer **OK**. Er wordt een kopie gemaakt van de projectverkoopkans op basis van de geselecteerde parameters en de nieuwe projectgebaseerde verkoopkans wordt geopend.


[!INCLUDE[footer-include](../includes/footer-banner.md)]