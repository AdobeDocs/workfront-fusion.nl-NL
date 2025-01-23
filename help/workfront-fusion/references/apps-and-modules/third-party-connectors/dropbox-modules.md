---
title: Dropbox
description: In a  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Dropbox gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.Dit staat u toe om activiteiten zoals controle, het zoeken, het terugwinnen van, het een lijst maken van, en het uitgeven van dossiers en omslagen in uw Dropbox te automatiseren.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2868'
ht-degree: 0%

---

# [!DNL Dropbox] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!UICONTROL Dropbox] of [!DNL Dropbox Business] gebruiken en deze koppelen aan meerdere toepassingen en services van derden. Hierdoor kunt u activiteiten zoals het controleren, zoeken, ophalen, weergeven, maken en bewerken van bestanden en mappen in uw [!UICONTROL Dropbox] automatiseren.

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

* Als u [!DNL Dropbox] -modules wilt gebruiken, moet u een [!DNL Dropbox] -account hebben.

>[!IMPORTANT]
>
>Dropbox moet toepassingen met meer dan 50 gebruikers goedkeuren.
>
>Voor meer informatie, zoek naar &quot;Goedkeuring van de Productie&quot;in de Dropbox ontwikkelaarsgids.

## API-informatie voor Dropbox

De verbindingslijn van de Dropbox gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.dropboxapi.com/2    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> 2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td><ul><li><p>Dropbox</p><p>v5.3.9</p></li><li><p>Dropbox Business</p><p>v1.0.12</p></li></ul></td> 
  </tr>
 </tbody> 
 </table>


## Verbinding maken met [!DNL Dropbox]

Verbinding maken voor uw [!DNL Dropbox] -modules:

1. Klik op **[!UICONTROL Add]** naast het vak Verbinding.

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor deze verbinding.</p>
        </td>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecteer of deze verbinding voor een productie of een non-productie milieu is.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</td>
        </tr>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!UICONTROL Dropbox] [!UICONTROL Client ID] in. </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Dropbox] [!UICONTROL Client Secret] in. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Account Type]</td>
        <td>Selecteer of u met een persoonlijke rekening van de Dropbox of een bedrijfsrekening (de Zaken van de Dropbox) verbindt.</td>
        </tr>
      </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.## [!DNL Dropbox] modules en hun velden

## [!DNL Dropbox] modules en hun velden

Wanneer u [!DNL Dropbox] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Dropbox] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggermodules](#trigger-modules)
* [Modules voor het krijgen van  [!DNL Dropbox]  dossiers en omslagen](#modules-for-getting-dropbox-files-and-folders)
* [Modules voor het creëren en het uitgeven van  [!DNL Dropbox]  dossiers en omslagen](#modules-for-creating-and-editing-dropbox-files-and-folders)
* [Overige modules](#other-modules)

### Triggermodules

#### [!UICONTROL Watch Files]

Deze triggertypemodule retourneert bestandsgegevens wanneer het bestand in een opgegeven map wordt gewijzigd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map die u wilt controleren op wijzigingen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch also subfolders]</td> 
   <td> <p> Schakel deze optie in om ook de submappen in de geselecteerde map te controleren op gewijzigde bestanden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modules voor het ophalen van [!DNL Dropbox] bestanden en mappen

* [[!UICONTROL Search Files/Folders]](#search-filesfolders)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Get a Folder Metadata]](#get-a-folder-metadata)
* [[!UICONTROL List All Files/Subfolders in a Folder]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL List File Revisions]](#list-file-revisions)

#### [!UICONTROL Search Files/Folders]

Deze zoekmodule zoekt naar records in een object in [!DNL Dropbox] dat overeenkomt met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map die u wilt doorzoeken. Deze module zoekt de volledige [!DNL Dropbox] als u geen map selecteert.</p> </td> 
  </tr> 
  <tr> 
   <td>Bestandsstatus</td> 
   <td> <p> Selecteer de bestandsstatus om de zoekopdracht te beperken tot de geselecteerde bestandsstatus.</p> </td> 
  </tr> 
  <tr> 
   <td>Bestandscategorieën</td> 
   <td> <p> Selecteer de bestandscategorieën om de zoekopdracht te beperken tot de geselecteerde categorieën.</p> </td> 
  </tr> 
  <tr> 
   <td>Bestandsextensies</td> 
   <td> <p> Kies de bestandsextensies waarnaar u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>Limiet </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Deze actiemodule downloadt een bestand uit een map.

U geeft het bestand en de locatie op.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

>[!NOTE]
>
>Deze module is nuttig om dossiers aan verdere modules te verstrekken.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>Wijze waarop bestanden worden geselecteerd</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of het bestand handmatig wilt selecteren.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Bestandspad / Bestand</p> </td> 
   <td> <p style="font-weight: bold;">Bestandspad</p> <p>Typ of wijs het doelpad naar het bestand toe.</p> <p style="font-weight: bold;">Bestand</p> <p>Selecteer het bestand in het menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Folder Metadata]

In deze actiemodule worden de gegevens van de gedeelde map opgehaald.

U geeft de id van de map op.

De module retourneert de id van de map en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>Gedeelde map-id</td> 
   <td> <p> Voer de id in van de map waarover u gegevens wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List All Files/Subfolders in a Folder]

In deze actiemodule worden bestanden of mappen in een bepaalde map weergegeven.

U geeft de id van de map op.

De module retourneert de id&#39;s van de bestanden of mappen en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>Lijst </td> 
   <td> <p>Selecteer of u bestanden of mappen wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>Alleen downloadbare bestanden tonen</td> 
   <td> <p> Schakel deze optie in als u alleen downloadbare bestanden wilt retourneren. Sommige bestandstypen, zoals Google Docs, kunnen niet worden gedownload.</p> </td> 
  </tr> 
  <tr> 
   <td>Map </td> 
   <td> <p>Voer de map in waarvan u bestanden of mappen wilt ophalen of wijs de map toe.</p> </td> 
  </tr> 
  <tr> 
   <td>Limiet </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt een lijst maken.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List File Revisions]

Deze actiemodule haalt alle bestandsrevisies (een versiegeschiedenis) van een bepaald bestand op.\
U geeft de id van het bestand op.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>Wijze waarop bestanden worden geselecteerd</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of het bestand handmatig wilt selecteren.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Bestandspad / Bestand</p> </td> 
   <td> <p style="font-weight: bold;">Bestandspad</p> <p>Typ of wijs het doelpad naar het bestand toe.</p> <p style="font-weight: bold;">Bestand</p> <p>Selecteer het bestand in het menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Limiet</p> </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt een lijst maken.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modules voor het maken en bewerken van [!DNL Dropbox] bestanden en mappen

* [[!UICONTROL Upload] een bestand](#upload-a-file)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Create/Overwrite a Text File]](#createoverwrite-a-text-file)
* [[!UICONTROL Create/Update a Share Link]](#createupdate-a-share-link)
* [[!UICONTROL Restore a File]](#restore-a-file)
* [[!UICONTROL Move a File/Folder]](#move-a-filefolder)
* [[!UICONTROL Rename a File/Folder]](#rename-a-filefolder)
* [[!UICONTROL Delete a File/Folder]](#delete-a-filefolder)

#### [!UICONTROL Upload a File]

Deze actiemodule uploadt een bestand naar een map.

U geeft informatie op zoals de locatie van het bestand, het bestand dat u wilt uploaden en een optionele nieuwe naam voor het bestand.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td> <p> Selecteer de map van de [!DNL Dropbox] waarnaar u het bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Voer het bestand in of wijs het toe dat u aan de hierboven geselecteerde map [!DNL Dropbox] wilt toevoegen.</p> <p style="font-weight: bold;">[!UICONTROL File name]</p> <p>Voer de bestandsnaam in of wijs deze toe, inclusief de bestandsextensie.</p> <p style="font-weight: bold;">[!UICONTROL File data]</p> <p>Ga of kaart de dossiergegevens in (van vorige module zoals [!UICONTROL Google Drive] &gt; [!UICONTROL Get a File)].</p> <p>Opmerking: de maximale grootte van het geüploade bestand is 150 MB.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Overwrite an existing file]</td> 
   <td> <p> Schakel deze optie in om het bestaande bestand te vervangen door het nieuwe bestand. Als deze optie niet is ingeschakeld, wordt de naam van het geüploade bestand gewijzigd.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Deze actiemodule maakt een nieuwe map.

U geeft het pad en een naam voor de map op.

De module retourneert de id van de map en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name] </td> 
   <td> <p>Voer de naam voor de nieuwe map in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Voer het pad in of wijs het toe op de plaats waar u een nieuwe map wilt maken.</p> <p>Opmerking:   <p>Als u een [!DNL Dropbox Business] account (met teamspaties) gebruikt, moet u de schuine streep <code>/</code> verwijderen of niet <strong>[!UICONTROL Click here] klikken om map </strong> te kiezen om een teammap in de hoofdmap te maken.</p> <p>Als de schuine streep niet wordt verwijderd, wordt een fout <code>[409] path/malformed_path/..</code> geretourneerd.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Auto rename]</td> 
   <td> <p> Schakel deze optie in om de naam van de nieuwe map te wijzigen als er al een map met dezelfde naam bestaat op de doellocatie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Overwrite a Text File]

In deze actiemodule wordt een DOC-bestand gemaakt of wordt de inhoud van een bestaand bestand overschreven.

U geeft het bronbestand en de map op.

De module retourneert de id van de map en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select to]</td> 
   <td> <p> Selecteer of u een DOC-bestand wilt maken of overschrijven.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de doellocatie waar u een bestand wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Typ of wijs het bestand toe dat u aan de map [!DNL Dropbox] wilt toevoegen.</p> <p style="font-weight: bold;">Bestandsnaam</p> <p>Voer de bestandsnaam in voor het nieuwe DOC-bestand (zonder extensie).</p> <p style="font-weight: bold;">Bestandsinhoud</p> <p>Voer de tekstinhoud van het DOC-bestand in.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Share Link]

In deze actiemodule wordt een openbare koppeling naar een bestand gemaakt.

U geeft het bestand en de informatie over de koppeling op.

De module retourneert de id van de koppeling en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path / File]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File Path]</p> <p>Typ of wijs het doelpad naar het bestand toe.</p> <p style="font-weight: bold;">[!UICONTROL File]</p> <p>Selecteer het bestand in het menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Requested Visibility]</p> </td> 
   <td> <p>Selecteer of de verbinding openbaar, voor team, of wachtwoord beperkt is.</p> <p>Opmerking: [!UICONTROL Team only] en [!UICONTROL Access with password] -opties zijn alleen beschikbaar voor gebruikers met een [!DNL Dropbox Pro] -versie of hoger.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Link's Expiration Date]</td> 
   <td> <p> Voer de datum en tijd in waarop de koppeling verloopt en niet meer toegankelijk is. Als dit veld leeg blijft, verloopt de koppeling niet. Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override=""> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p> <p>Opmerking: [!UICONTROL Team only] en [!UICONTROL Access with password] -opties zijn alleen beschikbaar voor gebruikers met [!UICONTROL Dropbox Pro] of hogere versies.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Link's Access Level]</p> </td> 
   <td> <p>Stel de machtigingen voor de ontvanger van de koppeling in.</p> <p><strong>[!UICONTROL Viewer]</strong> Gebruikers die de koppeling gebruiken, kunnen de inhoud weergeven en opmerkingen plaatsen.</p> <p><strong>[!UICONTROL Editor]</strong> Gebruikers die de koppeling gebruiken, kunnen de inhoud bewerken, weergeven en opmerkingen plaatsen.</p> <p><strong>[!UICONTROL Max]</strong> Gebruikers die de koppeling gebruiken, ontvangen het maximale toegangsniveau waarop u de koppeling kunt instellen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Restore a File]

In deze actiemodule wordt een vorige versie van een bestand hersteld.

U geeft het bestand en het nummer van de gewenste revisie op.

De module retourneert de id van de versie en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path] / [!UICONTROL File]</p> </td> 
   <td> <p><strong>[!UICONTROL File Path]</strong> </p> <p>Typ of wijs het doelpad naar het bestand toe.</p> <p><strong>[!UICONTROL File]</strong> </p> <p>Selecteer het bestand in het menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Revision]</p> </td> 
   <td> <p>Ga of kaart het revisieaantal van de revisie in u wilt herstellen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder]

Deze actiemodule verplaatst een bestand of map naar een andere locatie.

U geeft het bestand of de map op en bepaalt hoe en waar u het bestand of de map wilt verplaatsen.

De module retourneert de id van het bestand of de map en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files] </td> 
   <td> <p>Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File/Folder Path] / [!UICONTROL File/Folder]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File/Folder Path]</p> <p>Voer het doelpad in of wijs dit toe aan het bestand of de map.</p> <p style="font-weight: bold;">[!UICONTROL File/Folder]</p> <p>Selecteer het bestand of de map in het menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL To Folder]</p> </td> 
   <td> <p>Voer de doellocatie voor het bestand of de map in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL New Name]</p> </td> 
   <td> <p>Voer de nieuwe naam voor het bestand of de map op de nieuwe locatie in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Auto Rename]</p> </td> 
   <td> <p>Schakel deze optie in om ervoor te zorgen dat als er al een bestand of map met dezelfde naam bestaat, de module de naam van het nieuwe bestand of de nieuwe map wijzigt door ([!UICONTROL NUMBER]) achter de bestands- of mapnaam toe te voegen. Anders wordt het bestand of de map op de doellocatie overschreven.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Allow ownership transfer]</p> </td> 
   <td> <p>Schakel deze optie in om verplaatsing door de eigenaar toe te staan, zelfs als dit zou leiden tot een eigendomsoverdracht voor de inhoud die wordt verplaatst.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File/Folder]

In deze actiemodule wordt de naam van een bestand of map gewijzigd.

U geeft het bestand of de map en de nieuwe naam op.

De module retourneert de id van het bestand of de map en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>Wijze waarop bestanden worden geselecteerd</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Pad naar bestand/map/bestand/map</p> </td> 
   <td> <p style="font-weight: bold;">Pad naar bestand/map</p> <p>Voer het doelpad in of wijs dit toe aan het bestand of de map.</p> <p style="font-weight: bold;">Bestand/map</p> <p>Selecteer het bestand of de map in het menu.</p> </td> 
  </tr> 
  <tr> 
   <td>Naam wijzigen </td> 
   <td> <p>Voer de [!UICONTROL target name] in voor het bestand, inclusief de bestandsextensie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File/Folder]

Met deze actiemodule verwijdert u een bestand of map.

U geeft het bestand of de map op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path] / [!UICONTROL File]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File Path]</p> <p>Typ of wijs het doelpad naar het bestand toe.</p> <p style="font-weight: bold;">[!UICONTROL File]</p> <p>Selecteer het bestand in het menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige modules

#### [!UICONTROL Make an API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Dropbox] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Dropbox] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van het invoeren van een pad dat relatief is ten opzichte van <code>https://api.dropboxapi.com</code> . Bijvoorbeeld: <code>/2/files/list_folder</code></p> <p>Nota: Voor de lijst van beschikbare eindpunten, zie de <a href="https://www.dropbox.com/developers/documentation/http/documentation"> Dropbox API v2 Documentatie </a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers] </td> 
   <td> <p>Voer de gewenste aanvraagheaders in. [!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p> Voer de queryreeks voor de aanvraag in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body] </td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:   <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Voorbeeld:** de volgende API vraag keert de eerste 10 dossiers van de [!DNL /Text files] omslag in uw [!DNL Dropbox] rekening terug:
>
>URL: `/2/files/list_folder`
>
>Lichaam:
> 
>`{`
>
>`"path": "/Text files",`
>
>`"limit": 10,`
>
>`"recursive": false,`
>
>`"include_deleted": false`
>
>`}`
>
>Overeenkomsten met de zoekopdracht vindt u in de sectie Uitvoer van de module onder [!UICONTROL Bundle] > [!UICONTROL Body] > vermeldingen.
>
>In ons voorbeeld werden 10 tickets geretourneerd:

## Algemene problemen

* [Kan een bestand niet uploaden of bijwerken](#unable-to-upload-or-update-a-file)
* [Afbeeldingen waarnaar via een gedeelde koppeling wordt verwezen, worden niet gerenderd](#image-referenced-via-a-shared-link-does-not-render)

### Kan een bestand niet uploaden of bijwerken

Er zijn verschillende situaties wanneer het uploaden of bijwerken van een bestand mislukt:

* Het geüploade bestand is te groot en overschrijdt de maximaal toegestane bestandsgrootte voor uw [!DNL Dropbox] -abonnement. U hebt ook de volledige opslaglimiet van uw [!DNL Dropbox] -account gebruikt. U moet bestaande bestanden verwijderen van uw [!DNL Dropbox] -account of uw abonnement upgraden.
* De eerder geselecteerde map waarnaar het bestand wordt geüpload, bestaat niet meer. Het scenario stopt en u moet de doelmap opnieuw selecteren.

### Afbeeldingen waarnaar via een gedeelde koppeling wordt verwezen, worden niet gerenderd

De URL die wordt geretourneerd door [!UICONTROL Dropbox] > [!UICONTROL Create a shared link] , is niet rechtstreeks gekoppeld aan een afbeelding, maar aan een pagina [!DNL Dropbox] . Als u het downloaden van de afbeelding wilt forceren, vervangt u het navolgende `?dl=0` door `?dl=1` . Als u wilt dat de afbeelding wordt gerenderd (bijvoorbeeld in een webbrowser of in Facebook Messenger), voegt u `&raw=1` toe aan de URL.

Als u de directe of ruwe verbinding van uw beeld voor uw website of voor andere [!DNL Workfront Fusion] modules moet krijgen, moet u eerste gedeelde URL op de volgende manier wijzigen:

Oorspronkelijke URL:

`https://www.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png?dl=0`

1. Vervang `www` door `dl` .
1. Verwijderen `?dl=0` .

Uiteindelijke URL:

`https://dl.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png`

Als u de URL automatisch wilt wijzigen, kunt u de functie `replace()` twee keer gebruiken:

* www door dl vervangen

  ![](/help/workfront-fusion/references/apps-and-modules/assets/www-to-dl-350x32.png)

* En om ?dl=0 te verwijderen

  ![](/help/workfront-fusion/references/apps-and-modules/assets/remove-dl0-350x33.png)

U kunt dit in één stap doen door de volgende functies te combineren:

![](/help/workfront-fusion/references/apps-and-modules/assets/replace-both-350x47.png)

U kunt het ook kopiëren en in het veld plakken. Vervang `1.url` door de URL.

```
{{replace(replace(1.url; "?dl=0"; ""); "www"; "dl")}}
```
