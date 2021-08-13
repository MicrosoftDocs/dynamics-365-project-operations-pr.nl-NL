---
title: Nieuwe of gewijzigde functies in Project Operations in juli 2021voor scenario's op basis van voorradige artikelen/productieorders
description: Dit onderwerp bevat informatie over de kwaliteitsupdates die beschikbaar zijn in de release van juli 2021 van Project Operations voor scenario´s op basis van voorradige artikelen/productieorders.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: dadcf3e9fa8432fb66f76b7c2f0fdb98bc00511d93984ea98fa30b4fc03fa426
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992695"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Nieuwe of gewijzigde functies in Project Operations in juli 2021voor scenario's op basis van voorradige artikelen/productieorders

_**Van toepassing op**: Project Operations voor scenario's op basis van voorradige artikelen/productieorders_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

- Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving, versie 10.0.20
 
### <a name="quality-updates"></a>Kwaliteitsupdates
                                                                                                                                                                                  
| Functiegebied                      | Referentienummer| Kwaliteitsupdate                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projectbeheer en boekhouding | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Kostentoezeggingsrecords van een opdracht tot inkoop worden gewist zodra de inkooporder is vrijgegeven via de afgifte van de opdracht tot inkoop.                                                                           |
| Projectbeheer en boekhouding | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Budgetvalidatie vindt twee keer plaats op een opdracht tot inkoop. Deze duplicatie betekent dat de opdracht niet kan worden afgesloten en dat de bijbehorende inkooporder niet wordt gemaakt.                                                                                                                        |
| Projectbeheer en boekhouding | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | De factureringsregel **Percentage om op te factureren** kan niet worden voltooid vanwege een afrondingsprobleem.                                                                              |
| Projectbeheer en boekhouding | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Wanneer u de transactie aanpast en het percentage decimalen heeft, worden de kostprijs en verkoopprijs niet correct aangepast.                                      |
| Projectbeheer en boekhouding | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | De verkenner voor bronnen van de financiële administratie toont uren voor één urenstaatregel voor meerdere urenstaatregels met verschillende activiteiten.                                      |
| Projectbeheer en boekhouding | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Opgeslagen weergaven en personalisatie van urenstaatregeldetails zorgen ervoor dat het systeem altijd de details voor de eerste urenstaat in de lijst opent bij een poging een urenstaat te openen.  |
| Projectbeheer en boekhouding | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Het hoofdknooppunt van het project verdwijnt en records van de werkspecificatiestructuur worden verwijderd na het importeren.                                                                                             |
| Projectbeheer en boekhouding | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Wanneer artikelen gedeeltelijk vanuit de artikelbehoefte worden ontvangen en uitgegeven, werkt het systeem het verkeerde budgetverbruikssaldo bij. |
| Projectbeheer en boekhouding | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Inkooporders voor projectbehoud tonen de totalen niet correct in het deelvenster **Totalen** of het raster **In afwachting van factuur**.                                                                  |
| Projectbeheer en boekhouding | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Bij het afsluiten van de voorraad worden kostenaanpassingen van projectartikelen geboekt op de saldorekening in plaats van op de winst- en verliesrekening.                                                            |
| Projectbeheer en boekhouding | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Een door een project geboekt transactieboekstuk en een schattingsboekstuk gebruiken USD als boekhoudvaluta, maar het bedrag geeft aan wat het CAD-equivalent zou zijn.              |
| Projectbeheer en boekhouding | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Toegezegde kosten met een artikelbehoefte en inkooporder zijn verkeerd in het inkooporderfactuurproces met een deelproductontvangstbewijs en deelfacturering.       |
| Projectbeheer en boekhouding | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Bij projectcorrectie wordt het verkoopbedrag niet correct bijgewerkt met indirecte kosten.                                                                                    |
| Projectbeheer en boekhouding | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | In de tabel **Urenstaat** ontbreekt een gedefinieerde relatie met de weergave **Werknemer/resource**.                                                                                   |
| Projectbeheer en boekhouding | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Kan het veld **Activiteitsnummer** niet invullen wanneer u het selecteert in het vervolgkeuzemenu voor een intercompany-urenstaat.                                                                 |
| Projectbeheer en boekhouding | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | U kunt een gepersonaliseerd veld voor **Doel** of **Beschrijving activiteit** niet toevoegen aan de volgende pagina´s: **Geboekte projecttransactie**, **Factuurvoorstel maken** en **Factuurvoorstel**.  |
| Projectbeheer en boekhouding | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Het verkeerde besturingselement voor leveringsdatum wordt verschaft wanneer u artikelbehoeften maakt met behulp van gegevensbeheer (**ProjSalesItemRequirementEntity**).                                              |
| Projectbeheer en boekhouding | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Wanneer u een projectcontract-ID selecteert in Finance, opent de geïntegreerde omgeving van Project Operations de pagina om een nieuw record te maken in plaats van het bestaande projectcontract te openen.                                                                                                                 |
| Projectbeheer en financiële administratie | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Het label "@SYS4083080" ("Kan geen uniek werknemersrecord vinden dat overeenkomt met de ingevoerde waarden") is niet vertaald naar het Deens.                                |
| Projectbeheer en boekhouding | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Het veld **Btw-groep artikel** kan niet worden bewerkt op een factuurvoorstel.                                                                               |
| Projectbeheer en boekhouding | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Toegezegde kosten worden overschat met niet-aftrekbare belastingbedragen.                                                                                                    |
| Projectbeheer en boekhouding | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Het boeken van een intercompany-urenstaat met meerdere projecten en verschillende financiële dimensies genereert onverwachte waarden in het grootboek.                             |
| Projectbeheer en boekhouding | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Factuurvoorstelregels worden gedupliceerd vanwege meerdere periodieke **Importeren uit opslag**-processen die tegelijkertijd worden uitgevoerd.                                      |
| Projectbeheer en boekhouding | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Er is een fout opgetreden bij het boeken van het creditnotafactuurvoorstel, zodat de transacties op het boekstuk niet in evenwicht zijn.    |
| Projectbeheer en boekhouding | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Toegezegde projectkosten worden onjuist nadat uitgestelde facturen in behandeling zijn vrijgegeven.                                                                             |
| Projectbeheer en financiële administratie | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | U kunt geen creditnota maken voor een projectverkooporder als de belasting in een andere valuta is dan de bedrijfsvaluta.                                      |
| Projectbeheer en boekhouding | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Wanneer u een contract verwijdert, wordt ook het aan de klant gekoppelde adres verwijderd.                                                                                     |
| Projectbeheer en boekhouding | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Een factuurvoorstel dat het resultaat is van een negatieve tijdtransactiecorrectie, kan niet worden geboekt.                                                                    |
| Reizen en onkosten                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Belasting wordt anders berekend in onkostennota's.                                                                                                                  |
| Reizen en onkosten                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | In release-update **DB72_Expense.updateTrvExpTransProjTransId()** mag met **trvExpTrans.ReferenceDataAreaId** de nieuwe nummerreeks niet worden gemaakt.                    |
| Reizen en onkosten                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Het ingevulde bedrag wordt niet weergegeven voor het verplichte veld.                                                                                                             |
| Reizen en onkosten                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Verbeteringen in de prestaties van het toevoegen van onkosten aan de onkostennota met behulp van de gebruikersinterface voor nieuw ontworpen onkosten.                                                            |
| Reizen en onkosten                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | U kunt geboekte onkostennota's verwijderen.                                                                                           |
| Reizen en onkosten                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Het bericht Onkostenbeleid wordt meerdere keren weergegeven.                                                                                                       |
| Reizen en onkosten                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Het veld **Betalingswijze** is opgenomen in het deelvenster **Nieuwe onkosten**.                                                                                                      |
| Reizen en onkosten                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Met de tool **Status van onkostendocument opnieuw instellen** moet de status van de onkostennota opnieuw worden ingesteld op **Concept** als de werkstroom niet is gevonden. 

### <a name="regulatory-updates"></a>Wijzigingen in regelgeving
Voor informatie over updates in regelgeving voor Finance and Operations-apps leest u [Wijzigingen in regelgeving](/dynamics365/finance/localizations/regulatory-updates). U kunt u ook aanmelden bij Lifecycle Services (LCS) en de geplande updates van de regelgeving bekijken met behulp van de probleemzoekfunctie. Met het Probleem zoeken kunt u zoeken op land, type functie en release.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
