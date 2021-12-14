---
title: Nieuwe of gewijzigde functies van september 2021 voor Project Operations voor scenario's op basis van voorradige artikelen/productieorders
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van september 2021 voor scenario's op basis van voorradige artikelen/productieorders.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815843"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Nieuwe of gewijzigde functies van september 2021 voor Project Operations voor scenario's op basis van voorradige artikelen/productieorders

_**Van toepassing op**: Project Operations voor scenario's op basis van voorradige artikelen/productieorders_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Projectbeheer en financiële administratie in een Dynamics 365 Finance-omgeving versie 10.0.21
 
## <a name="quality-updates"></a>Kwaliteitsupdates

| Functiegebied | Referentienummer | Kwaliteitsupdate |
|---|---|---|
| Projectbeheer en boekhouding | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Als de rol van inkoopmanager toegang heeft gekregen tot één rechtspersoon, krijgt deze ook toegang tot alle projecten in alle rechtspersonen. |
| Projectbeheer en boekhouding | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Er treedt een btw-afrondingsprobleem op terwijl een creditnota wordt verrekend met een originele projectfactuur. |
| Projectbeheer en boekhouding | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Gebruik een alternatief projectbudget voor budgetverificatie. |
| Projectbeheer en boekhouding | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | De prijsgroep **Verkoopprijs uur** wordt niet berekend op basis van de structuur voor werkspecificatie voor projectoffertes. |
| Projectbeheer en boekhouding | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Schrapping van raming mislukt wanneer de functie **Valuta van projectcontract inschakelen voor ramingsberekening** is ingeschakeld. |
| Projectbeheer en boekhouding | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Ontbinding van btw in factoren op basis van hoeveelheid wordt toegevoegd aan het verkoopprijsbedrag wanneer gebruiksbelasting wordt gebruikt voor de btw-groep van het project-onkostenjournaal. |
| Projectbeheer en boekhouding | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Voorwaardelijke belasting wordt niet correct berekend voor de laatste betaling wanneer leveranciersinhoudingen en vooruitbetaling worden toegepast op inkooporderfacturen. |
| Projectbeheer en boekhouding | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Tracering van correctie werkt niet voor beginsaldojournalen. |
| Projectbeheer en boekhouding | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Toewijzing van projectbudgetrevisie per periode** wordt verdeeld over alle budgetperiodes. Wanneer de toewijzing wordt ingediend, wordt de record niet gewist. |
| Projectbeheer en boekhouding | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | OHW-boekingen (onderhanden werk) naar het grootboek zijn met een onjuist bedrag geboekt. |
| Projectbeheer en boekhouding | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Goedkeuring van het projecturenjournaal werkt niet. |
| Projectbeheer en boekhouding | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | De verkoopprijs van de projectaanpassing wordt niet bijgewerkt met indirecte kosten wanneer de financieringslimiet niet is gemarkeerd. |
| Projectbeheer en boekhouding | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Er kan geen artikelbehoefte worden gemaakt wanneer de tabelkop Verkoop wordt gefactureerd en de ondersteunende inkooporder voor bestaande regels is voltooid. |
| Projectbeheer en boekhouding | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Het inhoudingsbedrag voor een factureringsregel met een mijlpaal voor een ander project wordt niet geboekt in de bijbehorende project-id die voor de mijlpaal is geselecteerd. In plaats daarvan wordt deze bij het eerste project geplaatst. |
| Projectbeheer en boekhouding | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Wanneer u **Financiële dimensieset** selecteert op een factuurvoorstel treedt de volgende fout op: "Kan object van het type 'Dynamics.AX.Application.FormIntControl' niet converteren naar type 'Dynamics.AX.Applicatie.FormStringControl'." |
| Projectbeheer en boekhouding | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Het rapport **Projectfactuur** slaat regels over. |
| Projectbeheer en boekhouding | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Er treedt een fout op wanneer u de kostencontrole voor een investeringsproject berekent. |
| Projectbeheer en boekhouding | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | De methode **ProjTable::InitFromCustTable - canDeletePostalAddress** veroorzaakt een prestatieprobleem. |
| Projectbeheer en boekhouding | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | De foutmelding moet duidelijker zijn dan "Onverwachte fout." |
| Projectbeheer en boekhouding | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | De batchverwerkingstaak voor het boeken van projectfacturen verwerkt en boekt het factuurvoorstel zelfs als de factuurregels niet zijn gegenereerd. |
| Projectbeheer en boekhouding | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Er treedt een afrondingsprobleem op wanneer de licentieconfiguratiesleutel voor de publieke sector is uitgeschakeld. Er wordt een onjuiste kost- of verkoopprijs gegenereerd op de urenstaat voor contracten met meerdere grondbronnen. |
| Projectbeheer en boekhouding | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | De projectverkoopprijs op een gefactureerde projectinkooporder wordt onjuist berekend wanneer het verkoopprijsmodel **Bijdrageverhouding** is. |
| Projectbeheer en boekhouding | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Het systeem houdt geen rekening met de actieve dagen ertussen wanneer dit het effectief arbeidstarief voor een werknemer berekent. |
| Projectbeheer en boekhouding | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Er treedt een boekingsfout op de intercompany-urenstaat op vanwege de volgende validatiefout: "Er is geen handelspartner geconfigureerd voor rechtspersoon." |
| Projectbeheer en boekhouding | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | De beschrijving van een inkooporder met een onkostencategorie wordt niet opgehaald in de geboekte projecttransactielijst. |
| Projectbeheer en boekhouding | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Er is een onjuiste omzetting op artikeljournalen die naar een project zijn geboekt. |
| Projectbeheer en boekhouding | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | U kunt een inkooporder ook bevestigen als de financieringslimiet is overschreden. |
| Projectbeheer en boekhouding | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | De sectie **Factuur corrigeren/annuleren** op een vrije-tekstfactuur verdwijnt wanneer een project-id wordt geselecteerd. |
| Projectbeheer en boekhouding | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Er zijn prestatieproblemen wanneer een projectfactuurvoorstel wordt geboekt vanuit een projectverkooporder die een voorraadartikel bevat. |
| Projectbeheer en boekhouding | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projectinkoopfacturen kunnen niet worden geboekt omdat de volgende fout optreedt: "Functie AccDistProcessorprojectExtension.createForProjectRevenueLine is onjuist aangeroepen." |
| Projectbeheer en boekhouding | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Update voor het maken van batchtaken voor projectramingen om het uitvoeren van meerdere subtaken te ondersteunen. |
| Projectbeheer en boekhouding | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | De status van een urenstaat kan niet worden bijgewerkt naar **Concept** wanneer de werkstroom vastzit in een status **Geannuleerd**. |
| Projectbeheer en boekhouding | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Inhoudingsbedragen worden niet berekend in het factuurvoorstel van de creditnota als er meerdere regels zijn. |
| Projectbeheer en boekhouding | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Wanneer u het bedrag op een gegenereerde factuur van een inkooporder probeert te wijzigen, treedt de volgende fout op: "De transacties op het boekstuk zijn niet in evenwicht vanaf XX/XX/XXXX. (valuta voor boekhouding: 0,00 - rapporteringsvaluta: 0,01)." |
| Projectbeheer en boekhouding | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Er is een prestatieprobleem wanneer een projectfactuurvoorstel in batchmodus wordt geboekt vanwege de samenvoeging met **GeneralJournalAccountEntry**. |
| Projectbeheer en boekhouding | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Er zijn prestatieproblemen wanneer een urenstaat wordt geboekt. |
| Projectbeheer en boekhouding | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | De hiërarchie van kostenramingen van de structuur voor werkspecificatie is niet correct uitgelijnd nadat alle taken zijn uitgevouwen of nadat een enkele taak handmatig is uitgevouwen. |
| Projectbeheer en boekhouding | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Het Excel-sjabloon voor projectofferte kan niet worden toegevoegd aan het menu **Openen in Excel**. |
| Projectbeheer en boekhouding | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Het belastingvrijstellingsnummer voor een rechtspersoon wordt niet opgenomen op de afgedrukte projectfactuur. |
| Projectbeheer en boekhouding | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Er worden geen financiële gegevens bijgewerkt in de voorraadeenheidsfout wanneer een project wordt aangepast met betrekking tot creditregels. |
| Projectbeheer en boekhouding | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Nadat u KB 461935 hebt toegepast, kunt u geen ramingen boeken als u overschakelt naar doorlopende nummerreeksen. |
| Projectbeheer en boekhouding | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** zorgt ervoor dat de mobiele app voor projecturenstaat voor Android niet meer reageert. |
| Projectbeheer en boekhouding | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | De teruggeboekte OHW-waarde van een factuurboeking wijkt af van de oorspronkelijk geboekte OHW-waarde uit de tijdsvermelding. |
| Projectbeheer en boekhouding | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Bij toegepaste voorschotten zijn de transacties op een boekstuk niet in evenwicht wanneer gefactureerde opbrengst voor een project wordt geboekt. |
| Projectbeheer en boekhouding | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Wanneer de functie voor **Verbetering van de prestaties van projectresourceplanning** is ingeschakeld, worden decimale waarden onjuist afgerond voor de beschikbaarheid en capaciteit van resources. |
| Projectbeheer en boekhouding | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Wanneer de functie **Projectramingen maken met behulp van meerdere batchtaken** is ingeschakeld, werkt het maken van ramingen in een batch met meerdere subtaken alleen voor de huidige periode. |
| Reizen en onkosten | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Beleid voor reisaanvragen wordt genegeerd en de werkstroom wordt zonder fouten goedgekeurd. |
| Reizen en onkosten | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>De mobiele app voor onkosten slaat de volgende informatie niet op de onkostenregel op:</p><ul><li>De project-id</li><li>Of de onkosten factureerbaar zijn</li><li>Het activiteitsnummer</li></ul> |
| Reizen en onkosten | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Het veld **Bijgevoegd ontvangstbewijzen** is ingesteld op **Ja** zelfs als de onkostenregel geen ontvangstbewijs heeft. |
| Reizen en onkosten | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Er treedt een fout op wanneer u de onkostencategorie probeert te wijzigen in **Persoonlijk**. |
| Reizen en onkosten | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Nadat een creditcardtransactie is gesplitst op persoonlijke onkosten, kunt u de bovenliggende onkosten niet bewerken en geen ontvangstbewijs bijvoegen. |
| Reizen en onkosten | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Het onkostenbeleid voor intercompany-transacties met een project-id werkt niet naar behoren. |
| Reizen en onkosten | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | De informatie over geboekte datum ontbreekt voor geboekte onkostennota's. |
| Reizen en onkosten | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Er zijn problemen met de betalingsmethode in de mobiele app voor onkosten. |
| Reizen en onkosten | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Een voor een werknemer gemaakte reisaanvraag, kan worden gebruikt voor de onkostennota van een andere werknemer vóór de machtigingsdatum. |
| Reizen en onkosten | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Wanneer u een onkostenpost maakt, worden veranderende waarden voor financiële dimensies niet correct bijgewerkt op het niveau van de boekhoudingsverdeling in de werkruimte **Onkostenbeheer**. |
| Reizen en onkosten | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | De goedkeuringsstatus van de hoofdonkostenregel wordt niet gesynchroniseerd met de goedkeuringsstatus van de werkstroom voor de gespecificeerde regel. |
| Reizen en onkosten | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Er treedt een fout op als u een onkostennota boekt en belastingteruggave is ingeschakeld. |
| Reizen en onkosten | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Een gemachtigde kan geen onkostendocumenten verwijderen voor een ontslagen werknemer. |
| Reizen en onkosten | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Het verwijderen van een onkostenregel duurt langer dan verwacht en beïnvloedt de prestaties. |
| Reizen en onkosten | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** veroorzaakt een verweesde record **TaxUncommitted**, omdat alleen **SourceDocumentLine** wordt verwijderd. |
| Reizen en onkosten | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** houdt geen rekening met **trvExpTrans.ReferenceDataAreaId** om de nieuwe nummerreeks te maken. |

## <a name="regulatory-updates"></a>Wijzigingen in regelgeving

Voor informatie over updates in regelgeving voor Finance and Operations-apps leest u [Wijzigingen in regelgeving](/dynamics365/finance/localizations/regulatory-updates). U kunt zich ook aanmelden bij Microsoft Dynamics Lifecycle Services (LCS) en het hulpprogramma Problemen zoeken gebruiken om de geplande updates van de regelgeving te bekijken. Met Problemen zoeken kunt u zoeken op land of regio, type functie en versie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
