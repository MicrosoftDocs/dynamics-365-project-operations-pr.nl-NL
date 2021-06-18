---
title: Geavanceerde contracten maken voor facturering op basis van voortgang
description: In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt genereren op basis van een percentage voltooid werk.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999665"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Geavanceerde contracten maken voor facturering op basis van voortgang
[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt maken op basis van een percentage voltooid werk. Factuurbedragen worden automatisch berekend voor de budgetcategorieën van werk dat u voor een project instelt. De timing van de factuur wordt bepaald wanneer u over het projectcontract met de klant onderhandelt.

Gebruik de procedures in dit onderwerp om een contract, een bijbehorend project en de factureringsregels op te stellen waarmee de factuurbedragen worden berekend voor de budgetcategorieën met werk die u voor het project instelt.

Nadat u het contract en het project hebt aangemaakt, kunt u de details van het project instellen. U kunt bijvoorbeeld activiteiten definiëren en werknemers aan het project toewijzen.

## <a name="example"></a>Voorbeeld

Uw organisatie is een softwareontwikkelingsbedrijf. U stemt ermee in om een salarisadministratiepakket voor een klant te ontwikkelen voor een totaalbedrag van 20.000 USD. Uw organisatie stemt ermee in om de klant te factureren wanneer u bepaalde percentages van het project voltooit. U stelt de volgende projectcategorieën in voor het werk, zodat u deze kunt gebruiken in het facturatieproces:

- Consultancy
- Ontwerp
- Installatie

U stelt ook factureringsregels in waarmee automatisch de factuurbedragen worden berekend voor het percentage projectwerk dat in elke categorie is voltooid.

De budgetmanager maakt een budget voor de projectcategorieën. De hoeveelheid voltooid werk wordt automatisch berekend als een percentage van het werkelijke werk in vergelijking met de gebudgetteerde bedragen.

## <a name="prerequisites"></a>Vereisten

Voordat u een project maakt dat factureringsregels gebruikt, moet u de nummerreeksen voor factureringsregels en een kostenjournaal instellen dat wordt gebruikt om voortgangsfacturen te boeken.

1. Ga naar **Projectmanagement en financiële administratie** \> **Instellen** \> **Parameters voor Projectmanagement en financiële administratie**.
2. Op de pagina **Parameters voor Projectmanagement en financiële administratie** stelt u op het tabblad **Nummerreeksen** de nummerreeks in die u wilt gebruiken wanneer factureringsregels worden gemaakt.
3. Ga naar **Projectmanagement en financiële administratie** \> **Journalen** \> **Vergoeding**.
4. Selecteer op de pagina **Kostenjournaal** de optie **Nieuw** en voer de journaalnaam in.

## <a name="create-a-contract-for-progress-billings"></a>Een contract maken voor voortgangsfacturen

Gebruik deze procedure om een projectcontract te creëren voor een project met een vaste prijs. U maakt een projectfactuur aan wanneer het werk dat aan het project is voltooid een bepaald percentage bereikt.

1. Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Projectcontracten**.
2. Selecteer op de pagina **Projectcontracten** de optie **Nieuw**.
3. Stel in het dialoogvenster **Nieuw projectcontract** de volgende velden in:

    - **Name**
    - **Type financiering**
    - **Financieringsbron**
    - **Verkoopvaluta**: standaard wordt deze valuta gebruikt voor klantfacturen die aan het projectcontract zijn gekoppeld. U kunt de verkoopvaluta echter op een specifieke klantfactuur wijzigen.

4. Selecteer **OK**. De informatie wordt gekopieerd naar de koptekst van de pagina **Projectcontracten**.
5. Vul op de pagina **Projectcontracten** vul de rest van de vereiste informatie voor het project in.

## <a name="create-a-project-for-progress-billings"></a>Een project maken voor voortgangsfacturen

Volg deze stappen om een project en eventuele subprojecten te maken die aan een projectcontract zijn gekoppeld.

1. Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Alle projecten**.
2. Selecteer op de pagina **Alle projecten** de optie **Nieuw**.
3. Selecteer in het dialoogvenster **Nieuw project** in het veld **Projecttype** de optie **Tijd en materiaal**.
4. Selecteer een projectgroep. Een projectgroep definieert de boekingsinformatie voor de projecten die aan de groep zijn toegewezen.
5. Selecteer **Project maken**.
6. Nadat het project is gemaakt, stelt u de projectfase in op **In proces**.

## <a name="create-a-budget-for-a-project"></a>Een budget maken voor een project

Budgetcategorieën worden gebruikt om automatisch de factuurbedragen te berekenen voor het percentage voltooid werk voor elke categorie. Volg deze stappen om budgetcategorieën te maken voor de geschatte kosten.

1. Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Alle projecten**.
2. Selecteer en open op de pagina **Alle projecten** het gewenste project.
3. Op de pagina **Projecten**, in het actievenster, op het tabblad **Plan**, in de groep **Begroting** selecteert u **Projectbudget**.
4. Voer op de pagina **Projectbudget** de geschatte kosten in voor elke categorie in het project.

## <a name="create-billing-rules-for-progress-billings"></a>Factureringsregels maken voor voortgangsfacturen

1. Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Projectcontracten**.
2. Selecteer op de pagina **Projectcontracten** een projectcontract en open het.
3. Selecteer **Toevoegen** op de projectcontractpagina in het sneltabblad **Factureringsregels**.
4. Selecteer **Voortgang** op de pagina **Factureringsregel** in het veld **Lijntype**.
5. Voer op het sneltabblad **Details van factureringsregels** in het veld **Contractwaarde** de totale waarde van het contract in.
6. Selecteer in het veld **Categorie** de categorie waarnaar u de kostentransactie wilt boeken.
7. Selecteer in het veld **Project** het project dat deze factureringsregel gebruikt.
8. Optioneel: wijs de factureringsregel toe aan extra projecten. Selecteer op het sneltabblad **Project** in de sectie **Beschikbare projecten** een project en selecteer vervolgens de pijl naar rechts om het project toe te voegen aan de sectie **Geselecteerde projecten**.
9. Optioneel: bereken het percentagebedrag dat de klant inhoudt op betalingen op een factuur. Selecteer op het sneltabblad **Inhoudingstermijnen voor betalingen** de financieringsbron en vul vervolgens het veld **Inhoudingspercentage** in.
10. Herhaal deze stappen om aanvullende factureringsregels voor het projectcontract te maken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]