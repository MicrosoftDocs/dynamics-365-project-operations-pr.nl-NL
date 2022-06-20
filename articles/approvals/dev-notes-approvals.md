---
title: Opmerkingen van de ontwikkelaar voor goedkeuringen
description: Dit artikel bevat aanvullende informatie voor ontwikkelaars over werken met goedkeuringen.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924746"
---
# <a name="developer-notes-for-approvals"></a>Opmerkingen van de ontwikkelaar voor goedkeuringen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations bevat validatielogica die zorgt voor een correcte recordovergang tijdens de goedkeuringsfasen. Correcte recordovergangen zorgen voor: 

  - Alle ondersteunende rijen worden gemaakt in gerelateerde tabellen, zoals journalen en werkelijke waarden.
  - De goedkeurder wordt gemarkeerd als een **Projectgoedkeurder** in het project voordat u verder gaat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]