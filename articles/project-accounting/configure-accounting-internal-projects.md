---
title: Boekhouding configureren voor interne projecten
description: Dit onderwerp bevat informatie over het instellen van boekhoudkundige principes voor interne projecten in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074498"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="57ed5-103">Boekhouding configureren voor interne projecten</span><span class="sxs-lookup"><span data-stu-id="57ed5-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="57ed5-104">_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_</span><span class="sxs-lookup"><span data-stu-id="57ed5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="57ed5-105">Met interne projecten kunnen bedrijven kosten bijhouden die zijn gerelateerd aan activiteiten die niet aan een klant zijn gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="57ed5-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="57ed5-106">Voorbeelden van interne projecten zijn:</span><span class="sxs-lookup"><span data-stu-id="57ed5-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="57ed5-107">Een product ontwikkelen, zoals een mobiele app, en de kosten bijhouden die aan de ontwikkeling zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="57ed5-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="57ed5-108">De tijd en onkosten vóór verkoop beheren.</span><span class="sxs-lookup"><span data-stu-id="57ed5-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="57ed5-109">Dit interne project vóór verkoop kan later naar een factureerbaar project worden omgezet als de offerte wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="57ed5-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="57ed5-110">Elk project dat niet aan een contract is gekoppeld, wordt in Dynamics 365 Project Operations behandeld als intern.</span><span class="sxs-lookup"><span data-stu-id="57ed5-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="57ed5-111">Projectkosten en opbrengstprofielen worden niet gebruikt om boekhoudregels voor het project te bepalen.</span><span class="sxs-lookup"><span data-stu-id="57ed5-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="57ed5-112">Interne projectkosten worden altijd geboekt met behulp van winst- en verliesprincipes.</span><span class="sxs-lookup"><span data-stu-id="57ed5-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="57ed5-113">Grootboekrekeningen voor boekingen worden gedefinieerd op de pagina **Boeking in grootboek instellen**.</span><span class="sxs-lookup"><span data-stu-id="57ed5-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="57ed5-114">Tijdtransacties worden geboekt door de rekening **Kosten** te debiteren en de rekening **Salaristoewijzing** te crediteren.</span><span class="sxs-lookup"><span data-stu-id="57ed5-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="57ed5-115">Onkostentransacties worden geboekt door de rekening **Kosten** te debiteren en de **Tegenrekening voor onkosten** te crediteren.</span><span class="sxs-lookup"><span data-stu-id="57ed5-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="57ed5-116">Nadat transacties naar het project zijn geboekt, worden als het project aan een projectcontract is gekoppeld alle samengevoegde transacties omgekeerd en worden nieuwe factureerbare transacties gemaakt.</span><span class="sxs-lookup"><span data-stu-id="57ed5-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="57ed5-117">De factureerbare transacties volgen de boekhoudregels die zijn gedefinieerd met betrekking tot projectkosten en het opbrengstprofiel.</span><span class="sxs-lookup"><span data-stu-id="57ed5-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


