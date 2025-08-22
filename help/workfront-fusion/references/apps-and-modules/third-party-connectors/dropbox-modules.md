---
title: Dropbox-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die gebruikmaken van Dropbox, en deze koppelen aan meerdere toepassingen en services van derden. Hierdoor kunt u activiteiten zoals het controleren, zoeken, ophalen, weergeven, maken en bewerken van bestanden en mappen in uw Dropbox automatiseren.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2956'
ht-degree: 0%

---

# [!DNL Dropbox] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!UICONTROL Dropbox] of [!DNL Dropbox Business] gebruiken, en deze koppelen aan meerdere toepassingen en services van derden. Hierdoor kunt u activiteiten zoals het controleren, zoeken, ophalen, weergeven, maken en bewerken van bestanden en mappen in uw [!UICONTROL Dropbox] automatiseren.

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

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

* Als u [!DNL Dropbox] -modules wilt gebruiken, moet u een [!DNL Dropbox] -account hebben.

>[!IMPORTANT]
>
>* Als u de Dropbox-aansluiting wilt gebruiken, moet u eerst een toepassing in Dropbox maken.
>  &#x200B;>   Zoek naar &quot;Een toepassing maken&quot; in de handleiding voor ontwikkelaars van Dropbox voor meer informatie.
>* Wanneer u de toepassing maakt, gebruikt u de volgende URI voor omleiding: `https://app.workfrontfusion.com/oauth/cb/dropbox`
>* Dropbox moet toepassingen met meer dan 50 gebruikers goedkeuren.
>  &#x200B;>   Zoek naar &quot;Productietoestemming&quot; in de Dropbox-handleiding voor ontwikkelaars voor meer informatie.

## Dropbox API-informatie

De Dropbox-connector gebruikt het volgende:

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

1. Klik in een willekeurige module op **[!UICONTROL Add]** naast het vak Verbinding.

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
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!UICONTROL Dropbox] [!UICONTROL Client ID] in. </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Dropbox] [!UICONTROL Client Secret] in. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Account Type]</td>
        <td>Selecteer of u verbinding maakt met een persoonlijke Dropbox-account of een zakelijke account (Dropbox Business).</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Exclude dropbox-api-path-root header]</td>
        <td>Schakel deze optie in om de header dropbox-api-path-root uit te sluiten voor Dropbox Apps met toegang tot App Folder</td>
        </tr>
      </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.## [!DNL Dropbox] modules en hun velden

## [!DNL Dropbox] modules en hun velden

Wanneer u [!DNL Dropbox] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Dropbox] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
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

* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Get a Folder Metadata]](#get-a-folder-metadata)
* [[!UICONTROL List All Files/Subfolders in a Folder]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL List File Revisions]](#list-file-revisions)
* [[!UICONTROL Search Files/Folders]](#search-filesfolders)

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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>Wijze waarop bestanden worden geselecteerd</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of het bestand handmatig wilt selecteren.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Bestandspad / Bestand</p> </td> 
   <td> <p><b>Bestandspad</b></p> <p>Typ of wijs het doelpad naar het bestand toe.</p> <p><b>Bestand</b></p> <p>Selecteer het bestand in het menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Limiet</p> </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt een lijst maken.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Files/Folders]

Deze zoekmodule zoekt naar records in een object in [!DNL Dropbox] dat overeenkomt met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map die u wilt doorzoeken. Deze module zoekt de volledige [!DNL Dropbox] rekening als u geen omslag selecteert.</p> </td> 
  </tr> 
  <tr> 
   <td>Bestandsstatus</td> 
   <td> <p> Selecteer de bestandsstatus die u in de zoekopdracht wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td>Bestandscategorieën</td> 
   <td> <p> Selecteer de bestandscategorieën die u in de zoekopdracht wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td>Bestandsextensies</td> 
   <td> <p>Voor elke dossieruitbreiding die u in het onderzoek wilt omvatten, klik <b> toevoegen punt </b> en ga of kaart de dossieruitbreiding in.</p> </td> 
  </tr> 
  <tr> 
   <td>Limiet </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modules voor het maken en bewerken van [!DNL Dropbox] bestanden en mappen

* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Create/Overwrite a Text File]](#createoverwrite-a-text-file)
* [[!UICONTROL Create/Update a Share Link]](#createupdate-a-share-link)
* [[!UICONTROL Delete a File/Folder]](#delete-a-filefolder)
* [[!UICONTROL Move a File/Folder]](#move-a-filefolder)
* [[!UICONTROL Rename a File/Folder]](#rename-a-filefolder)
* [[!UICONTROL Restore a File]](#restore-a-file)
* [[!UICONTROL Upload] een bestand](#upload-a-file)

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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name] </td> 
   <td> <p>Voer de naam voor de nieuwe map in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Voer het pad in of wijs het toe op de plaats waar u een nieuwe map wilt maken.</p> <p>Opmerking:   <p>Als u een [!DNL Dropbox Business] rekening (met teamruimten) gebruikt, moet u de schuine streep <code>/</code> verwijderen, of <strong> klikt hier niet om omslag </strong> te kiezen om een teamomslag in de wortel tot stand te brengen.</p> <p>Als de schuine streep niet wordt verwijderd, wordt een fout <code>[409] path/malformed_path/..</code> geretourneerd.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Auto rename]</td> 
   <td> <p> Schakel deze optie in om de naam van de nieuwe map te wijzigen als er al een map met dezelfde naam bestaat op de doellocatie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Overwrite a Text File]

Deze actiemodule maakt een DOC-bestand of overschrijft de inhoud van een bestaand bestand.

U geeft het bronbestand en de map op.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select to]</td> 
   <td> <p> Selecteer of u een DOC-bestand wilt maken of overschrijven.</p><ul><li><b>Maken</b></p>Selecteer de map waarin u een bestand wilt maken.</li><li><b>Overschrijven</b><p>Selecteer hoe u het bestand wilt kiezen dat u wilt overschrijven, wijs vervolgens het bestandspad toe of selecteer het bestand. </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de inhoud van het bronbestand toe. </p> <p>Als u een dossier creeert, uitgezocht <b> Leeg </b>.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path / File]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File Path]</p> <p>Typ of wijs het pad naar het doelbestand toe.</p> <p style="font-weight: bold;">[!UICONTROL File]</p> <p>Selecteer het doelbestand.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Requested Visibility]</p> </td> 
   <td> <p>Selecteer of de verbinding openbaar, voor team, of wachtwoord beperkt is.</p> <p><b>Opmerking:</b></p><p> [!UICONTROL Team only] is alleen beschikbaar voor Dropbox Business-accounts. [!UICONTROL Access with password] is alleen beschikbaar voor [!DNL Dropbox Pro] - of Dropbox Business-accounts.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Link's Expiration Date]</td> 
   <td> <p> Voer de datum en tijd in waarop de koppeling verloopt en niet meer toegankelijk is. Als dit veld leeg blijft, verloopt de koppeling niet. Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override=""> Druk van het Type </a>.</p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Link's Access Level]</p> </td> 
   <td> <p>Stel de machtigingen voor de ontvanger van de koppeling in.</p> <ul><li><strong>[!UICONTROL Viewer]</strong> <p>Gebruikers die de koppeling gebruiken, kunnen de inhoud weergeven en opmerkingen plaatsen.</p> </li><li><strong>[!UICONTROL Editor]</strong><p> Gebruikers die de koppeling gebruiken, kunnen de inhoud bewerken, weergeven en opmerkingen plaatsen. Dit toegangsniveau is alleen beschikbaar voor documenten in de cloud.</p> </li><li><strong>[!UICONTROL Max]</strong> <p>Gebruikers die de koppeling gebruiken, ontvangen het maximale toegangsniveau waarop u de koppeling kunt instellen.</p></li><ul> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File or Folder Path] / [!UICONTROL File or Folder]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File/Folder Path]</p> <p>Voer het doelpad in of wijs dit toe aan het bestand of de map.</p> <p style="font-weight: bold;">[!UICONTROL File/Folder]</p> <p>Selecteer het bestand of de map in het menu.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files / folders] </td> 
   <td> <p>Selecteer of u het bestands- of mappad wilt toewijzen of invoeren, of selecteer het bestand of de map handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File / Folder Path] /</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File/Folder Path]</p> <p>Voer het doelpad in of wijs dit toe aan het bestand of de map.</p> <p style="font-weight: bold;">[!UICONTROL File/Folder]</p> <p>Selecteer of u een bestand of map verplaatst, en vervolgens het bestand of de map.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>Wijze waarop bestanden worden geselecteerd</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Pad naar bestand/map/bestand/map</p> </td> 
   <td> <p style="font-weight: bold;">Pad naar bestand/map</p> <p>Voer het doelpad in of wijs dit toe aan het bestand of de map.</p> <p style="font-weight: bold;">Bestand/map</p> <p>Selecteer of u een bestand of map verplaatst, en vervolgens het bestand of de map.</p> </td> 
  </tr> 
  <tr> 
   <td>Naam wijzigen </td> 
   <td> <p>Voer de nieuwe naam voor het bestand in, inclusief de bestandsextensie.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td> <p> Selecteer de map van de [!DNL Dropbox] waarnaar u het bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> <p><b>Opmerking:</b></p><p> De maximale grootte van het geüploade bestand is 150 MB.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Overwrite an existing file]</td> 
   <td> <p> Schakel deze optie in om het bestaande bestand te vervangen door het nieuwe bestand. Als deze optie niet is ingeschakeld, wordt de naam van het geüploade bestand gewijzigd.</p> </td> 
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
   <td> <p>Zie [!DNL Dropbox] Verbinding maken met <a href="#create-a-connection-to-dropbox" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van het invoeren van een pad dat relatief is ten opzichte van <code>https://api.dropboxapi.com</code> . Bijvoorbeeld: <code>/2/files/list_folder</code></p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers] </td> 
   <td> <p>Voer de gewenste aanvraagheaders in. Workfront Fusion voegt automatisch machtigingsheaders toe.</p> </td> 
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

>[!BEGINSHADEBOX]

**Voorbeeld:**

De volgende API-aanroep retourneert de eerste 10 bestanden in de map [!DNL /Text files] in uw [!DNL Dropbox] -account:

URL: `/2/files/list_folder`

Lichaam:

```
{
"path": "/Text files",
"limit": 10,
"recursive": false,
"include_deleted": false
}
```

Overeenkomsten met de zoekopdracht vindt u in de sectie Uitvoer van de module onder [!UICONTROL Bundle] > [!UICONTROL Body] > vermeldingen.

In ons voorbeeld werden 10 tickets teruggegeven.

>[!ENDSHADEBOX]

## Algemene problemen

* [Kan een bestand niet uploaden of bijwerken](#unable-to-upload-or-update-a-file)
* [Afbeeldingen waarnaar via een gedeelde koppeling wordt verwezen, worden niet gerenderd](#image-referenced-via-a-shared-link-does-not-render)

### Kan een bestand niet uploaden of bijwerken

Het uploaden of bijwerken van een bestand kan een van de volgende oorzaken hebben:

* Het geüploade bestand is te groot en overschrijdt de maximaal toegestane bestandsgrootte voor uw [!DNL Dropbox] -abonnement. U hebt ook de volledige opslaglimiet van uw [!DNL Dropbox] -account gebruikt. U moet bestaande bestanden verwijderen van uw [!DNL Dropbox] -account of uw abonnement upgraden.
* De eerder geselecteerde map waarnaar het bestand wordt geüpload, bestaat niet meer. Het scenario stopt en u moet de doelmap opnieuw selecteren.

### Afbeeldingen waarnaar via een gedeelde koppeling wordt verwezen, worden niet gerenderd

De URL die wordt geretourneerd door [!UICONTROL Dropbox] > [!UICONTROL Create a shared link] , is niet rechtstreeks gekoppeld aan een afbeelding, maar aan een pagina [!DNL Dropbox] . Als u het downloaden van de afbeelding wilt forceren, vervangt u het navolgende `?dl=0` door `?dl=1` . Als u de afbeelding wilt renderen (bijvoorbeeld in een webbrowser of in de Facebook Messenger), voegt u `&raw=1` toe aan de URL.

Als u de directe of ruwe verbinding van uw beeld voor uw website of voor andere modules van Workfront Fusion moet krijgen, moet u eerste gedeelde URL op de volgende manier wijzigen:

Oorspronkelijke URL:

`https://www.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png?dl=0`

1. Vervang `www` door `dl` .
1. Verwijderen `?dl=0` .

Uiteindelijke URL:

`https://dl.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png`

Als u de URL automatisch wilt wijzigen, kunt u de functie `replace()` twee keer gebruiken:

* www door dl vervangen

  ![ vervang www met dl ](/help/workfront-fusion/references/apps-and-modules/assets/www-to-dl-350x32.png)

* En om ?dl=0 te verwijderen

  ![ verwijder DL ](/help/workfront-fusion/references/apps-and-modules/assets/remove-dl0-350x33.png)

U kunt dit in één stap doen door de volgende functies te combineren:

![ vervang allebei ](/help/workfront-fusion/references/apps-and-modules/assets/replace-both-350x47.png)

U kunt het ook kopiëren en in het veld plakken. Vervang `1.url` door de URL.

```
{{replace(replace(1.url; "?dl=0"; ""); "www"; "dl")}}
```
