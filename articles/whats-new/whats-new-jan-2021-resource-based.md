---
title: Nieuwe functies van januari 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de release van januari 2021 van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e5bfd3c790dac51895cde04e08d1fa62f4457e8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5292063"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van januari 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_


Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

  - Project Operations in Dataverse-omgeving, versie 4.6.0.154
  - Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving, versie 10.0.16

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| **Implementatie en configuratie** | 2106818 | De hernoeming van de webresource die problemen veroorzaakte bij het aanpassen van een pagina, is opgelost. |
| **Facturering en prijzen** | 2091908 | De zichtbaarheid van de opties **Prijzen vergrendelen** en **Huidige prijzen gebruiken** op de pagina **Factuur** wanneer Project Operations is geïnstalleerd samen met Dynamics 365 Field Service is opgelost. |
| **Facturering en prijzen** | 2103058 | **Projecttotalen** is vernieuwd om null-waarden te kunnen verwerken voor de werkelijke kosten van een taak. |
| **Facturering en prijzen** | 2116100 | Verbeterde foutmeldingen die worden gebruikt met de functionaliteit **Boekingen corrigeren op werkelijke waarden**. |
| **Facturering en prijzen** | 2116129 | Verbeterde zichtbaarheid van kostenramingen op het tabblad **Schattingen** op de pagina **Projecten**. |
| **Facturering en prijzen** | 2119112 | Vaste aggregatie van werkelijke verkopen en werkelijke kosten wanneer verschillende wisselkoersen worden gebruikt. |
| **Facturering en prijzen** | 2134705 | De fout 'Kan eigenschap **getResourceString** van niet gedefinieerd niet lezen' wanneer de pagina **Factuur** wordt geopend en Field Service wordt geïnstalleerd. |
| **Beheer van verkoopkansen** | 2022195 | Het taakgebaseerde factureringsraster op de pagina **Project** bevat een pictogram dat aangeeft dat er een contract- of prijsopgaveregel is gekoppeld aan die taak. |
| **Beheer van verkoopkansen** | 2029135 | De bedrijfsprocesfout opgelost die optreedt wanneer een gebruiker probeert een factuurregel te openen op een bevestigde factuur waarop een voorschotbedrag is gefactureerd. |
| **Beheer van verkoopkansen** | 2040713 | De scriptfout opgelost die optreedt bij het maken van een factuur op basis van een contract waarbij Field Service is geïnstalleerd. |
| **Projecten plannen en bijhouden** | 2090202 | Bedrijfsregels die niet meer worden gebruikt, gemarkeerd als **Afgeschaft**. |
| **Tijd en onkosten** | 2091249 | Aangescherpte controles, zodat gebruikers de taak niet kunnen wijzigen op een ingediende of goedgekeurde tijdsvermelding. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projectbeheer en boekhouding in Dynamics 365 Finance

| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| **Projectbeheer en boekhouding** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Onjuist contractbedrag op de pagina **A conto** voor een project met een vaste prijs met meerdere financieringsbronnen. |
| **Projectbeheer en boekhouding** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | De tijdelijke aanduiding **Invoiceproposal.PSAnfRefProjId** geeft niet de project-id weer voor de workflow **Projectfactuurvoorstellen controleren**. |
| **Projectbeheer en boekhouding** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | De verkeerde datum voor contantkorting wordt gebruikt bij het boeken van projectfactuurvoorstellen. |
| **Projectbeheer en boekhouding** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Door het verwijderen en lezen van resourcetoewijzingen in Project Operations wordt de invoer van projectprognoses in Finance verdubbeld. |
| **Projectbeheer en boekhouding** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | In project Operations kunt u geen projectschattingen in Dataverse maken zonder een contractregel op het project. |
| **Projectbeheer en boekhouding** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | De financiële dimensie van een projectonkostentransactie wordt niet gesynchroniseerd met het gerelateerde boekstuk en de boekhoudingsverdeling van de onkostendeclaratie wanneer kosten naar Saldo worden geboekt. |
| **Projectbeheer en boekhouding** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Het filter **Factuurstatus** in geboekte projecttransacties voor projecten met een vaste prijs werkt niet. |
| **Projectbeheer en boekhouding** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Schrapping van omgekeerde schatting werkt niet in de sectie **Periodiek**. |
| **Projectbeheer en boekhouding** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Factuurvoorstelregels kunnen worden verwijderd in Project Operations wanneer er een integratie is met Dataverse. |
| **Projectbeheer en boekhouding** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Voorkom het inschakelen van meerdere contractregels zonder Dataverse-integratie. |
| **Projectbeheer en boekhouding** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Wanneer facturering op rekening gelijk is aan winst en verlies, wordt de gefactureerde omzet weergegeven als nul op de pagina Ramingen. |
| **Projectbeheer en boekhouding** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Factuurcorrecties werken niet in geïntegreerde omgevingen. |
| **Projectbeheer en boekhouding** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Bij het boeken van OHW-verkoopwaarde bij intercompany-projectfacturering wordt de verkeerde rekening gekozen. |
| **Projectbeheer en boekhouding** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | In Project Operations kunnen afhankelijkheden van schattingstaken in Dataverse niet worden bijgewerkt. |
| **Projectbeheer en boekhouding** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Het herhaaldelijk verwijderen van project Operations-integratiejournalen in Finance leidt tot gegevensverlies. |
| **Projectbeheer en boekhouding** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | De volgende fout treedt op tijdens het boeken van een projectfactuurvoorstel: 'Transactie komt niet overeen met aangiftevaluta wanneer de afgetrokken voorschotfactuur er weer bij wordt opgeteld'. |
| **Projectbeheer en boekhouding** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | De verkeerde project-id wordt opgenomen in inhoudingen nadat het standaardprojectcontract is bijgewerkt in Project Operations. |
| **Projectbeheer en boekhouding** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Schatting en omzetverantwoording kunnen niet worden voltooid wanneer Project Operations is ingeschakeld. |
| **Projectbeheer en boekhouding** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Als u in Project Operations een project uit een contract verwijdert, wordt het standaardproject voor het contract niet gereset. |
| **Projectbeheer en boekhouding** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | In Project Operations worden op een intercompany-factuur de verkeerde onkostenregels weergegeven in de lijst **Regel toevoegen**. |
| **Reizen en onkosten** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Onkostenregels kunnen niet worden geboekt omdat uurinstellingen ontbreken op de contractregel. |
| **Reizen en onkosten** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Als validatie van project/ categorie verplicht is, zijn de onkostencategorieën die aan het project zijn gekoppeld, niet zichtbaar in de onkostendeclaratie. |
| **Reizen en onkosten** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Het saldo van het kasvoorschot wordt niet bijgewerkt wanneer een onkostendeclaratie per regel wordt geboekt. |
| **Reizen en onkosten** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | De taak **Betalingsgegevens bijwerken** mislukt na het ongedaan maken van verrekeningen waarbij een factuur is verrekend met twee of meer betalingstransacties. |
| **Reizen en onkosten** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Er is een probleem met de berekening van de maaltijdaftrek op de laatste dag voor de per diem onkostencategorie. |
| **Reizen en onkosten** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Het rapport **Onkostentype per werknemer** toont geen gespecificeerde onkosten als de eerste verbinding van de gebruiker in de taal es-MX was. |
| **Reizen en onkosten** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | De leveranciersbetaling voor een onkostendeclaratiefactuur gebruikt de verkeerde verzamelrekening voor het boeken van vereffeningen. |
| **Reizen en onkosten** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Wanneer een onkostendeclaratie wordt geboekt met **Groepering van transacties toestaan op basis van een tegenrekening voor betaling** en **Boekhouddatum corrigeren bij boeking** is ingeschakeld, geeft dat aan dat de boekhouddatums niet zijn gegroepeerd in de tabel **Boekhoudingsverdeling**, die van invloed is op de omzetbelastinggegevens. |
| **Reizen en onkosten** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Toewijzing van onkostensubcategorieën wordt verwijderd wanneer het selectievakje Gebruiken in onkosten wordt uitgeschakeld en vervolgens opnieuw ingeschakeld. |
| **Reizen en onkosten** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Er kan geen intercompany-onkostendeclaratie worden gemaakt als de project-id is toegevoegd op headerniveau. |
| **Reizen en onkosten** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Er is een probleem met onkostenbetalingen wanneer het onkostenbedrag hoger is dan het kasvoorschotbedrag. |
| **Reizen en onkosten** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Het veld **Project-id** op een intercompany-onkostendeclaratie is leeg als de gebruikersrol is toegewezen aan een specifieke organisatie. |
| **Reizen en onkosten** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | De onkostencategorie is vergrendeld bij het toevoegen van een nieuwe onkostenregel. |
| **Reizen en onkosten** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Het specificeren van onkostendeclaratieregels die al zijn gesplitst, resulteert in een onvolledig geboekt crediteuren-/grootboekboekstuk. Vanwege de duplicatie van **TRVEXPTRANS.SOURCEDOCUMENTLINE** is de Accounting Source Explorer ook verbroken. |
| **Reizen en onkosten** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | De index die is toegevoegd aan de tabel **TRVREQUISITIONLINE** waarvoor de klant duplicaten heeft, resulteert in een fout tijdens de upgrade. |
| **Reizen en onkosten** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | In Project Operations kan tijd met intercompany-taken in Dataverse niet worden gemaakt of goedgekeurd. |

## <a name="regulatory-updates"></a>Wijzigingen in regelgeving

Voor informatie over updates in regelgeving voor Finance and Operations-apps leest u [Wijzigingen in regelgeving](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). U kunt ook inloggen op LCS en de geplande updates van de regelgeving bekijken met de tool Probleem zoeken. Met het Probleem zoeken kunt u zoeken op land, type functie en release.


[!INCLUDE[footer-include](../includes/footer-banner.md)]