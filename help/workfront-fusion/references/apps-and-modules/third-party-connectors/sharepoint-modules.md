---
title: SharePoint-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Microsoft SharePoint Online gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 5af0b7ab4646502418f188854fdec43bcacc7549
workflow-type: tm+mt
source-wordcount: '3224'
ht-degree: 0%

---

# Microsoft SharePoint Online-modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die gebruikmaken van Microsoft SharePoint Online, en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie</td> 
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten</p>
   <p>of</p>
   <p>Verouderd: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Select- of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u Microsoft SharePoint Online-modules wilt gebruiken, hebt u een Microsoft SharePoint Online-account nodig.

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

## Microsoft SharePoint Online verbinden met [!DNL Workfront Fusion] {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [Verbind Microsoft SharePoint Online met  [!DNL Workfront Fusion]  gebruikend a [!DNL Microsoft]  rekening](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [Verbind Microsoft SharePoint Online met  [!DNL Workfront Fusion]  gebruikend geavanceerde montages](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)
* [Microsoft SharePoint Online verbinden met  [!DNL Workfront Fusion]  het gebruiken van certificaatvergunning](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-certificate-authorization)

### Microsoft SharePoint Online verbinden met [!DNL Workfront Fusion] via een [!DNL Microsoft] -account

U kunt uw [!DNL Microsoft] -account gebruiken om een verbinding met Microsoft SharePoint Online te maken. Voor instructies over het verbinden van uw [!DNL Sharepoint] rekening met [!DNL Workfront Fusion], zie [ een verbinding tot stand brengen  [!DNL Adobe Workfront Fusion]  - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Microsoft SharePoint Online verbinden met [!DNL Workfront Fusion] via geavanceerde instellingen

Schakel de optie Geavanceerde instellingen tonen in om referenties op te nemen in de verbinding. Voor dit type van verbinding, hebt u een identiteitskaart van de Cliënt, Geheime cliënt, en identiteitskaart van de Huurder nodig.

1. Klik in een willekeurige SharePoint-module op **[!UICONTROL Add]** in de buurt van het veld Verbinding om het vak **[!UICONTROL Create a connection]** te openen.
1. Klik op **[!UICONTROL Show advanced settings]**.
1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>Om cliëntgeloofsbrieven te gebruiken, uitgezochte <b> Microsoft 365 E-mail </b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Voer een naam in voor de verbinding.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Voer de client-id in voor de SharePoint-toepassing waarmee u verbinding maakt. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client secret]</p> </td> 
      <td>Voer het clientgeheim in voor de SharePoint-toepassing waarmee u verbinding maakt.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Tenant ID]</p> </td> 
      <td>Voer de huurder-id in van de SharePoint-app waarmee u verbinding maakt.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik **verdergaan** om de verbinding te bewaren en aan de module terug te keren.

### Microsoft SharePoint Online verbinden met [!DNL Workfront Fusion] certificaatverificatie

U kunt certificaatautorisatie gebruiken om verbinding te maken met SharePoint.

>[!IMPORTANT]
>
>Als u certificaatautorisatie wilt gebruiken, moet u eerst een app maken in Microsoft Entra en het certificaat daar uploaden.
>
>Voor instructies, zie [ hoe te om certificaatautoriteiten voor Microsoft te vormen Entra op certificaat-gebaseerde authentificatie ](https://learn.microsoft.com/en-us/entra/identity/authentication/how-to-configure-certificate-authorities) in de documentatie van Microsoft.

1. Klik in een willekeurige SharePoint-module op **[!UICONTROL Add]** in de buurt van het veld Verbinding om het vak **[!UICONTROL Create a connection]** te openen.
1. Klik op **[!UICONTROL Show advanced settings]**.
1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>Om certificaatvergunning te gebruiken, uitgezochte <b> Microsoft SharePoint Online (Auth van de Waarschuwing) </b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Voer een naam in voor de verbinding.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Voer de client-id in voor de SharePoint-toepassing waarmee u verbinding maakt. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Thumbprint]</p> </td> 
      <td>Voer de miniatuur in voor de SharePoint-toepassing waarmee u verbinding maakt.</td> 
     </tr> 
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Voer het certificaat of de persoonlijke sleutel in die is gegenereerd toen uw referenties in Microsoft werden gemaakt. </p>
          <p>Uw persoonlijke sleutel of certificaat uitnemen:</p>
          <ol>
            <li>
              <p>Klik op <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li>
            <p>Selecteer of u een certificaat of een persoonlijke sleutel uitpakt.</li>
            <li>
              <p>Selecteer het type bestand dat u extraheert.</p>
            </li>
            <li>
              <p>Selecteer het bestand dat de persoonlijke sleutel of het certificaat bevat.</p>
            </li>
            <li>
              <p>Voer het wachtwoord voor het bestand in.</p>
            </li>
            <li>
              <p>Klik op <b>[!UICONTROL Save]</b> om het bestand uit te pakken en terug te keren naar de verbindingsinstelling.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody> 
   </table>

1. Klik **verdergaan** om de verbinding te bewaren en aan de module terug te keren.

## Microsoft SharePoint-modules en hun velden

Wanneer u Microsoft SharePoint Online-modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende Microsoft SharePoint Online-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

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
* [Een map ophalen](#get-a-folder)
* [Een map of bestand bijwerken](#update-a-folder-or-a-file)
* [Mapitems controleren](#watch-folder-items)

#### Een bestand maken

Deze module retourneert wijzigingen die zijn aangebracht in SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van de map waarin u wijzigingen wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL Drive ID]</strong> en <strong>[!UICONTROL Folder ID]</strong> van de locatie in waar u het bestand wilt maken of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie waar u het bestand wilt maken. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
      <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p>
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van de map die u wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL Drive ID]</strong> en <strong>[!UICONTROL Folder ID]</strong> van de locatie in waar u de map wilt maken of wijs deze toe.</p> </li> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van het bestand dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL File ID]</strong> in of wijs deze toe voor het bestand dat u wilt ophalen.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie van het bestand. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Een map ophalen

In deze module worden gegevens over de opgegeven map opgehaald

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and File                IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van het bestand dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Folder path]</strong> in of wijs deze toe voor de map die u wilt ophalen.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie van de map. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Een map of bestand bijwerken

Deze actiemodule werkt de metagegevens van een map of bestand bij

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and File                IDs]</td> 
   <td> <p>Selecteer hoe u de locatie wilt identificeren van het bestand dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Folder or item ID]</strong> in of wijs deze toe voor de map of het bestand dat u wilt ophalen.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de locatie van de map. </p> </li> 
    </ul> </td> 
  </tr> 
  </tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Voor elk meta-gegevensgebied dat u wilt bijwerken, <b> toevoegen punt </b> en ingaan de weg en de waarde van het gebied.</td> 
  <tr>
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
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
* [Details ophalen](#get-details)
* [[!UICONTROL List Items]](#list-items)
* [[!UICONTROL Move an Item]](#move-an-item)
* [[!UICONTROL Update an Item]](#update-an-item)
* [[!UICONTROL Watch Items] (gepland)](#watch-items-scheduled)


#### [!UICONTROL Copy an Item]

Deze actiemodule kopieert een bestaand item in een SharePoint-lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Site-, station- en map-id's invoeren</td> 
   <td> <p>Selecteer hoe u de site en het station wilt identificeren waarop het item staat dat u wilt kopiëren.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL Drive ID]</strong> en <strong>[!UICONTROL Item ID]</strong> van het item dat u wilt kopiëren in of wijs deze toe.</p> </li> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>Selecteer hoe u de site en het station wilt identificeren waarop u een item wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Typ of wijs de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL List ID]</strong> toe waar u het item wilt maken.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de lijst bevat waar u een item wilt maken en selecteer vervolgens de lijst. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Voor elk gebied dat u voor het nieuwe punt wilt plaatsen, <b> toevoegen punt </b> en ingaan de sleutel van het gebied (die het gebied) identificeert en de waarde die u het nieuwe punt voor dat gebied wilt hebben.</td> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt verwijderen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> van het item dat u wilt verwijderen in of wijs deze toe.</p> </li> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> in of wijs deze toe van het item waarvoor u gegevens wilt retourneren.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site met de lijst waarvan u een item wilt ophalen, selecteer vervolgens de lijst en selecteer vervolgens het item. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Details ophalen

Deze module haalt itemdetails op van de opgegeven URL.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> Typ of wijs de URL toe van het item waarvoor u de details wilt ophalen. </td> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>Selecteer hoe u de lijst wilt identificeren waarvan u items wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL List ID]</strong> in of wijs deze toe voor de lijst waarvoor u items wilt weergeven.</p> </li> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Site-, station- en map-id's invoeren</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt verplaatsen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> in of wijs deze toe voor het item dat u wilt verplaatsen.</p> </li> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt bijwerken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> , <strong>[!UICONTROL List ID]</strong> en <strong>[!UICONTROL Item ID]</strong> van het item dat u wilt bijwerken in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die het item bevat dat u wilt bijwerken, selecteer vervolgens de lijst en selecteer vervolgens het item. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Voor elk gebied dat u voor het nieuwe punt wilt bijwerken, <b> toevoegen punt </b> en ingaan de sleutel van het gebied (die het gebied) identificeert en de nieuwe waarde die u het punt voor dat gebied wilt hebben.</td> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Selecteer of u lijsten wilt volgen door aanmaaktijd (nieuwe items) of door wijzigingstijd (bijgewerkte items).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren en welke lijst u wilt bekijken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Typ of wijs de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL List ID]</strong> toe die u wilt controleren.</p> </li> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren waarop u een lijst wilt maken.</p> 
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
   <td>Voor elke kolom die u voor de nieuwe lijst wilt plaatsen, <b> voeg punt </b> toe, ga a <strong>[!UICONTROL Name]</strong> voor het gebied in, en selecteer <strong>[!UICONTROL Type]</strong> van waarde die u de nieuwe kolom wilt hebben.</td> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>Selecteer hoe u de site en de lijst wilt identificeren die het item bevatten dat u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Ga of kaart <strong>[!UICONTROL Site ID]</strong> en <strong> identiteitskaart van de Lijst </strong> in die u wilt terugkeren.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de lijst bevat die u wilt ophalen en selecteer vervolgens de lijst. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Lists]

Deze actiemodule wint een lijst van alle punten in een gespecificeerde plaats terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren waarvan u lijsten wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Typ of wijs de <strong>[!UICONTROL Site ID]</strong> toe die de lijsten bevat die u wilt retourneren.</p> </li> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Selecteer of u lijsten wilt volgen door aanmaaktijd (nieuwe items) of door wijzigingstijd (bijgewerkte items).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site ID]</td> 
   <td> <p>Selecteer hoe u de site wilt identificeren die u wilt controleren voor lijsten.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Typ of wijs de <strong>[!UICONTROL Site ID]</strong> toe waar u lijsten wilt controleren.</p> </li> 
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

* [Een pagina ophalen](#get-a-page)
* [Lijstpagina&#39;s](#list-pages)
* [Pagina&#39;s publiceren](#publish-a-page)
* [Pagina&#39;s controleren](#watch-pages)

#### [!UICONTROL Get a Page]

Deze actiemodule retourneert de gegevens van een opgegeven pagina.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
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

#### Lijstpagina&#39;s

Deze module wint een lijst van alle pagina&#39;s terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Pages]</td> 
   <td> <p>Selecteer hoe u de pagina's wilt identificeren die u wilt weergeven.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> in of wijs de site toe die de pagina's bevat die u wilt weergeven.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de pagina's bevat die u wilt weergeven.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal pagina's in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Pagina&#39;s publiceren

Deze actiemodule publiceert de nieuwste versie van de geselecteerde pagina.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Publish a page]</td> 
   <td> <p>Selecteer hoe u de pagina wilt identificeren die u wilt publiceren.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> en <strong>[!UICONTROL Page ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer de site die de pagina bevat die u wilt publiceren en selecteer vervolgens de pagina.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Pagina&#39;s controleren

Deze triggermodule start een scenario wanneer een pagina op de opgegeven site wordt gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site ID]</td> 
   <td> <p>Selecteer hoe u de pagina's wilt identificeren die u wilt weergeven.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Site ID]</strong> in of wijs de site toe die de pagina's bevat die u wilt controleren.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Selecteer de site die de pagina's bevat die u wilt controleren.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal pagina's in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Selecteer hoe u de site en het station wilt identificeren waarop het item staat dat u wilt bijwerken.</p> 
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
   <td> <p>Zie [!DNL Workfront Fusion] Connect Microsoft SharePoint Online <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> in dit artikel voor instructies over het verbinden van uw Microsoft SharePoint Online-account met [!DNL Workfront Fusion]</a> .</p> </td> 
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
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object. Bijvoorbeeld <code>{"Content-type":"application/json"}</code> . [!DNL Workfront Fusion] voegt de machtigingsheaders voor u toe.</p> </td> 
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
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to [!DNL Workfront Fusion], see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer een bestaande webhaak of klik op Toevoegen en voer de verbinding in om een nieuwe webhaak te maken.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
