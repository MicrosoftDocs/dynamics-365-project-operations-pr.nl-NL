---
title: Implementeer aangepaste velden voor de mobiele Microsoft Dynamics 365 Project Timesheet-app op iOS en Android
description: Dit onderwerp biedt algemene patronen voor het gebruik van extensies om aangepaste velden te implementeren.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003020"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="cd469-103">Implementeer aangepaste velden voor de mobiele Microsoft Dynamics 365 Project Timesheet-app op iOS en Android</span><span class="sxs-lookup"><span data-stu-id="cd469-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd469-104">Dit onderwerp biedt algemene patronen voor het gebruik van extensies om aangepaste velden te implementeren.</span><span class="sxs-lookup"><span data-stu-id="cd469-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="cd469-105">De volgende onderwerpen komen aan bod:</span><span class="sxs-lookup"><span data-stu-id="cd469-105">The following topics are covered:</span></span>

- <span data-ttu-id="cd469-106">De verschillende gegevenstypen die het aangepaste veldframework ondersteunt</span><span class="sxs-lookup"><span data-stu-id="cd469-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="cd469-107">Alleen-lezen of bewerkbare velden in urenstaatvermeldingen weergeven en door de gebruiker verstrekte waarden weer in de database opslaan</span><span class="sxs-lookup"><span data-stu-id="cd469-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="cd469-108">Alleen-lezen velden weergeven in de header van de urenstaat</span><span class="sxs-lookup"><span data-stu-id="cd469-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="cd469-109">Andere aangepaste bedrijfslogica integreren om standaardwaarden in velden in te voeren en aanvullende validatie uit te voeren</span><span class="sxs-lookup"><span data-stu-id="cd469-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="cd469-110">Publiek</span><span class="sxs-lookup"><span data-stu-id="cd469-110">Audience</span></span>

<span data-ttu-id="cd469-111">Dit onderwerp is bedoeld voor ontwikkelaars die hun aangepaste velden integreren in de mobiele Microsoft Dynamics 365 Project Timesheet-toepassing die beschikbaar is voor Apple iOS en Google Android.</span><span class="sxs-lookup"><span data-stu-id="cd469-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="cd469-112">De aanname is dat lezers bekend zijn met X++-ontwikkeling en de functionaliteit van projecturenstaten.</span><span class="sxs-lookup"><span data-stu-id="cd469-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="cd469-113">Gegevenscontract - X++-klasse TSTimesheetCustomField</span><span class="sxs-lookup"><span data-stu-id="cd469-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="cd469-114">De klasse **TSTimesheetCustomField** is de X++-gegevenscontractklasse die informatie vertegenwoordigt over een aangepast veld voor de functionaliteit voor urenstaten.</span><span class="sxs-lookup"><span data-stu-id="cd469-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="cd469-115">Lijsten van de aangepaste veldobjecten worden doorgegeven aan zowel het TSTimesheetDetails-gegevenscontract als het TSTimesheetEntry-gegevenscontract om aangepaste velden in de mobiele app weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cd469-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="cd469-116">**TSTimesheetDetails** - Het contract voor de header van de urenstaat.</span><span class="sxs-lookup"><span data-stu-id="cd469-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="cd469-117">**TSTimesheetEntry** - Het transactiecontract voor de urenstaat.</span><span class="sxs-lookup"><span data-stu-id="cd469-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="cd469-118">Groepen van deze objecten met dezelfde projectinformatie en waarden voor **timesheetLineRecId** vormen een regel.</span><span class="sxs-lookup"><span data-stu-id="cd469-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="cd469-119">fieldBaseType (typen)</span><span class="sxs-lookup"><span data-stu-id="cd469-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="cd469-120">De eigenschap **FieldBaseType** voor het object **TsTimesheetCustom** bepaalt het type veld dat in de app wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd469-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="cd469-121">De volgende waarden voor **Types** worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="cd469-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="cd469-122">Waarde voor Types</span><span class="sxs-lookup"><span data-stu-id="cd469-122">Types value</span></span> | <span data-ttu-id="cd469-123">Type</span><span class="sxs-lookup"><span data-stu-id="cd469-123">Type</span></span>              | <span data-ttu-id="cd469-124">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cd469-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="cd469-125">0</span><span class="sxs-lookup"><span data-stu-id="cd469-125">0</span></span>           | <span data-ttu-id="cd469-126">Tekenreeks (en Enum)</span><span class="sxs-lookup"><span data-stu-id="cd469-126">String (and Enum)</span></span> | <span data-ttu-id="cd469-127">Het veld wordt weergegeven als een tekstveld.</span><span class="sxs-lookup"><span data-stu-id="cd469-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="cd469-128">0</span><span class="sxs-lookup"><span data-stu-id="cd469-128">1</span></span>           | <span data-ttu-id="cd469-129">Integer</span><span class="sxs-lookup"><span data-stu-id="cd469-129">Integer</span></span>           | <span data-ttu-id="cd469-130">De waarde wordt weergegeven als een getal zonder decimalen.</span><span class="sxs-lookup"><span data-stu-id="cd469-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="cd469-131">2</span><span class="sxs-lookup"><span data-stu-id="cd469-131">2</span></span>           | <span data-ttu-id="cd469-132">Real</span><span class="sxs-lookup"><span data-stu-id="cd469-132">Real</span></span>              | <span data-ttu-id="cd469-133">De waarde wordt weergegeven als een getal met decimalen.</span><span class="sxs-lookup"><span data-stu-id="cd469-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="cd469-134">Als u de reële waarde als valuta in de app wilt weergeven, gebruikt u de eigenschap **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="cd469-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="cd469-135">U kunt de eigenschap **numberOfDecimals** gebruiken om het aantal getoonde decimalen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="cd469-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="cd469-136">5</span><span class="sxs-lookup"><span data-stu-id="cd469-136">3</span></span>           | <span data-ttu-id="cd469-137">Date</span><span class="sxs-lookup"><span data-stu-id="cd469-137">Date</span></span>              | <span data-ttu-id="cd469-138">Datumnotaties worden bepaald door de instelling **Datum-, tijden- en getalnotatie** van de gebruiker die is gespecificeerd onder **Voorkeur voor taal en land/regio** in **Gebruikersopties**.</span><span class="sxs-lookup"><span data-stu-id="cd469-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="cd469-139">4</span><span class="sxs-lookup"><span data-stu-id="cd469-139">4</span></span>           | <span data-ttu-id="cd469-140">Booleaanse waarde</span><span class="sxs-lookup"><span data-stu-id="cd469-140">Boolean</span></span>           | |
| <span data-ttu-id="cd469-141">15</span><span class="sxs-lookup"><span data-stu-id="cd469-141">15</span></span>          | <span data-ttu-id="cd469-142">GUID</span><span class="sxs-lookup"><span data-stu-id="cd469-142">GUID</span></span>              | |
| <span data-ttu-id="cd469-143">16</span><span class="sxs-lookup"><span data-stu-id="cd469-143">16</span></span>          | <span data-ttu-id="cd469-144">Int64</span><span class="sxs-lookup"><span data-stu-id="cd469-144">Int64</span></span>             | |

- <span data-ttu-id="cd469-145">Als de eigenschap **stringOptions** niet is opgegeven voor het object **TSTimesheetCustomField**, wordt een vrij tekstveld aan de gebruiker verstrekt.</span><span class="sxs-lookup"><span data-stu-id="cd469-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="cd469-146">De eigenschap **stringLength** kan worden gebruikt om de maximale tekenreekslengte in te stellen die gebruikers kunnen invoeren.</span><span class="sxs-lookup"><span data-stu-id="cd469-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="cd469-147">Als de eigenschap **stringOptions** wordt verstrekt voor het object **TSTimesheetCustomField**, zijn die lijstelementen de enige waarden die gebruikers kunnen selecteren met behulp van optieknoppen (keuzerondjes).</span><span class="sxs-lookup"><span data-stu-id="cd469-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="cd469-148">In dit geval kan het tekenreeksveld fungeren als een opsommingswaarde voor gebruikersinvoer.</span><span class="sxs-lookup"><span data-stu-id="cd469-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="cd469-149">Als u de waarde in de database wilt opslaan als een enum, wijst u de tekenreekswaarde handmatig opnieuw toe aan de enum-waarde voordat u opslaat in de database met behulp van een opdrachtenreeks (zie de sectie "Opdrachtenreeks gebruiken voor de klasse TSTimesheetEntryService om een urenstaatvermelding uit de app opnieuw op te slaan in de database" verderop in dit onderwerp voor een voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="cd469-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="cd469-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="cd469-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="cd469-151">U kunt deze eigenschap gebruiken om reële waarden als valuta op te maken.</span><span class="sxs-lookup"><span data-stu-id="cd469-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="cd469-152">Deze benadering is alleen van toepassing als de waarde **fieldBaseType** **Real** is.</span><span class="sxs-lookup"><span data-stu-id="cd469-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="cd469-153">**TSCustomFieldExtendedType:None** – Er wordt geen opmaak toegepast.</span><span class="sxs-lookup"><span data-stu-id="cd469-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="cd469-154">**TSCustomFieldExtendedType::Currency** - Formatteer de waarde als valuta.</span><span class="sxs-lookup"><span data-stu-id="cd469-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="cd469-155">Als valutanotatie actief is, kan het veld **stringValue** worden gebruikt om de valutacode door te geven die in de app moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd469-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="cd469-156">De waarde is een alleen-lezen waarde.</span><span class="sxs-lookup"><span data-stu-id="cd469-156">The value is a read-only value.</span></span>

    <span data-ttu-id="cd469-157">Het veld **realValue** bevat het geldbedrag dat in de database moet worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="cd469-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="cd469-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="cd469-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="cd469-159">U kunt deze eigenschap gebruiken om aan te geven waar het aangepaste veld in de app moet verschijnen.</span><span class="sxs-lookup"><span data-stu-id="cd469-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="cd469-160">**TSCustomFieldSection::Header** - Het veld verschijnt in de sectie **Meer details weergeven** in de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="cd469-161">Deze velden zijn altijd alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="cd469-161">These fields are always read-only.</span></span>
- <span data-ttu-id="cd469-162">**TSCustomFieldSection::Line** - Het veld wordt weergegeven na alle kant-en-klare regelvelden in urenstaatvermeldingen.</span><span class="sxs-lookup"><span data-stu-id="cd469-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="cd469-163">Deze velden kunnen bewerkbaar of alleen-lezen zijn.</span><span class="sxs-lookup"><span data-stu-id="cd469-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="cd469-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="cd469-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="cd469-165">Deze eigenschap identificeert het veld wanneer waarden die de app levert opnieuw worden opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="cd469-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="cd469-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="cd469-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="cd469-167">Deze eigenschap identificeert het veld wanneer waarden die de app levert opnieuw worden opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="cd469-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="cd469-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="cd469-168">isEditable (NoYes)</span></span>

<span data-ttu-id="cd469-169">Stel deze eigenschap in op **Yes** om aan te geven dat het veld in de sectie voor het invoeren van urenstaten door gebruikers moet kunnen worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="cd469-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="cd469-170">Stel de eigenschap in op **No** om het veld alleen-lezen te maken.</span><span class="sxs-lookup"><span data-stu-id="cd469-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="cd469-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="cd469-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="cd469-172">Stel deze eigenschap in op **Yes** om aan te geven dat het veld in de sectie voor het invoeren van urenstaten verplicht moet zijn.</span><span class="sxs-lookup"><span data-stu-id="cd469-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="cd469-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="cd469-173">label (str)</span></span>

<span data-ttu-id="cd469-174">Deze eigenschap geeft het label aan dat naast het veld in de app wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd469-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="cd469-175">stringOptions (lijst met tekenreeksen)</span><span class="sxs-lookup"><span data-stu-id="cd469-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="cd469-176">Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **String**.</span><span class="sxs-lookup"><span data-stu-id="cd469-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="cd469-177">Als **stringOptions** is ingesteld, worden de tekenreekswaarden die beschikbaar zijn voor selectie via optieknoppen (keuzerondjes) gespecificeerd door de tekenreeksen in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cd469-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="cd469-178">Als er geen tekenreeksen zijn opgegeven, is vrije tekstinvoer in het tekenreeksveld toegestaan (zie de sectie "Opdrachtenreeks gebruiken voor de klasse TSTimesheetEntryService om een urenstaatvermelding uit de app opnieuw op te slaan in de database" verderop in dit onderwerp voor een voorbeeld).</span><span class="sxs-lookup"><span data-stu-id="cd469-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="cd469-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="cd469-179">stringLength (int)</span></span>

<span data-ttu-id="cd469-180">Deze eigenschap specificeert de maximale lengte voor een tekenreeksveld.</span><span class="sxs-lookup"><span data-stu-id="cd469-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="cd469-181">Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **String**.</span><span class="sxs-lookup"><span data-stu-id="cd469-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="cd469-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="cd469-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="cd469-183">Deze eigenschap specificeert het aantal decimalen dat wordt weergegeven voor een reëel veld.</span><span class="sxs-lookup"><span data-stu-id="cd469-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="cd469-184">Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Real**.</span><span class="sxs-lookup"><span data-stu-id="cd469-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="cd469-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="cd469-185">orderSequence (int)</span></span>

<span data-ttu-id="cd469-186">Deze eigenschap bepaalt de volgorde waarin de aangepaste velden in de app worden weergegeven wanneer er meer dan één aangepast veld is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="cd469-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="cd469-187">Velden met lagere getallen worden als eerste weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd469-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="cd469-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="cd469-188">booleanValue (boolean)</span></span>

<span data-ttu-id="cd469-189">Voor velden van het type **Boolean**, geeft deze eigenschap de booleaanse waarde van het veld door tussen de server en de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="cd469-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="cd469-190">guidValue (guid)</span></span>

<span data-ttu-id="cd469-191">Voor velden van het type **GUID**, geeft deze eigenschap de GUID-waarde (Globally Unique Identifier) van het veld door tussen de server en de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="cd469-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="cd469-192">int64Value (int64)</span></span>

<span data-ttu-id="cd469-193">Voor velden van het type **Int64**, geeft deze eigenschap de int64-waarde van het veld door tussen de server en de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="cd469-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="cd469-194">intValue (int)</span></span>

<span data-ttu-id="cd469-195">Voor velden van het type **Int**, geeft deze eigenschap de int-waarde van het veld door tussen de server en de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="cd469-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="cd469-196">realValue (real)</span></span>

<span data-ttu-id="cd469-197">Voor velden van het type **Real**, geeft deze eigenschap de reële waarde van het veld door tussen de server en de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="cd469-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="cd469-198">stringValue (str)</span></span>

<span data-ttu-id="cd469-199">Voor velden van het type **String**, geeft deze eigenschap de tekenreekswaarde van het veld door tussen de server en de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="cd469-200">Het wordt ook gebruikt voor velden van het type **Real** die zijn opgemaakt als valuta.</span><span class="sxs-lookup"><span data-stu-id="cd469-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="cd469-201">Voor die velden wordt de eigenschap gebruikt om de valutacode door te geven aan de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="cd469-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="cd469-202">dateValue (date)</span></span>

<span data-ttu-id="cd469-203">Voor velden van het type **Date**, geeft deze eigenschap de datumwaarde van het veld door tussen de server en de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="cd469-204">Een aangepast veld weergeven en opslaan in de sectie voor het invoeren van de urenstaat</span><span class="sxs-lookup"><span data-stu-id="cd469-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="cd469-205">Hieronder ziet u een schermopname van het maken van een urenstaatvermelding in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="cd469-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="cd469-206">Het toont de kant-en-klare velden en een aangepast veld in de secite "Tijdinvoer" genaamd "Testtekenreeks" waarvoor al een enum-waarde "Tweede optie" is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="cd469-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Aangepast veld Testtekenreeks in de app](media/timesheet-entry.jpg)



<span data-ttu-id="cd469-208">Hieronder ziet u een schermopname van de mobiele app van de gebruiker die een van de enum-opties selecteert die beschikbaar zijn voor het aangepaste veld "Testtekenreeks".</span><span class="sxs-lookup"><span data-stu-id="cd469-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="cd469-209">De twee opties zijn "Eerste optie" en "Tweede optie" weergegeven als keuzerondjes.</span><span class="sxs-lookup"><span data-stu-id="cd469-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="cd469-210">De tweede optie is momenteel geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="cd469-210">The second option is currently selected.</span></span>

![Optieknoppen (keuzerondjes) voor het aangepaste veld Testtekenreeks](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="cd469-212">De tabel TSTimesheetLine uitbreiden zodat deze een aangepast veld heeft</span><span class="sxs-lookup"><span data-stu-id="cd469-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="cd469-213">In typische scenario's is het waarschijnlijk zo dat de gegevens voor een aangepast veld in de sectie voor urenstaatinvoer worden opgeslagen in de tabel TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="cd469-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="cd469-214">Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTrans-record die wordt verstrekt of als deze geen specifieke recordcontext hebben (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).</span><span class="sxs-lookup"><span data-stu-id="cd469-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="cd469-215">Merk op dat aangepaste velden geen ondersteunende databaserecords hoeven te hebben.</span><span class="sxs-lookup"><span data-stu-id="cd469-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="cd469-216">Ze kunnen dynamisch worden gegenereerd op basis van X++-logica.</span><span class="sxs-lookup"><span data-stu-id="cd469-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="cd469-217">Deze benadering kan handig zijn in alleen-lezen scenario's (zie de sectie "Opdrachtenreeks gebruiken voor de klasse TSTimesheetDetails, methode buildCustomFieldListForHeader, om urenstaatdetails in te vullen" voor een voorbeeld van dynamisch gegenereerde aangepaste veldwaarden.)</span><span class="sxs-lookup"><span data-stu-id="cd469-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="cd469-218">Hieronder wordt een schermopname weergegeven van de toepassingsobjectstructuur in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cd469-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="cd469-219">Het toont een uitbreiding van de tabel TSTimesheetLine met het veld TestLineString toegevoegd als een aangepast veld.</span><span class="sxs-lookup"><span data-stu-id="cd469-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Regeltekenreeks](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="cd469-221">Opdrachtenreeks gebruiken voor de methode buildCustomFieldList van de klasse TSTimesheetSettings om een veld weer te geven in de sectie voor urenstaatinvoer</span><span class="sxs-lookup"><span data-stu-id="cd469-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="cd469-222">Deze code regelt de weergave-instellingen voor het veld in de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="cd469-223">Het bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld verschijnt.</span><span class="sxs-lookup"><span data-stu-id="cd469-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="cd469-224">Het volgende voorbeeld toont een tekenreeksveld voor tijdinvoer.</span><span class="sxs-lookup"><span data-stu-id="cd469-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="cd469-225">Dit veld heeft twee opties, **Eerste optie** en **Tweede optie**, die beschikbaar zijn via optieknoppen (keuzerondjes).</span><span class="sxs-lookup"><span data-stu-id="cd469-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="cd469-226">Het veld in de app is gekoppeld aan het veld **TestLineString** dat wordt toegevoegd aan de tabel TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="cd469-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="cd469-227">Let op het gebruik van de methode **TSTimesheetCustomField::newFromMetatdata()** om de initialisatie van de aangepaste veldeigenschappen te vereenvoudigen: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** en **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="cd469-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="cd469-228">U kunt deze parameters ook handmatig instellen, als u dat wilt.</span><span class="sxs-lookup"><span data-stu-id="cd469-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="cd469-229">Opdrachtenreeks gebruiken voor de methode buildCustomFieldListForEntry van de klasse TSTimesheetEntry om waarden in te voeren in een urenstaatvermelding</span><span class="sxs-lookup"><span data-stu-id="cd469-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="cd469-230">De methode **buildCustomFieldListForEntry** wordt gebruikt om waarden in te voeren op de opgeslagen urenstaatregels in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="cd469-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="cd469-231">Er is een TSTimesheetTrans-record nodig als parameter.</span><span class="sxs-lookup"><span data-stu-id="cd469-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="cd469-232">Velden uit dat record kunnen worden gebruikt om de aangepaste veldwaarde in de app in te vullen.</span><span class="sxs-lookup"><span data-stu-id="cd469-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="cd469-233">Opdrachtenreeks gebruiken voor de klasse TSTimesheetEntryService om een urenstaatvermelding van de app opnieuw op te slaan in de database</span><span class="sxs-lookup"><span data-stu-id="cd469-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="cd469-234">Als u een aangepast veld bij normaal gebruik weer wilt opslaan in de database, moet u meerdere methoden uitbreiden:</span><span class="sxs-lookup"><span data-stu-id="cd469-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="cd469-235">De methode **timesheetLineNeedsUpdating** wordt gebruikt om te bepalen of de regelrecord is gewijzigd door de gebruiker in de app en moet worden opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="cd469-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="cd469-236">Als prestaties geen probleem zijn, kan deze methode worden vereenvoudigd zodat deze altijd **true** retourneert.</span><span class="sxs-lookup"><span data-stu-id="cd469-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="cd469-237">De methoden **populateTimesheetLineFromEntryDuringCreate** en **populateTimesheetLineFromEntryDuringUpdate** kunnen worden uitgebreid zodat ze waarden invoeren in de databaserecord TSTimesheetLine vanuit de TSTimesheetEntry-gegevenscontractrecord die wordt verstrekt.</span><span class="sxs-lookup"><span data-stu-id="cd469-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="cd469-238">In het onderstaande voorbeeld ziet u hoe de toewijzing tussen het databaseveld en het invoerveld handmatig wordt uitgevoerd via X++-code.</span><span class="sxs-lookup"><span data-stu-id="cd469-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="cd469-239">De methode **populateTimesheetWeekFromEntry** kan ook worden uitgebreid als het aangepaste veld dat is toegewezen aan het object **TSTimesheetEntry** moet terugschrijven naar de databasetabel TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="cd469-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="cd469-240">In het volgende voorbeeld wordt de waarde **firstOption** of **secondOption** die de gebruiker in de database selecteert opgeslagen als een onbewerkte tekenreekswaarde.</span><span class="sxs-lookup"><span data-stu-id="cd469-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="cd469-241">Als het databaseveld een veld is van het type **Enum**, kunnen die waarden handmatig worden toegewezen aan een enum-waarde en vervolgens worden opgeslagen in een enum-veld in de databasetabel.</span><span class="sxs-lookup"><span data-stu-id="cd469-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="cd469-242">Een aangepast veld weergeven in de headersectie van de urenstaat</span><span class="sxs-lookup"><span data-stu-id="cd469-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="cd469-243">Hieronder ziet u een schermopname van de weergave van een urenstaat in de mobiele app door een gebruiker.</span><span class="sxs-lookup"><span data-stu-id="cd469-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="cd469-244">De knop "Meer informatie" is geselecteerd in de rechterbovenhoek om de optie "Meer details weergeven" te tonen.</span><span class="sxs-lookup"><span data-stu-id="cd469-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Opdracht Meer details weergeven](media/show-more.png)

<span data-ttu-id="cd469-246">Hieronder ziet u een schermopname van de sectie "Meer" van een urenstaat in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="cd469-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="cd469-247">Een aangepast veld met de naam "Benuttingspercentage van deze urenstaat (berekend aangepast veld)" is toegevoegd aan de headersectie van de urenstaat.</span><span class="sxs-lookup"><span data-stu-id="cd469-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="cd469-248">Een alleen-lezen waarde van "0,667" is ingesteld voor het aangepaste veld.</span><span class="sxs-lookup"><span data-stu-id="cd469-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sectie Meer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="cd469-250">De tabel TSTimesheetTable uitbreiden zodat deze een aangepast veld heeft</span><span class="sxs-lookup"><span data-stu-id="cd469-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="cd469-251">In typische scenario's is het waarschijnlijk zo dat de gegevens voor een aangepast veld in de headersectie worden opgehaald uit de tabel TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="cd469-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="cd469-252">Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTable-record die wordt verstrekt of als deze geen specifieke recordcontext hebben (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).</span><span class="sxs-lookup"><span data-stu-id="cd469-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="cd469-253">Merk op dat aangepaste velden geen ondersteunende databaserecords hoeven te hebben.</span><span class="sxs-lookup"><span data-stu-id="cd469-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="cd469-254">Ze kunnen dynamisch worden gegenereerd op basis van X++-logica.</span><span class="sxs-lookup"><span data-stu-id="cd469-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="cd469-255">Het volgende voorbeeld toont deze benadering.</span><span class="sxs-lookup"><span data-stu-id="cd469-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="cd469-256">Velden in de headersectie zijn altijd alleen-lezen in de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="cd469-257">Opdrachtenreeks gebruiken voor de methode buildCustomFieldList van de klasse TSTimesheetSettings om een veld weer te geven in de headersectie</span><span class="sxs-lookup"><span data-stu-id="cd469-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="cd469-258">Deze code regelt de weergave-instellingen voor het veld in de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="cd469-259">Het bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld verschijnt.</span><span class="sxs-lookup"><span data-stu-id="cd469-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="cd469-260">Het volgende voorbeeld toont een berekende waarde in de headersectie in de app.</span><span class="sxs-lookup"><span data-stu-id="cd469-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="cd469-261">Opdrachtenreeks gebruiken voor de methode buildCustomFieldListForHeader van de klasse TSTimesheetDetails om urenstaatdetails in te vullen</span><span class="sxs-lookup"><span data-stu-id="cd469-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="cd469-262">De methode **buildCustomFieldListForHeader** wordt gebruikt om details van de urenstaatheader in te vullen in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="cd469-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="cd469-263">Er is een TSTimesheetTable-record nodig als parameter.</span><span class="sxs-lookup"><span data-stu-id="cd469-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="cd469-264">Velden uit dat record kunnen worden gebruikt om de aangepaste veldwaarde in de app in te vullen.</span><span class="sxs-lookup"><span data-stu-id="cd469-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="cd469-265">In het volgende voorbeeld worden geen waarden uit de database gelezen.</span><span class="sxs-lookup"><span data-stu-id="cd469-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="cd469-266">In plaats daarvan gebruikt X++ logica om een berekende waarde te genereren die vervolgens in de app wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="cd469-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="cd469-267">Andere mogelijkheden voor configureerbaarheid/uitbreidbaarheid</span><span class="sxs-lookup"><span data-stu-id="cd469-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="cd469-268">Extra validatie toevoegen voor de app</span><span class="sxs-lookup"><span data-stu-id="cd469-268">Adding additional validation for the app</span></span>

<span data-ttu-id="cd469-269">De bestaande logica voor urenstaatfunctionaliteit op databaseniveau zal nog steeds werken zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="cd469-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="cd469-270">Als u de voltooiing van bewerkingen voor opslaan of verzenden wilt onderbreken en een specifiek foutbericht wilt weergeven, kunt u **throw error("bericht aan gebruiker")** toevoegen naar de code via een opdrachtextensie.</span><span class="sxs-lookup"><span data-stu-id="cd469-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="cd469-271">Hier zijn drie voorbeelden van handige uitbreidbare methoden:</span><span class="sxs-lookup"><span data-stu-id="cd469-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="cd469-272">Als **validateWrite** voor de tabel TSTimesheetLine **false** retourneert tijdens het opslaan van een urenstaatregel, wordt een foutmelding weergegeven in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="cd469-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="cd469-273">Als **validateSubmit** voor de tabel TSTimesheetTable **false** retourneert tijdens het indienen van de urenstaat in de app, wordt een foutmelding weergegeven aan de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="cd469-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="cd469-274">Logica die velden invult (bijvoorbeeld **Regeleigenschap**) tijdens de methode **insert** voor de tabel TSTimesheetLine wordt nog steeds uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="cd469-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="cd469-275">Kant-en-klare velden verbergen en markeren als alleen-lezen via configuratie</span><span class="sxs-lookup"><span data-stu-id="cd469-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="cd469-276">Vanuit de projectparameters kunt u kant-en-klare velden alleen-lezen maken of verbergen in de mobiele app.</span><span class="sxs-lookup"><span data-stu-id="cd469-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="cd469-277">Stel de opties in de sectie **Mobiele urenstaten** in op het tabblad **Urenstaat** van de pagina **Parameters voor Projectmanagement en financiële administratie**.</span><span class="sxs-lookup"><span data-stu-id="cd469-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projectparameters](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="cd469-279">De activiteiten wijzigen die beschikbaar zijn voor selectie via extensies</span><span class="sxs-lookup"><span data-stu-id="cd469-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="cd469-280">De activiteiten die beschikbaar zijn voor selectie voor een project worden ingevuld via de methoden **getActivitiesForproject()** en **getActivityQuery()** in de klasse **TsTimesheetprojectService**.</span><span class="sxs-lookup"><span data-stu-id="cd469-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="cd469-281">U kunt de opdrachtenreeks gebruiken om dit gedrag aan te passen aan uw bedrijfsscenario voor de activiteiten die beschikbaar zijn voor selectie voor een specifiek project.</span><span class="sxs-lookup"><span data-stu-id="cd469-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="cd469-282">Een standaardprojectcategorie invoeren in urenstaatvermeldingen</span><span class="sxs-lookup"><span data-stu-id="cd469-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="cd469-283">Het invoeren van een standaardprojectcategorie voor urenstaatvermeldingen vindt plaats op drie niveaus.</span><span class="sxs-lookup"><span data-stu-id="cd469-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="cd469-284">U kunt de opdrachtenreeks gebruiken om het gedrag op een of alle van deze niveaus uit te breiden om het gewenste gedrag te bereiken.</span><span class="sxs-lookup"><span data-stu-id="cd469-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="cd469-285">De volgende hiërarchie wordt gebruikt:</span><span class="sxs-lookup"><span data-stu-id="cd469-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="cd469-286">De app probeert de standaardcategorie uit de projectresource op te halen.</span><span class="sxs-lookup"><span data-stu-id="cd469-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="cd469-287">Deze standaardcategorie is ingesteld in de methoden **getCurrentUserResource** en **getDelegatedResourcesForCurrentUser** in de klasse **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="cd469-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="cd469-288">Als de standaardcategorie niet is opgegeven op het resourceniveau van het project, probeert de app deze uit de projectactiviteit op te halen.</span><span class="sxs-lookup"><span data-stu-id="cd469-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="cd469-289">Deze standaardcategorie is ingesteld in de methode **getActivitiesForproject** in de klasse **TSTimesheetprojectService**.</span><span class="sxs-lookup"><span data-stu-id="cd469-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="cd469-290">Als de standaardcategorie niet is opgegeven op het activiteitsniveau van het project, wordt de standaardcategorie uit de projectactiviteit opgehaald.</span><span class="sxs-lookup"><span data-stu-id="cd469-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="cd469-291">Deze standaardcategorie is ingesteld in de methode **getProjectDetailsbyRule** in de klasse **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="cd469-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]