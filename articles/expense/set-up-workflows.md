---
title: Werkstromen instellen voor onkostenbeheer
description: U kunt een werkstroomproces instellen dat wordt gebruikt om reis- en onkostendocumenten te beoordelen en goed te keuren.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127692"
---
# <a name="set-up-workflows-for-expense-management"></a>Werkstromen instellen voor onkostenbeheer

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U kunt een werkstroomproces instellen om reis- en onkostendocumenten te beoordelen en goed te keuren. U kunt werkstromen definiëren voor onkostennota's, aanvragen voor reis- en verblijfskostenvergoeding en aanvragen voor kasvoorschotten.

Een werkstroom vertegenwoordigt een bedrijfsproces. In een werkstroom wordt gedefinieerd hoe een document door het systeem wordt verwerkt. De werkstroom geeft ook aan wie een taak moet voltooien of een document moet goedkeuren. Het gebruik van het werkstroomsysteem in uw organisatie heeft verschillende voordelen:

- **Consistente processen**: u kunt het goedkeuringsproces definiëren voor specifieke documenten, zoals inkoopaanvragen en onkostennota's. Het gebruik van het werkstroomsysteem zorgt ervoor dat documenten op een consistente en efficiënte manier worden verwerkt en goedgekeurd.
- **Zichtbaarheid van het proces**: u kunt de status, geschiedenis en prestatiestatistieken van een specifieke werkstroominstantie volgen. Dit helpt u om te bepalen of er wijzigingen in de werkstroom moeten worden aangebracht om de efficiëntie te verbeteren.
- **Gecentraliseerde werklijst**: gebruikers kunnen een gecentraliseerde werklijst weergeven om de werkstroomtaken en goedkeuringen te bekijken die aan hen zijn toegewezen. 

## <a name="workflow-types"></a>Werkstroomtypen

De onderstaande tabel bevat de werkstroomtypen die u kunt maken in **Onkostenbeheer**.


|              <strong>Type</strong>              |                   <strong>Gebruik dit type voor het volgende</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatisch goedkeuren van onkostenrapporten</strong> |            Maken van goedkeuringswerkstromen voor onkostennota's.             |
|  <strong>Automatisch boeken van onkostennota's</strong>   |        Maken van werkstromen voor het automatisch boeken van onkostennota's.        |
|       <strong>Onkostenregelitem</strong>        |     Maken van goedkeuringswerkstromen voor regelitems in onkostennota's.      |
| <strong>Automatisch boeken van onkostenregelitems</strong> | Maken van werkstromen voor het automatisch boeken van van regelitems in onkostennota's. |
|       <strong>Reiskosten</strong>       |          Maken van goedkeuringswerkstromen voor aanvragen voor reis- en verblijfskostenvergoeding.           |
|      <strong>Aanvraag voor kasvoorschot</strong>      |         Maken van goedkeuringswerkstromen voor aanvragen voor kasvoorschotten.          |
|        <strong>Btw-afschrijving</strong>        | maken van goedkeuringswerkstromen voor het innen van btw (belasting toegevoegde waarde).  |
