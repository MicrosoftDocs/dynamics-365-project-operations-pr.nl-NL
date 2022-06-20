---
title: Nieuwe aangepaste-entiteitformulieren toevoegen (Project Service Automation 2.x)
description: Dit artikel bevat informatie over het toevoegen van aangepaste-entiteitformulieren voor verkoopkansen, prijsopgaven, orders of facturen in Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922722"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Nieuwe aangepaste-entiteitformulieren toevoegen (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Het veld Type 

Dynamics 365 Project Service Automation is afhankelijk van het veld **Type** (**msdyn\_ordertype**) van de entiteiten Verkoopkans, Prijsopgave, Order en Factuur om **werkgebaseerde** versies van deze entiteiten te onderscheiden van **artikelgebaseerde** en **servicegebaseerde** versies. Werkgebaseerde versies van deze entiteiten worden afgehandeld door PSA. Veel bedrijfslogica aan de client- en serverzijde van de oplossing is afhankelijk van het veld **Type**. Daarom is het belangrijk dat het veld wordt geïnitialiseerd met een juiste waarde wanneer de entiteiten worden gemaakt. Een onjuiste waarde kan leiden tot onjuist gedrag en sommige bedrijfslogica wordt mogelijk niet correct uitgevoerd.

## <a name="automatic-form-switching"></a>Automatisch schakelen tussen formulieren

Om mogelijke gegevensbeschadigingen en onverwachte gedragingen te voorkomen die worden veroorzaakt door de onjuiste initialisatie en bewerking van de verkoopentiteitsrecords, bevat PSA nu logica voor het automatisch schakelen tussen formulieren in standaardformulieren. Deze logica leidt gebruikers naar het juiste formulier voor het werken met de werkgebaseerde versie of een ander type van de entiteit Verkoopkans, Prijsopgave, Order of Factuur. Wanneer een gebruiker de werkgebaseerde versie van een entiteit Verkoopkans, Prijsopgave, Order of Factuur opent, wordt het formulier overgeschakeld naar **Projectgegevens**.

De logica voor het automatisch schakelen tussen formulieren is afhankelijk van de toewijzing tussen de waarde **formId** en het veld **msdyn\_ordertype**. Alle standaardformulieren zijn toegevoegd aan die toewijzing. Aangepaste formulieren moeten echter handmatig worden toegevoegd om aan te geven welke versie van de entiteit hiermee moet worden verwerkt. Dit is gebaseerd op het veld **veld msdyn\_order**. Als de formulierschakeling ontbreekt in de toewijzing, schakelt de logica over naar het standaardformulier, op basis van de waarde die is opgeslagen in het veld **msdyn\_ordertype** van de entiteit.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Aangepaste formulieren toevoegen en de logica voor het schakelen tussen formulier inschakelen

In het volgende voorbeeld ziet u hoe u het aangepaste formulier **Mijn projectgegevens** toevoegt zodat het werkt met werkgebaseerde mogelijkheden. Hetzelfde proces wordt gebruikt om aangepaste formulieren toe te voegen zodat deze werken met prijsopgaven, orders en facturen.

Volg deze stappen om een aangepaste versie van het formulier **Projectgegevens** te maken.

1. Open in de entiteit Verkoopkans het formulier **Projectgegevens** en sla een kopie op onder de naam **Mijn projectgegevens**.
2. Open het nieuwe formulier en zorg er vervolgens in de eigenschappen voor dat de scripts voor formulierinitialisatie uit het formulier **Projectgegevens** aanwezig zijn. 

    > [!IMPORTANT]
    > Verwijder de scripts niet. Anders kunnen sommige gegevens onjuist worden geïnitialiseerd.

3. Controleer of het veld **Type** (**msdyn\_ordertype**) aanwezig is in het formulier. 

    > [!IMPORTANT]
    > Verwijder dit veld niet. Anders mislukken de initialisatiescripts.

4. Zoek de waarde **formId** van het nieuwe formulier. U kunt deze stap op twee manieren uitvoeren:

    - Exporteer het formulier **Mijn projectgegevens** als onderdeel van een onbeheerde oplossing en zoek de waarde **formId** op in het bestand customization.xml van de geëxporteerde oplossing.
    - Open het formulier **Mijn projectgegevens** in de formuliereneditor en zoek vervolgens naar de GUID (Globally Unique Identifier) naast de parameter **fromId** in de URL, zoals wordt weergegeven in de volgende afbeelding.

    ![De waarde formId van het nieuwe formulier in de URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Maak een toewijzing van **msdyn\_ordertype** voor de waarde **formId** door de webresource msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js te bewerken. Verwijder de code uit de resource en vervang deze door de volgende code.

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

6. Sla de aanpassingen op en publiceer deze.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
