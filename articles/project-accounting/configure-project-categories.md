---
title: Projectcategorieën configureren
description: In dit onderwerp krijgt u informatie over het instellen van projectcategorieën.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287502"
---
# <a name="configure-project-categories"></a>Projectcategorieën configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Project Operations biedt robuuste mogelijkheden voor het categoriseren van omzet en onkosten voor projecten. Categorieën bieden de mogelijkheid om te rapporteren over projecttransacties, deze te analyseren en het boeken naar het grootboek te stimuleren.

Het volgende diagram illustreert de correlatie tussen transactiecategorieën, gedeelde categorieën en projectcategorieën. 

Transactiecategorieën vormen de basisgroepering voor projecttransacties. Binnen die groepering bestaat er een verzameling gedeelde categorieën die kunnen worden gedeeld tussen toepassingen en modules. Projectcategorieën zijn het meest gedetailleerde niveau van categorieën. Projectcategorieën hebben specifiek betrekking op rechtspersonen, modules en toepassingen.

![Correlatie tussen transactiecategorieën, gedeelde categorieën en projectcategorieën](media/project-categories.png)

## <a name="transaction-categories"></a>Transactiecategorieën

Transactiecategorieën vertegenwoordigen de basisgroepering voor projecttransacties en zijn niet specifiek gerelateerd aan een bedrijf of transactietype. Contoso Robotics gebruikt bijvoorbeeld de transactiecategorieën Ontwerp, Reizen, Installatie en Service om projecttransacties te groeperen.

Transactiecategorieën worden gedefinieerd in de Project Operations-module. 
1. Ga naar **Instellingen** \> **Transactiecategorieën** om het formulier te openen. 
2. Maak een nieuwe transactiecategorie door **Nieuw** of **Importeren vanuit Excel** te selecteren.

## <a name="shared-categories"></a>Gedeelde categorieën

Dynamics 365 gebruikt het concept Gedeelde categorieën om uitgaven in verschillende toepassingen te categoriseren, zoals Dynamics 365 Finance, Dynamics 365 Supply Chain en Dynamics 365 Project Operations. Voor elke gemaakte transactiecategorie worden in Project Operations automatisch vier gerelateerde gedeelde categorieën gemaakt: Uren, Onkosten, Tarieven en Artikel. U kunt de gedeelde categorieën bekijken en aanpassen door naar **Projectmanagement en financiële administratie** \> **Instellingen** \> **Categorieën** \> **Gedeelde categorieën** te gaan.

## <a name="project-categories"></a>Productcategorieën

Projectcategorieën staan voor het meest gedetailleerde niveau van categorieconfiguratie en moeten afzonderlijk en voor elk bedrijf worden geconfigureerd door een projectaccountant.

1. Ga naar **Projectmanagement en financiële administratie** \> **Instellingen** \> **Categorieën** \> **Projectcategorieën**.
2. Selecteer **Nieuw**.
3. Selecteer de **categorie-id** van de gedeelde categorie die u in de vorige sectie hebt gemaakt. Met Project Operations kunt u ook alleen die gedeelde categorieën gebruiken die aan transactiecategorieën zijn gekoppeld.
4. Selecteer een categoriegroep.

## <a name="category-groups"></a>Categoriegroepen

Categoriegroepen worden gebruikt om eigenschappen, voornamelijk boekingsprofielen, te delen tussen gerelateerde projectcategorieën. Er moet minimaal één categoriegroep zijn voor elk transactietype en aan elke projectcategorie wordt een groep toegewezen.

De boekingsspecificaties in Project Operations worden gedefinieerd door de profielregels voor projectkosten en -inkomsten, projectcategorieën en categoriegroepen. U kunt categoriegroepen instellen door naar **Projectmanagement en financiële administratie** \> **Instellingen** \> **Categorieën** \> **Categoriegroepen** te gaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]