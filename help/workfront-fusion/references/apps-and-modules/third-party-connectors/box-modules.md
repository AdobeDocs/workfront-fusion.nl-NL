---
title: Box-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Box gebruiken en deze koppelen aan meerdere toepassingen en services van derden. bewaakt een opgegeven map om te controleren op bestandswijzigingen, om bestaande bestanden te wijzigen en te verwijderen of om nieuwe bestanden te uploaden naar een map.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# Box-modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Box] gebruiken en deze koppelen aan meerdere toepassingen en services van derden. bewaakt een opgegeven map om te controleren op bestandswijzigingen, om bestaande bestanden te wijzigen en te verwijderen of om nieuwe bestanden te uploaden naar een map.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Als u [!DNL Box] -modules wilt gebruiken, moet u een [!DNL Box] -account hebben.

## Box API-informatie

De Box-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] modules en hun velden

Wanneer u [!DNL Box] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Box] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

* [[!UICONTROL New File Event]](#new-file-event)
* [Nieuwe mapgebeurtenis](#new-folder-event)
* [[!UICONTROL Watch Files]](#watch-files)

#### [!UICONTROL New File Event]

Deze instant triggermodule start een scenario wanneer een geselecteerde actie plaatsvindt op een bestand.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer de webhaak die u wilt gebruiken om uitgaande berichten te bekijken of voeg een webhaak toe. </p><p>Als u een webhaak wilt toevoegen, klikt u op <strong>[!UICONTROL Add]</strong> en voert u de naam en de verbinding van de webhaak in, het bestand dat u wilt controleren en de triggers waarop u wilt letten.</p> <p> Voor instructies over het verbinden van uw [!UICONTROL Box] rekening met [!UICONTROL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> verbinden met de dienst - Basisinstructies </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Nieuwe mapgebeurtenis

Deze instant triggermodule start een scenario wanneer de selectieactie in de map plaatsvindt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer de webhaak die u wilt gebruiken om uitgaande berichten te bekijken of voeg een webhaak toe. </p><p>Als u een webhaak wilt toevoegen, klikt u op <strong>[!UICONTROL Add]</strong> en voert u de naam en de verbinding van de webhaak in, de map die u wilt controleren en de triggers die u wilt controleren.</p> <p> Voor instructies over het verbinden van uw [!UICONTROL Box] rekening met [!UICONTROL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> verbinden met de dienst - Basisinstructies </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Files]

Deze triggermodule start een scenario wanneer een nieuw bestand wordt toegevoegd of een bestaand bestand wordt bijgewerkt in een map die wordt gecontroleerd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Box] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  <tr> 
   <td role="rowheader">Controleren in map</td> 
   <td> <p>Selecteer de map die u wilt controleren. Een scenario kan op één enkele omslag letten.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Controle</td> 
   <td> <p>Selecteer het type bestanden dat u wilt bekijken.</p> 
    <ul> 
     <li> <p><strong> slechts nieuwe dossiers </strong> </p> <p>Het scenario wordt gestart wanneer een nieuw bestand wordt toegevoegd.</p> </li> 
     <li> <p><strong> Nieuwe dossiers en alle veranderingen </strong> </p> <p>Het scenario begint wanneer een dossier wordt toegevoegd, of wanneer de dossierinhoud of een dossierattribuut (zoals zijn naam) wordt gewijzigd.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Maximumaantal gedownloade bestanden</p> </td> 
   <td> <p>Ga het hoogste aantal dossiers in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

<!--* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] a file](#upload-a-file)-->
* [Een map maken](#create-a-folder)
* [Een map ophalen](#get-a-folder)
* [Metagegevens van map ophalen](#get-folder-metadata)
* [Maak een API Vraag](#make-an-api-call)
* [Metagegevens van map bijwerken](#update-folder-metadata)

<!--#### [!UICONTROL Delete a file] 

This action module deletes a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module downloads a file.

You specify the ID of the file.

>[!NOTE]
>
>This module is useful for providing files to subsequent modules.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file] 

This action module updates a file.

You specify the ID of the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file] 

This action module uploads a file.

You specify the file. You can also provide a new filename for the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder where you want to upload the file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If this module is not successful, consider the following:
>
>* The size of the file might exceed the maximum file size limit for your [!DNL Box] plan, or you may have used all of your [!DNL Box] account's storage quota. To get more storage space, delete existing files from [!DNL Box] or upgrade your [!DNL Box] account.
>* [!DNL Box] does not upload more than one files with the same name to a single folder. If the destination folder contains a file with the same name as the file being uploaded, the scenario run terminates with an error. To avoid this, rename the file. If you want to update the file, use the **[!UICONTROL Update a file]** module.-->

#### Een map maken

Deze actiemodule maakt een nieuwe lege map in de opgegeven bovenliggende map.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Box] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Voer een naam voor de nieuwe map in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder]</td> 
   <td> <p>Selecteer de map waarin u de nieuwe map wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Upload Email Access]</td> 
   <td> <p>Wanneer deze parameter is ingesteld, kunnen gebruikers bestanden e-mailen naar het e-mailadres dat automatisch voor deze map is gemaakt. Met de opties voor medewerkers kunt u alleen geregistreerde e-mails voor deelnemers gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Synchronization State]</td> 
   <td> <p>Geeft aan of een map moet worden gesynchroniseerd met het apparaat van de gebruiker. Deze wordt gebruikt door Box Sync (gestopt) en wordt niet gebruikt door Box Drive.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een map ophalen

Deze actiemodule haalt details voor een map op, inclusief de eerste 100 items in de map.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Box] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selecteer de map waarvoor u de gegevens wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Metagegevens van map ophalen

Deze actiemodule wint omslagmeta-gegevens door omslag ID terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Box] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Selecteer het bereik dat u voor deze metagegevensophaling wilt gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selecteer de map waarvoor u metagegevens wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Maak een API Vraag

Deze actiemodule maakt een aangepaste aanroep van de Box API.



<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie [!DNL Bynder] Verbinding maken <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref"> met Workfront Fusion [!DNL Bynder] in dit artikel voor instructies over het verbinden van uw </a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://api.box.com</code> . <p>Voorbeeld: <code>/2.0/users/me</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
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

#### Metagegevens van map bijwerken

In deze actiemodule worden de metagegevens van een map gemaakt of bijgewerkt.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Box] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Selecteer het bereik dat u wilt gebruiken voor deze update van metagegevens.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selecteer de map waarvoor u metagegevens wilt bijwerken.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Zoekopdrachten

#### Inhoud zoeken

Deze zoekmodule zoekt naar items die beschikbaar zijn voor de gebruiker of de hele onderneming.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Box] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Voer de tekenreeks in of wijs de tekenreeks toe waarnaar u wilt zoeken. Deze query wordt gekoppeld aan itemnamen, beschrijvingen, tekstinhoud van bestanden en diverse andere velden van de verschillende itemtypen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Selecteer of u naar inhoud die aan de gebruiker wordt geassocieerd zoekt de waarvan geloofsbrieven voor de verbinding worden gebruikt in deze module wordt gebruikt, of het zoeken naar inhoud verbonden aan de volledige onderneming.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Selecteer of u naar bestanden, mappen of webkoppelingen zoekt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>Selecteer of u wilt sorteren op relevantie of op gewijzigde datum.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trash Content]</td> 
   <td> <p>Selecteer of u de verouderde inhoud of de inhoud wilt zoeken die niet is vervormd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder IDs]</td> 
   <td> <p>Om in een specifieke omslag te zoeken, voor elke omslag u wilt zoeken, <b> toevoegen punt </b> en ingaan identiteitskaart van de omslag. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created From]</td> 
   <td> <p>Als u wilt zoeken naar elementen die in een bepaald datumbereik zijn gemaakt, voert u de vroegste datum in het bereik in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created to]</td> 
   <td> <p>Als u wilt zoeken naar elementen die in een bepaald datumbereik zijn gemaakt, voert u de laatste datum in het bereik in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Updated From]</td> 
   <td> <p>Als u wilt zoeken naar elementen die in een bepaald datumbereik zijn bijgewerkt, voert u de vroegste datum in het bereik in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Updated to]</td> 
   <td> <p>Als u wilt zoeken naar elementen die in een bepaald datumbereik zijn bijgewerkt, voert u de laatste datum in het bereik in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Voor elk attribuut dat u in de reactie van de module wilt terugkeren, klik <b> toevoegen punt </b> en ga het gebied in.</p><p>Hiermee kunt u velden aanvragen die normaal niet worden geretourneerd in een standaardreactie. Houd er rekening mee dat het opgeven van deze parameter het effect heeft dat geen van de standaardvelden wordt geretourneerd in het antwoord, tenzij dit expliciet wordt opgegeven. </p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Extensions]</td> 
   <td> <p>Als u de zoekopdracht wilt beperken tot specifieke bestandsextensies, voert u een door komma's gescheiden lijst met bestandsextensies in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size From]</td> 
   <td> <p>Als u wilt zoeken naar elementen in een specifiek formaatbereik, voert u het kleine uiteinde van het bereik in bytes in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size To]</td> 
   <td> <p>Als u wilt zoeken naar elementen in een specifiek formaatbereik, voert u het grote uiteinde van het bereik in bytes in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner User ID]</td> 
   <td> <p>Als u wilt zoeken naar elementen die eigendom zijn van specifieke gebruikers, voert u een door komma's gescheiden lijst met eigenaars-id's in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal resultaten in dat u de module in elke uitvoeringscyclus wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>


