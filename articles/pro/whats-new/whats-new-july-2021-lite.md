---
title: Nieuwe functies juli 2021 - Project Operations Lite-implementatie
description: Dit onderwerp bevat informatie over de kwaliteitsupdates die beschikbaar zijn in de release van juli 2021 van Project Operations Lite-implementatie.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 475ceea3a6c6db9fe63e3950eaca5d9074faa766
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583946"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Nieuwe functies juli 2021 - Project Operations Lite-implementatie

_Van toepassing op: Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

  - Project Operations in Dataverse-omgeving versie 4.12.0.148 or 4.12.0.152.

## <a name="quality-updates"></a>Kwaliteitsupdates
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
| Algemeen                       | 2376405              | Probleem met door uitgevers aangestuurde update opgelost (kwaliteitsupdate is beschikbaar in versie 4.12.0.152)                                                                                                                     |
