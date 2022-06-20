---
title: Demogegevens toepassen op een Finance-cloudomgeving
description: In dit artikel wordt uitgelegd hoe u demogegevens van Project Operations toepast op een door Dynamics 365 Finance Cloud gehoste omgeving.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 4ce53c171929f0610c53025becaebea46d902c90
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924654"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Demogegevens toepassen op een Finance-cloudomgeving

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

> [!IMPORTANT]
> Dit artikel is alleen van toepassing op Microsoft Dynamics 365 Finance versie 10.0.13 en kan alleen worden uitgevoerd op een door de cloud gehoste omgeving. Voltooi de stappen in dit artikel **VOORDAT** u kwaliteitsupdates toepast op de omgeving.

1. Open in uw LCS-project de pagina **Omgevingsdetails**. Deze bevat de details bevat die nodig zijn om verbinding te maken met de omgeving met behulp van Remote Desktop Protocol (RDP).

![Omgevingsdetails.](./media/1EnvironmentDetails.png)

De eerste set gemarkeerde referenties zijn de referenties van het lokale account en bevatten een hyperlink naar de externe desktopverbinding. De inloggegevens omvatten de gebruikersnaam en het wachtwoord van de omgevingsbeheerder. De tweede set referenties wordt gebruikt om in deze omgeving in te loggen op SQL Server.

2. Maak verbinding met de omgeving via de hyperlink in **Lokale accounts** en gebruik de **Lokale accountreferenties** voor de verificatie.
3. Ga naar **Internet Information Services** > **Toepassingsgroepen** > **AOSService** en stop de service. U stopt de service op dit punt, zodat u kunt doorgaan met het vervangen van de SQL-database.

![AOS stoppen.](./media/2StopAOS.png)

4. Ga naar **Services** en stop de volgende twee items:

- Microsoft Dynamics 365 Unified Operations: Batchbeheerservice
- Microsoft Dynamics 365 Unified Operations: Raamwerk voor gegevensimport/-export

![Services stoppen.](./media/3StopServices.png)

5. Open Microsoft SQL Server Management Studio. Log in met SQL-serverreferenties en gebruik de axdbadmin-gebruiker en het wachtwoord van de LCS-pagina **Omgevingsdetails**.

![SQL Server Management Studio.](./media/4SSMS.png)

6. Zoek in Object Explorer **Databases** naar **AXDB**. U vervangt de database door een nieuwe database in het [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopieer het zipbestand naar de virtuele machine waarmee u op afstand verbinding hebt en pak de zipinhoud uit.
8. Klik met de rechtermuisknop in SQL Server Management Studio op **AxDB** en selecteer **Taken** > **Herstellen** > **Database**.

![Database herstellen.](./media/5RestoreDatabase.png)

9. Selecteer **Bronapparaat** en navigeer naar het bestand dat is geëxtraheerd uit de zip die u hebt gekopieerd.

![Bronapparaten.](./media/6SourceDevice.png)

10. Selecteer **Opties** en vervolgens **De bestaande database overschrijven** en **Bestaande verbindingen met de doeldatabase sluiten**. 
11. Selecteer **OK**.

![Instellingen herstellen.](./media/7RestoreSetting.png)

U ontvangt een bevestiging dat de AXDB-herstelbewerking is gelukt. Nadat u deze bevestiging hebt ontvangen, kunt u SQL Services Management Studio sluiten.

12. Ga terug naar **Internet Information Services** > **Toepassingsgroepen** > **AOSService** en start de AOSService.
13. Ga naar **Services** en start de twee services die u eerder stopte.

14. Zoek het hulpprogramma AdminUserProvisioning op deze VM. Kijk onder K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Voer het .ext-bestand uit met uw gebruikersadres in het veld **E-mailadres**. 
16. Selecteer **Verzenden**.

![Gebruiker met beheerdersrechten inrichten.](./media/8AdminUserProvisioning.png)

Dit duurt een paar minuten. U ontvangt een bevestigingsbericht dat de gebruiker met beheerdersrechten met succes is bijgewerkt.

17. Voer ten slotte de opdrachtprompt uit als Beheerder en voer iisreset uit

![IIS opnieuw instellen.](./media/9IISReset.png)

18. Sluit de externe bureaubladsessie en gebruik de LCS-pagina **Omgevingsdetails** om in te loggen op de omgeving en te bevestigen dat deze werkt zoals verwacht.

![Financën en bedrijfsactiviteiten.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]