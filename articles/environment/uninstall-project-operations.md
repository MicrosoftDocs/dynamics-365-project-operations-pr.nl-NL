---
title: De installatie van Dynamics 365 Project Operations ongedaan maken
description: Dit onderwerp biedt informatie over de manier waarop u Dynamics 365 Project Operations kunt verwijderen.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783637"
---
# <a name="uninstall-dynamics-365-project-operations"></a>De installatie van Dynamics 365 Project Operations ongedaan maken 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Als u Dynamics 365 Project Operations wilt verwijderen, moet u de rol Beheerder krijgen.

1. Ga naar **Instellingen** > **Oplossingen**.

    ![De pagina Instellingen.](./media/uninstall-proj-ops-solutions.png)
  
2. Verwijder de oplossingen in de exacte volgorde waarin ze in de volgende tabel worden vermeld. 

    | Stap | Oplossingsnaam                                    | Opmerking                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 0 | msdyn_ProjectServiceUpgrade_managed.cab            | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 2 | ProjectOperations_Anchor                           | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 5 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 5 | ProjectService                                     | Geen aanvullende opmerkingen.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Geen aanvullende opmerkingen.                                                                         |
    | 7 | ProjectServiceCore                                 | Geen aanvullende opmerkingen.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 9 | FieldServiceCommon                                 | Vereist voor twee keer wegschrijven met Dynamics 365 Finance of Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Vereist voor twee keer wegschrijven met Dynamics 365 Finance of Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Vereist voor Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Vereist voor Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Vereist voor Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Vereist voor Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Vereist voor Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Vereist voor Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Vereist voor Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 19 | Dynamics365Notes                                   | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 21 | DualWriteCore                                      | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 23 | Dynamics365AssetManagement                         | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 26 | HCMCommon                                          | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 28 | Partij                                              | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 29 | Dynamics365Company                                 | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 30 | CurrencyExchangeRates                              | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
    | 31 | AssetCommon                                        | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
