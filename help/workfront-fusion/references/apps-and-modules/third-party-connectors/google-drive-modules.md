---
title: Google Drive-modules
description: De  [!DNL Adobe Workfront Fusion Google Drive]  modules laten u toe om te controleren, te zoeken, tot stand te brengen, bij te werken, te schrappen, en uw dossiers, omslag, of gedeelde aandrijving in uw  [!DNL Google Drive] te beheren.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2489'
ht-degree: 0%

---

# [!DNL Google Drive] modules

Met de modules [!DNL Adobe Workfront Fusion] [!DNL Google Drive] kunt u uw bestanden, mappen of gedeelde stations in uw [!DNL Google Drive] controleren, zoeken, maken, bijwerken, verwijderen en beheren.

In een [!DNL Adobe Workfront Fusion] -scenario kunt u uw [!DNL Google Drive] -account verbinden met meerdere toepassingen en services van derden.

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

## Informatie over Google Drive API

De Google Drive-aansluiting gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://www.googleapis.com/drive/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v4.1.2</td> 
  </tr>
 </tbody> 
 </table>



## Verbinding maken [!DNL Google Drive] met [!DNL Workfront Fusion]

Als u [!DNL @gmail.com] of [!DNL @googlemail.com] gebruiker bent moet u een cliënt OAuth op [ tot stand brengen  [!DNL Google Cloud Platform] ](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) om [!UICONTROL Client ID] en [!UICONTROL Client Secret] te verkrijgen.

Voor geleidelijke instructies op hoe te om tot de cliënt OAuth (en verkrijg [!UICONTROL Client ID] en [!UICONTROL Client Secret]) te leiden, zie [  [!DNL Adobe Workfront Fusion]  verbinden  [!DNL Google Services]  gebruikend een cliënt van douaneOAuth ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Voor instructies over het aansluiten van uw [!DNL Google Drive] rekening aan [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL Google Drive] modules en hun velden

Wanneer u [!DNL Google Drive] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Google Drive] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

* [[!UICONTROL Watch Files In Folder]](#watch-files-in-folder)
* [[!UICONTROL Watch All Files]](#watch-all-files)
* [[!UICONTROL Watch shared files]](#watch-shared-files)
* [[!UICONTROL Watch Comments]](#watch-comments)

#### [!UICONTROL Watch Files In Folder]

Hiermee worden de bestandsgegevens opgehaald wanneer een bestand in de opgegeven map wordt toegevoegd of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Select the folder to be watched]</td>
    <td >Selecteer de map op uw station waarin u de bestanden wilt bekijken.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL What files to watch]</td>
   <td> <p>Selecteer het type bestanden dat u wilt bekijken.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Documents] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Spreadsheets] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Slides] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Drawings] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Watch]</td>
    <td>Selecteer of u nieuwe bestanden en alle wijzigingen, of alleen nieuwe bestanden wilt bekijken.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Maximum number of downloaded files]</td>
    <td>Stel het maximumaantal resultaten in dat [!DNL Workfront Fusion] gedurende één cyclus downloadt (het aantal herhalingen per uitgevoerde scenario).</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch All Files]

Hiermee worden de bestandsgegevens opgehaald wanneer een bestand in uw [!DNL Google Drive] wordt toegevoegd of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>Selecteer het type bestanden dat u wilt bekijken.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Documents] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Spreadsheets] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Slides] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Drawings] wilt converteren.</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Selecteer of u nieuwe bestanden en alle wijzigingen, of alleen nieuwe bestanden wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>Stel het maximumaantal resultaten in dat [!DNL Workfront Fusion] gedurende één cyclus downloadt (het aantal herhalingen per uitgevoerde scenario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch shared files]

Triggers wanneer een nieuw dossier aan u wordt gedeeld, of een bestaand gedeeld dossier wordt bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select the folder to be watched]</td> 
   <td>Selecteer de gedeelde map waarin u de bestanden wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>Selecteer het type bestanden dat u wilt bekijken.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Documents] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Spreadsheets] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Slides] wilt converteren.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] bestanden om op te maken]</td>
    <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Drawings] wilt converteren.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Selecteer of u nieuwe bestanden en alle wijzigingen, of alleen nieuwe bestanden wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>Stel het maximumaantal resultaten in dat [!DNL Workfront Fusion] gedurende één cyclus downloadt (het aantal herhalingen per uitgevoerde scenario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comments]

Triggert wanneer een opmerking wordt toegevoegd of gewijzigd aan het geselecteerde bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File]</td> 
   <td>Selecteer het bestand dat u wilt controleren voor opmerkingen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Selecteer of u alle wijzigingen wilt controleren of alleen voor nieuwe opmerkingen</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned comments]</td> 
   <td>Stel het maximumaantal opmerkingen in dat [!DNL Workfront Fusion] gedurende één cyclus retourneert (het aantal herhalingen per uitgevoerde scenario).</td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Upload a File]](#upload-a-file)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File]](#delete-a-file)
* [[!UICONTROL Move a File/Folder to Trash]](#move-a-filefolder-to-trash)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Search for Files/Folders]](#search-for-filesfolders)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Get a share link]](#get-a-share-link)

#### [!UICONTROL Upload a File]

Uploadt een bestand naar uw [!DNL Google Drive] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Destination]</td> 
   <td> <p>Selecteer de bestemming waarnaar u een bestand wilt uploaden.</p> 
    <ul> 
     <li>[!DNL My Drive]</li> 
     <li>[!DNL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>Selecteer de map waarnaar u een bestand wilt uploaden. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>Selecteer of u een dossier wilt gebruiken dat van een vorige module wordt overgegaan, of als u het dossier manueel in kaart wilt brengen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>Selecteer de bestandsnaam. Deze optie is beschikbaar als u "[!UICONTROL Map]"op het [!UICONTROL source file] gebied selecteert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>Selecteer het gegevensbestand dat u wilt uploaden. Deze optie is beschikbaar als u "[!UICONTROL Map]"op het [!UICONTROL source file] gebied selecteert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>Voer een titel in voor het nieuwe bestand.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a file]</td> 
   <td>Als u deze optie inschakelt, kan de module bestanden converteren naar de corresponderende [!DNL Google] -indeling.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

De metagegevens of inhoud van een bestand wordt bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer de bestemming waarnaar u een bestand wilt uploaden.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Move to a folder]</td> 
   <td>Als u het bestand naar een andere map wilt verplaatsen, selecteert u de map waarnaar u het bestand wilt verplaatsen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>Voer een titel in voor het bijgewerkte bestand.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Change a file content]</td> 
   <td>Selecteer of u de inhoud van het bestand wilt vervangen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>Selecteer of u een dossier wilt gebruiken dat van een vorige module wordt overgegaan, of als u het dossier manueel in kaart wilt brengen. Dit veld is beschikbaar als u de inhoud van het bestand in het vorige veld wilt wijzigen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>Selecteer de bestandsnaam. Deze optie is beschikbaar als u "[!UICONTROL Map]"op het [!UICONTROL source file] gebied selecteert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>Selecteer het gegevensbestand dat u wilt uploaden. Deze optie is beschikbaar als u "[!UICONTROL Map]"op het [!UICONTROL source file] gebied selecteert.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

Hiermee wordt een bestand naar de nieuwe locatie gekopieerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer de bestemming waarnaar u een bestand wilt uploaden.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>Selecteer de map waarin het bestand dat u wilt kopiëren zich bevindt/</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the copy]</td> 
   <td>Voer een titel in voor het nieuwe bestand. Laat dit veld leeg als u de oorspronkelijke bestandsnaam niet wilt wijzigen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

Hiermee verwijdert u een bestand of map definitief.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u wilt verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder to Trash]

Hiermee verplaatst u een bestand of map naar de prullenbak.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u naar de prullenbak wilt verplaatsen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Hiermee wordt het bestand met de opgegeven id opgehaald.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] bestanden om op te maken]</td> 
   <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Documents] wilt converteren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Spreadsheets] bestanden om op te maken]</td> 
   <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Spreadsheets] wilt converteren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] bestanden om op te maken]</td> 
   <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Slides] wilt converteren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] bestanden om op te maken]</td> 
   <td>Selecteer de bestandsindeling waarnaar u [!DNL Google Drawings] wilt converteren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Files/Folders]

Hiermee zoekt u bestanden of mappen op basis van zoekcriteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer het doel dat u wilt zoeken.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL List a folder]</td> 
   <td>Navigeer naar de map waarnaar u de bestanden of mappen wilt zoeken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td> <p> Selecteer of u naar bestanden, mappen of beide wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Search]</p> </td> 
   <td> <p>Selecteer het type zoekopdracht dat u wilt uitvoeren.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search within file/folder names]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Voer een deel van de bestandsnaam of de volledige bestandsnaam (inclusief het achtervoegsel) in waarnaar u wilt zoeken.</p> </li> 
       <li> <p><strong>[!UICONTROL Search Options]</strong> </p> <p>Selecteer of u naar de nauwkeurige termijn wilt zoeken, of als u naar namen wilt zoeken die de onderzoekstermijn bevatten.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Fulltext] search </strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Voer een zoekterm in die u in de [!DNL Google Drive] wilt zoeken.</p> </li> 
      </ul> </li> 
     <li> <p><strong> ga de vraag van het douaneonderzoek </strong> in </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Voer de aangepaste zoekquery in. Raadpleeg de sectie [!UICONTROL Search for Files] van dit artikel voor meer informatie.</p> </li> 
       <li> <p><strong> voegt de omslag hierboven aan de vraag </strong> wordt geselecteerd toe </p> <p>Zoekt naar de map in de bovenliggende verzameling. Alle bestanden en mappen in de hierboven geselecteerde map worden gevonden.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td>Stel het maximumaantal bestanden of mappen in dat [!DNL Workfront Fusion] tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td>Schakel deze optie in om ervoor te zorgen dat het scenario niet wordt gestopt als de module geen resultaten retourneert.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Maakt een map op de opgegeven locatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer de bestemming waarnaar u een bestand wilt uploaden.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New folder location]</td> 
   <td>Navigeer naar de locatie waar u een nieuwe map wilt maken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the new folder]</td> 
   <td>Voer een naam in voor de map die u maakt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Share folder]</td> 
   <td>Selecteer deze optie als u de map wilt delen met iedereen met de koppeling [!UICONTROL Share] . Anders is de deelkoppeling alleen voor de eigenaar.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a share link]

Hiermee wordt de koppeling voor delen van een bestand opgehaald in Google Drive.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Google Drive] met [!UICONTROL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Google Drive] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand waarvoor u de gedeelde koppeling wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

## Problemen oplossen

### Kan een bestand niet uploaden of bijwerken

Er zijn verschillende situaties wanneer het uploaden of bijwerken van een bestand mislukt:

* Het geüploade bestand is te groot en overschrijdt de maximale bestandsgrootte die is toegestaan voor uw [!DNL Google Drive] -abonnement of u hebt de opslaglimiet van [!DNL Google Drive] overschreden. U kunt uw opslagabonnement upgraden of bestaande bestanden verwijderen uit de service [!DNL Google Drive] .
* De geselecteerde map waarnaar het bestand moet worden geüpload, bestaat niet meer. Het scenario stopt en het is dan nodig om opnieuw een doelmap te selecteren.

## Bestanden zoeken

In de dossiers van de Lijst van de module in een omslag kunt u uw eigen vraag gebruiken die uit deze delen bestaat:

* **[!UICONTROL Field]** - Kenmerk van het bestand dat wordt doorzocht, bijvoorbeeld het kenmerk `name` van het bestand.

* **[!UICONTROL Operator]** - Test die op de gegevens wordt uitgevoerd om een overeenkomst te leveren, bijvoorbeeld `contains` .

* **[!UICONTROL Value]** - De inhoud van het kenmerk dat wordt getest, bijvoorbeeld de naam van het bestand `My cool document` .

Combineer clausules met de conjunctions `and` of `or`, en ontken de vraag met `not`.

* [Velden](#fields)
* [Waardetypen](#value-types)
* [Operatoren](#operators)
* [Voorbeelden](#examples)

### Velden

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Veld </th> 
   <th>Type waarde </th> 
   <th>Operatoren</th> 
   <th> <p> Beschrijving</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup> 1 </sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Naam van het bestand.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup> 2, 3 </sup> </td> 
   <td> <p> Volledige tekst van het bestand, inclusief naam, beschrijving, inhoud en indexeerbare tekst.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME-type van het bestand.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> datum <sup> 4 </sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Datum van de laatste wijziging in het bestand.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> datum <sup> 4 </sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> De datum waarop de gebruiker het laatst een bestand heeft bekeken.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Of het bestand zich in de prullenbak bevindt of niet.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Geeft aan of het bestand is gestart of niet.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collectie </td> 
   <td><code>in </code> </td> 
   <td> <p>Geeft aan of de [!UICONTROL parents] -verzameling de opgegeven id bevat.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collectie </td> 
   <td><code>in </code> </td> 
   <td> <p>Gebruikers die eigenaar zijn van het bestand.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collectie </td> 
   <td><code>in </code> </td> 
   <td> <p>Gebruikers die gemachtigd zijn om het bestand te wijzigen.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collectie </td> 
   <td><code>in </code> </td> 
   <td> <p>Gebruikers die gemachtigd zijn het bestand te lezen.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Bestanden in de collectie "Gedeeld met mij" van de gebruiker.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collectie</td> 
   <td><code>has </code> </td> 
   <td> <p> Eigenschappen van aangepaste openbare bestanden.</p> </td> 
  </tr> 
 </tbody> 
</table>

Overweeg het volgende over exploitanten op deze gebieden:

* De operator `contains` voert alleen overeenkomende voorvoegsels uit voor een `title` .

  De titel &#39;HelloWorld&#39; komt bijvoorbeeld overeen met `title contains 'Hello'` maar niet met `title contains 'World'` .

* De operator `contains` voert alleen overeenkomende bewerkingen uit op hele tekenreeksen voor `fullText` .

  Als bijvoorbeeld de volledige tekst van een document de tekenreeks &quot;HelloWorld&quot; bevat, retourneert de query `fullText contains 'HelloWorld'` alleen een resultaat. Zoekopdrachten als `fullText contains 'Hello'` resulteren niet in dit scenario.

* De operator `contains` komt overeen met een exacte alfanumerieke uitdrukking als deze wordt omringd door dubbele aanhalingstekens.

  Als de `fullText` van een document bijvoorbeeld de tekenreeks &quot;Hello there world&quot; bevat, retourneert de query `fullText contains '"Hello there"'` een resultaat, maar de query `fullText contains '"Hello world"'` niet.

  Omdat de zoekopdracht alfanumeriek is en de `fullText` van een document de tekenreeks &quot;Hello_world&quot; bevat, retourneert de query `fullText contains '"Hello world"'` bovendien een resultaat.

* Velden met de datum `type` zijn momenteel niet met elkaar vergelijkbaar, alleen met constante datums.

### Waardetypen

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Type waarde</th> 
   <th> <p> Notities</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Omgeven met enkele aanhalingstekens '. Escape enkele aanhalingstekens in query's met <code>\'</code>, bijvoorbeeld <code> 'Valentine\'s Day'</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>of <code>false</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>Datum </td> 
   <td> <p>RFC 3339-indeling, de standaardtijdzone is UTC, bijvoorbeeld <code>2012-06-04T12:00:00-08:00</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operatoren

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notities</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>De inhoud van de ene tekenreeks staat in de andere.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> De inhoud van een tekenreeks of Booleaanse waarde is gelijk aan de andere.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> De inhoud van een tekenreeks of Booleaanse waarde is niet gelijk aan de andere tekenreeks.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> Een datum is eerder dan een andere datum.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> Een datum is eerder dan of gelijk aan een andere datum.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> Een datum is later dan een andere datum.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> Een datum is later dan of gelijk aan een andere datum.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>Een element is bevat binnen een inzameling.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Retourbestanden die overeenkomen met beide clausules.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Retourbestanden die overeenkomen met een van beide componenten.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Hiermee wordt een zoekclausule genegeerd.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>Een verzameling bevat een element dat overeenkomt met de parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

Voor samengestelde clausules, kunt u haakjes gebruiken om clausules samen te groeperen. Bijvoorbeeld:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` Met deze zoekopdracht worden alle bestanden geretourneerd met een MIME-type voor afbeeldingen of video die de laatste wijziging na 4 juni 2012 heeft ondergaan. Omdat `and` - en `or` -operatoren van links naar rechts worden geëvalueerd, zonder haakjes, retourneert het bovenstaande voorbeeld alleen afbeeldingen die na 4 juni 2012 zijn gewijzigd, maar retourneert het alle video&#39;s, zelfs die voor 4 juni 2012.

### Voorbeelden

Alle voorbeelden op deze pagina tonen de niet-gecodeerde `<q>q</q>` parameter, waarbij `title = 'hello'` als `title+%3d+%27hello%27` wordt gecodeerd. Clientbibliotheken verwerken deze codering automatisch.

* Bestanden zoeken met de naam &quot;hello&quot;
  <pre>title = 'hello'</pre>
* Mappen zoeken met het mapspecifieke MIME-type
  <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Zoeken naar bestanden die geen mappen zijn
  <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Zoeken naar bestanden met een naam die de woorden &quot;hello&quot; en &quot;goodbye&quot; bevat
  <pre>title bevat 'hello' en [!UICONTROL name] bevat 'goodbye'</pre>
* Bestanden zoeken met een naam die niet het woord &quot;hello&quot; bevat
  <pre>geen titel bevat 'hello'</pre>
* Zoeken naar bestanden met het woord &quot;hello&quot; in de inhoud
  <pre>fullText bevat 'hello'</pre>
* Zoeken naar bestanden zonder het woord &quot;hello&quot; in de inhoud
  <pre>not fullText contains 'hello'</pre>
* Zoeken naar bestanden met de exacte uitdrukking &quot;hello world&quot; in de inhoud
  <pre>fullText bevat '"hello world"'fullText bevat '"hello_world"'</pre>
* Bestanden zoeken met een query die het teken &quot;\&quot; bevat (bijvoorbeeld &quot;\authors&quot;)
  <pre>fullText bevat '\\authors'</pre>
* Zoeken naar bestanden die door de gebruiker kunnen worden geschreven `test@example.org`
  <pre>'test@example.org' in [!DNL writers]</pre>
* Zoek de id `1234567` in de `parents` -verzameling. Hiermee worden alle bestanden en mappen gevonden die zich direct in de map met de id `1234567` bevinden.
  <pre>'1234567' in [!UICONTROL parents]</pre>
* Zoek naar alias identiteitskaart `appDataFolder` in de `parents` inzameling. Dit vindt alle dossiers en omslagen die direct onder de [ omslag van Gegevens van de Toepassing ](https://developers.google.com/drive/api/v2/appdata) worden gevestigd.
  <pre>'appDataFolder' in bovenliggende items</pre>
* Zoeken naar bestanden die kunnen worden geschreven door de gebruikers `test@example.org` en `test2@example.org`
  <pre>'test@example.org' in schrijvers en 'test2@example.org' in schrijvers</pre>
* Zoeken naar bestanden met de tekst &quot;belangrijk&quot; die zich in de prullenbak bevinden
  <pre>fullText bevat 'main' en traped = true</pre>
* Bestanden zoeken die na 4 juni 2012 zijn gewijzigd
  <pre>modifiedDate &gt; "2012-06-04T12 :00: 00"// de standaardtijdzone is UTC</pre><pre>modifiedDate &gt; "2012-06-04T12 :00: 00-08:00"</pre>
* Bestanden zoeken die met de geautoriseerde gebruiker worden gedeeld met &quot;hello&quot; in de naam
  <pre>sharedWithMe en title bevat 'hello'</pre>
* Onderzoek naar dossiers met het bezit van het a [ douanedossier ](https://developers.google.com/drive/api/v2/properties) genoemd `additionalID` met de waarde `8e8aceg2af2ge72e78`.
  <pre>eigenschappen hebben { key='additionalID' en value='8e8aceg2af2ge72e78' en visibility='PRIVATE' }</pre>

Source van deze gids is [[!DNL Google Drive]  documentatie ](https://developers.google.com/drive/api/v2/search-shareddrives).
