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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483942"
---
# <a name="developer-notes-for-approvals"></a>Opmerkingen van de ontwikkelaar voor goedkeuringen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dynamics 365 Project Operations bevat validatielogica die zorgt voor een correcte recordovergang tijdens de goedkeuringsfasen. Correcte recordovergangen zorgen voor: 

  - Alle ondersteunende rijen worden gemaakt in gerelateerde tabellen, zoals journalen en werkelijke waarden.
  - De goedkeurder wordt gemarkeerd als een **Projectgoedkeurder** in het project voordat u verder gaat.