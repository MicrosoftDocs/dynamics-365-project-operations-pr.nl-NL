---
title: Nieuwe of gewijzigde functies van oktober 2021 voor Project Operations voor scenario's op basis van voorradige artikelen/productieorders
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van oktober 2021 voor scenario's op basis van voorradige artikelen/productieorders.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029937"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Nieuwe of gewijzigde functies van oktober 2021 voor Project Operations voor scenario's op basis van voorradige artikelen/productieorders

_**Van toepassing op**: Project Operations voor scenario's op basis van voorradige artikelen/productieorders_

Dit artikel is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.22
 
## <a name="quality-updates"></a>Kwaliteitsupdates

| Functiegebied | Referentienummer | Kwaliteitsupdate |
|--------------|------------------|----------------|
| Projectbeheer en financiële administratie | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Onderhanden projectwerk (OHW) en transitorische opbrengstbedragen worden niet correct teruggeboekt wanneer een intercompany-klantfactuur wordt geboekt. |
| Projectbeheer en financiële administratie | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | De functionaliteit **Voorkomen van projectafsluiting als er openstaande transacties zijn** werkt niet. |
| Projectbeheer en financiële administratie | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | De factureringsclassificatie op een vrije-tekstfactuur vult niet automatisch dimensies van projecten in wanneer die functionaliteit is ingeschakeld. |
| Projectbeheer en financiële administratie | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | In niet-intercompany scenario's worden OHW en transitorische opbrengstbedragen niet correct teruggeboekt wanneer de projectfactuur wordt geboekt. |
| Projectbeheer en financiële administratie | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debet- en creditwaarden worden omgewisseld wanneer de Microsoft Excel-invoegtoepassing wordt gebruikt met het project-onkostenjournaal en het veld **Tegenrekeningtype** is ingesteld op **Project**. |
| Projectbeheer en financiële administratie | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Het bedrag dat in projecttransacties wordt geboekt, wordt te hoog opgegeven op een projectinkooporder die voorraadartikelen bevat en niet-aftrekbare belastingbedragen heeft wanneer **UseTax** is gemarkeerd. |
| Projectbeheer en financiële administratie | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Het systeem verdeelt het bedrag tussen de projectwinst- en verliesrapporten en de project-OHW-rapporten. |
| Projectbeheer en financiële administratie | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Voorhanden voorraad is onjuist nadat een gedeeltelijk geretourneerde artikelvereiste wordt aangepast. |
| Projectbeheer en financiële administratie | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Resourcenamen worden gedupliceerd in Project Operations wanneer deze worden bewerkt in Microsoft Project. |
| Projectbeheer en financiële administratie | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Intercompany-onkostenrapporten met crediteuren in afwachting van factuurkosten van intercompany-leveranciers worden eerst geboekt naar het boekingstype **OHW-kosten project**. Tijdens de verwerking worden de kosten met betrekking tot de raming echter geboekt naar het boekingstype **Projectkosten** in plaats van het verwachte boekingstype **Intercompany-kosten**. |
| Projectbeheer en financiële administratie | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Resultaten van leveranciersinhoudingen in projectonkostentransacties worden niet weergegeven. |
| Projectbeheer en financiële administratie | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | De urenstaat moet het transactiebedrag in de transactievaluta afronden op een opgegeven aantal decimalen in alle boekhoudingsverdelingen en algemene journaaltoewijzingsposten. |
| Projectbeheer en financiële administratie | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Hoeveelheden projectartikelbehoeften worden automatisch bijgewerkt wanneer de geplande orders worden gefiatteerd. |
| Projectbeheer en financiële administratie | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Het boekstuknummer, het transactietype leverancierssaldo en het accountnummer kunnen niet worden teruggeboekt op de vooruitbetalingsfactuur van een inkooporder. |
| Projectbeheer en financiële administratie | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | De intercompany-leveranciersfactuur wordt verbroken wanneer integratie van leveranciersfacturen is ingeschakeld. |
| Projectbeheer en financiële administratie | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Wanneer u een project-onkostenjournaal aanmaakt, wordt het kostenbedrag weergegeven in het veld **Tegoed**. |
| Projectbeheer en financiële administratie | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | De betalingsvoorwaarden op projectfacturen werken niet zoals verwacht. |
| Projectbeheer en financiële administratie | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Urenstaatboekstukken kunnen opnieuw worden gebruikt wanneer de nummerreeks is ingesteld als doorlopend. |
| Projectbeheer en financiële administratie | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANKRIJK: De logica voor **Handmatig inhoudingsbedrag** komt niet overeen met de logica voor **Automatisch inhoudingsbedrag** in het projectcontract-factuurvoorstel. |
| Projectbeheer en financiële administratie | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Wanneer de leveranciersinhouding wordt vrijgegeven, bevat de boekstukboeking onjuiste aanvullende regels. |
| Projectbeheer en financiële administratie | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Wanneer het veld **Factuurdatum** op de pagina **Factuurvoorstel maken** wordt gewijzigd, kan de volgende fout optreden: "Objectverwijzing niet ingesteld op een exemplaar van een object." |
| Projectbeheer en financiële administratie | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Er treedt een fout op wanneer u probeert een urenstaat goed te keuren van de werkstroom **TSLine** en er een urenstaatbeleid is voor zaterdag en zondag. |
| Projectbeheer en financiële administratie | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Het projectitemtype beginsaldo is uitgesloten van **Transactieoverzichten van factuurvoorstel** wanneer het factuurtotaal van het factuurvoorstel wordt berekend. |
| Projectbeheer en financiële administratie | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Als de verbruikskosten op een projectproductieorder 0 (nul) zijn, treedt de volgende fout op wanneer u probeert te schatten: "Poging om te delen door nul." |
| Projectbeheer en financiële administratie | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | De mobiele app voor projecturenstaat voor Android reageert niet meer. Het probleem heeft te maken met **TimeEntryDataManager ArgumentNullException**. |
| Projectbeheer en financiële administratie | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Het integratiejournaal van Project Operations mislukt wanneer u dit boekt, omdat een account dimensies mist. De account waarvoor de dimensies ontbreken, is echter niet de account waarnaar u boekt. |
| Projectbeheer en financiële administratie | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Het filter **ToDate** in zoekopdrachten wordt niet gewist wanneer het wordt verwijderd uit het dialoogvenster **Selecteren** op de pagina **Kosten boeken**. |
| Projectbeheer en financiële administratie | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Alle verdeling opnieuw instellen** mislukt en toont een fout voor de urenstaten die zijn gemaakt voor een project van het type **Alleen tijd**. |
| Projectbeheer en financiële administratie | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Het tabblad **Project** kan niet worden bewerkt op een openstaande leveranciersfactuur wanneer de inkoopcategorie aan het artikel wordt toegewezen. |
| Projectbeheer en financiële administratie | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Het navigatiedeelvenster ontbreekt als u niet bent aangemeld bij project Operations Dataverse. |
| Projectbeheer en financiële administratie | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Voor intercompany-transacties voor projectcorrectie zijn er problemen in het doelbedrijf. |
| Projectbeheer en financiële administratie | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Toegezegde kosten voor een project berekenen de verkeerde hoeveelheid en kostprijs als de inkooporder is verwerkt door **Jaarultimoproces van inkooporder** in grootboek. |
| Projectbeheer en financiële administratie | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Wanneer een projectproductieorder met kwaliteitsorders als voltooid wordt gerapporteerd, treedt de volgende fout op: "Geen virtuele transactie gemarkeerd met voorraadtransactie." |
| Projectbeheer en financiële administratie | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Wanneer een projectgerelateerde crediteurenfactuur wordt geboekt, treedt de volgende fout op: "Vaste-tekstproject - kosten - artikel bestaat niet." |
| Projectbeheer en financiële administratie | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Indirecte kosten worden verdubbeld wanneer u handmatig opbrengst samenvoegt. |
| Projectbeheer en financiële administratie | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Opbrengsten samenvoegen en OHW-boekingen produceren geen transacties. |
| Projectbeheer en financiële administratie | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Activering van de prijs in behandeling mislukt voor een standaardkostenpost wanneer er een ontvangen projectinkooporder bestaat. |
| Projectbeheer en financiële administratie | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | De teruggeboekte OHW-waarde van een factuurboeking wijkt af van de oorspronkelijk geboekte OHW-waarde uit een tijdsvermelding. |
| Projectbeheer en financiële administratie | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Er is een boekingsprobleem voor project - gefactureerde opbrengst bij toegepaste voorschotten waarbij de transacties op een boekstuk niet in evenwicht zijn. |
| Projectbeheer en financiële administratie | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Het maken van een raming nadat een factuurvoorstel is geboekt, blokkeert het importeren van correctieregels in Project Operations. |
| Projectbeheer en financiële administratie | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Wijziging van een volledig gefactureerde mijlpaalrecord zou niet mogelijk moeten zijn. |
| Projectbeheer en financiële administratie | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Wanneer automatische toeslagen worden gebruikt, kan de intercompany-klantfactuur voor een urenstaat niet worden geboekt en wordt er een foutmelding weergegeven. |
| Projectbeheer en financiële administratie | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Het adres van een subproject is niet correct bijgewerkt. |
| Projectbeheer en financiële administratie | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | De kostprijs voor artikelbehoeften wordt bijgewerkt met de inkoopprijs voor geconsolideerde inkooporders. |
| Projectbeheer en financiële administratie | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | De geboekte kosten zijn niet correct nadat de aankoopprijs is bijgewerkt en de parameter **Wijzigingsbeheer activeren** is ingeschakeld. |
| Reizen en onkosten | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alle gebruikerskosten zijn te zien wanneer u zoekt naar een categorie in de mobiele app voor onkosten. |
| Reizen en onkosten | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Er worden onjuiste bedragen voor leveranciers- en btw-transacties geboekt op basis van een onkostenpost die is gemaakt op basis van een creditcardtransactie. |
| Reizen en onkosten | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Er wordt een irrelevant waarschuwingsbericht weergegeven wanneer u de pagina's van de onkostennota vernieuwt. |
| Reizen en onkosten | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | De verkeerde tussentijdse fiatteur wordt gebruikt wanneer u een tussentijdse fiatteur verwijdert en vervolgens opnieuw indient via werkstroom. |
| Reizen en onkosten | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Er treedt een boekingsfout op die verband houdt met de kilometerstand. |
| Reizen en onkosten | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Verdeling werkt de rechtspersoon niet bij wanneer een niet-gekoppelde transactie opnieuw wordt toegevoegd aan de onkostennota voor intercompany-onkosten. |

### <a name="regulatory-updates"></a>Wijzigingen in regelgeving

Zie [Regelgevende updates](/dynamics365/finance/localizations/regulatory-updates) voor informatie over updates van regelgeving voor apps voor financiën en bedrijfsactiviteiten. U kunt zich ook aanmelden bij Microsoft Dynamics Lifecycle Services (LCS) en het hulpprogramma Problemen zoeken gebruiken om de geplande updates van de regelgeving te bekijken. Met Problemen zoeken kunt u zoeken op land of regio, type functie en versie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
