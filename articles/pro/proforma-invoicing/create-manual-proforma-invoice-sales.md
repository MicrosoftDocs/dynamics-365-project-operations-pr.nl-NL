---
title: Handmatig een pro-formafactuur maken - lite
description: Dit onderwerp bevat informatie over het handmatig maken van pro-formafacturen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764497"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Handmatig een pro-formafactuur maken - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In Dynamics 365 Project Operations kunnen pro-formafacturen indien nodig handmatig worden aangemaakt. U kunt handmatig een pro-formafactuur maken op de lijstpagina **Projectcontracten** of op de detailpagina **Projectcontract**.

##  <a name="project-contracts-list-page"></a>Lijstpagina Projectcontracten

Selecteer op de lijstpagina **Projectcontracten** een of meer projectcontracten en maak facturen voor alle geselecteerde records.

Het systeem controleert welke van de geselecteerde projectcontracten een backlog heeft voor **Gereed voor facturering** die een datum heeft die vóór de datum van vandaag ligt. Op basis van deze contracten worden conceptpro-formafacturen gemaakt. Als een projectcontract meerdere klanten heeft, kan er één factuur per klant worden gemaakt en meerdere facturen per projectcontract.

Alle gemaakte projectfacturen zijn beschikbaar op de pagina **Factuur** in de sectie **Facturering** van het gebied **Verkoop**.

## <a name="project-contract-details-page"></a>Detailpagina Projectcontract

Een pro-formafactuur kan ook worden gemaakt op basis van de **Projectcontract**-detailpagina. Het systeem verifieert welk projectcontract een backlog voor **Gereed voor facturering** heeft die een datum heeft die vóór de datum van vandaag ligt. Op basis van deze contracten worden conceptpro-formafacturen gemaakt op basis van het aantal klanten op elke contractregel.

Als er één pro-formafactuur wordt gemaakt, wordt de pagina **Factuur** geopend. Als er meerdere facturen worden aangemaakt voor dat projectcontract, opent de lijstpagina **Facturen** om alle gemaakte facturen weer te geven.
