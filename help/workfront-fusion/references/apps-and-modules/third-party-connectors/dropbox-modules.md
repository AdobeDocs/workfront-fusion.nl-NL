---
title: Dropbox-modules
description: In a  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Dropbox gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.Dit staat u toe om activiteiten zoals controle, het zoeken, het terugwinnen van, het lijst van een lijst maken van, en het uitgeven van dossiers en omslagen in uw Dropbox te automatiseren.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '3203'
ht-degree: 0%

---

# [!DNL Dropbox] modules

In een [!DNL Adobe Workfront Fusion] scenario, kunt u werkschema&#39;s automatiseren die [!UICONTROL  Dropbox ] of [!DNL Dropbox Business] gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.Dit staat u toe om activiteiten zoals controle, het zoeken, het terugwinnen van, het lijst maken van, en het uitgeven van dossiers en omslagen in uw [!UICONTROL  Dropbox ] te automatiseren.

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
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
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

* Als u [!DNL Dropbox] -modules wilt gebruiken, moet u een [!DNL Dropbox] -account hebben.

>[!IMPORTANT]
>
>Dropbox moet toepassingen met meer dan 50 gebruikers goedkeuren.
>
>Zoek naar &quot;Productietoestemming&quot; in de Dropbox-handleiding voor ontwikkelaars voor meer informatie.

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

1. In om het even welke module, voegt de klik **[!UICONTROL toe]** naast het vakje van de Verbinding.

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
        <td role="rowheader">[!UICONTROL-omgeving]</td>
        <td>Selecteer of deze verbinding voor een productie of een non-productie milieu is.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL-type]</td>
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
        <td role="rowheader">[!UICONTROL-accounttype]</td>
        <td>Selecteer of u verbinding maakt met een persoonlijke Dropbox-account of een zakelijke account (Dropbox Business).</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Exclude dropbox-api-path-root header]</td>
        <td>Schakel deze optie in om de header dropbox-api-path-root uit te sluiten voor Dropbox Apps met toegang tot App Folder</td>
        </tr>
      </tbody>
    </table>

1. Klik **[!UICONTROL verdergaan]** om de verbinding te bewaren en aan de module terug te keren.## [!DNL Dropbox] modules en hun velden

## [!DNL Dropbox] modules en hun velden

Wanneer u [!DNL Dropbox] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Dropbox] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggermodules](#trigger-modules)
* [Modules voor het krijgen van  [!DNL Dropbox]  dossiers en omslagen](#modules-for-getting-dropbox-files-and-folders)
* [Modules voor het creëren en het uitgeven van  [!DNL Dropbox]  dossiers en omslagen](#modules-for-creating-and-editing-dropbox-files-and-folders)
* [Overige modules](#other-modules)

### Triggermodules

#### [!UICONTROL  de Dossiers van het Controle ]

Deze triggertypemodule retourneert bestandsgegevens wanneer het bestand in een opgegeven map wordt gewijzigd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
   <td> <p>Selecteer de map die u wilt controleren op wijzigingen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch ook subfolders]</td> 
   <td> <p> Schakel deze optie in om ook de submappen in de geselecteerde map te controleren op gewijzigde bestanden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modules voor het ophalen van [!DNL Dropbox] bestanden en mappen

* [[!UICONTROL  Download een Dossier ]](#download-a-file)
* [[!UICONTROL  krijgt Metagegevens van de Omslag ]](#get-a-folder-metadata)
* [[!UICONTROL  maak een lijst van Alle Dossiers/Subfolders in een Omslag ]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL  Herzieningen van het Dossier van de Lijst ]](#list-file-revisions)
* [[!UICONTROL  Dossiers/Omslagen van het Onderzoek ]](#search-filesfolders)

#### [!UICONTROL  Download een Dossier ]

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
   <td>[!UICONTROL-verbinding] </td> 
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

#### [!UICONTROL  krijgt Metagegevens van de Omslag ]

In deze actiemodule worden de gegevens van de gedeelde map opgehaald.

U geeft de id van de map op.

De module retourneert de id van de map en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>Gedeelde map-id</td> 
   <td> <p> Voer de id in van de map waarover u gegevens wilt ophalen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  maak een lijst van Alle Dossiers/Subfolders in een Omslag ]

In deze actiemodule worden bestanden of mappen in een bepaalde map weergegeven.

U geeft de id van de map op.

De module retourneert de id&#39;s van de bestanden of mappen en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
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

#### [!UICONTROL  Herzieningen van het Dossier van de Lijst ]

Deze actiemodule haalt alle bestandsrevisies (een versiegeschiedenis) van een bepaald bestand op.\
U geeft de id van het bestand op.

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
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

#### [!UICONTROL  Dossiers/Omslagen van het Onderzoek ]

Deze zoekmodule zoekt naar records in een object in [!DNL Dropbox] dat overeenkomt met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Voer de zoekterm in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map] </td> 
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

* [[!UICONTROL  creeer een Omslag ]](#create-a-folder)
* [[!UICONTROL  creeer/vervang een Dossier van de Tekst ]](#createoverwrite-a-text-file)
* [[!UICONTROL  creeer/werk een Verbinding van het Aandeel ] bij](#createupdate-a-share-link)
* [[!UICONTROL  Schrap een Dossier/een Omslag ]](#delete-a-filefolder)
* [[!UICONTROL  Beweeg een Dossier/een Omslag ]](#move-a-filefolder)
* [[!UICONTROL  noem een Dossier/een Omslag ] anders](#rename-a-filefolder)
* [[!UICONTROL  herstel een Dossier ]](#restore-a-file)
* [[!UICONTROL  uploadt ] a- Dossier](#upload-a-file)

#### [!UICONTROL  creeer een Omslag ]

Deze actiemodule maakt een nieuwe map.

U geeft het pad en een naam voor de map op.

De module retourneert de id van de map en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-mapnaam] </td> 
   <td> <p>Voer de naam voor de nieuwe map in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-map]</p> </td> 
   <td> <p>Voer het pad in of wijs het toe op de plaats waar u een nieuwe map wilt maken.</p> <p>Opmerking:   <p>Als u een [!DNL Dropbox Business] rekening (met teamruimten) gebruikt, moet u de schuine streep <code>/</code> verwijderen, of <strong> klikt hier niet om omslag </strong> te kiezen om een teamomslag in de wortel tot stand te brengen.</p> <p>Als de schuine streep niet wordt verwijderd, wordt een fout <code>[409] path/malformed_path/..</code> geretourneerd.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Auto rename]</td> 
   <td> <p> Schakel deze optie in om de naam van de nieuwe map te wijzigen als er al een map met dezelfde naam bestaat op de doellocatie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  creeer/vervang een Dossier van de Tekst ]

Deze actiemodule maakt een DOC-bestand of overschrijft de inhoud van een bestaand bestand.

U geeft het bronbestand en de map op.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL selecteren tot]</td> 
   <td> <p> Selecteer of u een DOC-bestand wilt maken of overschrijven.</p><ul><li><b>Maken</b></p>Selecteer de map waarin u een bestand wilt maken.</li><li><b>Overschrijven</b><p>Selecteer hoe u het bestand wilt kiezen dat u wilt overschrijven, wijs vervolgens het bestandspad toe of selecteer het bestand. </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source-bestand]</p> </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de inhoud van het bronbestand toe. </p> <p>Als u een dossier creeert, uitgezocht <b> Leeg </b>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  creeer/werk een Verbinding van het Aandeel ] bij

In deze actiemodule wordt een openbare koppeling naar een bestand gemaakt.

U geeft het bestand en de informatie over de koppeling op.

De module retourneert de id van de koppeling en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-manier waarop bestanden worden geselecteerd]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-bestandspad / -bestand]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL-bestandspad]</p> <p>Typ of wijs het pad naar het doelbestand toe.</p> <p style="font-weight: bold;">[!UICONTROL-bestand]</p> <p>Selecteer het doelbestand.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL heeft zichtbaarheid aangevraagd]</p> </td> 
   <td> <p>Selecteer of de verbinding openbaar, voor team, of wachtwoord beperkt is.</p> <p><b>Opmerking:</b></p><p> [!Alleen het UICONTROL-team] is alleen beschikbaar voor zakelijke Dropbox-accounts. [!UICONTROL Access with password] is alleen beschikbaar voor [!DNL Dropbox Pro] - of Dropbox Business-accounts.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Link's Expiration Date]</td> 
   <td> <p> Voer de datum en tijd in waarop de koppeling verloopt en niet meer toegankelijk is. Als dit veld leeg blijft, verloopt de koppeling niet. Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override=""> Druk van het Type </a>.</p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!Toegangsniveau van de Verbinding UICONTROL]</p> </td> 
   <td> <p>Stel de machtigingen voor de ontvanger van de koppeling in.</p> <ul><li><strong>[!UICONTROL Viewer] </strong> <p>Gebruikers die de koppeling gebruiken, kunnen de inhoud weergeven en opmerkingen plaatsen.</p> </li><li><strong>[!UICONTROL Editor]</strong><p> Gebruikers die de koppeling gebruiken, kunnen de inhoud bewerken, weergeven en opmerkingen plaatsen. Dit toegangsniveau is alleen beschikbaar voor documenten in de cloud.</p> </li><li><strong>[!UICONTROL Max] </strong> <p>Gebruikers die de koppeling gebruiken, ontvangen het maximale toegangsniveau waarop u de koppeling kunt instellen.</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL  Schrap een Dossier/een Omslag ]

Met deze actiemodule verwijdert u een bestand of map.

U geeft het bestand of de map op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-manier waarop bestanden worden geselecteerd]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File or Folder Path] / [!UICONTROL File or Folder]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL-bestands-/mappad]</p> <p>Voer het doelpad in of wijs dit toe aan het bestand of de map.</p> <p style="font-weight: bold;">[!UICONTROL-bestand/map]</p> <p>Selecteer het bestand of de map in het menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  Beweeg een Dossier/een Omslag ]

Deze actiemodule verplaatst een bestand of map naar een andere locatie.

U geeft het bestand of de map op en bepaalt hoe en waar u het bestand of de map wilt verplaatsen.

De module retourneert de id van het bestand of de map en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Methode om bestanden/mappen te selecteren] </td> 
   <td> <p>Selecteer of u het bestands- of mappad wilt toewijzen of invoeren, of selecteer het bestand of de map handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-bestand / mappad] /</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL-bestands-/mappad]</p> <p>Voer het doelpad in of wijs dit toe aan het bestand of de map.</p> <p style="font-weight: bold;">[!UICONTROL-bestand/map]</p> <p>Selecteer of u een bestand of map verplaatst, en vervolgens het bestand of de map.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL naar map]</p> </td> 
   <td> <p>Voer de doellocatie voor het bestand of de map in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Nieuwe naam]</p> </td> 
   <td> <p>Voer de nieuwe naam voor het bestand of de map op de nieuwe locatie in.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Naam automatisch wijzigen]</p> </td> 
   <td> <p>Schakel deze optie in om ervoor te zorgen dat als er al een bestand of map met dezelfde naam bestaat, de module de naam van het nieuwe bestand of de nieuwe map wijzigt door ([!UICONTROL NUMBER]) achter de bestands- of mapnaam toe te voegen. Anders wordt het bestand of de map op de doellocatie overschreven.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL toestaan eigendomsoverdracht]</p> </td> 
   <td> <p>Schakel deze optie in om verplaatsing door de eigenaar toe te staan, zelfs als dit zou leiden tot een eigendomsoverdracht voor de inhoud die wordt verplaatst.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  noem een Dossier/een Omslag ] anders

In deze actiemodule wordt de naam van een bestand of map gewijzigd.

U geeft het bestand of de map en de nieuwe naam op.

De module retourneert de id van het bestand of de map en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
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


#### [!UICONTROL  herstel een Dossier ]

In deze actiemodule wordt een vorige versie van een bestand hersteld.

U geeft het bestand en het nummer van de gewenste revisie op.

De module retourneert de id van de versie en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-manier waarop bestanden worden geselecteerd]</td> 
   <td> <p> Selecteer of u het bestandspad wilt toewijzen of invoeren, of selecteer het bestand handmatig.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL-bestandspad] / [!UICONTROL-bestand]</p> </td> 
   <td> <p><strong>[!UICONTROL-bestandspad]</strong> </p> <p>Typ of wijs het doelpad naar het bestand toe.</p> <p><strong>[!UICONTROL File]</strong> </p> <p>Selecteer het bestand in het menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Revision]</p> </td> 
   <td> <p>Ga of kaart het revisieaantal van de revisie in u wilt herstellen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL  upload een Dossier ]

Deze actiemodule uploadt een bestand naar een map.

U geeft informatie op zoals de locatie van het bestand, het bestand dat u wilt uploaden en een optionele nieuwe naam voor het bestand.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-map]</td> 
   <td> <p> Selecteer de map van de [!DNL Dropbox] waarnaar u het bestand wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source-bestand]</p> </td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> <p><b>Opmerking:</b></p><p> De maximale grootte van het geüploade bestand is 150 MB.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL overschrijft een bestaand bestand]</td> 
   <td> <p> Schakel deze optie in om het bestaande bestand te vervangen door het nieuwe bestand. Als deze optie niet is ingeschakeld, wordt de naam van het geüploade bestand gewijzigd.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Overige modules

#### [!UICONTROL  maak een API Vraag ]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Dropbox] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Dropbox] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL-verbinding] </td> 
   <td> <p>Zie <a href="#create-a-connection-to-dropbox" class="MCXref xref"> Verbinding maken met [!DNL Dropbox]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Dropbox] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van het invoeren van een pad dat relatief is ten opzichte van <code>https://api.dropboxapi.com</code> . Bijvoorbeeld: <code>/2/files/list_folder</code></p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL, methode]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-kopteksten] </td> 
   <td> <p>Voer de gewenste aanvraagheaders in. [!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL-queryreeks]</td> 
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

De gelijken van het onderzoek kunnen in de Output van de module onder [!UICONTROL  Bundel ] worden gevonden > [!UICONTROL  Lichaam ] > ingangen.

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

URL die door [!UICONTROL  Dropbox ] wordt teruggekeerd > [!UICONTROL  creeer een gedeelde verbinding ] niet direct met een beeld, maar met een [!DNL Dropbox] pagina verbindt. Als u het downloaden van de afbeelding wilt forceren, vervangt u het navolgende `?dl=0` door `?dl=1` . Als u de afbeelding wilt renderen (bijvoorbeeld in een webbrowser of in de Facebook Messenger), voegt u `&raw=1` toe aan de URL.

Als u de directe of ruwe verbinding van uw beeld voor uw website of voor andere [!DNL Workfront Fusion] modules moet krijgen, moet u eerste gedeelde URL op de volgende manier wijzigen:

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
