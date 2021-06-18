---
title: Tijdsvermeldingen maken
description: Dit onderwerp bevat informatie over het maken van tijdsvermeldingen.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999260"
---
# <a name="create-time-entries"></a><span data-ttu-id="6ad08-103">Tijdsvermeldingen maken</span><span class="sxs-lookup"><span data-stu-id="6ad08-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6ad08-104">In eerdere versies van Dynamics 365 Project Service Automation werden tijdsvermeldingen per week ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="6ad08-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="6ad08-105">In versie 3 van Project Service Automation worden tijdsvermeldingen per dag ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="6ad08-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="6ad08-106">Nadat een paar keer vermeldingen zijn gemaakt, kunt u ze bulksgewijs maken of kopiëren.</span><span class="sxs-lookup"><span data-stu-id="6ad08-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="6ad08-107">Een tijdsvermelding maken</span><span class="sxs-lookup"><span data-stu-id="6ad08-107">Create a time entry</span></span>

<span data-ttu-id="6ad08-108">Volg deze stappen om een tijdsvermelding te maken.</span><span class="sxs-lookup"><span data-stu-id="6ad08-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="6ad08-109">Selecteer **Nieuw** op de pagina **Tijdsvermeldingen**.</span><span class="sxs-lookup"><span data-stu-id="6ad08-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="6ad08-110">Voer in het dialoogvenster **Snelle invoer: tijdsvermelding** de duur van de tijdsvermelding in minuten, uren of dagen in.</span><span class="sxs-lookup"><span data-stu-id="6ad08-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="6ad08-111">De duur moet als volgt worden ingevoerd:  *x* minuten, *x* uur of *x* dagen.</span><span class="sxs-lookup"><span data-stu-id="6ad08-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="6ad08-112">De uren en dagen kunnen ook worden ingevoerd als decimale waarden, bijvoorbeeld *x,x* uur of *x,x* dagen.</span><span class="sxs-lookup"><span data-stu-id="6ad08-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="6ad08-113">Selecteer het type tijdsvermelding en het project waarvoor u de tijd invoert.</span><span class="sxs-lookup"><span data-stu-id="6ad08-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="6ad08-114">Zoek in **het veld** Projecttaak de taak voor deze tijdsvermelding.</span><span class="sxs-lookup"><span data-stu-id="6ad08-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ad08-115">Als u een tijdsvermelding maakt voor een taak die niet aan een gebruiker is toegewezen, selecteert u in het veld **Projecttaak** de knop **Zoeken**, en selecteert u vervolgens **Weergave wijzigen** en **Alle actieve projecttaken** om alle taken te vermelden.</span><span class="sxs-lookup"><span data-stu-id="6ad08-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="6ad08-116">Voer een omschrijving in als een omschrijving vereist is en selecteer vervolgens **Opslaan en sluiten**.</span><span class="sxs-lookup"><span data-stu-id="6ad08-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="6ad08-117">Nadat de tijdsvermelding is gemaakt en opgeslagen, kunt u deze bewerken in het tijdinvoerraster.</span><span class="sxs-lookup"><span data-stu-id="6ad08-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="6ad08-118">Het tijdinvoerraster ondersteunt twee indelingen:</span><span class="sxs-lookup"><span data-stu-id="6ad08-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="6ad08-119">U kunt tijdsvermeldingen invoeren in de notatie **uu:mm**.</span><span class="sxs-lookup"><span data-stu-id="6ad08-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="6ad08-120">Deze indeling wordt vervolgens geconverteerd naar uren en breuken.</span><span class="sxs-lookup"><span data-stu-id="6ad08-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="6ad08-121">U kunt uren en breuken rechtstreeks invoeren.</span><span class="sxs-lookup"><span data-stu-id="6ad08-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="6ad08-122">Houd er rekening mee dat de fracties van een uur geen minuten zijn.</span><span class="sxs-lookup"><span data-stu-id="6ad08-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="6ad08-123">1,5 uur staat voor 1 uur en 30 minuten.</span><span class="sxs-lookup"><span data-stu-id="6ad08-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="6ad08-124">Dezelfde regel geldt voor fracties van een dag.</span><span class="sxs-lookup"><span data-stu-id="6ad08-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="6ad08-125">Eén dag is 24 uur en 0,5 dagen vertegenwoordigt 12 uur.</span><span class="sxs-lookup"><span data-stu-id="6ad08-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="6ad08-126">Tijdsvermeldingen in bulk maken</span><span class="sxs-lookup"><span data-stu-id="6ad08-126">Bulk create time entries</span></span>

<span data-ttu-id="6ad08-127">Nadat er enkele tijdsvermeldingen zijn gemaakt, kunt u ze kopiëren en bulksgewijs extra tijdsvermeldingen maken.</span><span class="sxs-lookup"><span data-stu-id="6ad08-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="6ad08-128">Selecteer **Nieuw** op de pagina **Week kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="6ad08-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="6ad08-129">Definieer in de veldgroep **Van-periode** in de velden **Begindatum** en **Einddatum** het datumbereik waaruit u tijdsvermeldingen wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="6ad08-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="6ad08-130">Geef in de veldgroep **Tot-periode** in het veld **Begindatum** de datum op waarop u tijdsvermeldingen wilt maken.</span><span class="sxs-lookup"><span data-stu-id="6ad08-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="6ad08-131">Selecteer **Kopiëren** om een kopie te maken van de tijdsvermeldingen die overeenkomen met de dag van de week die is opgegeven in de veldgroep **Tot-periode**.</span><span class="sxs-lookup"><span data-stu-id="6ad08-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="6ad08-132">De tijdsvermelding van maandag van vorige week wordt bijvoorbeeld gekopieerd naar maandag voor de week die is aangegeven in de veldgroep **Tot-periode**.</span><span class="sxs-lookup"><span data-stu-id="6ad08-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="6ad08-133">Gegevens voor tijdsvermeldingen importeren</span><span class="sxs-lookup"><span data-stu-id="6ad08-133">Import data for time entries</span></span>

<span data-ttu-id="6ad08-134">U kunt gegevens importeren uit projectboekingen en -toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="6ad08-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="6ad08-135">Wanneer u gegevens importeert, kunt u het datumbereik opgeven van de boekingen die u wilt importeren en vervolgens expliciet de boekingen selecteren die moeten worden gemaakt als tijdsvermeldingen in **Concept**.</span><span class="sxs-lookup"><span data-stu-id="6ad08-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="6ad08-136">Functies voor groeperen op, sorteren, zoeken en filteren</span><span class="sxs-lookup"><span data-stu-id="6ad08-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="6ad08-137">U tijdsvermeldingen groeperen en filteren op de dimensies die in de kolommen zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="6ad08-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="6ad08-138">Selecteer in het veld **Groeperen op** de dimensie die u wilt gebruiken om tijdsvermeldingen te filteren.</span><span class="sxs-lookup"><span data-stu-id="6ad08-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="6ad08-139">U kunt de records met tijdsvermeldingen ook in oplopende of aflopende volgorde sorteren met behulp van de sorteerpijl op de kolomkoppen.</span><span class="sxs-lookup"><span data-stu-id="6ad08-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="6ad08-140">Bovendien kunt u items weergeven of verbergen door de knop **Filteren** in de kolomkoppen te selecteren en vervolgens in het **zoekvak** de tekst in te voeren die moet worden gebruikt om tijdsvermeldingen te zoeken op projectnaam, projecttaak, tijdsvermelding of resource.</span><span class="sxs-lookup"><span data-stu-id="6ad08-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]