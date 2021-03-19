---
title: Nieuwe aangepaste-entiteitformulieren toevoegen (Project Service Automation 2.x)
description: Dit onderwerp bevat informatie over het toevoegen van aangepaste-entiteitformulieren voor verkoopkansen, prijsopgaven, orders of facturen in Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284847"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="7781e-103">Nieuwe aangepaste-entiteitformulieren toevoegen (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="7781e-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="7781e-104">Het veld Type</span><span class="sxs-lookup"><span data-stu-id="7781e-104">Type field</span></span> 

<span data-ttu-id="7781e-105">Dynamics 365 Project Service Automation is afhankelijk van het veld **Type** (**msdyn\_ordertype**) van de entiteiten Verkoopkans, Prijsopgave, Order en Factuur om **werkgebaseerde** versies van deze entiteiten te onderscheiden van **artikelgebaseerde** en **servicegebaseerde** versies.</span><span class="sxs-lookup"><span data-stu-id="7781e-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="7781e-106">Werkgebaseerde versies van deze entiteiten worden afgehandeld door PSA.</span><span class="sxs-lookup"><span data-stu-id="7781e-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="7781e-107">Veel bedrijfslogica aan de client- en serverzijde van de oplossing is afhankelijk van het veld **Type**.</span><span class="sxs-lookup"><span data-stu-id="7781e-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="7781e-108">Daarom is het belangrijk dat het veld wordt geïnitialiseerd met een juiste waarde wanneer de entiteiten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7781e-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="7781e-109">Een onjuiste waarde kan leiden tot onjuist gedrag en sommige bedrijfslogica wordt mogelijk niet correct uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7781e-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="7781e-110">Automatisch schakelen tussen formulieren</span><span class="sxs-lookup"><span data-stu-id="7781e-110">Automatic form switching</span></span>

<span data-ttu-id="7781e-111">Om mogelijke gegevensbeschadigingen en onverwachte gedragingen te voorkomen die worden veroorzaakt door de onjuiste initialisatie en bewerking van de verkoopentiteitsrecords, bevat PSA nu logica voor het automatisch schakelen tussen formulieren in standaardformulieren.</span><span class="sxs-lookup"><span data-stu-id="7781e-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="7781e-112">Deze logica leidt gebruikers naar het juiste formulier voor het werken met de werkgebaseerde versie of een ander type van de entiteit Verkoopkans, Prijsopgave, Order of Factuur.</span><span class="sxs-lookup"><span data-stu-id="7781e-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="7781e-113">Wanneer een gebruiker de werkgebaseerde versie van een entiteit Verkoopkans, Prijsopgave, Order of Factuur opent, wordt het formulier overgeschakeld naar **Projectgegevens**.</span><span class="sxs-lookup"><span data-stu-id="7781e-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="7781e-114">De logica voor het automatisch schakelen tussen formulieren is afhankelijk van de toewijzing tussen de waarde **formId** en het veld **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="7781e-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="7781e-115">Alle standaardformulieren zijn toegevoegd aan die toewijzing.</span><span class="sxs-lookup"><span data-stu-id="7781e-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="7781e-116">Aangepaste formulieren moeten echter handmatig worden toegevoegd om aan te geven welke versie van de entiteit hiermee moet worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="7781e-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="7781e-117">Dit is gebaseerd op het veld **veld msdyn\_order**.</span><span class="sxs-lookup"><span data-stu-id="7781e-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="7781e-118">Als de formulierschakeling ontbreekt in de toewijzing, schakelt de logica over naar het standaardformulier, op basis van de waarde die is opgeslagen in het veld **msdyn\_ordertype** van de entiteit.</span><span class="sxs-lookup"><span data-stu-id="7781e-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="7781e-119">Aangepaste formulieren toevoegen en de logica voor het schakelen tussen formulier inschakelen</span><span class="sxs-lookup"><span data-stu-id="7781e-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="7781e-120">In het volgende voorbeeld ziet u hoe u het aangepaste formulier **Mijn projectgegevens** toevoegt zodat het werkt met werkgebaseerde mogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="7781e-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="7781e-121">Hetzelfde proces wordt gebruikt om aangepaste formulieren toe te voegen zodat deze werken met prijsopgaven, orders en facturen.</span><span class="sxs-lookup"><span data-stu-id="7781e-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="7781e-122">Volg deze stappen om een aangepaste versie van het formulier **Projectgegevens** te maken.</span><span class="sxs-lookup"><span data-stu-id="7781e-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="7781e-123">Open in de entiteit Verkoopkans het formulier **Projectgegevens** en sla een kopie op onder de naam **Mijn projectgegevens**.</span><span class="sxs-lookup"><span data-stu-id="7781e-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="7781e-124">Open het nieuwe formulier en zorg er vervolgens in de eigenschappen voor dat de scripts voor formulierinitialisatie uit het formulier **Projectgegevens** aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="7781e-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="7781e-125">Verwijder de scripts niet.</span><span class="sxs-lookup"><span data-stu-id="7781e-125">Don't remove the scripts.</span></span> <span data-ttu-id="7781e-126">Anders kunnen sommige gegevens onjuist worden geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="7781e-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="7781e-127">Controleer of het veld **Type** (**msdyn\_ordertype**) aanwezig is in het formulier.</span><span class="sxs-lookup"><span data-stu-id="7781e-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="7781e-128">Verwijder dit veld niet.</span><span class="sxs-lookup"><span data-stu-id="7781e-128">Don't remove this field.</span></span> <span data-ttu-id="7781e-129">Anders mislukken de initialisatiescripts.</span><span class="sxs-lookup"><span data-stu-id="7781e-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="7781e-130">Zoek de waarde **formId** van het nieuwe formulier.</span><span class="sxs-lookup"><span data-stu-id="7781e-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="7781e-131">U kunt deze stap op twee manieren uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="7781e-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="7781e-132">Exporteer het formulier **Mijn projectgegevens** als onderdeel van een onbeheerde oplossing en zoek de waarde **formId** op in het bestand customization.xml van de geëxporteerde oplossing.</span><span class="sxs-lookup"><span data-stu-id="7781e-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="7781e-133">Open het formulier **Mijn projectgegevens** in de formuliereneditor en zoek vervolgens naar de GUID (Globally Unique Identifier) naast de parameter **fromId** in de URL, zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="7781e-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![De waarde formId van het nieuwe formulier in de URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="7781e-135">Maak een toewijzing van **msdyn\_ordertype** voor de waarde **formId** door de webresource msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js te bewerken.</span><span class="sxs-lookup"><span data-stu-id="7781e-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="7781e-136">Verwijder de code uit de resource en vervang deze door de volgende code.</span><span class="sxs-lookup"><span data-stu-id="7781e-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="7781e-137">Sla de aanpassingen op en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="7781e-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]