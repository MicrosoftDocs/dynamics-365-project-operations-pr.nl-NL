---
title: Aangepaste oplossingen maken voor prijsdimensies
description: In dit onderwerp wordt uitgelegd hoe u een aangepaste oplossing kunt maken bij het maken van aangepaste prijsdimensies.
author: Rumant
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284982"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Aangepaste oplossingen maken voor prijsdimensies

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Alle wijzigingen in aangepaste prijsdimensies moeten in een aparte oplossing plaatsvinden. Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren. Nadat u de vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.

1. Selecteer **Instellingen** > **Oplossingen** en selecteer vervolgens **Nieuw**. 
2. Noem de oplossing **\<your organization name> prijsdimensies**, voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.

> ![Een aangepaste oplossing maken voor prijsdimensies](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Alle vereiste entiteiten en gerelateerde onderdelen toevoegen aan de oplossing Prijsdimensie
U moet de volgende Project Service-entiteiten toevoegen aan uw prijsoplossing. Voltooi de stappen in deze procedure om een aantal belangrijke schemawijzigingen in de prijsoplossing door te voeren, zodat de entiteiten de nieuwe prijsdimensies opmerken.

1. Selecteer de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**. 
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.
3. Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:

- Actueel
- Boekbare resource
- Schattingsregel
- Projecttaak
- Factuurregeldetail
- Journaalregel
- Detail van projectcontractregels
- Projectteamlid
- Details prijsopgaveregel
- Opslag voor rolprijs
- Rolprijs 
- Tijdsvermelding 

> ![Bestaande entiteiten toevoegen aan de oplossing voor prijsdimensies](media/Existing-entities-to-PD-solution.png)

> ![Oplossingsonderdelen selecteren](media/Dimension-Components.png)

> [!NOTE]
> Zorg ervoor dat alle formulieren en weergaven voor elk van de geselecteerde entiteiten worden opgenomen.

4. Wanneer u wordt gevraagd of u eventuele afhankelijke entiteiten voor de hierboven geselecteerde entiteiten wilt opnemen, selecteert u **Nee**.

> ![Niet alle gerelateerde onderdelen opnemen](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]