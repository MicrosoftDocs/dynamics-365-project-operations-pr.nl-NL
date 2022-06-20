---
title: Nieuwe functies van maart 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van maart 2022 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910900"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van maart 2022 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

*Van toepassing op: Project Operations voor scenario's op basis van resources/niet-voorradige artikelen*

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.30.0.99
- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.25

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

Dagvergoedingen worden nu ondersteund in de nieuwe en opnieuw ontworpen moderne werkruimte voor onkosten. Bedrijven die dagvergoedingen gebruiken, kunnen deze functie inschakelen om gebruikers een gemakkelijke manier te bieden om hun dagvergoedingen in te dienen en vergoed te krijgen. Zie [Dagvergoedingen](../expense/per-diem-expenses.md) voor meer informatie.

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

De volgende lijst toont de toewijzingen voor twee keer wegschrijven die zijn gewijzigd of toegevoegd in de release van Project Operations van maart 2022.

| **Entiteitstoewijzing** | **Bijgewerkte versie** | **Opmerkingen** |
| --- | --- | --- |
| Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten msdyn\_projectvendorinvoicelines | 1.0.0.3 | Toewijzingen bijgewerkt om deze af te stemmen op de entiteit van de leveranciersfactuurregel in Dataverse. <br>Activeer de toewijzingsversie 1.0.0.4 niet. In de volgende maandelijkse update is deze gereed voor gebruik in combinatie met Finance-omgeving versie 10.0.26. |

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Sommige functies en mogelijkheden werken mogelijk niet correct als de nieuwste versie van de toewijzing niet wordt geactiveerd. U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de toewijzing activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in de sectie [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) van de probleemoplossingsgids voor Twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Tijd en onkosten | 2388011 | Afwijzingsopmerkingen weergeven aan indieners van tijdinvoer tijdens bulkgoedkeuring. |
| Projecten plannen en bijhouden | 2495294 | Projectdetails mogen niet bewerkbaar zijn op de pagina **Taakdetails**. |
| Facturering en prijzen | 2499605 | Contractmijlpalen die zijn gemaakt op basis van offertemijlpalen zijn ten onrechte als alleen-lezen gemarkeerd. |
| Projecten plannen en bijhouden | 2506050 | De bewerkingsset blijft een uur in behandeling als er geen wijziging is om op te slaan. De set wordt dan ten onrechte gemarkeerd als **Mislukt**, terwijl deze onmiddellijk moet worden voltooid. |
| Facturering en prijzen | 2507401 | Standaard contracteenheden worden onjuist ingevoerd in projecten vanwege onjuiste caching. |
| Facturering en prijzen | 2541660 | **Validatie van het maken van verkooporders** in twee keer wegschrijven mag alleen van toepassing zijn op projectgebaseerde orders. |
| Facturering en prijzen | 2552745 | Belasting wordt niet verdeeld tussen klanten die regels voor gesplitste facturering hebben ingesteld. |
| Facturering en prijzen | 2558859 | Verbeterde foutmeldingen bij het instellen van prijsdimensies. |
| Facturering en prijzen | 2558933 | **Importeren uit projectramingen** mislukt wanneer **msdyn\_project** wordt toegevoegd als prijsdimensie. |
| Facturering en prijzen | 2559101 | Het verwijderen van projectparameters wordt niet geblokkeerd en veroorzaakt problemen. |
| Verkoopkansenbeheer | 2570390 | De invoegtoepassing voor twee keer wegschrijven dwingt het accounttype **Klant** af voor offertes, orders en verkoopkansen, zelfs als dat accounttype niet correct is. |
| Facturering en prijzen | 2586097 | Werkelijke kosten bij een gesplitste factuur worden niet teruggeboekt wanneer een project wordt verwijderd uit een projectcontractregel. |
| Facturering en prijzen | 2589619 | Belasting op toe te voegen materiaal wordt toegepast op niet-gefactureerde verkoopwaarden en de factuur. |
| Verkoopkansenbeheer | 2594015 | Een offerte kan niet als binnengehaald worden afgesloten voor klanten die **Netto 60** als betalingsvoorwaarden hanteren. |
| Projecten plannen en bijhouden | 2595841 | In Project for the Web ontvangen gebruikers een foutbericht over een ontbrekende **msdyn\_actualstart** wanneer ze een nieuwe resourceaanvraag maken. |
| Tijd en onkosten | 2602511 | Het veld **Afgewezen door** voor tijdsvermeldingen geeft **Systeem** aan in plaats van een benoemde gebruiker als afwijzer. |
| Tijd en onkosten | 2602528 | Een projectgoedkeurder kan tijd goedkeuren voor projecten waarvoor deze niet als goedkeurder is vermeld. |
| Facturering en prijzen | 2608550 | Een correctiefactuur kan worden bevestigd, zelfs als er geen wijzigingen zijn in het origineel. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

| Functiegebied | Referentienummer | Kwaliteitsupdate |
| --- | --- | --- |
| Projectbeheer en financiële administratie | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | De toegestane lengte van het veld **Categorie-id** komt niet overeen in Finance en Project Operations. |
| Projectbeheer en financiële administratie | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projecten met een vaste prijs kunnen niet worden geëlimineerd wanneer het veld **Facturering op account** is ingesteld op **Winst en verlies** en het principe **Voltooid percentage** wordt gebruikt. |
| Projectbeheer en financiële administratie | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Er is een onjuiste standaard btw-groep ingevoerd vanuit de projectinstellingen op onkostenregels in het integratiejournaal van Project Operations. |
| Projectbeheer en financiële administratie | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | U kunt de dimensies van de koptekst van het projectfactuurvoorstel niet bewerken in een geïntegreerde implementatie met Project Operations. |
| Projectbeheer en financiële administratie | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Facturen van intercompany-leveranciers mogen niet worden geïntegreerd met Dataverse. |
| Projectbeheer en financiële administratie | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | De valuta van de klantsaldi en de rapportagevaluta komen niet overeen. |
| Projectbeheer en financiële administratie | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | U kunt een projectfactuur boeken, zelfs als de klant in de wachtstand staat voor alle facturen. |
| Projectbeheer en financiële administratie | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | De knop **Alle regels verwijderen** ontbreekt in projectfactuurvoorstellen met de weergaven **Koptekst** en **Regels**. |
| Projectbeheer en financiële administratie | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Wanneer u een leveranciersfactuur boekt, treedt de volgende fout op: "De boekhouddatum voor de factuur moet in hetzelfde boekjaar vallen als de gerelateerde inkooporder. Voer het eindejaarsproces van de inkooporder uit of wijzig de datum in het huidige boekjaar." |
| Reizen en onkosten | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | De vastgelegde kosten voor een project worden niet vrijgegeven nadat de vastgelegde kosten van de reisaanvraag zijn vrijgegeven. |
| Reizen en onkosten | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | De volgende fout treedt op wanneer u een onkostennota indient: "Stack-trace: het bedrijf bestaat niet." |
| Reizen en onkosten | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | De standaard **project-id** wordt niet ingevoerd op onkostennota's wanneer de parameter **Activiteit voor journaal vereisen** is geselecteerd voor het project. |
| Reizen en onkosten | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | De knop **Onkosten boeken** werkt niet correct in Project Operations voor scenario's op basis van resources/niet-voorradige artikelen. |
| Reizen en onkosten | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Er is een probleem met **Tarief per mijl** voor een kilometeronkostendeclaratie die passagiers omvat. |
| Reizen en onkosten | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Onkostenvergoedingen voor werknemers worden niet correct opgeteld wanneer twee verschillende voertuigtypen worden gebruikt in de onkostencategorie **Kilometerstanden**. |
| Reizen en onkosten | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | De zoekopdracht voor het veld **Project** op een reisaanvraagregel retourneert niet de juiste lijst met projecten. |
| Reizen en onkosten | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometerstand in beoordeling** toont een waarschuwing in onkostennota's. |
| Reizen en onkosten | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | De OCR-service (Optical Character Recognition) voor ontvangsten werkt niet vanwege een probleem met de URL van de OCR-service voor onkosten. |
| Reizen en onkosten | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Wanneer de functie **Mogelijkheid om terugkerende kosten snel te specificeren** is ingeschakeld, veranderen de bedragen op specificatieregels op onkostennota's telkens wanneer de pagina **Specificeren** wordt geopend. |
| Reizen en onkosten | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | U kunt een onkostennota niet verwijderen als de tussentijdse lijst meer dan één goedkeurder heeft. |

## <a name="removed-and-deprecated-features"></a>Verwijderde en afgeschafte functies

In het artikel [Verwijderde of afgeschafte functies in Project Operations](removed-depreciated-features-project.md) onderwerp beschrijft functies die zijn verwijderd of afgeschaft voor Dynamics 365 Project Operations.

- Een verwijderde functie is niet langer beschikbaar in het product.
- Een afgeschafte functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Er wordt 12 maanden voordat een functie wordt verwijderd uit het product een aankondiging van afschaffing weergegeven in het artikel [Verwijderde of afgeschafte functies in Project Operations](removed-depreciated-features-project.md).

Voor wijzigingen die fouten veroorzaken en alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal gaat het bij deze wijzigingen om functionele updates die moeten worden doorgevoerd in de compiler.
