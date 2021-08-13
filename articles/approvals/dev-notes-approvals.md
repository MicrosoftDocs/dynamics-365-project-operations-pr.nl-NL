---
title: Opmerkingen van de ontwikkelaar voor goedkeuringen
description: Dit onderwerp bevat aanvullende informatie voor ontwikkelaars over het werken met goedkeuringen.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991660"
---
# <a name="developer-notes-for-approvals"></a>Opmerkingen van de ontwikkelaar voor goedkeuringen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations bevat validatielogica die zorgt voor een correcte recordovergang tijdens de goedkeuringsfasen. Correcte recordovergangen zorgen voor: 

  - Alle ondersteunende rijen worden gemaakt in gerelateerde tabellen, zoals journalen en werkelijke waarden.
  - De goedkeurder wordt gemarkeerd als een **Projectgoedkeurder** in het project voordat u verder gaat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]