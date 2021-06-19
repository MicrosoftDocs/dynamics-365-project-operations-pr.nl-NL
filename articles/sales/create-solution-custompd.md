---
title: Een oplossing maken voor aangepaste prijsdimensies
description: Dit onderwerp bevat informatie over het maken van oplossingen voor aangepaste prijsdimensies.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010330"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Een oplossing maken voor aangepaste prijsdimensies

 _**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_ 

>[!IMPORTANT]
>Alle wijzigingen in aangepaste prijsdimensies moeten in een aparte oplossing plaatsvinden. Deze belangrijke aanbevolen procedure biedt flexibiliteit om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar andere exemplaren te publiceren. Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren voor hergebruik.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Een oplossing maken voor aangepaste prijsdimensies

1.  Selecteer **Instellingen** > **Oplossingen** en selecteer vervolgens **Nieuw**.
2.  Noem de oplossing *prijsdimensies <your organization name>*.
3. Geef de overige vereiste gegevens op en selecteer vervolgens **Opslaan**.

  ![Oplossing maken voor aangepaste prijsdimensies](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Alle vereiste entiteiten en gerelateerde onderdelen toevoegen aan de oplossing Prijsdimensie

Voeg de volgende Project Service-entiteiten toe aan uw prijsoplossing om belangrijke schemawijzigingen in de prijsoplossing aan te brengen. Nadat u deze procedure hebt voltooid, zullen de entiteiten de nieuwe prijsdimensies herkennen.

1.  Selecteer **Instellingen** > **Oplossingen** en dubbelklik vervolgens op de **<*naam van uw organisatie*> prijsdimensies**.
2.  Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.
3.  Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:
 
   - **Actueel**
   - **Boekbare resource**
   - **Schattingsregel**
   - **Projecttaak**
   - **Factuurregeldetail**
   - **Journaalregel**
   - **Detail van projectcontractregels**
   - **Projectteamlid**
   - **Details prijsopgaveregel**
   - **Opslag voor rolprijs**
   - **Rolprijs**
   - **Tijdsvermelding**
 
   ![Aangepaste oplossing voor prijsdimensies voor bestaande entiteiten toevoegen](./media/Existing-entities-to-PD-solution.png)
 
 4. Bekijk voor elke entiteit de componenten die worden toegevoegd en de definitieve lijst met entiteitsactiva voor elke entiteit. 

   >[!NOTE]
   > Neem alle formulieren en weergaven voor elk van de geselecteerde entiteiten op.

  ![Toegevoegde entiteiten](./media/solution-component-selection.png)


5.  Wanneer u wordt gevraagd om afhankelijke entiteiten voor de geselecteerde entiteiten op te nemen, selecteert u **Nee, neem geen vereiste componenten op.**

    ![Inclusief afhankelijke entiteiten](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]