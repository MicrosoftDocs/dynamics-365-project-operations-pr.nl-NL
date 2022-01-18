---
title: Fout door onjuiste valuta
description: Dit onderwerp bevat informatie voor het oplossen van problemen met fout door een niet-overeenkomende valuta, die optreedt wanneer u specifieke recordtypen opslaat.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903393"
---
# <a name="currency-mismatch-error"></a>Fout door onjuiste valuta 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Wanneer u een project, contract, prijsopgave of boekbare resource opslaat, kan deze fout verschijnen: **Valuta van het bedrijf dat eigenaar is, komt niet overeen met de valuta van de contracterende eenheid. Kies een ander bedrijf als eigenaar of een andere contracterende eenheid voor het projectcontract om door te gaan**. De reden hiervoor is dat de valuta van de contracterende eenheid voor de record en de valuta van het bedrijf dat eigenaar is niet overeenkomen.


## <a name="resolution"></a>Oplossing

Ga als volgt te werk om dit probleem te omzeilen:
- Controleer de valuta van de contracterende eenheid voor deze record. U kunt de valuta zien door de record van de organisatie-eenheid te openen en de waarde te verifiëren op het tabblad **Algemeen** in het veld **Valuta**.
- Controleer de valuta van het bedrijf dat eigenaar is. U kunt de valuta zien door naar **Gerelateerd** > **Grootboeken** in de bedrijfsrecord te gaan. Dubbelklik op de grootboekrecord die aan het bedrijf is gekoppeld en controleer de waarde op het tabblad **Algemeen** in het veld **Valuta voor boekhouding**.

Als de valuta die is ingesteld in de contracterende eenheid en de grootboekrecord niet overeenkomen, past u de configuratie aan of selecteert u andere waarden wanneer u de record opslaat. Het systeem vereist dat deze records overeenkomen om correcte intercompany-factureringsstromen te garanderen. Voor meer informatie over de intercompany-configuraties, zie [Intercompany-transacties maken](../../project-accounting/create-intercompany-transactions.md).

Als de bedrijfsrecord geen gekoppelde grootboekrecord heeft, geeft dit aan dat er een configuratie ontbreekt bij het instellen van de omgeving. De configuratie moet worden gecorrigeerd door de systeembeheerder. De systeembeheerder moet naar **Configuraties voor dubbel schrijven** gaan en **Toewijzing voor dubbel schrijven grootboeken** stoppen en herstarten met de eerste synchronisatie van deze toewijzing en de bijbehorende vereisten. Zie voor meer informatie [Toewijzingsversies van dubbel wegschrijven voor Project Operations](../../environment/resource-dual-write-maps.md).
