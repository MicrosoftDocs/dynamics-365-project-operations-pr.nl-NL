---
title: Integratiejournaal in Project Operations
description: Dit artikel bevat informatie over werken met het integratiejournaal in Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541071"
---
# <a name="integration-journal-in-project-operations"></a>Integratiejournaal in Project Operations

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Met tijd-, onkosten-, vergoedings- en materiaalposten maakt u **werkelijke** transacties die de operationele weergave van het voltooide werk voor een project vertegenwoordigen. Dynamics 365 Project Operations biedt accountants een tool om transacties te beoordelen en de kenmerken van de financiële administratie naar behoefte aan te passen. Nadat de controle en aanpassingen zijn voltooid, worden de transacties geboekt naar de subadministratie en het grootboek van het project. Een accountant kan deze werkzaamheden uitvoeren met behulp van het dagboek **Project Operations-integratie** (**Dynamics 365 Finance** > **Projectbeheer en financiële administratie** > **Dagboeken** > Dagboek **Project Operations-integratie**).

![Integratiejournaalstroom.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Records maken in het integratiejournaal in Project Operations

Records in het Project Operations-integratiejournaal worden gemaakt met behulp van het periodieke proces **Importeren uit opslagtabel**. U kunt dit proces uitvoeren door naar **Dynamics 365 Finance** > **Projectbeheer en financiële administratie** > **Periodiek** > **Project Operations-integratie** > **Importeren uit faseringstabel** te gaan. U kunt het proces interactief uitvoeren of het proces zo configureren dat het op de achtergrond wordt uitgevoerd.

Wanneer het periodieke proces wordt uitgevoerd, worden alle werkelijke waarden gevonden die nog niet zijn toegevoegd aan het Project Operations-integratiejournaal. Er wordt een journaalregel aangemaakt voor elke daadwerkelijke transactie.
Het systeem groepeert journaalregels in afzonderlijke dagboeken op basis van de waarde die is geselecteerd in het veld **Periode-eenheid in dagboek voor Project Operations-integratie** (**Finance** > **Projectbeheer en financiële administratie** > **Instellingen** > **Projectbeheer- en boekhoudingsparameters**, tabblad **Project Operations in Dynamics 365 Customer Engagement**). Mogelijke waarden voor dit veld zijn:

  - **Dagen**: werkelijke waarden zijn gegroepeerd op transactiedatum. Voor elke dag wordt een apart dagboek aangemaakt.
  - **Maanden**: werkelijke waarden zijn gegroepeerd per kalendermaand. Voor elke maand wordt een apart dagboek aangemaakt.
  - **Jaren**: werkelijke waarden zijn gegroepeerd per kalenderjaar. Voor elk jaar wordt een apart dagboek aangemaakt.
  - **Alles**: alle werkelijke transacties worden in hetzelfde integratiejournaal opgenomen. Als het journaal niet beschikbaar is wanneer het periodieke proces wordt uitgevoerd, bijvoorbeeld als het journaal bezig is met het boeken van transacties, wordt een nieuw journaal aangemaakt.

Journaalregels worden gemaakt op basis van de werkelijke waarden van het project. De volgende lijst bevat enkele van de meer opvallende standaard- en transformatieregels:

  - Elke feitelijke projecttransactie heeft een regel in het Project Operations-integratiejournaal. Kosten en niet-gefactureerde verkooptransacties voor het factureringstype voor tijd en materiaal worden op afzonderlijke regels weergegeven.
  - Het veld **Datum** staat voor de datum van de transactie. Het veld **Boekhouddatum** geeft de datum waarop de transactie in het grootboek is geregistreerd. Als de boekingsdatum in een [afgesloten financiële periode](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) valt en de parameter **Boekhouddatum automatisch instellen op openstaande grootboekperiode** is ingesteld op het tabblad **Financieel** van de pagina **Projectbeheer en boekhoudparameters**, zal het systeem de boekhouddatum van de transactie aanpassen aan de eerste datum in de volgende openstaande periode.
  - Het veld **Boekstuk** geeft het boekstuknummer weer voor elke daadwerkelijke transactie. De nummerreeks van het boekstuk wordt gedefinieerd op het tabblad **Nummerreeksen** op de pagina **Projectbeheer en boekhoudparameters**. Elke regel krijgt een nieuw nummer toegewezen. Nadat het boekstuk is geboekt, kunt u zien hoe kosten en niet-gefactureerde verkooptransacties samenhangen door **Gerelateerde boekstukken** te selecteren op de pagina **Vouchertransactie**.
  - In het veld **Categorie** wordt een projecttransactie weergegeven en standaardwaarden op basis van de transactiecategorie voor de gerelateerde werkelijke projectwaarde.
    - Als **Transactiecategorie** is ingesteld in de werkelijke projectwaarde en een gerelateerde **Projectcategorie** bestaat in een bepaalde rechtspersoon, wordt de categorie standaard ingesteld op deze projectcategorie.
    - Als **Transactiecategorie** niet is ingesteld in de werkelijke projectwaarden, gebruikt het systeem de waarde in het veld **Standaardinstellingen projectcategorie** op het tabblad **Project Operations in Dynamics 365 Customer Engagement** op de pagina **Projectbeheer- en boekhoudingsparameters**.
  - Het veld **Resource** geeft de projectresource aan met betrekking tot deze transactie. De resource wordt gebruikt als referentie in projectfactuurvoorstellen aan klanten.
  - Voor het veld **Wisselkoers** wordt standaard **Valutawisselkoers** ingesteld in Dynamics 365 Finance. Als de wisselkoersinstellingen ontbreken, kan het periodieke proces **Importeren uit verzameltabel** de record niet toevoegen aan een journaal en wordt een foutmelding toegevoegd aan het taakuitvoeringslogboek.
  - Het veld **Regeleigenschap** geeft het factureringstype aan in de werkelijke projectwaarden. Regeleigenschap en factureringstypetoewijzing worden gedefinieerd op het tabblad **Project Operations in Dynamics 365 Customer Engagement** op de pagina **Projectbeheer- en boekhoudingsparameters**.

Alleen de volgende boekhoudkenmerken kunnen worden bijgewerkt in de Project Operations-integratiejournaalregels:

- **Btw-groep facturering** en **Btw-groep voor factuurartikel**
- **Financiële dimensies** (met de actie **Bedragen verdelen**)

Integratiejournaalregels kunnen worden verwijderd. Niet-geboekte regels worden echter opnieuw in het journaal ingevoegd nadat u het periodieke proces **Importeren uit verzameltabel** hebt uitgevoerd.

### <a name="post-the-project-operations-integration-journal"></a>Het Project Operations-integratiejournaal boeken

Wanneer u het integratiejournaal boekt, worden een projectsubadministratie en grootboektransacties gecreëerd. Deze worden later gebruikt bij klantfacturering, opbrengstentoerekening en financiële rapportage.

Het geselecteerde integratiejournaal van Project Operations kan worden geboekt met **Boeken** op de pagina van het integratiejournaal van Project Operations. Alle dagboeken kunnen automatisch worden geboekt door een proces uit te voeren via **Periodieken** > **Project Operations-integratie** > **Project Operations-integratiejournaal boeken**.

De boeking kan interactief worden uitgevoerd of in batch plaatsvinden. Houd er rekening mee dat alle dagboeken met meer dan 100 regels automatisch in een batch worden geboekt. Voor betere prestaties wanneer dagboeken met veel regels in een batch worden geboekt, schakelt u de functie **Project Operations-integratiejournaal boeken met meerdere batchtaken** in de werkruimte **Functiebeheer** in. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Alle regels met boekingsfouten overboeken naar een nieuw journaal

> [!NOTE]
> Als u deze mogelijkheid wilt gebruiken, schakelt u de functie **Alle regels met boekingsfouten overboeken naar een nieuw Project Operations-integratiejournaal** in de werkruimte **Functiebeheer** in.

Met deze functie kan de ervaring met het Project Operations-integratiejournaal worden verbeterd. Als de functie is ingeschakeld, verhinderen problemen met de tijden voor twee keer wegschrijven en instellingsproblemen niet langer dat geldige tijdschriften worden geboekt. Tijdens het boeken naar het Project Operations-integratiejournaal valideert het systeem elke regel in het journaal. Alle regels zonder fouten bevatten worden geboekt en er wordt een nieuw journaal gemaakt voor alle regels met boekingsfouten.

Als u de journaals met boekingsfoutregels wilt bekijken, gaat u naar **Projectmanagement en boekhouding**\> **Journaals**\> **Project Operations-integratiejournaal** en filtert u de lijst met journaals op basis van het veld **Oorspronkelijk journaal**. De volgende afbeelding toont een voorbeeld waarbij de journaals op de pagina **Project Operations-integratiejournaal** op deze manier zijn gefilterd.

![Oorspronkelijk journaal weergegeven op de pagina Project Operations-integratiejournaal.](./media/transferLines-originalJournal.png)

Als een periodieke batchtaak is geconfigureerd om het integratiejournaal te boeken, wordt het boeken opnieuw geprobeerd en worden de journaals geboekt als het probleem met timing is verholpen. Alle resterende journaals moeten handmatig worden onderzocht door de logboeken te bekijken en de vereiste actie te ondernemen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
