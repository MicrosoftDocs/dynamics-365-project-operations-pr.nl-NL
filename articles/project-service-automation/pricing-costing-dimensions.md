---
title: Startpagina voor prijs- en kostendimensies
description: Dit onderwerp biedt een overzicht van prijsdimensies.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750736"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Startpagina voor prijs- en kostendimensies

De dimensies die worden gebruikt bij personeelszaken om prijzen en kosten in te stellen, vallen in twee categorieën:

- Mensen
- Gepland werk

Hierdoor zijn er twee typen prijsdimensiewaarden beschikbaar in Project Service Automation (PSA): 

- **Optiesets** - Dimensies die vaste opsommingen voor een set waarden zijn.
- **Op entiteiten gebaseerde waarden** - Dimensies die een gevarieerde set waarden kunnen zijn.

## <a name="pricing-dimensions"></a>Prijsdimensies

PSA wordt geleverd met een standaardset prijsdimensies. U kunt deze bekijken door naar **Project Service** > **Parameters** te gaan. Controleer in de parameterrecord op het tabblad **Op bedrag gebaseerde prijsdimensies** of voor de rol **msdyn_resourcecategory** en de resource-organisatie-eenheid **msdyn_organizationalunit** de velden **Van toepassing op verkoop** en **Van toepassing op kosten** op **Ja** zijn ingesteld. Dit stelt u in staat om de prijs en kosten voor elke combinatie van rol en organisatie-eenheid in te stellen.

![Schermopname van Project Service-parameters waarin 'Van toepassing op verkoop' is gemarkeerd](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Als u de kant-en-klare velden van rol en organisatie-eenheid hebt gebruikt als prijsdimensies vóór versie 3 van PSA, is er geen waarneembare wijziging. U kunt Project Service blijven gebruiken zoals u dat gewend was. 

Als u de prijs of kosten voor uw resources vaststelt met behulp van extra kenmerken, kunt u aangepaste velden, entiteiten en dimensies maken. Zie de volgende onderwerpen voor meer informatie, maar houd er rekening mee dat u de procedures in de onderstaande volgorde moet uitvoeren:

- [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md)
- [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](field-references.md)
- [Aangepaste velden instellen als prijsdimensies](set-up-pricing-dimensions.md)
- [Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>De prijs van personeelstijd bepalen
Hoe een organisatie de prijs van personeelstijd bepaalt, is vaak een belangrijke strategische overweging die rechtstreeks van invloed is op de winstgevendheid van de organisatie. Werk samen met de financiële teams en groepshoofden wanneer uw organisatie klaar is om te bepalen hoe zij facturerings- en kostentarieven voor personeelstijd wil instellen.

Een andere overweging voor de prijsbepaling is onder andere de vraag of u velden of entiteiten die momenteel geen prijsdimensies zijn, opnieuw wilt gebruiken, maar ze dan wilt toepassen als een prijsdimensie voor uw organisatie. Velden, zoals **Transactiecategorie** (**msdyn_transactioncategory**) en **Boekbare resource** (**bookableresource**), zijn voorbeelden van mogelijk geschikte dimensies. 

U dient ook te overwegen of uw prijsdimensie een tabel of een optieset moet zijn. Als u verwacht dat u meer dan 10 of 12 wijzigingen in de waarden van een dimensie moet aanbrengen en u aanvullende kenmerken voor deze waarden nodig hebt, kunt u een entiteit maken in plaats van een optieset. Voor het onderhouden van een optieset, zoals het toevoegen of verwijderen van waarden, is een beheerder of ontwikkelaar vereist, terwijl het toevoegen van nieuwe rijen aan een tabel kan worden gedaan door de meeste gebruikers.

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
