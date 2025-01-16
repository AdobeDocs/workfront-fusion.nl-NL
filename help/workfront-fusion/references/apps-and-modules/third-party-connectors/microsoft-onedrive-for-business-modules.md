---
title: Microsoft OneDrive voor bedrijfsmodules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL Microsoft OneDrive for Business] gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 657bea46-064e-4333-8e86-81678bb1c3bd
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive for Business] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Microsoft OneDrive for Business] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Als u [!DNL Microsoft OneDrive for Business] met [!DNL Adobe Workfront Fusion] wilt gebruiken, hebt u een [!DNL Microsoft] -account nodig.

Voor instructies over het verbinden van uw [!DNL OneDrive for Business] rekening met [!DNL Workfront Fusion], zie [ een verbinding aan Adobe  [!DNL Workfront Fusion]  - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md) tot stand brengen



## De service [!DNL Microsoft OneDrive for Business] verbinden met [!DNL Workfront Fusion]

Voor instructies over het aansluiten van uw [!DNL Microsoft OneDrive for Business] rekening aan [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
>
>Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.

## [!DNL Microsoft OneDrive for Business] modules en hun velden

Wanneer u [!DNL Microsoft OneDrive for Business] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Microsoft OneDrive for Business] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

* [[!UICONTROL Watch files]](#watch-files)
* [[!UICONTROL Watch folders]](#watch-folders)

#### [!UICONTROL Watch files]

Deze triggermodule wordt geactiveerd wanneer een nieuw bestand wordt toegevoegd of bijgewerkt in een map die wordt gecontroleerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Drive ID]</p> </td> 
   <td> <p>Selecteer het station dat u wilt controleren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p> Selecteer de map die u wilt controleren. In een scenario kunt u slechts één map controleren.</p> <p>Tip: als u meerdere mappen wilt bijhouden, maakt u een onafhankelijk scenario voor elk van deze mappen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL I want to watch]</p> </td> 
   <td> <p>Selecteer of u nieuwe bestanden en alle wijzigingen wilt bekijken, of alleen nieuwe bestanden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned rows]</td> 
   <td> <p> Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch folders]

Deze triggermodule wordt geactiveerd wanneer een nieuwe map wordt toegevoegd aan de map die wordt gecontroleerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Drive ID]</p> </td> 
   <td> <p>Selecteer het station dat u wilt controleren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p> Selecteer de map die u wilt controleren. In een scenario kunt u slechts één map controleren.</p> <p>Tip: als u meerdere mappen wilt bijhouden, maakt u een onafhankelijk scenario voor elk van deze mappen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL I want to watch]</p> </td> 
   <td> <p>Selecteer of u nieuwe mappen en alle wijzigingen wilt bekijken, of alleen nieuwe mappen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned rows]</td> 
   <td> <p> Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Upload a file]](#upload-a-file)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a sharing link]](#get-a-sharing-link)

#### [!UICONTROL Upload a file]

Deze actiemodule uploadt een binair of tekstbestand naar een opgegeven map

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer het station waarnaar u een bestand wilt uploaden.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map in het station.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL If the file with the same name exists]</td> 
   <td> <p> Selecteer wat u wilt doen als een bestand met dezelfde naam als het bestand dat u probeert te uploaden al bestaat.</p> 
    <ul> 
     <li>[!UICONTROL Replace the existing file]</li> 
     <li>[!UICONTROL Rename the new file]</li> 
     <li>[!UICONTROL End with an error]</li> 
    </ul> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

Met deze actiemodule wordt het opgegeven bestand naar de prullenbak verplaatst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer het station waaruit u een bestand wilt verwijderen.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p>Voer de id in van het bestand dat u wilt verwijderen. </p> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Deze actiemodule haalt het bestand met de opgegeven id op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer het station waarvan u een bestand wilt ophalen.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p>Voer de id in van het bestand dat u wilt ophalen. </p> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a folder]

Maakt een map in de opgegeven bovenliggende map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><strong>[!UICONTROL Connection]</strong> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Drive ID]</strong> </td> 
   <td> <p>Selecteer het station waarop u een nieuwe map wilt maken.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Folder]</strong> </td> 
   <td> <p>Selecteer de map waarin u een nieuwe map wilt maken.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Folder name]</strong> </td> 
   <td>Voer een naam voor de nieuwe map in of wijs deze toe.</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer het station waaruit u een bestand wilt verwijderen.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td> <p>Voer de id in van de map die u wilt verwijderen of wijs deze toe. </p> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a sharing link]

Deze module wint een verbinding terug die u kunt delen om toegang tot het gespecificeerde dossier te verlenen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Selecteer het station waarnaar u een bestand wilt uploaden.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enter]</td> 
   <td> <p>Selecteer of u een bestand wilt kiezen met de bestands-id of het bestandspad. Voer de bestands-id of het pad in het veld in dat wordt weergegeven.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permission type]</p> </td> 
   <td> <p>Selecteer of u wilt dat personen die de koppeling ontvangen, lees- en schrijfmachtigingen hebben of alleen-lezen.</p> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Scope]</td> 
   <td> <p> Selecteer of u het bestand toegankelijk wilt maken voor iedereen die over de koppeling beschikt of alleen toegankelijk wilt zijn voor leden van uw organisatie.</p> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>
