---
title: De installatie van Dynamics 365 Project Operations ongedaan maken
description: Dit artikel bevat informatie over hoe het verwijderen van Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911958"
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
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Sla deze oplossing over als deze niet wordt gevonden.                                                            |
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
