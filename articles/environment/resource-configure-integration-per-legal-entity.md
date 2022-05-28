---
title: De integratie van Project Operations per rechtspersoon configureren
description: Dit onderwerp bevat informatie over het instellen van de integratie per rechtspersoon in Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585832"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>De integratie van Project Operations per rechtspersoon configureren 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp leidt u door de stappen die nodig zijn om Dynamics 365 Project Operations te configureren per rechtspersoon.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Functietoetsen inschakelen in Dynamics 365 Finance

Voer de volgende stappen uit om de vereiste functies in te schakelen.

1. Ga in Dynamics 365 Finance naar de werkruimte **Functiebeheer**.
2. Zoek in **Lijst met functies** naar de volgende functies en schakel ze in:
  
    - **Meerdere contractregels inschakelen voor een project**
    - **Project Operations inschakelen in Dynamics 365 Customer Engagement**

> [!NOTE]
> Als **Functietoetsen** niet wordt vermeld, controleert u of uw Finance-versie voldoet aan de minimale versievereiste (toepassingsversie 10.0.13 met alle kwaliteitsupdates toegepast of hoger). Selecteer **Controleren op updates** om de lijst met functies te vernieuwen.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Het implementatiescenario van Project Operations voor een rechtspersoon definiëren

U kunt Project Operations inschakelen in Dynamics 365 Customer Engagement op het niveau van een rechtspersoon. U kunt één rechtspersoon hebben die Project Operations in Dynamics 365 Customer Engagement gebruikt voor scenario's op basis van resources/niet-voorraad. In dezelfde omgeving kunt u nog een rechtspersoon hebben die Project Operations gebruikt voor scenario's op basis van voorradige artikelen/productieorders.

1. Ga in Dynamics 365 Finance naar **Projectbeheer en financiële administratie** > **Instellingen** > **Algemene projectbeheer- en boekhoudingsparameters**.
2. Selecteer in de lijst met beschikbare rechtspersonen entiteiten waarvoor meerdere contractregels en functies van Project Operations in Dynamics 365 Customer Engagement worden ingeschakeld. Laat rechtspersonen die Project Operations gebruiken voor scenario's op basis van voorradige artikelen/productieorders uitgeschakeld.

> [!NOTE]
> Een rechtspersoon kan alleen worden geselecteerd als deze geen bestaande projecten heeft.

## <a name="configure-project-management-and-accounting-parameters"></a>Parameters voor Projectbeheer en financiële administratie configureren

Elke rechtspersoon die Project Operations in Dynamics 365 Customer Engagement gebruikt, heeft een set standaardparameters nodig. Deze parameters zijn geconfigureerd op het tabblad **Project Operations** op de pagina **Parameters voor Projectbeheer en financiële administratie** bladzijde. De parameters zijn:

  - **Standaardwaarden voor factureringstype**: Project Operations gebruikt een vaste set standaardinstellingen voor factureringstypes die moeten worden toegewezen aan regeleigenschappen in Finance. Maak een record voor elk factureringstype: **Niet gespecificeerd**, **Toerekenbaar**, **Niet-toerekenbaar**, **Gratis** en **Niet beschikbaar**.
  - **Standaardinstellingen projectcategorie**: selecteer de standaardprojectcategorieën die voor elk transactietype moeten worden gebruikt. Deze standaardinstellingen worden gebruikt in **Integratiejournaal in Project Operations** en in schattingen waar geen transactiecategorie is gespecificeerd voor de werkelijke projectwaarden.
  - **Prognoses**: selecteer het prognosemodel dat moet worden gebruikt voor schattingen van tijd en onkosten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]