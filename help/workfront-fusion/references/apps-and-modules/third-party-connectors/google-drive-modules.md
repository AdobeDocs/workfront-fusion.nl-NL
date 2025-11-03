---
title: Google Drive-modules
description: De  [!DNL Adobe Workfront Fusion Google Drive]  modules laten u toe om te controleren, te zoeken, tot stand te brengen, bij te werken, te schrappen, en uw dossiers, omslag, of gedeelde aandrijving in uw  [!DNL Google Drive] te beheren.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1678'
ht-degree: 0%

---

# [!DNL Google Drive] modules

Met de Adobe Workfront Fusion [!DNL Google Drive] -modules kunt u uw bestanden, mappen of gedeelde stations in uw [!DNL Google Drive] controleren, zoeken, maken, bijwerken, verwijderen en beheren.

In een Adobe Workfront Fusion-scenario kunt u uw [!DNL Google Drive] -account verbinden met meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk Adobe Workfront Workflow-pakket en elk Adobe Workfront Automation and Integration-pakket</p><p>Workfront Ultimate</p><p>Workfront Prime en Select packages, met extra aanschaf van Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p><p>Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie</td> 
   <td>
   <p>Exploitatie gebaseerd: geen Workfront Fusion-licentievereisten</p>
   <p>Connectorgebaseerde (verouderde): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

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



## Verbinding maken [!DNL Google Drive] met Workfront Fusion

Als u [!DNL @gmail.com] of [!DNL @googlemail.com] gebruiker gebruikt, moet u een OAuth cliënt op [!DNL Google Cloud Platform] tot stand brengen om uw [!UICONTROL Client ID] en [!UICONTROL Client Secret] te verkrijgen.

Voor geleidelijke instructies op hoe te om de cliënt OAuth (en verkrijg [!UICONTROL Client ID] en [!UICONTROL Client Secret]) tot stand te brengen, zie [ de Fusie van Adobe Workfront van Connect aan  [!DNL Google Services]  gebruikend een douaneOAuth cliënt ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Voor instructies over het aansluiten van uw [!DNL Google Drive] rekening aan [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL Google Drive] modules en hun velden

Wanneer u [!DNL Google Drive] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Google Drive] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

* [[!UICONTROL Watch all files]](#watch-all-files)
* [[!UICONTROL Watch comments]](#watch-comments)
* [[!UICONTROL Watch files in folder]](#watch-files-in-folder)
* [[!UICONTROL Watch shared files]](#watch-shared-files)

#### [!UICONTROL Watch all files]

Deze triggermodule start een scènelijn wanneer een bestand in uw [!DNL Google Drive] wordt toegevoegd of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
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
   <td>Stel het maximumaantal resultaten in dat Workfront Fusion gedurende één cyclus zal downloaden (het aantal herhalingen per uitgevoerde scenario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comments]

Deze triggermodule start een scenario wanneer een opmerking wordt toegevoegd aan of gewijzigd in het geselecteerde bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
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
   <td>Stel het maximumaantal opmerkingen in dat Workfront Fusion gedurende één cyclus retourneert (het aantal herhalingen per uitgevoerde scenario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch files in folder]

Deze triggermodule start een scenario wanneer een bestand wordt toegevoegd of gewijzigd in de opgegeven map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
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
    <td>Stel het maximumaantal resultaten in dat Workfront Fusion gedurende één cyclus zal downloaden (het aantal herhalingen per uitgevoerde scenario).</td>
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
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
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
   <td>Stel het maximumaantal resultaten in dat Workfront Fusion gedurende één cyclus zal downloaden (het aantal herhalingen per uitgevoerde scenario).</td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Copy a file]](#copy-a-file)
* [[!UICONTROL Create a fFolder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Get a share link]](#get-a-share-link)
* [[!UICONTROL Move a file to trash]](#move-a-filefolder-to-trash)
* [[!UICONTROL Search for Files/Folders]](#search-for-filesfolders)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Upload a File]](#upload-a-file)

#### [!UICONTROL Copy a file]

Deze actiemodule kopieert een bestand naar de nieuwe locatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer de bestemming waarnaar u een bestand wilt kopiëren.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>Selecteer de map met het bestand dat u wilt kopiëren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u wilt kopiëren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the copy]</td> 
   <td>Voer een titel in voor het nieuwe bestand. Laat dit veld leeg als u de oorspronkelijke bestandsnaam niet wilt wijzigen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a folder]

Deze actiemodule maakt een map op de opgegeven locatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer de bestemming waar u een map wilt maken.</p> 
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

#### [!UICONTROL Delete a file]

Met deze actiemodule wordt een bestand of map permanent verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u wilt verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Deze actiemodule wint het dossier met gespecificeerde identiteitskaart terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
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

#### [!UICONTROL Get a share link]

Deze actiemodule haalt de koppeling voor delen voor een bestand op in Google Drive.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand waarvoor u de gedeelde koppeling wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a file to trash]

Met deze actiemodule verplaatst u een bestand of map naar de prullenbak.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u naar de prullenbak wilt verplaatsen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Files/Folders]

Deze zoekmodule zoekt naar bestanden of mappen op basis van zoekcriteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer het doelstation dat u wilt zoeken.</p> 
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
   <td>Stel het maximumaantal bestanden of mappen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td>Schakel deze optie in om ervoor te zorgen dat het scenario niet wordt gestopt als de module geen resultaten retourneert.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

Deze actiemodule werkt de metagegevens of inhoud van een bestand bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Selecteer de bestemming die het bestand bevat dat u wilt bijwerken.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Move to a folder]</td> 
   <td>Als u het bestand naar een specifieke map wilt verplaatsen, selecteert u de map waarnaar u het bestand wilt verplaatsen.</td> 
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
   <td>Als u de inhoud vervangt, selecteert u een bronbestand uit een vorige module of wijst u de naam en gegevens van het bronbestand toe.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Conver a file]</td> 
   <td>Schakel deze optie in om het bestand om te zetten in de corresponderende Google-bestandsindeling.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

Uploadt een bestand naar uw [!DNL Google Drive] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Google Drive] Verbinding maken <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref"> met [!DNL Google Drive] voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion</p> </td> 
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
   <td>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</td> 
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

## Problemen oplossen

### Kan een bestand niet uploaden of bijwerken

Er zijn verschillende redenen waarom het uploaden of bijwerken van een bestand mislukt:

* Het geüploade bestand is te groot en overschrijdt de maximale bestandsgrootte die is toegestaan voor uw [!DNL Google Drive] -abonnement of u hebt de opslaglimiet van [!DNL Google Drive] overschreden. U kunt uw opslagabonnement upgraden of bestaande bestanden verwijderen uit de service [!DNL Google Drive] .
* De geselecteerde map waarnaar het bestand moet worden geüpload, bestaat niet meer. In dit geval stopt het scenario en moet u een andere doelmap in de module selecteren.

<!-- Not present February 2025

## Search for files

In the module List files in a folder you can use your own query which consists of these parts:

* **[!UICONTROL Field]** - Attribute of the file that is being searched, for example, the attribute `name` of the file.

* **[!UICONTROL Operator]** - Test that is performed on the data to provide a match, for example, `contains`.

* **[!UICONTROL Value]** - The content of the attribute that is tested, for example, the name of the file `My cool document`.

Combine clauses with the conjunctions `and` or `or`, and negate the query with `not`.

* [Fields](#fields)
* [Value types](#value-types)
* [Operators](#operators)
* [Examples](#examples)

### Fields 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Field </th> 
   <th>Value Type </th> 
   <th>Operators</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Name of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Full text of the file including name, description, content, and indexable text.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME type of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date of the last modification to the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date that the user last viewed a file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Whether the file is in the trash or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Whether the file is starred or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Whether the [!UICONTROL parents] collection contains the specified ID.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who own the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to modify the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to read the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Files that are in the user's "Shared with me" collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Public custom file properties.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following about operators in these fields:

* The `contains` operator only performs prefix matching for a `title`.

   For example, the title "HelloWorld" matches for `title contains 'Hello'` but not for `title contains 'World'`.

* The `contains` operator only performs matching on entire string tokens for `fullText`.

   For example, if the full text of a doc contains the string "HelloWorld" only the query `fullText contains 'HelloWorld'` returns a result. Queries such as `fullText contains 'Hello'` would not return results in this scenario.

* The `contains` operator matches on an exact alphanumeric phrase if it is surrounded by double quotes.

   For example, if the `fullText` of a doc contains the string "Hello there world", then the query `fullText contains '"Hello there"'` returns a result, but the query `fullText contains '"Hello world"'` does not.

   Furthermore, because the search is alphanumeric, if the `fullText` of a doc contains the string "Hello_world", then the query `fullText contains '"Hello world"'` returns a result.

* Fields of `type` date are currently not comparable to each other, only to constant dates.

### Value types

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Value Type</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Surround with single quotes '. Escape single quotes in queries with <code>\'</code>, e.g.,<code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>or <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>RFC 3339 format, default timezone is UTC, e.g., <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operators

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>The content of one string is present in the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> The content of a string or boolean is equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> The content of a string or boolean is not equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> A date is earlier than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> A date is earlier than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> A date is later than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> A date is later than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>An element is contained within a collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Return files that match both clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Return files that match either clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Negates a search clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>A collection contains an element matching the parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

For compound clauses, you can use parentheses to group clauses together. For example:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` This search returns all files with an image or video MIME type that their last modification was after June 4, 2012. Because `and` and `or` operators are evaluated from left to right, without parentheses, the above example would return only images modified after June 4, 2012, but would return all videos, even those before June 4, 2012.

### Examples 

All examples on this page show the unencoded `<q>q</q>` parameter, where `title = 'hello'` is encoded as `title+%3d+%27hello%27`. Client libraries handle this encoding automatically.

* Search for files with the name "hello"
   <pre>title = 'hello'</pre>
* Search for folders using the folder-specific MIME type
   <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Search for files that are not folders
   <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Search for files with a name containing the words "hello" and "goodbye"
   <pre>title contains 'hello' and [!UICONTROL name] contains 'goodbye'</pre>
* Search for files with a name that does not contain the word "hello"
   <pre>not title contains 'hello'</pre>
* Search for files containing the word "hello" in the content
   <pre>fullText contains 'hello'</pre>
* Search for files not containing the word "hello" in the content
   <pre>not fullText contains 'hello'</pre>
* Search for files containing the exact phrase "hello world" in the content
   <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Search for files with a query containing the "\" character (e.g., "\authors")
   <pre>fullText contains '\\authors'</pre>
* Search for files writeable by the user `test@example.org`
   <pre>'test@example.org' in [!DNL writers]</pre>
* Search for the ID `1234567` in the `parents` collection. This finds all files and folders located directly in the folder whose ID is `1234567`.
   <pre>'1234567' in [!UICONTROL parents]</pre>
* Search for the alias ID `appDataFolder` in the `parents` collection. This finds all files and folders located directly under the [Application Data folder](https://developers.google.com/drive/api/v2/appdata).
   <pre>'appDataFolder' in parents</pre>
* Search for files writeable by the users `test@example.org` and `test2@example.org`
   <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Search for files containing the text "important" which are in the trash
   <pre>fullText contains 'important' and trashed = true</pre>
* Search for files modified after June 4th 2012
   <pre>modifiedDate > '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate > '2012-06-04T12:00:00-08:00'</pre>
* Search for files shared with the authorized user with "hello" in the name
   <pre>sharedWithMe and title contains 'hello'</pre>
* Search for files with a [custom file property](https://developers.google.com/drive/api/v2/properties) named `additionalID` with the value `8e8aceg2af2ge72e78`.
   <pre>properties has { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }</pre>

Source of this guide is [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).

-->
