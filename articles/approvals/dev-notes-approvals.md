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
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="5b1b0-103">Opmerkingen van de ontwikkelaar voor goedkeuringen</span><span class="sxs-lookup"><span data-stu-id="5b1b0-103">Developer notes for Approvals</span></span>

<span data-ttu-id="5b1b0-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="5b1b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b1b0-105">Dynamics 365 Project Operations bevat validatielogica die zorgt voor een correcte recordovergang tijdens de goedkeuringsfasen.</span><span class="sxs-lookup"><span data-stu-id="5b1b0-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="5b1b0-106">Correcte recordovergangen zorgen voor:</span><span class="sxs-lookup"><span data-stu-id="5b1b0-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="5b1b0-107">Alle ondersteunende rijen worden gemaakt in gerelateerde tabellen, zoals journalen en werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="5b1b0-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="5b1b0-108">De goedkeurder wordt gemarkeerd als een **Projectgoedkeurder** in het project voordat u verder gaat.</span><span class="sxs-lookup"><span data-stu-id="5b1b0-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
