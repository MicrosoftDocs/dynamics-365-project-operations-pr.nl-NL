---
title: Overzicht van prijsdimensies
description: Dit onderwerp bevat informatie over prijsdimensies in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650180"
---
# <a name="pricing-dimensions-overview"></a>Overzicht van prijsdimensies

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

De dimensies die worden gebruikt bij personeelszaken om prijzen en kosten in te stellen, vallen in twee categorieën:

- Mensen
- Gepland werk

Hierdoor zijn er twee typen prijsdimensiewaarden beschikbaar:

- **Optiesets**: dimensies die vaste opsommingen voor een set waarden zijn.
- **Op entiteiten gebaseerde waarden**: dimensies die een gevarieerde reeks waarden kunnen zijn.

## <a name="pricing-dimensions"></a>Prijsdimensies

Dynamics 365 Project Operations wordt geleverd met een standaardset prijsdimensies. U kunt deze prijsdimensies bekijken door naar **Project Operations** > **Parameters** te gaan. Controleer in de parameterrecord op het tabblad **Op bedrag gebaseerde prijsdimensies** of voor de rol **msdyn_resourcecategory** en de resource-organisatie-eenheid **msdyn_organizationalunit** de velden **Van toepassing op verkoop** en **Van toepassing op kosten** op **Ja** zijn ingesteld. Als deze velden zijn ingeschakeld, kunt u de prijs en kosten voor elke combinatie van rol en organisatie-eenheid instellen.

![Schermopname van Project Service-parameters waarin 'Van toepassing op verkoop' is gemarkeerd](media/PS-OOB-parameters.png)

Als u de prijs of kosten voor uw resources vaststelt met behulp van extra kenmerken, kunt u aangepaste velden, entiteiten en dimensies maken. Voor meer informatie raadpleegt u de volgende onderwerpen. 
  
  > [!NOTE]
  > De procedures moeten worden voltooid in de volgorde waarin ze worden vermeld.

1. [Een oplossing maken voor aangepaste prijsdimensies](../sales/create-solution-custompd.md)
2. [Aangepaste velden en entiteiten maken](create-custom-fields-entities-pricing-dimensions.md)
3. [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten ](add-custom-fields-price-setup-transactional-entities.md)
4. [Aangepaste velden instellen als prijsdimensies ](set-up-custom-fields-pricing-dimensions.md)
5. [Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>De prijs van personeelstijd bepalen
Hoe een organisatie de prijs van personeelstijd bepaalt, is vaak een belangrijke strategische overweging die rechtstreeks van invloed is op de winstgevendheid van de organisatie. Werk samen met de financiële teams en groepshoofden wanneer uw organisatie klaar is om te bepalen hoe zij facturerings- en kostentarieven voor personeelstijd wil instellen.

Een andere overweging voor de prijsbepaling is onder andere de vraag of u velden of entiteiten die momenteel geen prijsdimensies zijn, opnieuw wilt gebruiken, maar ze dan wilt toepassen als een prijsdimensie voor uw organisatie. Velden, zoals **Transactiecategorie** (**msdyn_transactioncategory**) en **Boekbare resource** (**bookableresource**), zijn voorbeelden van mogelijk geschikte dimensies. 

Overweeg ook of uw prijsdimensie een tabel of een optieset moet zijn. Als u verwacht dat u meer dan 10 of 12 wijzigingen in de waarden van een dimensie moet aanbrengen en u aanvullende kenmerken voor deze waarden nodig hebt, kunt u een entiteit maken in plaats van een optieset. Voor het onderhouden van een optieset, zoals het toevoegen of verwijderen van waarden, is een beheerder of ontwikkelaar vereist, terwijl het toevoegen van nieuwe rijen aan een tabel kan worden gedaan door de meeste gebruikers.

In het volgende voorbeeld worden de factureringstarieven weergegeven die zijn ingesteld op basis van de rol en de organisatie-eenheid waartoe de resource behoort. Kostentarieven zijn meestal gebaseerd op de salarisbandbreedte van de werknemer en de organisatie-eenheid waartoe deze behoort. In dit voorbeeld zien de tabellen met facturerings- en kostentarieven er als volgt uit.

**Voorbeeld van factureringstarieven**

| Rol        | Organisatie-eenheid    |Eenheid      |Prijs      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Ontwikkelaar   | Contoso US  |Hour | 200|USD     |
| Ontwikkelaar   | Contoso India |Hour|   112|USD     |


**Voorbeeld van kostentarieven**

| Salarisbandbreedte     | Organisatie-eenheid    |Eenheid      |Prijs      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Mijn bedrijf_Bandbreedte1 | Contoso US  |Hour | 145|USD     |
| Mijn bedrijf_Bandbreedte2 | Contoso India |Hour|   67|USD     |
