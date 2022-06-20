---
title: Instellingen voor verkoopkansen - lite
description: Dit artikel biedt informatie over projectgebaseerde deals en projectgebaseerde verkoopkansregels.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e2a95c57bff326237fb97a6cf432096833369eb8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934406"
---
# <a name="header-details-for-project-opportunities"></a>Koptekstdetails voor projectverkoopkansen

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

De header van de verkoopkans bevat de algemene informatie over een projectgebaseerde deal die van toepassing is op alle regels van de projectgebaseerde verkoopkans.

Projectmatige verkoopkansen in Dynamics 365 Project Operations zijn uitbreidingen van verkoopkansen in Dynamics 365 Sales. Deze uitbreidingen bieden aanvullende functionaliteit die specifiek is en vereist voor projectgebaseerde verkoopkansen. Deze extensies kunnen nieuwe velden en lintacties bevatten die beschikbaar zijn in projectgebaseerde verkoopkansen. Mogelijk merkt u dat sommige velden, functionaliteit en standaardlogica die beschikbaar zijn in Sales, niet beschikbaar zijn in Project Operations.

De volgende tabel bevat de velden in een projectgebaseerde verkoopkans die uniek zijn voor Project Operations of die een aantal belangrijke gedragsveranderingen vertonen ten opzichte van verkoopkansen in Sales.

| **Veld** | **Locatie** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Type | Tabblad Algemeen (verborgen) | Deze optieset heeft de volgende opties:</br>- Op werk gebaseerd (alleen beschikbaar in Project Operations)</br>- Op artikel gebaseerd (alleen beschikbaar als Project Operations en Sales zijn geïnstalleerd)</br>- Op onderhoud gebaseerd (beschikbaar wanneer Field Service is geïnstalleerd) | Wanneer u Project Operations gebruikt, wordt deze veldwaarde automatisch ingesteld op **Op werk gebaseerd** waardoor de verkoopkans wordt ingedeeld als projectgebaseerd. Een verkoopkans moet projectgebaseerd zijn om alle projectspecifieke uitbreidingen en functionaliteit in het downstream-verkoopproces voor deze deal in te schakelen. |
| Contact | Tabblad Algemeen | Verwijzing naar de primaire contactpersoon van de klant voor deze deal. | |
| Account | Tabblad Algemeen | Verwijzing naar het bedrijf of de accountrecord van de klant. | |
| Accountmanager | Tabblad Algemeen | De naam van de accountmanager voor deze projectgebaseerde verkoopkans. | De accountmanager is verantwoordelijk voor het beheren van de relatie met de klant tot aan de afronding van dit project. De contracterende eenheid wordt standaard ingesteld op basis van de record met boekbare resources die is gekoppeld aan de accountmanager. |
| Contracterende eenheid | Tabblad Algemeen | De organisatie-eenheid die verantwoordelijk is voor de oplevering van het project of de projecten die bij deze deal horen. | De contracterende eenheid is de divisie van het bedrijf dat de projecten zal voltooien nadat de deal is gesloten. Elke contracterende eenheid heeft een valuta en deze valuta wordt gebruikt om de geschatte en werkelijke kosten te rapporteren die tijdens het project zijn gemaakt. |

Voor alle andere velden en secties op het tabblad **Samenvatting** van de verkoopkans raadpleegt u [Verkoopkansen maken of bewerken (Verkoop en Verkoophub)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
