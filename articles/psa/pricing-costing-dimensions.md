---
title: Startpagina voor prijs- en kostendimensies
description: Dit onderwerp biedt een overzicht van prijsdimensies.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151292"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Startpagina voor prijs- en kostendimensies

[!include [banner](../includes/psa-now-project-operations.md)]

De dimensies die worden gebruikt om arbeidsprijzen en -kosten in projectgebaseerde organisaties vast te stellen, worden beïnvloed door de volgende kenmerken:

- Mensen die werk doen dat vergelijkbaar is met hun ervaring, rol of geografie
- Uit te voeren werkzaamheden die vergelijkbaar zijn met de complexiteit of het tijdstip van de dag

Gezien de typische aard van deze kenmerken van het werk en de mensen die nodig zijn om het werk uit te voeren, zijn er twee soorten prijsdimensiewaarden beschikbaar in Project Service Automation: 

- **Optiesets**: kenmerken die vaste opsommingen voor een set waarden zijn.
- **Op entiteiten gebaseerde waarden**: kenmrken die een gevarieerde reeks waarden kunnen hebben die eindig zijn, maar in de loop van de tijd kunnen veranderen.

## <a name="pricing-dimensions"></a>Prijsdimensies

PSA wordt geleverd met een standaardset prijsdimensies. U kunt deze bekijken door naar **Project Service** > **Parameters** te gaan. Controleer in de parameterrecord op het tabblad **Op bedrag gebaseerde prijsdimensies** of voor de rol **msdyn_resourcecategory** en de resource-organisatie-eenheid **msdyn_organizationalunit** de velden **Van toepassing op verkoop** en **Van toepassing op kosten** op **Ja** zijn ingesteld. Dit stelt u in staat om de prijs en kosten voor elke combinatie van rol en organisatie-eenheid in te stellen.

![Schermopname van Project Service-parameters waarin 'Van toepassing op verkoop' is gemarkeerd](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Als u de kant-en-klare velden van rol en organisatie-eenheid hebt gebruikt als prijsdimensies vóór versie 3 van PSA, is er geen waarneembare wijziging. U kunt Project Service blijven gebruiken zoals u dat gewend was. 

Als u de prijs of kosten voor uw resources vaststelt met behulp van extra kenmerken, kunt u aangepaste velden, entiteiten en dimensies maken. Zie de volgende onderwerpen voor meer informatie, maar houd er rekening mee dat u de procedures in de onderstaande volgorde moet uitvoeren:

- [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md)
- [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](field-references.md)
- [Aangepaste velden instellen als prijsdimensies ](set-up-pricing-dimensions.md)
- [Kenmerken van invoegtoepassingen bijwerken om nieuwe prijsdimensies op te nemen](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>De prijs van personeelstijd bepalen
Hoe een organisatie de prijs van personeelstijd bepaalt, is vaak een belangrijke strategische overweging die rechtstreeks van invloed is op de winstgevendheid van de organisatie. Werk samen met de financiële teams en groepshoofden wanneer uw organisatie klaar is om te bepalen hoe zij facturerings- en kostentarieven voor personeelstijd wil instellen.

Een andere overweging voor de prijsbepaling is onder andere de vraag of u velden of entiteiten die momenteel geen prijsdimensies zijn, opnieuw wilt gebruiken, maar ze dan wilt toepassen als een prijsdimensie voor uw organisatie. Velden, zoals **Transactiecategorie** (**msdyn_transactioncategory**) en **Boekbare resource** (**bookableresource**), zijn voorbeelden van mogelijk geschikte dimensies. 

Overweeg ook of uw prijsdimensie een tabel of een optieset moet zijn. Als u verwacht dat u meer dan 10 of 12 wijzigingen in de waarden van een dimensie moet aanbrengen en u aanvullende kenmerken voor deze waarden nodig hebt, maakt u een entiteit in plaats van een optieset. Voor het onderhouden van een optieset, zoals het toevoegen of verwijderen van waarden, is een beheerder of ontwikkelaar vereist, terwijl het toevoegen van nieuwe rijen aan een tabel kan worden gedaan door de meeste zakelijke gebruikers.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]