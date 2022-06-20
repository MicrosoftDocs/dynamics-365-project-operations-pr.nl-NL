---
title: De financiële administratie voor conceptfactuurvoorstellen voor projecten corrigeren
description: In dit artikel wordt uitgelegd hoe u boekhoudkundige informatie op een concept-factuurvoorstel kunt aanpassen.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921204"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>De financiële administratie voor conceptfactuurvoorstellen voor projecten corrigeren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

*Operationele details* voor projectfacturen worden door de projectmanager onderhouden op een pro-formafactuur. Deze details omvatten de beslissing over de uren, onkosten, materialen of mijlpalen die moeten worden gefactureerd, de tarieven en de toepassing van vooruitbetalings- en voorschotbedragen. Nadat u de oorspronkelijke pro-formafactuur hebt bevestigd, kunt u de operationele details aanpassen door een [corrigerende pro-formafactuur](../proforma-invoicing/corrective-invoices.md) te maken en te bevestigen.

*Details financiële administratie* voor projectfacturen worden onderhouden in een klantgericht factuurdocument. Deze details omvatten de btw-berekening en de financiële dimensies die op de factuur worden toegepast. In dit artikel leest u hoe u deze boekhoudgegevens kunt aanpassen op een concept-projectfactuurvoorstel.

## <a name="adjust-sales-tax"></a>Btw aanpassen

Standaard btw-groepen voor facturering en btw-groepen voor artikelen kunnen rechtstreeks in het factuurvoorsteldocument worden aangepast. Als u deze groepen wilt aanpassen, selecteert u **Bewerken** en voert u vervolgens op elke regel van een projectfactuurvoorstel een nieuwe waarde in het veld **Btw-groep** of **Btw-groep artikel** in.

## <a name="adjust-financial-dimensions"></a>Financiële dimensies aanpassen

### <a name="header-dimensions"></a>Koptekstdimensies

Standaard worden financiële dimensies voor facturen afgeleid van de niet-gefactureerde projecttransactierecords die worden gefactureerd. Met systeeminstellingen kunt u echter financiële dimensies in de koptekst van projectfactuurvoorstellen gebruiken om klantsaldi te boeken. Als u deze functionaliteit wilt inschakelen, selecteert u **Updates van projectdimensies voor klanten toestaan** op het tabblad **Financiële gegevens** van de pagina **Projectbeheer- en boekhoudingsparameters**.

Financiële dimensies op factuurkopteksten kunnen worden bewerkt voordat een factuur wordt geboekt. Ga op de pagina **Projectfactuurvoorstel** naar de weergave **Koptekst** en bewerk vervolgens waarden bewerken op het tabblad **Financiële dimensies**.

De weergave **Koptekst** is alleen beschikbaar nadat het systeembeheerder de functie **Formulieren voor projectfactuurvoorstel en factuurjournaal gebruiken met de weergave Koptekst en Regels** heeft ingeschakeld in de werkruimte **Functiebeheer**. Voor deze functie is Finance-update 10.0.25 of hoger vereist.

### <a name="line-dimensions"></a>Regel dimensies

Financiële dimensies kunnen niet rechtstreeks op een regel van een projectfactuurvoorstel worden bewerkt. Voer in plaats daarvan de volgende stappen uit om financiële dimensies voor een projectfactuurvoorstel aan te passen.

1. Selecteer op het projectfactuurvoorstel **Alles verwijderen** om de regels van het projectfactuurvoorstel te verwijderen.

    De knop **Alles verwijderen** is alleen beschikbaar nadat de systeembeheerder de functie **Factuurvoorstelregels verwijderen wanneer Project Operations wordt gebruikt voor scenario´s op basis van resources/niet-voorradige artikelen** in de werkruimte **Functiebeheer** heeft ingeschakeld.

2. De financiële dimensies aanpassen:

    - **Transacties op rekening (mijlpalen voor facturering)**: ga naar **Alle projecten** \> **Beheren** \> **Transacties op rekening** en selecteer de mijlpaal die moet worden aangepast. Werk vervolgens op het tabblad **Financiële dimensies** de waarden indien nodig bij.
    - **Tijd-, onkosten- en materiaaltransacties**: selecteer op de pagina **Geboekte projecttransacties** **Financiële administratie aanpassen** om de financiële dimensies bij te werken.

3. Nadat u klaar bent met het aanpassen van de financiële dimensiewaarden, gaat u naar **Projectbeheer en financiële administratie** \> **Periodiek** \> **Integratie Project Operations** en selecteert u **Importeren uit opslagtabel** om het periodieke proces uit te voeren. In dat proces worden de bijgewerkte financiële dimensiewaarden gebruikt om de regels van projectfactuurvoorstellen opnieuw te maken. De bijgewerkte waarden worden vervolgens gebruikt in het projectsubgrootboek en het grootboek wanneer de projectfactuur wordt geboekt.
