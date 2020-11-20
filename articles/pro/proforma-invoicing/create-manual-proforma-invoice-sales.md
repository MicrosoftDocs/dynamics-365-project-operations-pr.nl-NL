---
title: Handmatig een pro-formafactuur maken - lite
description: Dit onderwerp bevat informatie over het handmatig maken van pro-formafacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176380"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Handmatig een pro-formafactuur maken - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In Dynamics 365 Project Operations kunnen pro-formafacturen indien nodig handmatig worden gemaakt. U kunt handmatig een pro-formafactuur maken op de lijstpagina **Projectcontracten** of op de detailpagina **Projectcontract**.

##  <a name="project-contracts-list-page"></a>Lijstpagina Projectcontracten

Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten en maak facturen voor alle geselecteerde records.

Er wordt gecontroleerd welke van de geselecteerde projectcontracten een achterstallige **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt. Op basis van deze contracten worden conceptpro-formafacturen gemaakt. Als een projectcontract meerdere klanten heeft, kan er één factuur per klant worden gemaakt en meerdere facturen per projectcontract.

Alle gemaakte projectfacturen zijn beschikbaar op de pagina **Factuur** in de sectie **Facturering** van het gebied **Verkoop**.

## <a name="project-contract-details-page"></a>Detailpagina Projectcontract

Een pro-formafactuur kan ook worden gemaakt op de detailpagina **Projectcontract**, waarmee de factuur voor dat specifieke projectcontract wordt gemaakt. Er wordt gecontroleerd of het projectcontract een achterstallige **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt. Op basis van deze contracten worden conceptpro-formafacturen gemaakt op basis van het aantal klanten op elke contractregel.

Als er één pro-formafactuur wordt gemaakt, wordt de pagina **Factuur** geopend. Als er meerdere facturen zijn gemaakt voor dat projectcontract, dan wordt de lijstpagina **Facturen** geopend om alle gemaakte facturen weer te geven.
