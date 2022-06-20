---
title: Valuta
description: Dit artikel biedt informatie over het toevoegen en verwijderen van valutatypen in Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0fbfd1039fe0a7401376bb8c27b118297fdc87f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921526"
---
# <a name="currency"></a>Valuta

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_



Valuta's bepalen de prijzen van producten in de productcatalogus en de kosten van transacties, zoals verkooporders. Als uw klanten geografisch verspreid zijn, kunt u hun valuta's toevoegen om uw transacties te beheren. Voeg de valuta's toe die het meest relevant zijn voor uw huidige en toekomstige zakelijke behoeften.  

> [!NOTE]
> Als uw omgeving een Common Data Service-omgeving is, u zich in het Power Platform-beheercentrum bevindt en de pagina **Valuta's** selecteert (**Omgevingen** > [selecteer omgeving] > **Instellingen** > **Zakelijk** > **Valuta's**), is de pagina leeg. Dit komt omdat het instellen van een valuta niet wordt ondersteund in Common Data Service-omgevingen.

## <a name="add-a-currency"></a>Een valuta toevoegen  
Voordat u met deze procedure begint, moet u controleren of uw beveiligingsrol systeembeheerdersmachtigingen bevat. 

1. Selecteer een omgeving in het Power Platform-beheercentrum. 
2. Selecteer **Instellingen** > **Zakelijk**.
3. Selecteer **Valuta's**.  
4. Selecteer **Nieuw**.  
5. Vul de informatie in.  


   |          Veld          |                                                                                                                                                                                                                                                                                                                                                                            Beschrijving                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Type valuta**    | - **Systeem** - Selecteer deze optie als u de valuta's wilt gebruiken die beschikbaar zijn in modelgestuurde apps in Dynamics 365. Selecteer **Opzoeken** om naar een valuta te zoeken. Als u een valutacode hebt geselecteerd, worden de waarden voor **Valutanaam** en **Valutasymbool** automatisch toegevoegd voor de geselecteerde valuta.<br />- **Aangepast** - Selecteer deze optie als u een valuta wilt toevoegen die niet beschikbaar is in modelgestuurde apps in Dynamics 365. In dit geval moet u de waarden voor **Valutacode**, **Valutanauwkeurigheid**, **Valutanaam**, **Valutasymbool** en **Valutaomrekening** handmatig invoeren. |
   |    **Valutacode**    |                                                                                                                                                                                                                                                                                                                                            Korte notatie voor de valuta. Zoals **USD** voor de Amerikaanse dollar.                                                                                                                                                                                                                                                                                                                                            |
   | **Valutanauwkeurigheid**  |                                                                                                                                                                                  Typ het aantal decimalen dat u voor de valuta wilt gebruiken.  U kunt een waarde tussen 0 en 4 invoeren. **Opmerking:** als u een precisiewaarde in het dialoogvenster **Systeeminstellingen** hebt ingesteld, wordt die waarde hier weergegeven.                                                                                                                                                                                  |
   |    **Valutanaam**    |                                                                                                                                                                                                                                         Als u een valutacode in de lijst met beschikbare valuta's in modelgestuurde apps in Dynamics 365 hebt geselecteerd, wordt de valutanaam voor de geselecteerde code hier weergegeven. Als u **Aangepast** als valutatype hebt geselecteerd, typt u de naam van de valuta.                                                                                                                                                                                                                                          |
   |   **Valutasymbool**   |                                                                                                                                                                                                                                                                      Als u een valutacode in de lijst met beschikbare valuta's hebt geselecteerd, wordt het symbool voor de geselecteerde valuta hier weergegeven. Als u **Aangepast** als valutatype hebt geselecteerd, voert u het symbool voor de nieuwe valuta in.                                                                                                                                                                                                                                                                       |
   | **Valutaomrekening** |                                                                                                                                                                                                                                     Typ de waarde van de geselecteerde valuta afgezet tegen de waarde van één Amerikaanse dollar. Dit is het omrekeningbedrag tussen de geselecteerde valuta en de basisvaluta. **Belangrijk:** werk deze waarde regelmatig bij om onnauwkeurigheden in berekeningen in uw transactie te voorkomen.                                                                                                                                                                                                                                      |


6. Als u gereed bent, selecteert u op de opdrachtbalk de optie **Opslaan** of **Opslaan en sluiten**.  

   > [!TIP]
   >  Als u een valuta wilt bewerken, selecteert u de valuta en typt of selecteert u de nieuwe waarden.  

## <a name="delete-a-currency"></a>Een valuta verwijderen  

1. Selecteer een omgeving in het Power Platform-beheercentrum. 
2. Selecteer **Instellingen** > **Zakelijk**.
3. Selecteer **Valuta's**.  
4. Selecteer in de weergegeven lijst de valuta die u wilt verwijderen.  
5. Selecteer **Verwijderen**.  
6. Bevestig de verwijdering.  

> [!IMPORTANT]
>  Valuta's die door andere records worden gebruikt, kunnen niet worden verwijderd, alleen gedeactiveerd. Wanneer u valutarecords deactiveert, worden de valutagegevens in bestaande records (zoals verkoopkansen of orders) niet verwijderd. U kunt de gedeactiveerde valuta echter niet meer selecteren voor nieuwe transacties.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]