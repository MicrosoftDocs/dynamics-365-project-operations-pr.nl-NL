---
title: Opmerkingen van de ontwikkelaar voor goedkeuringen
description: Dit onderwerp bevat aanvullende informatie voor ontwikkelaars over het werken met goedkeuringen.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996785"
---
# <a name="developer-notes-for-approvals"></a>Opmerkingen van de ontwikkelaar voor goedkeuringen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations bevat validatielogica die zorgt voor een correcte recordovergang tijdens de goedkeuringsfasen. Correcte recordovergangen zorgen voor: 

  - Alle ondersteunende rijen worden gemaakt in gerelateerde tabellen, zoals journalen en werkelijke waarden.
  - De goedkeurder wordt gemarkeerd als een **Projectgoedkeurder** in het project voordat u verder gaat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]