---
title: Nieuwe functies van november 2020 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de release van november 2020 van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b76ebbff1cc2720e699334601d425879f2d20770
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600368"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van november 2020 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

- Project Operations in CDS-omgeving, versie 4.4.0.70
- Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving versie 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Updates voor Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

### <a name="project-operations-on-cds"></a>Project Operations in CDS

| Functiegebied                 | Referentienummer | Kwaliteitsupdate                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verkoopkansenbeheer       | 2036993          | Schattingsregels en contractregels voor resourcetoekenningen worden bijgewerkt in winnende prijsopgaven wanneer het type prijsopgaveregel **Alle taken** is.                                                 |
| Facturering en prijzen          | 2070392          | Projectcontractregels op de factuur nemen elke keer toe als **Factuurtransacties vernieuwen** wordt geselecteerd.                                                                         |
| Projectplanning             | 2043336          | Kan de record van een projectteamlid niet verwijderen.                                                                                                                                  |
| Projectplanning             | 2046013          | Inconsistent gedrag voor kolommen met schattingen tijdens laden versus bij verandering van type tijdfase.                                                                                   |
| Projectplanning             | 2046647          | Begin- en eindtijden wijken een uur af wanneer resourcevereisten worden gegenereerd door projectteamleden.                                                                      |
| Projectplanning             | 2053879          | (In de komende CDS-uitrol) PublishUnassignedAssignments onderbreekt een poging om een taak op te slaan bij de fout "De doorgegeven waarde voor ConditionOperator.In is leeg".                       |
| Projectplanning             | 2055501          | Als **Startdatum van project** leeg is, veroorzaakt dat een fout in de planning.                                                                                                      |
| Projectplanning             | 2066817          | Kan geen generieke resource maken met Personen selecteren in het tabblad **Taken**.                                                                                                   |
| Projectplanning             | 2067034          | De knop **Details weergeven** is niet beschikbaar op de pagina **Details van de taak**.                                                                                                       |
| Resourcebeheer          | 2046667          | Generieke teamleden worden niet verwijderd, zelfs niet nadat aan alle bronnen is voldaan.                                                                                                    |
| Snelle invoer van tijd en onkosten | 2047499          | De knop **Nieuw** op de pagina Tijdsvermelding opent de pagina **Nieuwe e-mailhandtekening**.                                                                                               |
| Snelle invoer van tijd en onkosten | 2059859          | Er wordt een onverwachte pop-up geopend wanneer u een onkostenpost maakt.                                                                                                                         |
| Overige                        | 2044181          | (Inkooporder verwijderen) Bij het verwijderen van msdyn_projectServiceCore_Patch en msdyn_ProjectServiceCore_solutions treedt de fout "Record is niet beschikbaar" op.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

| Functiegebied        | Referentienummer | Kwaliteitsupdate                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Omzetverantwoording | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Voltooid schattingspercentage voor project is onjuist wanneer het contract vreemde valuta gebruikt en werkvoortgangspercentage voor voltooiingsmethode.                     |
| Inkomstenverantwoording | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Kan geen schattingen boeken met de voltooiingsmethode **Werkelijke kosten**.                                                                                                    |
| Inkomstenverantwoording | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Verwijderen mislukt vanwege een fout in een onevenwichtig boekstuk wanneer de bedrijfsvaluta en de transactievaluta verschillend zijn.                                              |
| Onkostenbeheer  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Voor gebruikers die geen beheerder zijn, worden de opzoekwaarden voor kolommen met onkostenregels, zoals **Project-id** en **Uitgavencategorie**, niet correct weergegeven in het gegevensconnectorframe. |
| Onkostenbeheer  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | De standaardregeleigenschap wordt niet weergegeven voor onkostencategorieën.                                                                                                         |
| Onkostenbeheer  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Onkostenintegratie moet de regeleigenschap uit de onkostennota bevatten.                                                                                             |
| Facturering           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Kan geen projectfactuurvoorstellen boeken vanwege de foutmelding dat de FD-combinatie niet is gevalideerd.                                                    |
| Facturering           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Kan transacties van de detailpagina **Factuur** niet weergeven.                                                                                                              |
| Facturering           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Factuurvoorstelregels kunnen worden verwijderd.                                                                                                                                  |
| Projectboekhouding  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Items in het menu **Prognose** zijn niet zichtbaar op de lijstpagina **Projecten**.                                                                                                   |
| Projectboekhouding  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Kan **Projectoverzicht**   > **Transacties en prognose** niet openen.                                                                                                       |
| Projectboekhouding  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Financiële administratie aanpassen** is niet ingeschakeld voor gefactureerde projecttransacties.                                                                                                  |
| Projectboekhouding  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Boekhoudgegevens zijn niet opgenomen in de tabel **ProjCDSActualsImport** wanneer het **Integratiejournaal** wordt geboekt.                                                  |
| Projectboekhouding  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | De vermelding voor de projectprognose wordt verdubbeld wanneer u een resourcetoewijzing verwijdert en weer toevoegt.                                                                            |
| Projectboekhouding  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Als u een koppeling met een project-id selecteert, wordt de URL van de CDS-dieptekoppeling niet geopend.                                                                                                         |
| Projectboekhouding  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Kan de startdatum van een taak in CDS niet bijwerken.                                                                                                                           |
| Projectboekhouding  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Als u de functie inschakelt, zijn meerdere contractregels niet mogelijk zonder CDS-integratie.                                                                                   |

### <a name="regulatory-updates"></a>Wijzigingen in regelgeving
Zie [Regelgevende updates](/dynamics365/finance/localizations/regulatory-updates) voor informatie over updates van regelgeving voor apps voor financiën en bedrijfsactiviteiten. U kunt ook inloggen op LCS en de geplande updates van de regelgeving bekijken met de tool Probleem zoeken. Met het Probleem zoeken kunt u zoeken op land, type functie en release.


[!INCLUDE[footer-include](../includes/footer-banner.md)]