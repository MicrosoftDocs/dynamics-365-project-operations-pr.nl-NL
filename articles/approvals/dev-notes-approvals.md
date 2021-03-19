---
title: Opmerkingen van de ontwikkelaar voor goedkeuringen
description: Dit onderwerp bevat aanvullende informatie voor ontwikkelaars over het werken met goedkeuringen.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290263"
---
# <a name="developer-notes-for-approvals"></a>Opmerkingen van de ontwikkelaar voor goedkeuringen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations bevat validatielogica die zorgt voor een correcte recordovergang tijdens de goedkeuringsfasen. Correcte recordovergangen zorgen voor: 

  - Alle ondersteunende rijen worden gemaakt in gerelateerde tabellen, zoals journalen en werkelijke waarden.
  - De goedkeurder wordt gemarkeerd als een **Projectgoedkeurder** in het project voordat u verder gaat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]