---
title: Niet-voorradige materialen aanschaffen via een in behandeling zijnde leveranciersfactuur
description: In dit onderwerp wordt uitgelegd hoe u in behandeling zijnde leveranciersfacturen registreert.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880634"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="3df3d-103">Niet-voorradige materialen aanschaffen via een in behandeling zijnde leveranciersfactuur</span><span class="sxs-lookup"><span data-stu-id="3df3d-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="3df3d-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="3df3d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3df3d-105">Als een bedrijf niet-voorradig materiaal voor een project aanschaft, kunnen de kosten direct op het project worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="3df3d-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="3df3d-106">Stel bijvoorbeeld dat Contoso Robotics US een vernieuwingsproject voor apparatuur uitvoert en softwarelicenties nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="3df3d-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="3df3d-107">Deze licenties worden aangeschaft bij een externe leverancier.</span><span class="sxs-lookup"><span data-stu-id="3df3d-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="3df3d-108">Met behulp van Dynamics 365 Finance registreert de crediteurenadministrateur een in behandeling zijnde leveranciersfactuur en rekent de licentiekosten rechtstreeks toe aan het vernieuwingsproject voor apparatuur.</span><span class="sxs-lookup"><span data-stu-id="3df3d-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="3df3d-109">Voordat u de functionaliteit gebruikt die in dit onderwerp wordt beschreven, moet u de vereiste configuraties bekijken en toepassen.</span><span class="sxs-lookup"><span data-stu-id="3df3d-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="3df3d-110">Zie [Niet-voorradige materialen en in behandeling zijnde leveranciersfacturen inschakelen](configure-materials-nonstocked.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3df3d-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="3df3d-111">Een projectgerelateerde in behandeling zijnde leveranciersfactuur boeken</span><span class="sxs-lookup"><span data-stu-id="3df3d-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="3df3d-112">In behandeling zijnde leveranciersfacturen kunnen worden geregistreerd op de pagina **In behandeling zijnde leveranciersfacturen** (**Leveranciers** > **Facturen** > **In behandeling zijnde leveranciersfacturen**).</span><span class="sxs-lookup"><span data-stu-id="3df3d-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="3df3d-113">Voer de volgende stappen uit om een projectgerelateerde in behandeling zijnde leveranciersfactuur te boeken:</span><span class="sxs-lookup"><span data-stu-id="3df3d-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="3df3d-114">Ga naar **Leveranciers** > **Facturen** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="3df3d-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="3df3d-115">Selecteer in het veld **Factuurrekening** een leverancier en voer in het veld **Nummer** de identificatie van de leveranciersfactuur in.</span><span class="sxs-lookup"><span data-stu-id="3df3d-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="3df3d-116">Voeg een regel toe aan de leveranciersfactuur en selecteer in het veld **Artikelnummer** het niet-voorradige artikel dat bij de leverancier is gekocht.</span><span class="sxs-lookup"><span data-stu-id="3df3d-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="3df3d-117">Leveranciersfactuurregels die zijn gebaseerd op een inkoopcategorie kunnen niet voor het project worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="3df3d-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="3df3d-118">Voeg de aangeschafte hoeveelheid toe.</span><span class="sxs-lookup"><span data-stu-id="3df3d-118">Add the quantity purchased.</span></span> <span data-ttu-id="3df3d-119">Het systeem vult de eenheidsprijs in op basis van de configuratie van de prijs voor het artikel dat niet op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="3df3d-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="3df3d-120">Controleer het totale bedrag en andere vereiste details op de regel.</span><span class="sxs-lookup"><span data-stu-id="3df3d-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="3df3d-121">Selecteer in de regeldetails, op het tabblad **Project**, de id van het project waarvoor dit artikel wordt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="3df3d-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="3df3d-122">Selecteer optioneel het activiteitnummer en werk de projectcategorie en regeleigenschap bij.</span><span class="sxs-lookup"><span data-stu-id="3df3d-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="3df3d-123">Boek de in behandeling zijnde leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="3df3d-123">Post pending vendor invoice.</span></span> <span data-ttu-id="3df3d-124">Wanneer de factuur is geboekt, registreert het systeem:</span><span class="sxs-lookup"><span data-stu-id="3df3d-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="3df3d-125">Het saldo van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="3df3d-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="3df3d-126">Het bedrag aan omzetbelasting.</span><span class="sxs-lookup"><span data-stu-id="3df3d-126">The sales tax amount.</span></span>
    - <span data-ttu-id="3df3d-127">De kosten voor het project worden geboekt op het inkoopintegratieaccount.</span><span class="sxs-lookup"><span data-stu-id="3df3d-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="3df3d-128">De daadwerkelijke transactie van het project in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3df3d-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="3df3d-129">Deze transactie wordt verder verwerkt met behulp van het [Project Operations Integration-journaal](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="3df3d-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="3df3d-130">Als dit journaal wordt geboekt, wordt het bedrag van het inkoopintegratieaccount verplaatst naar het projectkostenaccount.</span><span class="sxs-lookup"><span data-stu-id="3df3d-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
