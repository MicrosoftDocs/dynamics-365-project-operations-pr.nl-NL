---
title: De financiële administratie voor conceptfactuurvoorstellen voor projecten corrigeren
description: In dit onderwerp wordt uitgelegd hoe u gegevens met betrekking tot de financiële administratie voor een conceptfactuurvoorstel kunt aanpassen.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999310"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>De financiële administratie voor conceptfactuurvoorstellen voor projecten corrigeren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

*Operationele details* voor projectfacturen worden door de projectmanager onderhouden op een pro-formafactuur. Deze details omvatten de beslissing over de uren, onkosten, materialen of mijlpalen die moeten worden gefactureerd, de tarieven en de toepassing van vooruitbetalings- en voorschotbedragen. Nadat u de oorspronkelijke pro-formafactuur hebt bevestigd, kunt u de operationele details aanpassen door een [corrigerende pro-formafactuur](../proforma-invoicing/corrective-invoices.md) te maken en te bevestigen.

*Details financiële administratie* voor projectfacturen worden onderhouden in een klantgericht factuurdocument. Deze details omvatten de btw-berekening en de financiële dimensies die op de factuur worden toegepast. Dit onderwerp bevat details over hoe deze gegevens van de financiële administratie kunnen worden aangepast op een conceptfactuurvoorstel voor een project.

## <a name="adjust-sales-tax"></a>Btw aanpassen

Standaard btw-groepen voor facturering en btw-groepen voor artikelen kunnen rechtstreeks in het factuurvoorsteldocument worden aangepast. Als u deze groepen wilt aanpassen, selecteert u **Bewerken** en voert u vervolgens op elke regel van een projectfactuurvoorstel een nieuwe waarde in het veld **Btw-groep** of **Btw-groep artikel** in.

## <a name="adjust-financial-dimensions"></a>Financiële dimensies aanpassen

Financiële dimensies kunnen niet rechtstreeks op een regel van een projectfactuurvoorstel worden bewerkt. Voer in plaats daarvan de volgende stappen uit om financiële dimensies voor een projectfactuurvoorstel aan te passen.

1. Selecteer op het projectfactuurvoorstel **Alles verwijderen** om de regels van het projectfactuurvoorstel te verwijderen.

    > [!NOTE]
    > De knop **Alles verwijderen** is alleen beschikbaar nadat de systeembeheerder de functie **Factuurvoorstelregels verwijderen wanneer Project Operations wordt gebruikt voor scenario´s op basis van resources/niet-voorradige artikelen** in de werkruimte **Functiebeheer** heeft ingeschakeld.

2. De financiële dimensies aanpassen:

    - **Transacties op rekening (mijlpalen voor facturering)**: ga naar **Alle projecten** \> **Beheren** \> **Transacties op rekening** en selecteer de mijlpaal die moet worden aangepast. Werk vervolgens op het tabblad **Financiële dimensies** de waarden indien nodig bij.
    - **Tijd-, onkosten- en materiaaltransacties**: selecteer op de pagina **Geboekte projecttransacties** **Financiële administratie aanpassen** om de financiële dimensies bij te werken.

3. Nadat u klaar bent met het aanpassen van de financiële dimensiewaarden, gaat u naar **Projectbeheer en financiële administratie** \> **Periodiek** \> **Integratie Project Operations** en selecteert u **Importeren uit opslagtabel** om het periodieke proces uit te voeren. In dat proces worden de bijgewerkte financiële dimensiewaarden gebruikt om de regels van projectfactuurvoorstellen opnieuw te maken. De bijgewerkte waarden worden vervolgens gebruikt in het projectsubgrootboek en het grootboek wanneer de projectfactuur wordt geboekt.
