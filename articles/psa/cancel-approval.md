---
title: Eerder goedgekeurde tijdsvermeldingen en onkostenposten annuleren
description: Dit onderwerp bevat informatie over het annuleren van een goedgekeurde projecttijd en onkostentransactie.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9e3bc94b626b88a2167e3a61472b768e2fb5c731
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590754"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Eerder goedgekeurde tijdsvermeldingen of onkostenposten annuleren

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In de nieuwste versie van Dynamics 365 Project Service Automation kunnen fiatteurs eerder goedgekeurde tijdsvermeldingen of onkostenposten annuleren.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Een eerder goedgekeurde tijdsvermelding of onkostenpost annuleren

Volg deze stappen om een eerder goedgekeurde tijdsvermelding of onkostenpost te annuleren.

1. Ga naar **Projecten** \> **Mijn werk** \> **Goedkeuringen**.
2. Wijzig op de lijstpagina **Goedkeuringen** de weergave in **Mijn eerdere goedkeuringen**. Er wordt een lijst weergegeven met de tijdsvermeldingen en onkostenposten die u eerder hebt goedgekeurd.
3. Selecteer een of meer vermeldingen of posten en selecteer vervolgens **Goedkeuring annuleren**. Er wordt een waarschuwingsbericht weergegeven.
4. Selecteer **OK** als u de goedkeuring wilt annuleren.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>De gevolgen van het annuleren van de goedkeuring van een tijdsvermelding of onkostenpost begrijpen

Wanneer een goedkeuring wordt geannuleerd, heeft dit zowel operationele als financiële gevolgen.

### <a name="operational-impact"></a>Operationele gevolgen

Wanneer een goedkeuring wordt geannuleerd, wordt de status van de record opnieuw ingesteld op **Concept** en wordt de goedkeuring niet meer weergegeven in de weergave **Mijn eerdere goedkeuringen**. In plaats daarvan wordt de geannuleerde goedkeuring weergegeven in de weergave **Tijdsvermeldingen voor goedkeuring** of **Onkostenposten voor goedkeuring**, afhankelijk van of het een tijdsvermelding of onkostenpost betreft. Bovendien wordt de status van de gerelateerde tijdsvermelding of onkostenpost gewijzigd in **Verzonden**, zodat de gerelateerde vermelding of post consistent is met goedkeuringen met de status **Concept.**

Als fiatteur kunt u enkele velden van een goedkeuring met de status **Concept** bewerken. Deze velden zijn **Factureringstype** en **Factureerbare uren voor tijdsvermeldingen**. Nadat u wijzigingen hebt aangebracht, kunt u de record opnieuw goedkeuren. U kunt deze ook afwijzen. Als u de goedkeuring van een tijdsvermelding afwijst, wordt de status van de vermelding gewijzigd in **Geretourneerd**. Als u de goedkeuring van een onkostenpost afwijst, wordt de status gewijzigd in **Afgewezen**. Functioneel gedragen geretourneerde en afgewezen posten en vermeldingen zich hetzelfde als een post of vermelding met de status **Concept**. Een lid van het projectteam kan de vereiste wijzigingen in de post/vermelding aanbrengen en deze vervolgens opnieuw indienen ter goedkeuring of de post/vermelding volledig verwijderen.

### <a name="financial-impact"></a>Financiële gevolgen

Een project wordt ook financieel beïnvloed wanneer een goedkeuring wordt geannuleerd. Ten eerste worden de corresponderende werkelijke waarden voor kosten en verkopen op de volgende manier bijgewerkt:

- De aanpassingsstatus wordt ingesteld op **Aangepast**.
- De factureringsstatus wordt ingesteld op **Geannuleerd**.

Vervolgens worden er stornoposten gemaakt in de tabel Werkelijke waarden. Om stornoposten te maken, kopieert het systeem de veldwaarden van de oorspronkelijke werkelijke waarden. De enige waarden die niet worden gekopieerd, zijn de hoeveelheidswaarden. In plaats daarvan worden deze waarden omgekeerd. Omgekeerde werkelijke waarden worden gemaakt voor de werkelijke waarden **Kosten** en **Niet-gefactureerde verkoop**. Het veld **Aanpassingsstatus** voor de omgekeerde werkelijke waarden wordt ingesteld op **Niet-aanpasbaar** en de factureringsstatus wordt ingesteld op **Geannuleerd**.

Als deze wijzigingen zijn doorgevoerd, komen de vastgelegde uitgaven voor het project en de omzetbacklog voor het project niet meer overeen met de bedragen die deze werkelijke waarden vertegenwoordigen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
