---
title: Uitgavenoverzicht van onderzoek naar federale subsidies
description: Dit onderwerp bevat informatie over het uitgavenoverzicht van onderzoek naar federale subsidies.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288958"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Uitgavenoverzicht van onderzoek naar federale subsidies

[!include [banner](../includes/banner.md)]

Volgens Office of Management and budget Circular A-133 zijn agentschappen die overheidsfondsen ontvangen, onderworpen aan auditvereisten, ook wel bekend als eenmalige audits. Het auditproces wordt gebruikt om op periodiek te rapporteren over de inkomsten en uitgaven van federale subsidies. Een deel van het auditrapport omvat het uitgavenoverzicht van federale subsidies (SEFA).

Het uitgavenoverzicht van het onderzoek naar federale subsidies omvat de titel en het nummer van de Catalog of Federal Domestic Assistance (CFDA), het nummer van de subsidie, het jaar van de subsidie, de naam van de federale instantie die de fondsen verstrekt en de naam van de doorgifte-entiteit. Het onderzoek geldt voor een bepaalde periode. Meestal is die periode hetzelfde als de financiële overzichtsperiode, dus een fiscaal jaar.

Het onderzoek heeft betrekking op subsidies met projectiedatums in het geselecteerde datumbereik. De kolom met het **uitgiftebureau** van het onderzoek toont de subsidieontvanger of, voor een doorgegeven subsidie, het subsidieverstrekker. Voor een doorgegeven subsidie bevat de kolom **Doorgiftebureau** de naam van de subsidieontvanger. Als het niet om een doorgegeven subsidie gaat, is de kolom **Doorgiftebureau** leeg.

## <a name="set-up-the-cfda-clusters"></a>CFDA-clusters instellen

U moet de CFDA-clusters instellen die kunnen worden gekoppeld aan de CFDA-nummers in het uitgavenoverzicht van het onderzoek naar federale subsidies.

1. Ga naar **Projectmanagement en financiële administratie \> Instellen \> Subsidies \> CFDA-clusters**.
2. Selecteer **Nieuw** om een CFDA-cluster (Catalog of Federal Domestic Assistance) te maken.
3. Voer de clusternaam in.
4. Selecteer **Opslaan** om uw wijzigingen op te slaan.

## <a name="set-up-cfda-numbers"></a>CFDA-nummers instellen

U moet de CFDA-nummers instellen die kunnen worden toegevoegd aan subsidies en opgenomen in het uitgavenoverzicht van het onderzoek naar federale subsidies.

1. Ga naar **Projectmanagement en financiële administratie \> Instellen \> Subsidies \> CFDA-nummers**.
2. Selecteer **Nieuw** als u een CFDA-nummer wilt maken.
3. Voer in de kolom **Nummer** het CFDA-nummer in.
4. Druk de **Tab**-toets.
5. Voer in de kolom **Beschrijving** de CFDA-titel in.
6. Druk de **Tab**-toets.
7. Optioneel: voeg in het veld **Programmacluster** de juiste CFDA-cluster toe.
8. Selecteer **Opslaan** om uw wijzigingen op te slaan.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Stel in voor welke subsidies moet worden gerapporteerd in het onderzoek naar het uitgavenoverzicht van federale subsidies

1. Ga naar **Projectmanagement en financiële administratie \> Subsidies \> Subsidies** en selecteer een bestaande subsidie.
2. Wijs op het sneltabblad **Instellen** in het veld **Catalog of Federal Domestic Assistance** het CFDA-nummer toe. Het CFDA-nummer van de subsidie bepaalt de CFDA-cluster voor rapportage.
3. Voer op het sneltabblad **Contactgegevens** de gegevens in van de subsidieverstrekker door deze stappen te volgen:

    1. Voer in het veld **Subsidieontvanger** de klant in die verantwoordelijk is voor de subsidie. Voor een bestaande subsidie is deze informatie mogelijk al ingevoerd.
    2. Geef aan of de subsidieontvanger de financier is. Als de subsidieontvanger de financier is, laat u het selectievakje **Doorgeven** uitgeschakeld. Als een andere klant de financier is en de subsidieontvanger verantwoordelijk is voor het uitgeven en bijhouden van het geld, selecteert u het selectievakje **Doorgeven**.

4. Als u het selectievakje **Doorgeven** in de vorige stap hebt ingeschakeld, voert u bij **Subsidieverstrekker** de klant in die de subsidie heeft verstrekt. Het subsidieverstrekker en de subsidieontvanger kunnen niet dezelfde klant zijn.

Dit is een voorbeeld van een doorgegeven subsidie:

De federale overheid financiert een infrastructuurproject voor een staat. De federale overheid verstrekt het geld aan de staat om te besteden. In dit geval is de federale overheid de subsidieverstrekker en de staat de subsidieafnemer.

> [!NOTE] 
> Wanneer u de functie voor het eerst inschakelt, worden de eerste CFDA-nummers ingevoerd met behulp van de bestaande nummers op subsidies.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Subsidies uitsluiten van SEFA-rapportage op basis van het type subsidie

1. Ga naar **Projectmanagement en financiële administratie \> Instellen \> Subsidies \> Subsidietypes**.
2. Schakel op het sneltabblad **Standaardinformatie** het selectievakje **Uitsluiten van uitgavenoverzicht van federale subsidies** in.
3. Selecteer **Opslaan** om uw wijzigingen op te slaan.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Het onderzoek naar het uitgavenoverzicht van federale subsidies uitvoeren

1. Ga naar **Projectmanagement en financiële administratie \> Rapporten en informatieverzoeken \> Informatieverzoek voor subsidies \> Uitgavenoverzicht van federale subsidies**.
2. Volg deze stappen in de sectie **Parameters**:

    1. Selecteer in het veld **Datuminterval** de code voor het datuminterval. Of bepaal het datuminterval in de velden **Begindatum** en **Einddatum**.
    2. Optioneel: als u alleen gefactureerde transacties als omzet in de aanvraag wilt opnemen, stelt u de optie **Alleen gefactureerde omzet opnemen** in op **Ja**.

## <a name="columns"></a>Kolommen

Het onderzoek naar het uitgavenoverzicht van federale subsidies omvat de volgende kolommen:

- Naam van Catalog of Federal Domestic Assistance-cluster
- Subsidieverstrekker
- Doorgiftebureau
- Subsidienaam
- Subsidie-id
- Id subsidieaanvraag
- Catalog of Federal Domestic Assistance
- Betalingsbewijzen
- Uitgaven


[!INCLUDE[footer-include](../includes/footer-banner.md)]