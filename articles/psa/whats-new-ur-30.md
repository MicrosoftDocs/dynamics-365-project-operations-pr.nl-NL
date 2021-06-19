---
title: Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 30, v3
description: In dit onderwerp vindt u een overzicht van de functies en oplossingen die beschikbaar zijn voor Project Service Automation updaterelease 30, v3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010420"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="bbd63-103">Wat is er nieuw of gewijzigd in Project Service Automation updaterelease 30, v3</span><span class="sxs-lookup"><span data-stu-id="bbd63-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bbd63-104">Met genoegen kondigen we de nieuwste update aan voor de toepassing Project Service Automation voor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bbd63-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bbd63-105">Deze release bevat enkele belangrijke verbeteringen op gebied van kwaliteit, prestaties en bruikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="bbd63-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bbd63-106">Deze versie is compatibel met Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bbd63-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bbd63-107">Als u deze release wilt bijwerken, gaat u online naar het Beheercentrum voor Dynamics 365 en naar de pagina Oplossingen om de update te installeren.</span><span class="sxs-lookup"><span data-stu-id="bbd63-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bbd63-108">Meer informatie vindt u in [Een voorkeursoplossing installeren, bijwerken of verwijderen](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="bbd63-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="bbd63-109">In dit onderwerp vindt u een overzicht van de functies en oplossingen die nieuw of gewijzigd zijn voor Project Service Automation v3, updaterelease 30.</span><span class="sxs-lookup"><span data-stu-id="bbd63-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="bbd63-110">Deze versie heeft een buildnummer van V3.10.51.61 en is algemeen beschikbaar via een zelfupdate in april 2021.</span><span class="sxs-lookup"><span data-stu-id="bbd63-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="bbd63-111">Updaterelease 30</span><span class="sxs-lookup"><span data-stu-id="bbd63-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bbd63-112">Opgeloste fouten</span><span class="sxs-lookup"><span data-stu-id="bbd63-112">Bug fixes</span></span>

<span data-ttu-id="bbd63-113">**Tijd en onkosten**</span><span class="sxs-lookup"><span data-stu-id="bbd63-113">**Time and Expense**</span></span>

<span data-ttu-id="bbd63-114">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="bbd63-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbd63-115">Er treedt een fout op wanneer u een tijdsvermelding maakt en opslaat op de pagina **Snelle invoer** als het veld **Rol** is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="bbd63-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="bbd63-116">Het filter Tijdsvermelding past de verkeerde filteroperator toe.</span><span class="sxs-lookup"><span data-stu-id="bbd63-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="bbd63-117">Gekopieerde urenstaten worden niet automatisch weergegeven wanneer u **Week kopiëren** selecteert in het besturingselement voor tijdsinvoer.</span><span class="sxs-lookup"><span data-stu-id="bbd63-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="bbd63-118">**Resourcebeheer**</span><span class="sxs-lookup"><span data-stu-id="bbd63-118">**Resource Management**</span></span>

<span data-ttu-id="bbd63-119">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="bbd63-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbd63-120">Wanneer u een boeking verlengt, is de boekingsstatus die aan de harde boeking is toegewezen onjuist.</span><span class="sxs-lookup"><span data-stu-id="bbd63-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="bbd63-121">Bij het verlengen van een boeking wordt de boekingsstatus gedefinieerd als **Toegezegd** in de metagegevens van de boekingsinstellingen gerespecteerd.</span><span class="sxs-lookup"><span data-stu-id="bbd63-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="bbd63-122">Als er geen geldige boekingsstatus is opgegeven, wordt het foutbericht niet correct gelokaliseerd.</span><span class="sxs-lookup"><span data-stu-id="bbd63-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="bbd63-123">**Projectbeheer**</span><span class="sxs-lookup"><span data-stu-id="bbd63-123">**Project Management**</span></span>

<span data-ttu-id="bbd63-124">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="bbd63-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbd63-125">Projecten kunnen niet in de ene valuta worden gemaakt en gerelateerde taken in een andere valuta bevatten.</span><span class="sxs-lookup"><span data-stu-id="bbd63-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="bbd63-126">**Verkoop**</span><span class="sxs-lookup"><span data-stu-id="bbd63-126">**Sales**</span></span>

<span data-ttu-id="bbd63-127">De volgende problemen zijn opgelost:</span><span class="sxs-lookup"><span data-stu-id="bbd63-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="bbd63-128">Wanneer een prijslijst wordt gekopieerd, worden prijzen niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="bbd63-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="bbd63-129">Het sluiten van een prijsopgave als gewonnen mislukt als de kostendetails een waarde voor de oorsprong hebben.</span><span class="sxs-lookup"><span data-stu-id="bbd63-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="bbd63-130">Voor de entiteit **Projecttaak** is de naam **Geschatte kosten** gewijzigd in **Geplande kosten (basis)** ​.</span><span class="sxs-lookup"><span data-stu-id="bbd63-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="bbd63-131">Een null-referentie-uitzondering wordt gegenereerd wanneer er facturen worden gemaakt of verwijderd.</span><span class="sxs-lookup"><span data-stu-id="bbd63-131">A null reference exception is generated when invoices are created or deleted.</span></span>
