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
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="63be1-103">Opmerkingen van de ontwikkelaar voor goedkeuringen</span><span class="sxs-lookup"><span data-stu-id="63be1-103">Developer notes for Approvals</span></span>

<span data-ttu-id="63be1-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="63be1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63be1-105">Dynamics 365 Project Operations bevat validatielogica die zorgt voor een correcte recordovergang tijdens de goedkeuringsfasen.</span><span class="sxs-lookup"><span data-stu-id="63be1-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="63be1-106">Correcte recordovergangen zorgen voor:</span><span class="sxs-lookup"><span data-stu-id="63be1-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="63be1-107">Alle ondersteunende rijen worden gemaakt in gerelateerde tabellen, zoals journalen en werkelijke waarden.</span><span class="sxs-lookup"><span data-stu-id="63be1-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="63be1-108">De goedkeurder wordt gemarkeerd als een **Projectgoedkeurder** in het project voordat u verder gaat.</span><span class="sxs-lookup"><span data-stu-id="63be1-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]