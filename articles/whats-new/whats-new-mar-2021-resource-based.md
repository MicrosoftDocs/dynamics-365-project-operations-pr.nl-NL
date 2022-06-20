---
title: Nieuwe functies van maart 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen
description: Dit artikel biedt informatie over de kwaliteitsupdates die beschikbaar zijn in de versie van Project Operations van maart 2021 voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932934"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nieuwe functies van maart 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit artikel is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

- Project Operations in Dataverse-omgeving, versie 4.8.0.91 
- Projectbeheer en financiële administratie in Dynamics 365 Finance-omgeving versie 10.0.16 

## <a name="quality-updates"></a>Kwaliteitsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse


| **Functiegebied** | **Referentienummer** | **Kwaliteitsupdate** |
| --- | --- | --- |
| Facturering en prijzen | 2133873 | De weergave van het valutasymbool voor **Verkoopprijs per eenheid** in het raster **Onkostenschattingen** is gecorrigeerd. |
| Facturering en prijzen | 2174616 | Wanneer een order wordt binnengehaald met een prijsopgave, wordt naar de aangepaste contractprijslijst verwezen op contractregeldetails die uit de prijsopgave worden gekopieerd. |
| Verkoopkansenbeheer | 2167475 | Vast belastingbedrag op de correctiefactuur waaruit een niet-gefactureerde werkelijke boeking is voortgekomen. |
| Verkoopkansenbeheer | 2176285 | Het belastingbedrag mag niet worden gekopieerd van verkoopcontract/prijsopgaveregeldetails naar kostencontract/prijsopgaveregeldetails. |
| Verkoopkansenbeheer | 2188079 | Regel voor gesplitste facturering mag niet worden gemaakt voor contracten die niet op werk zijn gebaseerd. |
| Planning en tracering | 2125274 | Kenmerk **Toewijzing twee keer wegschrijven voor project** voor **Toewijzing van startdatum van project** bijgewerkt van **msdyn\_taskearlieststart** naar **msdyn\_actualstart**. |
| Planning en tracering | 2138853 | Projectkopieerfunctie bijgewerkt om ervoor te zorgen dat de regels voor onkostenschatting die verwijzen naar taken naar het bestemmingsproject worden gekopieerd. |
| Planning en tracering | 2154306 | Problemen opgelost met het verwijderen van onkostenschattingen in Project Operations voor op resources gebaseerde scenario's. |
| Planning en tracering | 2173259 | Projectkopieerfunctie bijgewerkt om ervoor te zorgen dat hiervoor niet het foutbericht **Structuur voor werkspecificatie wordt gekopieerd** wordt weergegeven in bepaalde scenario's. |
| Tijd en onkosten | 2148910 | Weergaveprobleem opgelost met de pagina **Vermelding bewerken** in het raster **Tijdsvermelding**. |
| Tijd en onkosten | 2159798 | Verscherpte controles om ervoor te zorgen dat goedgekeurde onkostenposten niet kunnen worden bewerkt. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projectbeheer en financiële administratie in Dynamics 365 Finance

Zie [Nieuwe functies van januari 2021 - Project Operations voor scenario's op basis van resources/niet-voorradige artikelen](whats-new-jan-2021-resource-based.md) voor meer informatie.

## <a name="regulatory-updates"></a>Wijzigingen in regelgeving

Zie [Regelgevende updates](/dynamics365/finance/localizations/regulatory-updates) voor informatie over updates van regelgeving voor apps voor financiën en bedrijfsactiviteiten. Een andere manier om meer te weten te komen over updates van regelgeving is door u aan te melden bij LCS en de geplande updates van regelgeving te bekijken met behulp van de tool Probleem zoeken. Met het Probleem zoeken kunt u zoeken op land, type functie en release.


[!INCLUDE[footer-include](../includes/footer-banner.md)]