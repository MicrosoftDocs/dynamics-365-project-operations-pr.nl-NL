---
title: Transactiecategorie gebruiken als prijsdimensie
description: Dit artikel bevat informatie over het gebruik van het veld Transactiecategorie als een prijsdimensie.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911688"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Transactiecategorie gebruiken als prijsdimensie


_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


In dit artikel wordt uitgelegd hoe u het veld **Transactiecategorie** kunt gebruiken als een prijsdimensie. 

## <a name="prerequisites"></a>Vereisten
Voordat u de procedures in dit artikel voltooit, moet u een nieuwe prijsdimensieoplossing voor uw organisatie hebben. Als u deze nog niet hebt gemaakt, raadpleegt u [Aangepaste velden en entiteiten maken als prijsdimensies](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Het veld Transactiecategorie toevoegen aan formulieren en weergaven
Als u het veld **Transactiecategorie** zichtbaar wilt maken in de oplossing voor de prijsdimensie, moet u het veld als een entiteit aan alle formulieren en weergaven toevoegen.

De volgende tabel bevat een overzicht van alle kant-en-klare formulieren en weergaven, per entiteit. U moet het nieuwe veld ook toevoegen aan eventuele aanvullende formulieren of weergaven in uw aangepaste entiteiten.

|  Entity        | Formulieren     |Weergaven        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolprijs| Gegevens |- Actieve resourcecategorieprijzen<br> - Gekoppelde resourcecategorieprijs |
|  Opslag voor rolprijs| Gegevens|- Actieve opslag voor rolprijs<br>- Gekoppelde opslag voor rolprijs |
|  Details van prijsopgaveregel|- Projectgegevens<br>- Snelle invoer van project| - Detail van actieve prijsopgaveregel<br>- Gecombineerde details van prijsopgaveregels<br>- Gekoppelde details van prijsopgaveregels |
|  Detail van projectcontractregels|- Projectgegevens<br>- Snelle invoer van project|- Gecombineerde contractregeldetails<br>- Actieve contractregeldetails<br>- Gekoppelde contractregeldetails |
|  Projecttaak|- Gegevens<br>- Nieuw formulier| &nbsp; |
|  Projectteamlid|- Gegevens<br>- Nieuw formulier|- Actieve projectteamleden<br>- Projectteamleden<br>- Gekoppelde projectteamleden |
|  Tijdsvermelding|- Gegevens<br>- Tijdsvermelding maken|- Mijn tijdsvermeldingen op datum<br>- Mijn tijdsvermeldingen voor deze week<br>- Tijdsvermeldingen voor goedkeuring|
|  Journaalregel|- Gegevens<br>- Snelle invoer|- Actieve journaalregels<br>- Gekoppelde journaalregel|
|  Factuurregeldetail|- Gegevens<br>- Snelle invoer|- Actieve factuurregeldetails<br>- Factureerbare factuurtransacties<br>- Gratis factuurtransacties<br>- Gekoppelde weergave van factuurregeldetail <br>- Niet-factureerbare factuurtransacties|
|  Actueel|- Gegevens<br>- Actieve werkelijke waarden| Gekoppelde werkelijke waarden |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Het veld Transactiecategorie instellen als prijsdimensie

1. Ga naar **Instellingen** > **Parameters**. 
2. Controleer op de pagina **Parameters** in het tabblad **Op bedrag gebaseerde prijsdimensies** of het raster de records in de entiteit **Prijsdimensies** weergeeft.
3. Voeg **Transactiecategorie** toe aan deze lijst en stel de velden **Van toepassing op kosten** en **Van toepassing op verkoop** in op **Ja**.
4. Selecteer in het veld **Dimensietype** de optie **Op bedrag gebaseerd** en selecteer vervolgens de prioriteit voor **Transactiecategorie** met betrekking tot kosten en verkopen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]