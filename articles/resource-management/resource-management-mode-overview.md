---
title: Overzicht van resourcebeheermodi
description: Dit artikel bevat informatie over functionaliteit voor resourcebeheer in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928426"
---
# <a name="resource-management-modes-overview"></a>Overzicht van resourcebeheermodi

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


Dynamics 365 Project Operations ondersteunt twee modi zodat u de algehele boekingsstroom kunt uitvoeren. De beheermodus wordt gedefinieerd als een projectparameter en kan worden gewijzigd als uw bedrijfsbehoeften veranderen.    

## <a name="central-mode"></a>Centrale modus
Voor organisaties die de toewijzing van resources aan projecten centraal regelen, vormt de modus Centraal een manier waarmee projectmanagers resourcevereisten op projectniveau kunnen definiëren. Het voldoen aan de resourcevereisten wordt gedelegeerd aan een resourcemanager. Projectmanagers kunnen resources accepteren of weigeren die door de resourcemanager worden voorgesteld.

![Centrale modus.](./media/resource-management-central.png)

Om resources te beheren met de Centrale modus, zie:

- [Algemene, boekbare resources toewijzen aan een taak en resourcevereisten genereren](/dynamics365/project-service/assign-generic-bookable-resource)
- [Benoemde resources boeken op basis van resourcevereisten](/dynamics365/project-service/book-named-resource)
- [Een resourceaanvraag indienen](/dynamics365/project-service/submit-resource-request)
- [Een resourceaanvraag afhandelen](/dynamics365/project-service/resource-management-fulfill-requests)
- [Een voorgestelde projectresource in een resourceaanvraag accepteren of afwijzen](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybride modus
In organisaties die flexibiliteit bij de toewijzing van resources nodig hebben, kunnen in de hybride modus zowel projectmanagers als resourcemanagers resources boeken.

![Hybride modus.](./media/resource-management-hybrid.png)

Bekijk, naast het ondersteunde proces in de centrale modus, de volgende artikelen om alle andere ondersteunde boekingsstromen in de hybride modus te beheren:

Een resource rechtstreeks boeken voor een project:
- [Benoemde, boekbare resources boeken voor een projectteam en taken toewijzen](/dynamics365/project-service/assign-named-bookable-resource)

Een resource boeken op basis van een resourcevereiste:
- [Algemene, boekbare resources toewijzen aan een taak en resourcevereisten genereren](/dynamics365/project-service/assign-generic-bookable-resource)
- [Benoemde resources boeken op basis van resourcevereisten](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]