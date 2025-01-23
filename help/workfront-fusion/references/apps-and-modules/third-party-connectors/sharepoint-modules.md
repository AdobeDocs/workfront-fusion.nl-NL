---
title: SharePoint-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die SharePoint gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2270'
ht-degree: 0%

---

# [!DNL SharePoint] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL SharePoint] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Als u [!DNL SharePoint] -modules wilt gebruiken, moet u een [!DNL SharePoint] -account hebben.

## SharePoint API-informatie

De SharePoint-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL SharePoint] met [!DNL Workfront Fusion] {#connect-sharepoint-to-workfront-fusion}

* [Verbind  [!DNL SharePoint]  met  [!DNL Workfront Fusion]  gebruikend a [!DNL Microsoft]  rekening](#connect-sharepoint-to-workfront-fusion-using-a-microsoft-account)
* [Verbind  [!DNL SharePoint]  met  [!DNL Workfront Fusion]  gebruikend geavanceerde montages](#connect-sharepoint-to-workfront-fusion-using-advanced-settings)

### Verbind [!DNL SharePoint] met [!DNL Workfront Fusion] via een [!DNL Microsoft] -account

Met uw [!DNL Microsoft] -account kunt u een verbinding maken met [!DNL SharePoint] . Voor instructies over het verbinden van uw [!DNL Sharepoint] rekening met [!DNL Workfront Fusion], zie [ een verbinding tot stand brengen  [!DNL Adobe Workfront Fusion]  - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Verbind [!DNL SharePoint] met [!DNL Workfront Fusion] gebruikend geavanceerde montages

Als u [!DNL SharePoint] wilt verbinden met [!DNL Workfront Fusion] zonder een [!DNL Microsoft] -account, hebt u een client-id, clientgeheim en huurnummer-id nodig.

1. Klik op **[!UICONTROL Add]** boven in het vak **[!DNL SharePoint]** om het vak **[!UICONTROL Create a connection]** te openen.

1. (Optioneel) Wijzig de standaardinstelling **[!UICONTROL Connection name]** .
1. Klik op **[!UICONTROL Show advanced settings]**.
1. Voer [!DNL SharePoint] **[!UICONTROL Client ID]** en **[!UICONTROL Client Secret]** in.

1. Klik op **[!UICONTROL Continue]**.
1. Voer in het aanmeldingsvenster dat wordt weergegeven uw aanmeldingsgegevens in om u aan te melden bij de app als u dat nog niet hebt gedaan.
1. (Voorwaardelijk) Als een knop **[!UICONTROL Allow]** wordt weergegeven, klikt u op de knop om de app te verbinden met [!DNL Workfront Fusion] .

## [!DNL SharePoint] modules en hun velden

Wanneer u [!DNL SharePoint] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL SharePoint] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Drive-item](#drive-item)
* [Item](#item)
* [Lijst](#list)
* [Pagina (Beta)](#page-beta)
* [Site](#site)
* [Overige](#other)

### Drive-item

* [Een bestand maken](#create-a-file)
* [Een map maken](#create-a-folder)
* [Een bestand ophalen](#get-a-file)
* [Mapitems controleren](#watch-folder-items)

#### Wijzigingen ophalen

Deze module retourneert wijzigingen die zijn aangebracht in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van de map waarin u wijzigingen wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Folder ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie waar u de wijzigingen wilt ophalen. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> </td> 
  </tr>  </tbody> 
</table>

#### Een map maken

Deze actiemodule maakt een nieuwe map in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van de map die u wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Folder ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie waar u de map wilt maken. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder name]</td> 
   <td>Voer een naam voor de nieuwe map in of wijs deze toe.</td> 
  </tr>
  </tbody> 
</table>

#### Een bestand ophalen

Deze actiemodule haalt het opgegeven SharePoint-bestand op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van het bestand dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL File ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie van het bestand. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Mapitems controleren

Deze triggermodule start een scenario wanneer een item wordt bijgewerkt in een map die u selecteert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van het bestand dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL folder ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie van de map die u wilt controleren. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Voer het maximumaantal items in dat [!DNL Workfront Fusion] tijdens één cyclus van uitvoering van het scenario moet retourneren.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Item

* [[!UICONTROL Copy an item]](#copy-an-item)
* [[!UICONTROL Create an item]](#create-an-item)
* [[!UICONTROL Delete an item]](#delete-an-item)
* [[!UICONTROL Get an Item]](#get-an-item)
* [[!UICONTROL List Items]](#list-items)
* [[!UICONTROL Move Item]](#move-an-item)
* [[!UICONTROL Update an item]](#update-an-item)
* [[!UICONTROL Watch Items] (gepland)](#watch-items-scheduled)


#### [!UICONTROL Copy Item]

Deze actiemodule kopieert een bestaand item in een SharePoint-lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Site-, station- en map-id's invoeren</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt kopiëren.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Selecteer in het veld Itemtype of u een veld of een map verplaatst.  Selecteer de site die het item bevat dat u wilt kopiëren, selecteer vervolgens de lijst en selecteer vervolgens het item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Voer de id in van de map waarnaar u het item wilt kopiëren of wijs deze toe. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Voer een naam in of wijs een naam toe aan de nieuwe kopie van het item. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an item]

Deze actiemodule maakt een nieuw item in een SharePoint-lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren en vermeld waar u een item wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL List ID]</strong> in de weergegeven velden in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de lijst bevat waar u een item wilt maken en selecteer vervolgens de lijst. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Voer voor elk veld dat u voor het nieuwe item wilt instellen de sleutel van het veld in (geeft het veld aan) en de waarde die het nieuwe item voor dat veld moet hebben.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an item]

Met deze actiemodule verwijdert u een bestaand item uit een SharePoint-lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt verwijderen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die het item bevat dat u wilt verwijderen, selecteer vervolgens de lijst en selecteer vervolgens het item. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Item]

Deze actiemodule retourneert de gegevens van een opgegeven item.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site met de lijst waarvan u een item wilt ophalen, selecteer vervolgens de lijst en selecteer vervolgens het item. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Items]

Deze actiemodule wint een lijst van alle punten in een gespecificeerde lijst terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>Selecteer hoe u de lijst wilt identificeren waarvan u items wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL List ID]</strong> in de weergegeven velden in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site met de lijst waaruit u items wilt ophalen en selecteer vervolgens de lijst. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal punten in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Item]

Deze actiemodule kopieert een bestaand item in een SharePoint-lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Site-, station- en map-id's invoeren</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt verplaatsen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Selecteer in het veld Itemtype of u een veld of een map verplaatst. Selecteer de site die het item bevat dat u wilt kopiëren, selecteer vervolgens de lijst en selecteer vervolgens het item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Voer de id in van de map waarnaar u het item wilt verplaatsen of wijs deze toe. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Voer een naam in of wijs een naam toe aan het verplaatste item. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an item]

Deze actiemodule werkt een bestaand item in een SharePoint-lijst bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt bijwerken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die het item bevat dat u wilt bijwerken, selecteer vervolgens de lijst en selecteer vervolgens het item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Voer voor elk veld dat u wilt bijwerken voor het nieuwe item de sleutel van het veld in (geeft het veld aan) en de nieuwe waarde die het item voor dat veld moet hebben.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Items] (gepland)

Deze triggermodule start een scenario wanneer een item wordt gemaakt of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Selecteer of u lijsten wilt volgen door aanmaaktijd (nieuwe items) of door wijzigingstijd (bijgewerkte items).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren en welke lijst u wilt bekijken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL List ID]</strong> in de weergegeven velden in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de site die u wilt controleren en selecteer vervolgens de lijst. Deze drop-down wint slechts volgende plaatsen terug.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal punten in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Lijst

* [[!UICONTROL Create a List]](#create-a-list)
* [[!UICONTROL Get a List]](#get-a-list)
* [[!UICONTROL List Lists]](#list-lists)
* [[!UICONTROL Watch Lists]](#watch-lists)

#### [!UICONTROL Create a List]

Deze actiemodule maakt een nieuwe lijst in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren en vermeld waar u een lijst wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Typ of wijs de <strong>[!UICONTROL Site ID]</strong> toe waar u een lijst wilt maken.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site waarop u een lijst wilt maken. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display Name]</td> 
   <td>Voer een naam voor de nieuwe lijst in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Voer een beschrijving voor de nieuwe lijst in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Add Columns]</td> 
   <td>Voor elke kolom die u voor de nieuwe lijst wilt plaatsen, ga <strong>[!UICONTROL Name]</strong> voor het gebied in, en selecteer <strong>[!UICONTROL Type]</strong> van waarde die u de nieuwe kolom wilt hebben.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a List]

Deze actiemodule retourneert de gegevens van een opgegeven lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Ga of kaart <strong>[!UICONTROL Site ID]</strong> en <strong> identiteitskaart van de Lijst </strong> op de gebieden in die verschijnen.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de lijst bevat die u wilt ophalen en selecteer vervolgens de lijst. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Lists]

Deze actiemodule wint een lijst van alle punten in een gespecificeerde lijst terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren waarvan u lijsten wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de lijsten bevat die u wilt ophalen. In de vervolgkeuzelijst worden alleen de volgende sites opgehaald.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal lijsten in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Lists]

Deze triggermodule start een scenario wanneer een lijst wordt gemaakt of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Selecteer of u lijsten wilt volgen door aanmaaktijd (nieuwe items) of door wijzigingstijd (bijgewerkte items).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren en welke lijst u wilt bekijken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> in of wijs deze toe op de locatie van de lijst die u wilt controleren.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de site die u wilt bekijken. Met de vervolgkeuzelijst haalt u alleen de volgende site op.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal lijsten in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Pagina (Beta)

>[!NOTE]
>
>API&#39;s in de `beta` versie in [!DNL Microsoft Graph] kunnen worden gewijzigd. Het gebruik van deze API&#39;s in productietoepassingen wordt niet ondersteund.

#### [!UICONTROL Get a Page]

Deze actiemodule retourneert de gegevens van een opgegeven pagina.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Page]</td> 
   <td> <p>Selecteer hoe u de pagina wilt identificeren die u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL Page ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de pagina bevat die u wilt ophalen en selecteer vervolgens de pagina.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Site

* [[!UICONTROL Get a Site]](#get-a-site)
* [[!UICONTROL Search Sites]](#search-sites)

#### [!UICONTROL Get a Site]

Deze actiemodule retourneert de gegevens van een opgegeven site.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Site]</td> 
   <td> <p>Selecteer hoe u de pagina wilt identificeren die u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die u wilt ophalen.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Sites]

Deze actiemodule zoekt naar sites op basis van een parameter die u opgeeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword of Display Name]</td> 
   <td> <p>Voer de zoekterm in of wijs deze toe waarnaar u de sites wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal plaatsen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige

* [Wijzigingen ophalen](#get-changes)
* [Maak een API Vraag](#make-an-api-call)
* [Gebeurtenissen bekijken](#watch-events)

#### Wijzigingen ophalen

Deze module haalt toevoegingen, updates, en schrappingen terug die in de omslag van SharePoint worden gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt bijwerken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de velden <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL Drive ID]</strong> en <strong>[!UICONTROL Folder ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die het item bevat dat u wilt bijwerken, selecteer vervolgens het station en selecteer vervolgens de map. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> Het teken identificeert vanaf welk punt de module zou moeten beginnen met het terugwinnen van veranderingen.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

In deze module kunt u een aangepaste API-aanroep uitvoeren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding maken [!DNL SharePoint] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL SharePoint] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van <code>https://graph.microsoft.com</code> . Voorbeeld:<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van de aanvraag toe in de vorm van een standaard JSON-object. Bijvoorbeeld <code>{"Content-type":"application/json"}</code> . [!DNL Workfront Fusion] voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selecteer het type gegevens dat u in uw API-aanroep wilt verzenden.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Gebeurtenissen van Let

Deze instant triggermodule start een scenario wanneer een item in SharePoint wordt toegevoegd, bijgewerkt of verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL SharePoint] account to [!DNL Workfront Fusion], see <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect [!DNL SharePoint] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer een bestaande webhaak of klik op Toevoegen om een nieuwe webhaak te maken.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
