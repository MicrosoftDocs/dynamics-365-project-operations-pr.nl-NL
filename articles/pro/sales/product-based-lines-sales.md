---
title: Productgebaseerde verkoopkansregels - lite
description: Dit onderwerp bevat informatie over productgebaseerde regelitems voor verkoopkansen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4f8da5258a1dd0aa4229654c0e1e222b8cf3a21a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272607"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="4d645-103">Productgebaseerde verkoopkansregels - lite</span><span class="sxs-lookup"><span data-stu-id="4d645-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="4d645-104">_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="4d645-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d645-105">Productgebaseerde verkoopkansregels zijn regelitems in de verkoopkans.</span><span class="sxs-lookup"><span data-stu-id="4d645-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="4d645-106">Deze afzonderlijke regelitems staan op de uiteindelijke factuur die aan de klant wordt verstrekt.</span><span class="sxs-lookup"><span data-stu-id="4d645-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="4d645-107">De factuur bevat geen andere aanvullende services.</span><span class="sxs-lookup"><span data-stu-id="4d645-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="4d645-108">De bijbehorende uitgaven en verbruik worden niet bijgehouden voor taken van gerelateerde projecten.</span><span class="sxs-lookup"><span data-stu-id="4d645-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="4d645-109">Productgebaseerde regels kunnen catalogusartikelen of inschrijfproducten zijn.</span><span class="sxs-lookup"><span data-stu-id="4d645-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="4d645-110">De meeste functionaliteit van productgebaseerde regels van een verkoopkansproduct volgt de functionaliteit die wordt geboden door de Dynamics 365 Sales-applicatie.</span><span class="sxs-lookup"><span data-stu-id="4d645-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="4d645-111">Zie [Producten toevoegen aan een verkoopkans](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity) voor meer informatie over productgebaseerde verkoopkansregels.</span><span class="sxs-lookup"><span data-stu-id="4d645-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="4d645-112">**Klantbudget** is een concept dat specifiek is voor projectgebaseerde verkoopkansregels.</span><span class="sxs-lookup"><span data-stu-id="4d645-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="4d645-113">Het veld **Klantbudget** houdt het bedrag bij dat de klant bereid is te betalen voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="4d645-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="4d645-114">Wanneer de omzetmethode uit het overzicht Verkoopkans **Door systeem berekend** is, worden de budgetwaarden van de klant over de verkoopkansregels samengevat om de geschatte omzet te berekenen.</span><span class="sxs-lookup"><span data-stu-id="4d645-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]