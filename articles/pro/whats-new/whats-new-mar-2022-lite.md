---
title: Nieuwe functies van maart 2022 - Lite-implementatie Project Operations
description: Dit onderwerp biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations Lite-implementatie van maart 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583744"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Nieuwe functies van maart 2022 - Lite-implementatie Project Operations

_Van toepassing op: Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Microsoft Dynamics 365 Project Operations:

- Project Operations in een Dataverse-omgeving versie 4.30.0.99

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

- Onderaanneming: het maken van leveranciersfacturen en het afstemmen van ervaringen

## <a name="quality-updates"></a>Kwaliteitsupdates

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

## <a name="removed-and-deprecated-features"></a>Verwijderde en afgeschafte functies

In het onderwerp [Verwijderde of afgeschafte functies in Project Operations](../../whats-new/removed-depreciated-features-project.md) onderwerp beschrijft functies die zijn verwijderd of afgeschaft voor Dynamics 365 Project Operations.

- Een verwijderde functie is niet langer beschikbaar in het product.
- Een afgeschafte functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Er wordt 12 maanden voordat een functie wordt verwijderd uit het product een aankondiging van afschaffing weergegeven in het onderwerp [Verwijderde of afgeschafte functies in Project Operations](../../whats-new/removed-depreciated-features-project.md).
