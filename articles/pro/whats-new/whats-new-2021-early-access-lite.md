---
title: Wat is er nieuw in de versie voor vroege toegang van wave 2 voor 2021 - Project Operations Lite-implementatie
description: Dit onderwerp bevat informatie over de functies die beschikbaar zijn in de versie voor vroege toegang van wave 2 voor 2021 van Project Operations Lite-implementatie.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323905"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Wat is er nieuw in de versie voor vroege toegang van wave 2 voor 2021 - Project Operations Lite-implementatie

_Van toepassing op: Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp is van toepassing op de volgende onderdelen en versies van Dynamics 365 Project Operations:

  - Project Operations in Dataverse-omgeving, versie 4.23.0.4

De release wordt alleen toegepast wanneer een omgeving is [aangemeld voor vroege toegang](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>In deze versie zijn de volgende functies opgenomen

[Onderaannemingsbeheer](../subcontracting/subcontracting_EA_scope.md) - Deze functie biedt betere zichtbaarheid en controle over alle aspecten van het werk aan een project. De preview van onderaannemingsbeheer omvat de volgende mogelijkheden:

  - Een projectmanager kan een subcontract opstellen met een leverancier. Standaard worden de prijslijsten die aan de leveranciersrecord zijn gekoppeld, gebruikt voor het subcontract. De leveranciersaccount heeft het relatietype **Verkoper** of **Leverancier**.
  - Een projectmanager kan alle aankopen specificeren als regelitems in het subcontract. Subcontractregels kunnen voor tijd, onkosten of producten zijn. De transactieklasse van de subcontractregel bepaalt waarvoor de regel dient.
  - De accountmanager van de leverancier en de projectmanager kunnen het subcontract herhalen. De prijzen kunnen worden aangepast in de inkoopprijslijsten die aan het subcontract zijn gekoppeld.
  - Tijdens het proces kan de accountmanager van de leverancier, als de subcontractregel voor tijd is, contactpersonen aan elke subcontractregel koppelen. Deze koppeling biedt informatie aan de projectmanager die aan het subcontract werkt. Wanneer een leverancierscontactpersoon aan een subcontractregel is gekoppeld, maakt het systeem automatisch een boekbare resource van de contactpersoon aan, als er nog geen boekbare resource bestaat.
  - De factureringsmethode op elke subcontractregel kan Vaste prijs of Tijd en materiaal zijn. Voor subcontractregels met een vaste prijs wordt een op mijlpalen gebaseerd factuurschema ingesteld.
