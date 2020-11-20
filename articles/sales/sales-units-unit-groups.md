---
title: Eenheden en eenhedengroepen
description: Dit onderwerp bevat informatie over hoe u eenheden en eenhedengroepen kunt maken in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131022"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="8bd2d-103">Eenheden en eenhedengroepen</span><span class="sxs-lookup"><span data-stu-id="8bd2d-103">Units and unit groups</span></span>

<span data-ttu-id="8bd2d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_</span><span class="sxs-lookup"><span data-stu-id="8bd2d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8bd2d-105">Eenheden zijn de hoeveelheden of de maateenheden waarin u uw producten of diensten verkoopt.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="8bd2d-106">Als u bijvoorbeeld benodigdheden voor tuinieren verkoopt, kunt u zaden in eenheden van pakketten, dozen en pallets verkopen.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="8bd2d-107">Een eenhedengroep is een verzameling van deze verschillende eenheden.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="8bd2d-108">Om de stappen in deze onderwerp te kunnen voltooien, moet u ervoor zorgen dat aan u de rol Systeembeheerder of Sales Professional Manager is toegewezen of dat u gelijkwaardige machtigingen hebt.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="8bd2d-109">Een eenhedengroep maken</span><span class="sxs-lookup"><span data-stu-id="8bd2d-109">Create a unit group</span></span>

1. <span data-ttu-id="8bd2d-110">Selecteer **Eenheden** in het siteoverzicht.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="8bd2d-111">Selecteer **Nieuw** en voer in het dialoogvenster **Eenhedengroep maken** de naam voor de eenhedengroep in.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="8bd2d-112">Voer in het veld **Primaire eenheid** de laagste algemeen gebruikte maateenheid in waarin het product wordt verkocht.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="8bd2d-113">U kunt bijvoorbeeld 'stuk' of 'ons' invoeren.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="8bd2d-114">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="8bd2d-115">Eenheden aan een eenhedengroep toevoegen</span><span class="sxs-lookup"><span data-stu-id="8bd2d-115">Add units to a unit group</span></span>

1. <span data-ttu-id="8bd2d-116">Open een eenhedengroep en selecteer op het tabblad **Gerelateerd** de optie **Eenheden**.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="8bd2d-117">U ziet dat de primaire eenheid al is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="8bd2d-118">Selecteer **Nieuwe eenheid toevoegen** en voer op de pagina **Snelle invoer: Eenheid** in het veld **Naam** de naam van de eenheid in.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="8bd2d-119">Voer in het veld **Hoeveelheid** het aantal van de eenheid in.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="8bd2d-120">Als een doos bijvoorbeeld twee stuks bevat, voert u '2' in.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="8bd2d-121">Selecteer in de **Basiseenheid** een basiseenheid om de laagste maateenheid voor de eenheid in te stellen.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="8bd2d-122">U kunt bijvoorbeeld 'Stuk' selecteren.</span><span class="sxs-lookup"><span data-stu-id="8bd2d-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="8bd2d-123">Selecteer **Opslaan**:</span><span class="sxs-lookup"><span data-stu-id="8bd2d-123">Select **Save**:</span></span>
