---
title: Artikelvereisten voor projectcontracten met meerdere financieringsbronnen
description: Dit onderwerp biedt informatie over het configureren en gebruiken van artikelvereisten met meerdere financieringsbronnen.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d4af03e02d3c2eb0d442e6213ff5b9cf583d54b3
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728106"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Artikelvereisten voor projectcontracten met meerdere financieringsbronnen

_**Van toepassing op:** Project Operations voor scenario's op basis van voorradige artikelen/productieorders_

Voor sommige contractuele overeenkomsten voor projectgebaseerde deliverables zijn mogelijk meerdere financieringsbronnen vereist. In dit onderwerp wordt uitgelegd hoe u de gewenste financieringsbronnen selecteert en configureert wanneer er meerdere bronnen nodig zijn voor een project of projectcontract.

## <a name="terminology"></a>Woordenlijst

- **Financieringsbron**: de entiteit die het projectcontractwerk financiert. Deze entiteit kan een interne organisatie zijn of een externe factuurrekening (klant of toekenning).
- **Projectklant**: de entiteit waaraan het projectwerk wordt geleverd.
- **Factuuraccount**: de externe entiteit die voor het projectwerk betaalt.

## <a name="example"></a>Voorbeeld

Contoso heeft een vernieuwingscontract voor apparatuur binnengehaald bij twee van zijn klanten: Adatum US en Adatum Corporate. Het contract omvat hardware- en installatiediensten die zullen worden geleverd aan Adatum US (de projectklant). De hardware wordt gefinancierd door Adatum Corporate (factuurrekening 1) en de installatiewerkzaamheden worden gefinancierd door Adatum US (factuurrekening 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Standaardregels voor factuuraccounts instellen voor artikelvereisten

### <a name="prerequisites"></a>Vereisten

- Microsoft Dynamics 365 Finance and Operations **versie 10.0.27 of hoger** is vereist om artikelvereisten te kunnen gebruiken die meerdere factuuraccounts hebben.
- Uw systeembeheerder moet de functie **Artikelvereisten met meerdere financieringsbronnen toestaan voor scenario's op basis van resources/niet-voorradige artikelen van Project Operations** inschakelen in de werkruimte **Functiebeheer**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>De standaardregels voor het factuuraccount instellen

Volg deze stappen om de standaardregels voor het factuuraccount in te stellen.

1. Ga naar **Projectmanagement en financiële administratie** \> **Instellen** \> **Parameters voor Projectmanagement en financiële administratie**.
1. Stel op het tabblad **Algemeen**, in de sectie **Verkooporders en artikelvereisten** de optie **Projecten met meerdere financieringsbronnen toestaan** in op **Ja**.
1. Geef in het veld **Standaardklant** op waar de projectleveringsklant voor de artikelbehoefte standaard vandaan komt:

    - **Van financieringsbron**: de standaard projectleveringsklant is afkomstig van de financieringsbron. Als er meerdere financieringsbronnen aan het projectcontract zijn gekoppeld, wordt de eerste financieringsbron in de lijst gebruikt.
    - **Van project**: de standaard projectleveringsklant is afkomstig van de klant die is geselecteerd in het veld **Projectrecordaccount**.

1. Optioneel: stel het standaard factuuraccount voor projectrecords in of wijzig dit:

    1. Ga naar **Projectbeheer en financiële administratie** \> **Projecten** \> **Alle projecten** en open de projectrecorddetails.
    2. Stel op het tabblad **Algemeen** het veld **Standaard factuuraccount** in of werk dit bij. Het account dat u opgeeft, wordt gebruikt als het standaard factuuraccount voor nieuwe artikelvereisten die voor het project worden gemaakt. Als u het veld leeg laat, wordt standaard het factuuraccount van de eerste financieringsbron van het projectcontract gebruikt. Gebruikers kunnen het account echter wijzigen wanneer ze de record opslaan.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Het factuuraccount dat u wilt gebruiken selecteren bij het maken van een artikelvereiste

Volg deze stappen voor het selecteren van het factuuraccount dat u wilt gebruiken bij het maken van een artikelvereiste.

1. Ga naar **Projectbeheer en financiële administratie** \> **Projecten** \> **Alle projecten** en selecteer de projectrecord.
1. Selecteer op het tabblad **Plannen** de optie **Artikelvereisten**.
1. Maak een nieuwe artikelvereisterecord.

    - Standaard is het veld **Factuuraccount** in de record ingesteld op het factuuraccount dat is ingesteld voor het project. U kunt de waarde van het veld **Factuuraccount** wijzigen en vervolgens de record opslaan. Nadat de record is opgeslagen, kunt u de waarde voor **Factuuraccount** niet meer bijwerken. Als u de waarde voor **Factuuraccount** moet bijwerken voor de artikelbehoefte, verwijdert u de bestaande artikelbehoefte en maakt u een nieuwe met de gewenste waarde.
    - Standaard is het veld **Klant** voor de artikelbehoefte ingesteld op basis van de waarde voor **Standaardklant** waarde die is ingesteld op de pagina **Projectbeheer- en boekhoudingsparameters**.

    Wanneer de artikelbehoefterecord is opgeslagen, koppelt het systeem deze aan de koptekstrecord **Verkooporder artikelbehoefte**. Als geen openstaande verkooporderkoptekst het geselecteerde factuuraccount heeft, maakt het systeem er een en koppelt de artikelbehoefteregel hieraan.

> [!NOTE]
> Artikelbehoeften worden altijd volledig gefactureerd aan het factuuraccount dat in de record is ingesteld. Het systeem ondersteunt momenteel geen regels voor financieringstoewijzing die artikelbehoeften hebben, en de boeking wordt niet gesplitst op basis van de instelling van regels voor financieringstoewijzing.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Een artikelbehoefte maken op basis van een artikelprognoserecord

Volg deze stappen om een artikelbehoefte te maken op basis van een artikelprognoserecord

1. Ga naar **Projectbeheer en financiële administratie** \> **Projecten** \> **Alle projecten** en selecteer de projectrecord.
1. Selecteer op het tabblad **Plannen** de optie **Artikelprognoses**.
1. Maak een nieuwe artikelprognoserecord.
1. Optioneel: selecteer op het tabblad **Project**, in het veld **Financieringsbron**, het gewenste factuuraccount.
1. Selecteer **Artikelbehoefte maken** en bevestig het bericht dat u ontvangt.

    > [!NOTE]
    > Het systeem kopieert de waarde voor **Financieringsbron** van de artikelprognoserecord naar de nieuw gemaakte artikelbehoefterecord.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Standaardfactuuraccount wanneer het systeem automatisch een artikelbehoefte maakt op basis van een inkooporderregel

Als de optie **Artikelbehoefte maken** is ingesteld op **Ja** op de pagina **Projectbeheer- en boekhoudingsparameters**, maakt het systeem automatisch een artikelbehoefte wanneer een nieuwe projectinkooporderregel wordt opgeslagen. Standaard zijn de velden **Factuuraccount** en **Artikelbehoefte** ingesteld op de waarde van het veld **Standaard factuuraccount** in de projectrecord. Het systeem biedt momenteel geen ondersteuning voor het bijwerken of wijzigen van het factuuraccount voor records van dit type.
