---
title: De projectstatus begrijpen
description: Dit onderwerp bevat informatie over de status die is toegewezen aan projecten in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074436"
---
# <a name="understand-project-status"></a><span data-ttu-id="50e61-103">De projectstatus begrijpen</span><span class="sxs-lookup"><span data-stu-id="50e61-103">Understand project status</span></span>

<span data-ttu-id="50e61-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="50e61-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="50e61-105">De sectie **Status** op de pagina **Projectentiteit** geeft een samenvatting van het project op basis van kosten en inspanning.</span><span class="sxs-lookup"><span data-stu-id="50e61-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="50e61-106">Statusoverzichtsvelden</span><span class="sxs-lookup"><span data-stu-id="50e61-106">Status summary fields</span></span>

- <span data-ttu-id="50e61-107">Het veld **Algehele projectstatus** is een veld dat kan worden bewerkt en waarin de algehele status van het project wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="50e61-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="50e61-108">Voor dit veld worden kleurcodes, zoals groen, geel en rood, gebruikt om een toenemend risico aan te geven.</span><span class="sxs-lookup"><span data-stu-id="50e61-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="50e61-109">In het veld **Opmerkingen** kan de projectmanager specifieke opmerkingen over de status invoeren.</span><span class="sxs-lookup"><span data-stu-id="50e61-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="50e61-110">Het veld **Status bijgewerkt op** kan niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="50e61-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="50e61-111">De waarde in dit veld is een tijdstempel die aangeeft wanneer de status voor het laatst is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="50e61-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="50e61-112">De velden **Planningsprestaties** en **Kostenprestaties** worden ingesteld vanuit het raster voor het bijhouden van de gegevens.</span><span class="sxs-lookup"><span data-stu-id="50e61-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="50e61-113">Wanneer de planning en kostenvariantie voor het hoofdknooppunt in de weergave **Inspanningen bijhouden** positief zijn, kunt u deze velden instellen op **Voor**.</span><span class="sxs-lookup"><span data-stu-id="50e61-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="50e61-114">Wanneer de planning en kostenvariantie voor het hoofdknooppunt negatief zijn, worden deze velden ingesteld op **Achter**.</span><span class="sxs-lookup"><span data-stu-id="50e61-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
