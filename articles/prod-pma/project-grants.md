---
title: Projectsubsidies
description: In dit onderwerp wordt uitgelegd hoe u een subsidie kunt aanmaken of wijzigen.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074745"
---
# <a name="project-grants"></a>Projectsubsidies

[!include [banner](../includes/banner.md)]

Een subsidie is een geldschenking voor een specifiek doel of project. Meestal zijn er beperkingen aan de manier waarop een subsidie kan worden besteed. In Projectbeheer en financiële administratie kunt u subsidies invoeren en volgen, en hun relaties voor projecten en projectcontracten definiëren. U kunt bijvoorbeeld de volgende taken uitvoeren:

- Koppel subsidies aan projecten en financieringsbronnen via koppelingen naar de pagina's **Project** en **Projectcontractdetails**.
- Voer wijzigingen in een subsidie in en volg ze bij de overgang van de ene status naar de andere.
- Voer kosten, aangevraagde bedragen en toegekende bedragen in en houd ze bij.
- Maak hoofdsubsidies en koppel er subbedragen aan.

U kunt een subsidie aanmaken door alle details in een nieuw record in te voeren, of u kunt de details van een bestaande subsidie kopiëren en deze vervolgens bijwerken.

## <a name="create-a-new-grant"></a>Een nieuwe subsidie maken

1. Ga naar **Projectmanagement en financiële administratie** \> **Subsidies** \> **Subsidies**.
2. Selecteer **Nieuw** \> **Subsidie**.
3. Voer op de pagina met subsidiedetails op het sneltabblad **Algemeen** in het veld **Subsidie-id** een alfanumerieke id in voor de subsidie.
4. Typ een naam voor de subsidie in het veld **Subsidie**.
5. Voeg in het veld **Omschrijving** details toe over de nieuwe subsidie.

    De meeste andere velden op de pagina zijn optioneel en u kunt zo weinig of zo veel informatie invoeren als u wilt.

    De volgende lijst beschrijft de informatie die wordt gespecificeerd op elk sneltabblad van de pagina met subsidiedetails:

    - **Algemeen** : voer de naam, de status, de beschrijving, het doel en het bedrag van de subsidie in.
    - **Contactgegevens** : voer details in over personeelsleden, de afdeling die de subsidie beheert en de subsidieontvanger of organisatiebron van de subsidie. U kunt ook aangeven of uw organisatie een doorgeefentiteit is die de subsidie ontvangt en deze vervolgens doorgeeft aan een andere ontvanger. Selecteer **Toevoegen** om contactgegevens toe te voegen, zoals telefoonnummers en e-mailadressen voor de organisatie die de subsidie verstrekt.
    - **Datums en deadlines** : vul datums in die betrekking hebben op de subsidie en de subsidieaanvraag. Voorbeelden zijn de vervaldatum van de aanvraag, de datum van indiening en de datum waarop de subsidie wordt goedgekeurd of afgewezen.
    - **Bijbehorende projecten en projectcontracten** : u kunt alleen informatie op dit sneltabblad invoeren als het veld **Subsidiestatus** op het sneltabblad **Algemeen** is ingesteld op **Actief** of **Toegekend**. Selecteer een van de volgende opties om de gerelateerde taak te voltooien:

        - **Financieringsbron toevoegen** : voeg een nieuwe financieringsbron toe voor de subsidie. U kunt nu alle details invoeren of u kunt de standaardinformatie gebruiken en deze later bijwerken.
        - **Projectcontract toevoegen** : toevoegen of bijwerken van projectcontractinformatie.
        - **Project toevoegen** : projectdetails toevoegen of bijwerken.

    - **Instellen** : voer details in over het afstemmen van de financiering, als deze informatie vereist is. Veel organisaties die subsidies toekennen, eisen dat ontvangers een bepaald bedrag van hun eigen geld of middelen uitgeven, dat overeenkomt met het bedrag dat in de subsidie wordt toegekend. In het veld **Lokaal project of tracking-id** kunt u een id invoeren die verschilt van de project-id.

        > [!NOTE]
        > Als een deel van de subsidie aan een andere organisatie wordt toegekend, stelt u de optie **Subontvanger** in op **Ja**. Voor subsidies die in de Verenigde Staten worden toegekend, kunt u aangeven of een subsidie zal worden toegekend onder een staatsmandaat of een federaal mandaat.

    - **Opnamegegevens** : informatie toevoegen of bijwerken over hoe vaak subsidiegelden kunnen worden opgenomen, gefactureerd of uitgegeven.

## <a name="create-a-new-grant-from-a-copy"></a>Een nieuwe subsidie maken op basis van een kopie

1. Ga naar **Projectmanagement en financiële administratie** \> **Subsidies** \> **Subsidies**.
2. Selecteer **Nieuw** \> **Kopiëren van subsidie**.
3. Voer een alfanumerieke identificatie en een naam in voor de nieuwe subsidie, en selecteer vervolgens **OK**.
4. Bekijk op de pagina met subsidiegegevens de details van de gekopieerde subsidie en breng de nodige wijzigingen aan. De meeste velden op de pagina zijn optioneel.

## <a name="view-or-modify-grant-details"></a>Details van subsidie bekijken of wijzigen

1. Ga naar **Projectmanagement en financiële administratie** \> **Subsidies** \> **Subsidies**.
2. Selecteer de subsidie die u wilt wijzigen.
3. Ga naar het actievenster en selecteer op het tabblad **Subsidie** in de groep **Onderhouden** de optie **Bewerken**.
4. Bekijk de details van de subsidie en breng de nodige wijzigingen aan.
