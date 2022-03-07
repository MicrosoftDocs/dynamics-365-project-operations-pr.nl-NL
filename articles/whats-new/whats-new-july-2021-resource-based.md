---
title: Nieuwe functies van juli 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit onderwerp bevat informatie over de kwaliteitsupdates die beschikbaar zijn in de release van juli 2021 van Project Operations voor scenario´s op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5dbf9c7158ce7d9e568e270791e7e7aaf8ce731d
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433512"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van juli 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

*Van toepassing op: Project Operations voor scenario's op basis van resources/niet-voorradige artikelen*

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

   - Project Operations in Microsoft Dataverse-omgeving versie 4.12.0.148.
   - Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving, versie 10.0.20.

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

In deze versie zijn de volgende functies opgenomen:

- Mogelijkheid voor beheerders om PSS-logboeken en Operations Set-logboeken te bekijken vanuit het instellingenmenu. De logboeken worden 90 dagen bewaard.

## <a name="project-operations-dual-write-maps-updates"></a>Updates van kaarten voor twee keer wegschrijven in Project Operations

Er zijn geen updates voor toewijzingen van twee keer wegschrijven in Project Operations in deze release.

Zie [Toewijzingsversies van twee keer wegschrijven voor Project Operations](../environment/resource-dual-write-maps.md) voor een actuele lijst en versies van toewijzingen van twee keer wegschrijven voor Project Operations.

Voer altijd de nieuwste versie van de toewijzing uit in uw omgeving en schakel alle gerelateerde tabeltoewijzingen in wanneer u de versie van uw Project Operations Dataverse-oplossing en Finance-oplossing bijwerkt. Bepaalde functies en mogelijkheden werken mogelijk niet correct als niet de meest recente versie van de toewijzing is geactiveerd. U kunt de actieve versie van de toewijzing zien op de pagina **Twee keer wegschrijven** in de kolom **Versie**. Activeer een nieuwe versie van de toewijzing door **Versies van tabeltoewijzing** te selecteren, de nieuwste versie te selecteren en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, past u de wijzigingen opnieuw toe. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.

Als u een probleem ondervindt bij het starten van de toewijzing, volgt u de instructies in het gedeelte [Probleem met ontbrekende tabelkolommen in toewijzingen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in de handleiding voor het oplossen van problemen met twee keer wegschrijven.

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Functiegebied**              | **Referentienummer** | **Kwaliteitsupdate**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturering en prijzen           | 2224046              | Het veld **Transactieklasse** is bewerkbaar op het tabblad **Details prijsopgaveregel**, maar wordt vergrendeld als u werkt vanuit de pagina **Details prijsopgaveregel**.                                                                     |
| Facturering en prijzen           | 2224400              | De actie **Prijsopgave sluiten als gewonnen** mislukt als een prijsopgave geen mijlpalen voor de datum heeft.                                                                                                                                    |
| Facturering en prijzen           | 2234089              | Wanneer u handmatig een productbeschrijving invoert, wordt deze gewist nadat u een hoeveelheid voor een materiaalschatting hebt ingevoerd.                                                                                                                         |
| Facturering en prijzen           | 2234100              | Het raster **Factureringsinstellingen van taak** bevat niet de kolom **Materiaal** en de bijbehorende waarde op het tabblad **Facturering taak** van het project.                                                                                                       |
| Facturering en prijzen           | 2277409              | De product-ID is niet beschikbaar in het contractregeldetail voor een materiaaltyperegel.                                                                                                                                        |
| Facturering en prijzen           | 2281728              | Als een contractregel wordt gemaakt, worden de werkelijke waarden onnodig opnieuw geëvalueerd, wat leidt tot een aanzienlijke toename van het gegevensvolume, wat weer van invloed is op de prestaties.                                                                                |
| Facturering en prijzen           | 2298668              | Journaalregels die zijn gekoppeld aan ingetrokken en verwijderde onkosten, worden niet verwijderd.                                                                                                                                     |
| Facturering en prijzen           | 2300192              | Wanneer meerdere gebruikers een factuur bewerken, is het mogelijk dat er een nieuw factuurregeldetail wordt gemaakt op een bevestigde factuur.                                                                                   |
| Facturering en prijzen           | 2301569              | Facturen kunnen niet worden gecorrigeerd als er een bedrag van \$0 is ingehouden.                                                                                                                                        |
| Facturering en prijzen           | 2307965              | Er treedt een fout op als er een categorieprijs wordt gemaakt met ontbrekende waarden.                                                                                                                           |
| Facturering en prijzen           | 2326870              | Er treedt een fout op in **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** als **producttypecode** null is.                                                                            |
| Facturering en prijzen           | 2332732              | Er treedt een fout op als een mijlpaal in de contractregel wordt gemaakt zonder een orderregel.                                                                                                                |
| Projecten plannen en bijhouden | 2181094              | De Project Scheduling-API ondersteunt nu PSS-logboeken en Operation Set-logboeken die 90 dagen worden bewaard.                                                                                                                  |
| Projecten plannen en bijhouden | 2254201              | Het label **Planningsmodus** wordt bijgewerkt met details waarmee de standaardlogica wordt beschreven.                                                                                                                                      |
| Projecten plannen en bijhouden | 2300252              | De **openProject**-responscache wordt bijgewerkt en bevat de tokeneigenaar in de cachesleutel, **basis-URL** en **Segment-URL** zodat **Aanvraag-URL** altijd opnieuw kan worden gemaakt als de **basis-URL** verandert. |
| Projecten plannen en bijhouden | 2301312              | **msdyn_membershipstatus** is verwijderd uit de weergave **Projectteamlid**.                                                                                                                                        |
| Projecten plannen en bijhouden | 2302759              | Producten worden onnodig opgehaald op de tabbladen **Resourcetoewijzingen**, **Schattingen** en **Onkostenschattingen**.                                                                                                        |
| Projecten plannen en bijhouden | 2308050              | **CopyProject** mislukt met de fout "Kan token niet ophalen om met externe service te communiceren".                                                                                                                           |
| Projecten plannen en bijhouden | 2322650              | De weergave **Projecttakenlijst** is bijgewerkt om standaard de datum van de taak weer te geven.                                                                                                            |
| Projecten plannen en bijhouden | 2327266              | **CopyProject** genereert de fout "Sleutel niet gevonden in woordenboek" bij het kopiëren van schattingen.                                                                                                      |
| Projecten plannen en bijhouden | 2328123              | **CopyProject** genereert de fout "Kan token niet ophalen om met externe service te communiceren".                                                                                                                          |
| Projecten plannen en bijhouden | 2336258              | **CopyProject** kopieert de positienamen van resources onjuist.                                                                                                                                                 |
| Facturering en prijzen           | 2224476              | Het veld **Boekbare resource** is niet correct standaard ingesteld op de aangemelde gebruiker op de pagina **Materiaalgebruik**.                                                                                                            |
| Resourcebeheer           | 2277249              | Er treedt een fout op wanneer een niet-projectgebaseerde resourcevereiste wordt bijgewerkt.                                                                                                            |
| Resourcebeheer           | 2323869              | Resourcegebruik herkent gefilterde resources niet correct.                                                                                                                                             |
| Tijd en onkosten              | 2176538              | Er worden onjuiste filteroperators toegepast op het besturingselement **Tijdsvermelding**.                                                                                                                                                   |
| Tijd en onkosten              | 2177462              | Als u een tijdsvermelding in het raster verwijdert, wordt de status van de knoppen **Indienen**, **Intrekken**, **Verwijderen** en **Vermelding bewerken** niet zoals verwacht bijgewerkt.                                                                                        |
| Tijd en onkosten              | 2299985              | Met **TimeEntriesImportFromResourceAssignment** wordt de begin-/eindtijd van de toewijzingscontouren niet bijgehouden.                                                                                                  |
| Tijd en onkosten              | 2318426              | Nadat een tijdsvermelding is ingediend, kunnen vergrendelde velden nog steeds worden bewerkt.                                                                                                                                   |
| Tijd en onkosten              | 2323749              | Er treedt een fout op wanneer onkosten worden gemaakt via het tabblad **Gerelateerd** van een boekbare resource.                                                                                                      |
| Tijd en onkosten              | 2327678              | Wanneer u een tijdsvermelding maakt via het tabblad **Gerelateerd** van een boekbare resource, wordt de bovenliggende resource niet doorgegeven aan het besturingselement voor tijdsvermelding.                                                                            |
| Algemeen                       | 2296857              | Voortgangstracering voor langlopende taken.                                                                                                                                                                        |
| Algemeen                       | 2253682              | De oplossing voor twee keer wegschrijven van Project Operations mag niet worden geïnstalleerd wanneer de kernoplossing voor twee keer wegschrijven is geïnstalleerd in een omgeving zonder de indelingsoplossing voor twee keer wegschrijven.                                                |
| Algemeen                       | 2316420              | De inrichting van de kern van Project Service mislukt als de business unit van de toepassingsgebruiker wordt gewijzigd.                                                                                                                     |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

| Functiegebied                      | Referentienummer | Kwaliteitsupdate                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projectbeheer en boekhouding | 4620267          | Kan formulieren om het veld **Doel** toe te voegen niet personaliseren voor de pagina´s **Geboekte projecttransactie**, **Factuurvoorstel maken** en **Factuurvoorstel**.                                                                                                                                                                                         |
| Projectbeheer en boekhouding | 4613449          | Wanneer u een projectcontract-ID selecteert in Finance, opent de geïntegreerde omgeving van Project Operations de pagina om een nieuw record te maken in plaats van de pagina voor reeds gemaakte projectcontracten.                                                                                                                                           |
| Projectbeheer en boekhouding | 4614445          | In de implementatie van het geïntegreerde scenario van Project Operations kunt u het veld **Btw-groep artikel** niet bewerken op het factuurvoorstel dat vanuit opslag is geïmporteerd. De btw-groep voor artikelen moet bewerkbaar zijn voor een open factuurvoorstel van alle transactietypen, inclusief rekening, uren, onkosten, vergoedingen en artikelen. |
| Projectbeheer en boekhouding |                  | Kan een factuurvoorstel niet boeken als gevolg van een negatieve tijdtransactiecorrectie.                                                                                                                                                                                                                                              |
| Projectbeheer en boekhouding |                  | Factuurvoorstelregels worden gedupliceerd vanwege meerdere periodieke **Importeren uit opslag**-processen die tegelijkertijd worden uitgevoerd.                                                                                                                                                                                                                |

