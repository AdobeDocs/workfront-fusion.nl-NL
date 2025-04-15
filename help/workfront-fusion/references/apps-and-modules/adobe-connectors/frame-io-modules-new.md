---
title: Frame.io-modules
description: De  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io]  rekening.
author: Becky
feature: Workfront Fusion
source-git-commit: c0b08b206f69d6af3b629c5d31cc0b840edea766
workflow-type: tm+mt
source-wordcount: '1869'
ht-degree: 0%

---

# [!DNL Frame.io] Beta-modules (V4)

>[!IMPORTANT]
>
>Dit artikel beschrijft de nieuwe (bèta) versie van de schakelaar Frame.io. Deze connector wordt gebruikt om verbinding te maken met Frame.io versie 4.
>
>Voor instructies op de erfenisversie van de schakelaar Frame.io, zie [ schakelaar van de Verouderde ouder Frame.io ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Met de modules [!DNL Adobe Workfront Fusion] [!DNL Frame.io] kunt u elementen en opmerkingen in uw [!DNL Frame.io] -account controleren, maken, bijwerken, ophalen of verwijderen.

Workfront biedt twee Frame.io-connectors, gebaseerd op de versie van Frame.io waarmee u verbinding maakt.

| Connector | Frame.io-versie |
|---|---|
| Frame.io (Beta) | V4 |
| Frame.io (Verouderd) | V3 |

Voor instructies op de erfenisversie van de schakelaar Frame.io, zie [ schakelaar van de Verouderde ouder Frame.io ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Voor een videoinleiding aan de Schakelaar Frame.io, zie:

* [ Frame.io ](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

Als u [!DNL Frame.io] modules wilt gebruiken, moet u een [!DNL Frame.io] account hebben

## Frame.io API-informatie

De connector Frame.io gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.frame.io/v2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Frame.io] met [!UICONTROL Adobe Workfront Fusion]

Het verbindingsproces is afhankelijk van de vraag of u de Verouderde Frame.io-connector of de Beta Frame.io-connector gebruikt.

1. Klik in een willekeurige Frame.io Beta-module op **[!UICONTROL Add]** naast het vak Verbinding.

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Selecteer of u een IMD-gebruikersverificatieverbinding of een IMS Server-naar-serververbinding wilt maken.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Voer een naam in voor deze verbinding.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Voer uw [!DNL Adobe] [!UICONTROL Client ID] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .<p>Voor instructies die van geloofsbrieven de plaats bepalen, zie <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" > Geloofsbrieven </a> in de de ontwikkelaarsdocumentatie van Adobe.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .<p>Voor instructies die van geloofsbrieven de plaats bepalen, zie <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" > Geloofsbrieven </a> in de de ontwikkelaarsdocumentatie van Adobe.</p>
        </tr>
       </tbody>
    </table>
1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## [!DNL Frame.io] modules en hun velden

Wanneer u [!DNL Frame.io] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Frame.io] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Assets](#assets)
* [Opmerkingen](#comments)
* [Mappen](#folders)
* [Projecten](#projects)
* [Aandelen](#shares)
* [Werkruimten](#workspaces)
* [Overige](#other)

### Assets

* [[!UICONTROL Create an asset]](#create-an-asset)
* [[!UICONTROL Delete an asset]](#delete-an-asset)
* [[!UICONTROL Get an asset]](#get-an-asset)
* [[!UICONTROL List assets]](#list-assets)
* [[!UICONTROL Update an asset]](#update-an-asset)

#### [!UICONTROL Create an asset] <!--different for v4-->

Deze actiemodule maakt een nieuw element.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer de account of wijs de id van de account toe die het project bevat waarvoor u middelen wilt maken.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecteer de werkruimte of wijs identiteitskaart van de werkruimte toe die het project bevat dat u activa voor wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project of wijs identiteitskaart van het project toe dat u activa voor wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Selecteer het pad waar u elementen wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Voer de naam in van het bestand dat u voor dit element wilt gebruiken.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Bestandsgrootte </td> 
    <td> <p>Voer de bestandsgrootte in bytes in of wijs deze toe.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Als u een bestand maakt, voert u de URL in van het bestand dat u wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Selecteer het mediatype voor dit element.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Delete an asset]

Met deze actiemodule verwijdert u een opgegeven element.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer de account of wijs de id toe van de account die het element bevat dat u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer of wijs het element toe dat u wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an asset]

Deze actiemodule haalt elementdetails op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer de account of wijs de id toe van de account die het element bevat dat u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer of wijs het element toe u wilt terugwinnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List assets]

Deze zoekmodule haalt alle elementen in de opgegeven projectmap op.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer de account of wijs de id van de account toe die de elementen bevat die u wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned assets] </td> 
   <td> <p>Ga of kaart het maximumaantal activa in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Opmerkingen

* [[!UICONTROL Create a Comment]](#create-a-comment)
* [[!UICONTROL Delete a Comment]](#delete-a-comment)
* [[!UICONTROL Get a Comment]](#get-a-comment)
* [[!UICONTROL List Comments]](#list-comments)
* [[!UICONTROL Update a Comment]](#update-a-comment)

#### [!UICONTROL Create a comment]

Deze actiemodule voegt een nieuwe opmerking of reactie toe aan het element.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer de account of wijs de id toe van de account die het element bevat waaraan u een opmerking wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecteer de account of wijs de id van de werkruimte toe die het element bevat waaraan u een opmerking wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project of wijs identiteitskaart van het project toe dat de activa bevat u een commentaar aan wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Selecteer het pad naar het element waaraan u een opmerking wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Voer de tekstinhoud van de opmerking of het antwoord in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Voer het framenummer in de video in waarnaar de opmerking moet worden gekoppeld.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>Als het element een PDF is, voert u de pagina in waaraan de opmerking moet worden gekoppeld of wijst u deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a comment]

In deze actiemodule wordt een bestaande opmerking verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer de account of wijs de id van de account toe die de opmerking bevat die u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Voer de id in van de opmerking die u wilt verwijderen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a comment]

Deze actiemodule wint details van de gespecificeerde commentaar terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer de account of wijs de id van de account toe die de opmerking bevat waarover u details wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Selecteer de opmerking waarover u details wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List comments]

Deze zoekmodule haalt alle opmerkingen van het opgegeven element op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe die de activa bevat die u commentaren van wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecteer of wijs de werkruimte toe die de activa bevat die u commentaren van wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project dat het element bevat waarvan u opmerkingen wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Selecteer het pad dat leidt naar het element waarvan u opmerkingen wilt weergeven.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments] </td> 
   <td> <p>Ga of kaart het maximumaantal commentaren in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a comment]

In deze actiemodule wordt een bestaande opmerking bewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe die het project bevat dat de activa bevat u een commentaar op wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Selecteer de opmerking die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Voer de tekstinhoud van de opmerking in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Voer het framenummer in de video in waarnaar de opmerking is gekoppeld.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>Als het element een PDF is, voert u de pagina in waaraan de opmerking is gekoppeld of wijst u deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Mappen

#### Een map maken

Deze actiemodule leidt tot een nieuwe omslag in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe waar u een omslag wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecteer of wijs de werkruimte toe waar u een omslag wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer de locatie waar u een map wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Selecteer het pad waar u een map wilt maken.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Naam </td> 
   <td> <p>Voer een naam voor de nieuwe map in of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projecten

* [Een project maken](#create-a-project)
* [Projecten weergeven](#list-projects)

#### Een project maken

Deze actiemodule leidt tot een nieuw project in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe waar u een project wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecteer of wijs de werkruimte toe waar u een project wilt tot stand brengen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Naam </td> 
   <td> <p>Ga of kaart een naam voor het nieuwe project in.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Projects]

Deze onderzoeksmodule wint alle projecten voor het gespecificeerde team terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe die de activa bevat die u projecten van wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecteer of wijs de werkruimte toe die de activa bevat die u projecten van wilt terugwinnen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned projects] </td> 
   <td> <p>Ga of kaart het maximumaantal projecten in
   u wilt de module tijdens elke cyclus van de scenariouitvoering terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Aandelen

* [Middelen toevoegen aan een koppeling voor delen](#add-an-asset-to-a-share-link)
* [Een koppeling voor delen maken](#create-a-share-link)

#### Middelen toevoegen aan een koppeling voor delen

Deze actiemodules voegen activa aan een aandeelverbinding in Frame.io toe.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe die de aandeelverbinding bevat die u activa aan wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share link ID] </td> 
   <td> <p>Selecteer of wijs de aandeelverbinding toe die u een middel aan wilt toevoegen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Voer de id in van het element dat u aan de deelkoppeling wilt toevoegen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een koppeling voor delen maken

Deze actiemodule leidt tot een nieuwe aandeelverbinding in Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe waar u een aandeelverbinding wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Selecteer of wijs de werkruimte toe waar u een aandeelverbinding wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer of wijs het project toe waar u een aandeelverbinding wilt tot stand brengen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Toegang </td> 
   <td> <p>Selecteer of deze koppeling openbare of beperkte toegang heeft.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Assets </td> 
   <td> <p>Voor elk element dat u aan de aandeelverbinding wilt toevoegen, klik <b> punt </b> toevoegen en identiteitskaart van activa ingaan.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Beschrijving </td> 
   <td> <p>Voer een beschrijving voor de deelkoppeling in of wijs deze toe.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Naam </td> 
   <td> <p>Voer de vervaldatum voor de deelkoppeling in of wijs deze toe.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Naam </td> 
   <td> <p>Voer een naam in of wijs een naam toe aan de nieuwe koppeling voor delen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Naam </td> 
   <td> <p>Ga of kaart een passphrase voor de aandeelverbinding in.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Werkruimten

#### Een werkruimte maken

Deze actiemodule leidt tot een nieuwe werkruimte in Frame.io

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe waar u een werkruimte wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer een nieuwe naam voor de werkruimte in of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Werkruimten weergeven

In deze module worden alle werkruimten in een account weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Selecteer of wijs de rekening toe die de activa bevat die u werkruimten van wilt terugwinnen.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned workspaces] </td> 
   <td> <p>Het maximum aantal werkruimten invoeren of toewijzen
   u wilt de module tijdens elke cyclus van de scenariouitvoering terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige

#### [!UICONTROL Make a custom API call]

In deze module kunt u een aangepaste API-aanroep uitvoeren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van <code>https://api.frame.io</code> . Voorbeeld: <code> /v4/me</code></p> <p>Opmerking: raadpleeg de [!DNL Frame.io] API-naslaggids voor de lijst met beschikbare eindpunten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string] </td> 
   <td> <p>Voer de queryreeks voor de aanvraag in. Voor elke parameter die u in het vraagkoord wilt omvatten, klik <b>[!UICONTROL Add item]</b> en ga de naam van het gebied en de gewenste waarde in.</p> </td> 
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


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
