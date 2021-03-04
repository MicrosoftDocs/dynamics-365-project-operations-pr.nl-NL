---
title: Implementeer aangepaste velden voor de mobiele Microsoft Dynamics 365 Project Timesheet-app op iOS en Android
description: Dit onderwerp biedt algemene patronen voor het gebruik van extensies om aangepaste velden te implementeren.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074618"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementeer aangepaste velden voor de mobiele Microsoft Dynamics 365 Project Timesheet-app op iOS en Android

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt algemene patronen voor het gebruik van extensies om aangepaste velden te implementeren. De volgende onderwerpen komen aan bod:

- De verschillende gegevenstypen die het aangepaste veldframework ondersteunt
- Alleen-lezen of bewerkbare velden in urenstaatvermeldingen weergeven en door de gebruiker verstrekte waarden weer in de database opslaan
- Alleen-lezen velden weergeven in de header van de urenstaat
- Andere aangepaste bedrijfslogica integreren om standaardwaarden in velden in te voeren en aanvullende validatie uit te voeren

## <a name="audience"></a>Publiek

Dit onderwerp is bedoeld voor ontwikkelaars die hun aangepaste velden integreren in de mobiele Microsoft Dynamics 365 Project Timesheet-toepassing die beschikbaar is voor Apple iOS en Google Android. De aanname is dat lezers bekend zijn met X++-ontwikkeling en de functionaliteit van projecturenstaten.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Gegevenscontract - X++-klasse TSTimesheetCustomField

De klasse **TSTimesheetCustomField** is de X++-gegevenscontractklasse die informatie vertegenwoordigt over een aangepast veld voor de functionaliteit voor urenstaten. Lijsten van de aangepaste veldobjecten worden doorgegeven aan zowel het TSTimesheetDetails-gegevenscontract als het TSTimesheetEntry-gegevenscontract om aangepaste velden in de mobiele app weer te geven.

- **TSTimesheetDetails** - Het contract voor de header van de urenstaat.
- **TSTimesheetEntry** - Het transactiecontract voor de urenstaat. Groepen van deze objecten met dezelfde projectinformatie en waarden voor **timesheetLineRecId** vormen een regel.

### <a name="fieldbasetype-types"></a>fieldBaseType (typen)

De eigenschap **FieldBaseType** voor het object **TsTimesheetCustom** bepaalt het type veld dat in de app wordt weergegeven. De volgende waarden voor **Types** worden ondersteund.

| Waarde voor Types | Type              | Opmerkingen |
|-------------|-------------------|-------|
| 0           | Tekenreeks (en Enum) | Het veld wordt weergegeven als een tekstveld. |
| 0           | Integer           | De waarde wordt weergegeven als een getal zonder decimalen. |
| 2           | Real              | De waarde wordt weergegeven als een getal met decimalen.<p>Als u de reële waarde als valuta in de app wilt weergeven, gebruikt u de eigenschap **fieldExtenededType**. U kunt de eigenschap **numberOfDecimals** gebruiken om het aantal getoonde decimalen in te stellen.</p> |
| 5           | Date              | Datumnotaties worden bepaald door de instelling **Datum-, tijden- en getalnotatie** van de gebruiker die is gespecificeerd onder **Voorkeur voor taal en land/regio** in **Gebruikersopties**. |
| 4           | Booleaanse waarde           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Als de eigenschap **stringOptions** niet is opgegeven voor het object **TSTimesheetCustomField** , wordt een vrij tekstveld aan de gebruiker verstrekt.

    De eigenschap **stringLength** kan worden gebruikt om de maximale tekenreekslengte in te stellen die gebruikers kunnen invoeren.

- Als de eigenschap **stringOptions** wordt verstrekt voor het object **TSTimesheetCustomField** , zijn die lijstelementen de enige waarden die gebruikers kunnen selecteren met behulp van optieknoppen (keuzerondjes).

    In dit geval kan het tekenreeksveld fungeren als een opsommingswaarde voor gebruikersinvoer. Als u de waarde in de database wilt opslaan als een enum, wijst u de tekenreekswaarde handmatig opnieuw toe aan de enum-waarde voordat u opslaat in de database met behulp van een opdrachtenreeks (zie de sectie "Opdrachtenreeks gebruiken voor de klasse TSTimesheetEntryService om een urenstaatvermelding uit de app opnieuw op te slaan in de database" verderop in dit onderwerp voor een voorbeeld).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

U kunt deze eigenschap gebruiken om reële waarden als valuta op te maken. Deze benadering is alleen van toepassing als de waarde **fieldBaseType** **Real** is.

- **TSCustomFieldExtendedType:None** – Er wordt geen opmaak toegepast.
- **TSCustomFieldExtendedType::Currency** - Formatteer de waarde als valuta.

    Als valutanotatie actief is, kan het veld **stringValue** worden gebruikt om de valutacode door te geven die in de app moet worden weergegeven. De waarde is een alleen-lezen waarde.

    Het veld **realValue** bevat het geldbedrag dat in de database moet worden opgeslagen.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

U kunt deze eigenschap gebruiken om aan te geven waar het aangepaste veld in de app moet verschijnen.

- **TSCustomFieldSection::Header** - Het veld verschijnt in de sectie **Meer details weergeven** in de app. Deze velden zijn altijd alleen-lezen.
- **TSCustomFieldSection::Line** - Het veld wordt weergegeven na alle kant-en-klare regelvelden in urenstaatvermeldingen. Deze velden kunnen bewerkbaar of alleen-lezen zijn.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Deze eigenschap identificeert het veld wanneer waarden die de app levert opnieuw worden opgeslagen in de database.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Deze eigenschap identificeert het veld wanneer waarden die de app levert opnieuw worden opgeslagen in de database.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Stel deze eigenschap in op **Yes** om aan te geven dat het veld in de sectie voor het invoeren van urenstaten door gebruikers moet kunnen worden bewerkt. Stel de eigenschap in op **No** om het veld alleen-lezen te maken.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Stel deze eigenschap in op **Yes** om aan te geven dat het veld in de sectie voor het invoeren van urenstaten verplicht moet zijn.

### <a name="label-str"></a>label (str)

Deze eigenschap geeft het label aan dat naast het veld in de app wordt weergegeven.

### <a name="stringoptions-list-of-strings"></a>stringOptions (lijst met tekenreeksen)

Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **String**. Als **stringOptions** is ingesteld, worden de tekenreekswaarden die beschikbaar zijn voor selectie via optieknoppen (keuzerondjes) gespecificeerd door de tekenreeksen in de lijst. Als er geen tekenreeksen zijn opgegeven, is vrije tekstinvoer in het tekenreeksveld toegestaan (zie de sectie "Opdrachtenreeks gebruiken voor de klasse TSTimesheetEntryService om een urenstaatvermelding uit de app opnieuw op te slaan in de database" verderop in dit onderwerp voor een voorbeeld).

### <a name="stringlength-int"></a>stringLength (int)

Deze eigenschap specificeert de maximale lengte voor een tekenreeksveld. Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Deze eigenschap specificeert het aantal decimalen dat wordt weergegeven voor een reëel veld. Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Deze eigenschap bepaalt de volgorde waarin de aangepaste velden in de app worden weergegeven wanneer er meer dan één aangepast veld is opgegeven. Velden met lagere getallen worden als eerste weergegeven.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Voor velden van het type **Boolean** , geeft deze eigenschap de booleaanse waarde van het veld door tussen de server en de app.

### <a name="guidvalue-guid"></a>guidValue (guid)

Voor velden van het type **GUID** , geeft deze eigenschap de GUID-waarde (Globally Unique Identifier) van het veld door tussen de server en de app.

### <a name="int64value-int64"></a>int64Value (int64)

Voor velden van het type **Int64** , geeft deze eigenschap de int64-waarde van het veld door tussen de server en de app.

### <a name="intvalue-int"></a>intValue (int)

Voor velden van het type **Int** , geeft deze eigenschap de int-waarde van het veld door tussen de server en de app.

### <a name="realvalue-real"></a>realValue (real)

Voor velden van het type **Real** , geeft deze eigenschap de reële waarde van het veld door tussen de server en de app.

### <a name="stringvalue-str"></a>stringValue (str)

Voor velden van het type **String** , geeft deze eigenschap de tekenreekswaarde van het veld door tussen de server en de app. Het wordt ook gebruikt voor velden van het type **Real** die zijn opgemaakt als valuta. Voor die velden wordt de eigenschap gebruikt om de valutacode door te geven aan de app.

### <a name="datevalue-date"></a>dateValue (date)

Voor velden van het type **Date** , geeft deze eigenschap de datumwaarde van het veld door tussen de server en de app.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Een aangepast veld weergeven en opslaan in de sectie voor het invoeren van de urenstaat

Hieronder ziet u een schermopname van het maken van een urenstaatvermelding in de mobiele app. Het toont de kant-en-klare velden en een aangepast veld in de secite "Tijdinvoer" genaamd "Testtekenreeks" waarvoor al een enum-waarde "Tweede optie" is ingesteld.

![Aangepast veld Testtekenreeks in de app](media/timesheet-entry.jpg)



Hieronder ziet u een schermopname van de mobiele app van de gebruiker die een van de enum-opties selecteert die beschikbaar zijn voor het aangepaste veld "Testtekenreeks".  De twee opties zijn "Eerste optie" en "Tweede optie" weergegeven als keuzerondjes. De tweede optie is momenteel geselecteerd.

![Optieknoppen (keuzerondjes) voor het aangepaste veld Testtekenreeks](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>De tabel TSTimesheetLine uitbreiden zodat deze een aangepast veld heeft

In typische scenario's is het waarschijnlijk zo dat de gegevens voor een aangepast veld in de sectie voor urenstaatinvoer worden opgeslagen in de tabel TSTimesheetLine. Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTrans-record die wordt verstrekt of als deze geen specifieke recordcontext hebben (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).

Merk op dat aangepaste velden geen ondersteunende databaserecords hoeven te hebben. Ze kunnen dynamisch worden gegenereerd op basis van X++-logica. Deze benadering kan handig zijn in alleen-lezen scenario's (zie de sectie "Opdrachtenreeks gebruiken voor de klasse TSTimesheetDetails, methode buildCustomFieldListForHeader, om urenstaatdetails in te vullen" voor een voorbeeld van dynamisch gegenereerde aangepaste veldwaarden.)

Hieronder wordt een schermopname weergegeven van de toepassingsobjectstructuur in Visual Studio. Het toont een uitbreiding van de tabel TSTimesheetLine met het veld TestLineString toegevoegd als een aangepast veld.

![Regeltekenreeks](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Opdrachtenreeks gebruiken voor de methode buildCustomFieldList van de klasse TSTimesheetSettings om een veld weer te geven in de sectie voor urenstaatinvoer

Deze code regelt de weergave-instellingen voor het veld in de app. Het bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld verschijnt.

Het volgende voorbeeld toont een tekenreeksveld voor tijdinvoer. Dit veld heeft twee opties, **Eerste optie** en **Tweede optie** , die beschikbaar zijn via optieknoppen (keuzerondjes). Het veld in de app is gekoppeld aan het veld **TestLineString** dat wordt toegevoegd aan de tabel TSTimesheetLine.

Let op het gebruik van de methode **TSTimesheetCustomField::newFromMetatdata()** om de initialisatie van de aangepaste veldeigenschappen te vereenvoudigen: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** en **numberOfDecimals**. U kunt deze parameters ook handmatig instellen, als u dat wilt.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Opdrachtenreeks gebruiken voor de methode buildCustomFieldListForEntry van de klasse TSTimesheetEntry om waarden in te voeren in een urenstaatvermelding

De methode **buildCustomFieldListForEntry** wordt gebruikt om waarden in te voeren op de opgeslagen urenstaatregels in de mobiele app. Er is een TSTimesheetTrans-record nodig als parameter. Velden uit dat record kunnen worden gebruikt om de aangepaste veldwaarde in de app in te vullen.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Opdrachtenreeks gebruiken voor de klasse TSTimesheetEntryService om een urenstaatvermelding van de app opnieuw op te slaan in de database

Als u een aangepast veld bij normaal gebruik weer wilt opslaan in de database, moet u meerdere methoden uitbreiden:

- De methode **timesheetLineNeedsUpdating** wordt gebruikt om te bepalen of de regelrecord is gewijzigd door de gebruiker in de app en moet worden opgeslagen in de database. Als prestaties geen probleem zijn, kan deze methode worden vereenvoudigd zodat deze altijd **true** retourneert.
- De methoden **populateTimesheetLineFromEntryDuringCreate** en **populateTimesheetLineFromEntryDuringUpdate** kunnen worden uitgebreid zodat ze waarden invoeren in de databaserecord TSTimesheetLine vanuit de TSTimesheetEntry-gegevenscontractrecord die wordt verstrekt. In het onderstaande voorbeeld ziet u hoe de toewijzing tussen het databaseveld en het invoerveld handmatig wordt uitgevoerd via X++-code.
- De methode **populateTimesheetWeekFromEntry** kan ook worden uitgebreid als het aangepaste veld dat is toegewezen aan het object **TSTimesheetEntry** moet terugschrijven naar de databasetabel TSTimesheetLineweek.

> [!NOTE]
> In het volgende voorbeeld wordt de waarde **firstOption** of **secondOption** die de gebruiker in de database selecteert opgeslagen als een onbewerkte tekenreekswaarde. Als het databaseveld een veld is van het type **Enum** , kunnen die waarden handmatig worden toegewezen aan een enum-waarde en vervolgens worden opgeslagen in een enum-veld in de databasetabel.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Een aangepast veld weergeven in de headersectie van de urenstaat

Hieronder ziet u een schermopname van de weergave van een urenstaat in de mobiele app door een gebruiker. De knop "Meer informatie" is geselecteerd in de rechterbovenhoek om de optie "Meer details weergeven" te tonen.  

![Opdracht Meer details weergeven](media/show-more.png)

Hieronder ziet u een schermopname van de sectie "Meer" van een urenstaat in de mobiele app. Een aangepast veld met de naam "Benuttingspercentage van deze urenstaat (berekend aangepast veld)" is toegevoegd aan de headersectie van de urenstaat. Een alleen-lezen waarde van "0,667" is ingesteld voor het aangepaste veld.

![Sectie Meer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>De tabel TSTimesheetTable uitbreiden zodat deze een aangepast veld heeft

In typische scenario's is het waarschijnlijk zo dat de gegevens voor een aangepast veld in de headersectie worden opgehaald uit de tabel TSTimesheetHeader. Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTable-record die wordt verstrekt of als deze geen specifieke recordcontext hebben (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).

Merk op dat aangepaste velden geen ondersteunende databaserecords hoeven te hebben. Ze kunnen dynamisch worden gegenereerd op basis van X++-logica. Het volgende voorbeeld toont deze benadering.

Velden in de headersectie zijn altijd alleen-lezen in de app.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Opdrachtenreeks gebruiken voor de methode buildCustomFieldList van de klasse TSTimesheetSettings om een veld weer te geven in de headersectie

Deze code regelt de weergave-instellingen voor het veld in de app. Het bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld verschijnt.

Het volgende voorbeeld toont een berekende waarde in de headersectie in de app.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Opdrachtenreeks gebruiken voor de methode buildCustomFieldListForHeader van de klasse TSTimesheetDetails om urenstaatdetails in te vullen

De methode **buildCustomFieldListForHeader** wordt gebruikt om details van de urenstaatheader in te vullen in de mobiele app. Er is een TSTimesheetTable-record nodig als parameter. Velden uit dat record kunnen worden gebruikt om de aangepaste veldwaarde in de app in te vullen. In het volgende voorbeeld worden geen waarden uit de database gelezen. In plaats daarvan gebruikt X++ logica om een berekende waarde te genereren die vervolgens in de app wordt weergegeven.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Andere mogelijkheden voor configureerbaarheid/uitbreidbaarheid

### <a name="adding-additional-validation-for-the-app"></a>Extra validatie toevoegen voor de app

De bestaande logica voor urenstaatfunctionaliteit op databaseniveau zal nog steeds werken zoals verwacht. Als u de voltooiing van bewerkingen voor opslaan of verzenden wilt onderbreken en een specifiek foutbericht wilt weergeven, kunt u **throw error("bericht aan gebruiker")** toevoegen naar de code via een opdrachtextensie. Hier zijn drie voorbeelden van handige uitbreidbare methoden:

- Als **validateWrite** voor de tabel TSTimesheetLine **false** retourneert tijdens het opslaan van een urenstaatregel, wordt een foutmelding weergegeven in de mobiele app.
- Als **validateSubmit** voor de tabel TSTimesheetTable **false** retourneert tijdens het indienen van de urenstaat in de app, wordt een foutmelding weergegeven aan de gebruiker.
- Logica die velden invult (bijvoorbeeld **Regeleigenschap** ) tijdens de methode **insert** voor de tabel TSTimesheetLine wordt nog steeds uitgevoerd.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Kant-en-klare velden verbergen en markeren als alleen-lezen via configuratie

Vanuit de projectparameters kunt u kant-en-klare velden alleen-lezen maken of verbergen in de mobiele app. Stel de opties in de sectie **Mobiele urenstaten** in op het tabblad **Urenstaat** van de pagina **Parameters voor Projectmanagement en financiële administratie**.

![Projectparameters](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>De activiteiten wijzigen die beschikbaar zijn voor selectie via extensies

De activiteiten die beschikbaar zijn voor selectie voor een project worden ingevuld via de methoden **getActivitiesForproject()** en **getActivityQuery()** in de klasse **TsTimesheetprojectService**. U kunt de opdrachtenreeks gebruiken om dit gedrag aan te passen aan uw bedrijfsscenario voor de activiteiten die beschikbaar zijn voor selectie voor een specifiek project.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Een standaardprojectcategorie invoeren in urenstaatvermeldingen

Het invoeren van een standaardprojectcategorie voor urenstaatvermeldingen vindt plaats op drie niveaus. U kunt de opdrachtenreeks gebruiken om het gedrag op een of alle van deze niveaus uit te breiden om het gewenste gedrag te bereiken. De volgende hiërarchie wordt gebruikt:

1. De app probeert de standaardcategorie uit de projectresource op te halen. Deze standaardcategorie is ingesteld in de methoden **getCurrentUserResource** en **getDelegatedResourcesForCurrentUser** in de klasse **TSTimesheetSettingsService**.
2. Als de standaardcategorie niet is opgegeven op het resourceniveau van het project, probeert de app deze uit de projectactiviteit op te halen. Deze standaardcategorie is ingesteld in de methode **getActivitiesForproject** in de klasse **TSTimesheetprojectService**.
3. Als de standaardcategorie niet is opgegeven op het activiteitsniveau van het project, wordt de standaardcategorie uit de projectactiviteit opgehaald. Deze standaardcategorie is ingesteld in de methode **getProjectDetailsbyRule** in de klasse **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]