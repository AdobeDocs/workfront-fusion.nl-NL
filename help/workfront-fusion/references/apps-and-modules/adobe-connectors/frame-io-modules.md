---
title: Frame.io (Verouderde) modules
description: Het [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] account.
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: 31266e79d736cdb055bb0ad36a75ac61ce426ec2
workflow-type: tm+mt
source-wordcount: '2205'
ht-degree: 0%

---

# [!DNL Frame.io] Verouderde modules

>[!IMPORTANT]
>
>In dit artikel wordt de verouderde versie van de Frame.io-connector beschreven. Deze connector wordt gebruikt om verbinding te maken met Frame.io versie 3.
>
>Zie Frame.io Bètaconnector[&#128279;](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md) voor instructies over de nieuwe (bèta)versie van de Frame.io connector.

Met de [!DNL Adobe Workfront Fusion] [!DNL Frame.io] modules kunt u activa en opmerkingen in uw [!DNL Frame.io] account controleren, maken, bijwerken, ophalen of verwijderen.

Workfront biedt twee Frame.io connectoren, gebaseerd op de versie van Frame.io waarmee u verbinding maakt.

| Connector | Frame.io versie |
|---|---|
| Frame.io (bèta) | V4 |
| Frame.io (Verouderd) | V3 |

Voor instructies op de nieuwe (bèta) versie van de schakelaar Frame.io, zie [ schakelaar van Frame.io Beta ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md).

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
   <p>Nieuw:</p> <ul><li>Select- of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultiem Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>Of</p>
   <p>Current: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Zie [Toegangsvereisten in documentatie](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md) voor meer informatie over de informatie in deze tabel.

Zie licenties voor[&#128279;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md) informatie over [!DNL Adobe Workfront Fusion] licenties[!DNL Adobe Workfront Fusion] .

+++

## Voorwaarden

Om modules te gebruiken [!DNL Frame.io] , moet u een [!DNL Frame.io] account hebben

## Frame.io API-informatie

De Frame.io connector maakt gebruik van het volgende:

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

U kunt verbinding maken met [!DNL Frame.io] via een API-token of met OAuth 2.0.

[Verbind met  [!DNL Frame.io]  gebruikend een API teken](#connect-to-frameio-using-an-api-token)

[Verbind met  [!DNL Frame.io]  gebruikend OAuth 2.0 PKCE](#connect-to-frameio-using-oauth-20-pkce)

### Verbinding maken met [!DNL Frame.io] via een API-token

Als u uw [!DNL Frame.io] -account wilt verbinden met [!DNL Workfront Fusion] via een API-token, moet u het API-token in uw [!DNL Frame.io] -account maken en dit in het dialoogvenster [!DNL Workfront Fusion] [!DNL Frame.io] [!UICONTROL Create a connection] invoegen.

1. Meld u aan bij uw [!DNL Frame.io] -account.
1. Ga naar de pagina **[!UICONTROL Tokens]** in de [!DNL Frame.io] Developer.
1. Klik op **[!UICONTROL New]**.
1. Voer de naam van het token in, selecteer het bereik dat u wilt gebruiken en klik op **[!UICONTROL Create]** .
1. Kopieer de opgegeven token.
1. Ga naar [!DNL Workfront Fusion] en open het dialoogvenster [!DNL Frame.io] module **[!UICONTROL Create a connection]** .
1. Selecteer in het **[!UICONTROL Connection type]** veld de optie **[!DNL Frame.io]**.
1. Voer het token in dat je in stap 5 hebt gekopieerd naar het **[!UICONTROL Your [!DNL Frame.io] API Key]** veld
1. Klik **[!UICONTROL Continue]** om de verbinding tot stand te brengen en terug te keren naar de module.

### Maak verbinding met [!DNL Frame.io] OAuth 2.0 PKCE

U kunt een verbinding maken met [!DNL Frame.io] OAuth 2.0 PKCE met een optionele client-ID. Als u een client-ID wilt opnemen in uw verbinding, moet u een OAuth 2.0-app maken in uw [!DNL Frame.io] account.

* [Maak verbinding met [!DNL Frame.io] behulp van OAuth 2.0 PKCE (zonder client-ID)](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [Maak verbinding met [!DNL Frame.io] behulp van OAuth 2.0 PKCE (met client-ID)](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### Maak verbinding met [!DNL Frame.io] behulp van OAuth 2.0 PKCE (zonder client-ID)

1. Ga naar [!DNL Workfront Fusion] en open het dialoogvenster van **[!UICONTROL Create a connection]** de [!DNL Frame.io] module.
1. Selecteer in het **[!UICONTROL Connection type]** veld de optie **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]**.
1. Voer een naam in voor de nieuwe verbinding in het **[!UICONTROL Connection name]** veld.
1. Klik op **[!UICONTROL Continue]** om de verbinding tot stand te brengen en terug te keren naar de module.

#### Verbinding maken met [!DNL Frame.io] via OAuth 2.0 PKCE (met client-id)

1. Maak een OAuth 2.0-app in [!DNL Frame.io] . Zie de [!DNL Frame.io] -documentatie op [!UICONTROL OAuth 2.0 Code Authorization Flow] voor instructies.

   >[!IMPORTANT]
   >
   >Wanneer u de OAuth 2.0-app maakt in [!DNL Frame.io] :
   >
   >* Voer het volgende in als de omleidings-URI:
   >   
   >     * **Noord- en Zuid-Amerika / APAC:**`https://app.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >     * **EMEA:**`https://app-eu.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >* Schakel de PCKE-optie in.


1. Kopieer de opgegeven `client_id` .
1. Ga naar [!DNL Workfront Fusion] en open het dialoogvenster [!DNL Frame.io] module **[!UICONTROL Create a connection]** .
1. Selecteer **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]** in het veld **[!UICONTROL Connection type]** .
1. Voer in het veld **[!UICONTROL Connection name]** een naam in voor de nieuwe verbinding.
1. Klik op **[!UICONTROL Show advanced settings]**.
1. Voer de `client_id` die u in stap 2 naar het veld **[!UICONTROL Client ID]** hebt gekopieerd in.
1. Klik op **[!UICONTROL Continue]** om de verbinding tot stand te brengen en terug te keren naar de module.

## [!DNL Frame.io] modules en hun vakgebieden

Wanneer u [!DNL Frame.io] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Frame.io] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Assets](#assets)
* [Opmerkingen](#comments)
* [Projecten](#projects)
* [Ander](#other)

### Activa

* [[!UICONTROL Create an Asset]](#create-an-asset)
* [[!UICONTROL Delete an Asset]](#delete-an-asset)
* [[!UICONTROL Get an Asset]](#get-an-asset)
* [[!UICONTROL List Assets]](#list-assets)
* [[!UICONTROL Update an Asset]](#update-an-asset)
* [[!UICONTROL Watch Asset Deleted]](#watch-asset-deleted)
* [[!UICONTROL Watch Asset Label Updated]](#watch-asset-label-updated)
* [[!UICONTROL Watch New Asset]](#watch-new-asset)

#### [!UICONTROL Create an Asset]

Met deze actiemodule wordt een nieuw element gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinding [!DNL Frame.io] maken met [!DNL Frame.io][!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team in kaart dat het project bezit dat u activa voor wilt creëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project of wijs identiteitskaart van het project toe dat u activa voor wilt tot stand brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map of wijs de id toe van de map waarin u middelen wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selecteer of u een map of bestand wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer de naam van het nieuwe bestand of de nieuwe map in.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">File Type </td> 
    <td> <p>Select the type of file you want to upload.</p> </td> 
   </tr>
  --> <!--
   <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>The file size in bytes.</p> </td> 
   </tr>
  --> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Als u een bestand maakt, voert u de URL in van het bestand dat u wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Als u een bestand maakt, voert u een korte beschrijving van het element in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Label] </td> 
   <td> <p>Als u een bestand maakt, selecteert u of het bestand in uitvoering is, moet worden gecontroleerd of goedgekeurd.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Asset]

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
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team toe dat het project bezit dat de activa bevat u wilt schrappen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecteer het project of het element dat u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map met het element dat u wilt verwijderen</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer of wijs het element toe dat u wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Asset]

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
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team in kaart dat het project bezit dat de activa bevat u details over wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecteer het project dat het element bevat waarover u details wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map met het element waarover u meer informatie wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer het element of wijs de id van het element toe waarover u details wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Assets]

Deze zoekmodule haalt alle elementen in de opgegeven projectmap op.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinding [!DNL Frame.io] maken met [!DNL Frame.io][!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team toe dat eigenaar is van het project dat de map bevat waaruit u middelen wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecteer het project dat de map bevat waaruit u middelen wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map waaruit u items wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Voer het maximum aantal activa in of wijs het maximum aantal activa toe dat u wilt dat de module retourneert tijdens elke uitvoeringscyclus van scenario's.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an Asset]

Met deze actiemodule kunt u de naam, beschrijving of aangepaste velden van een bestaand item bijwerken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinding [!DNL Frame.io] maken met [!DNL Frame.io][!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team toe dat eigenaar is van het project waarvoor u een item wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project of wijs de ID toe van het project waarvoor u een asset wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map of wijs de ID toe van de map waarin u een asset wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Voer de ID in of wijs deze toe van het item dat u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer de naam van het bijgewerkte bestand in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Voer een korte beschrijving in van het bijgewerkte element.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Deleted]

Deze trekkermodule begint een scenario wanneer activa die tot het gespecificeerde team behoren wordt geschrapt.

Omdat dit een directe trigger is, moet u een webhaak selecteren of maken die de module kan gebruiken.

Als u een webhaak toevoegt, voert u de volgende informatie in.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Voer een naam in voor de webhaak, bijvoorbeeld ''Element verwijderd''.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinding [!DNL Frame.io] maken met [!DNL Frame.io][!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer het team waarvoor deze webhook is gemaakt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Label Updated]

Deze triggermodule start een scenario wanneer een label voor een element dat eigendom is van de opgegeven teamset, wordt gewijzigd of verwijderd.

Omdat dit een directe trigger is, moet u een webhaak selecteren of maken die de module kan gebruiken.

Als u een webhaak toevoegt, voert u de volgende informatie in.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Voer een naam voor de webhaak in, bijvoorbeeld "Status van element bijgewerkt".</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer het team waarvoor deze webhaak is gemaakt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Asset]

Deze trekkermodule begint een scenario wanneer een nieuw middel voor het gespecificeerde team wordt gecreeerd.

Omdat dit een directe trigger is, moet u een webhook selecteren of maken die de module wilt gebruiken.

Als u een webhook toevoegt, voert u de volgende gegevens in.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Voer een naam in voor de webhaak, bijvoorbeeld "Element gemaakt".</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer het team waarvoor deze webhaak is gemaakt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Opmerkingen

* [[!UICONTROL Create a Comment]](#create-a-comment)
* [[!UICONTROL Delete a Comment]](#delete-a-comment)
* [[!UICONTROL Get a Comment]](#get-a-comment)
* [[!UICONTROL List Comments]](#list-comments)
* [[!UICONTROL Update a Comment]](#update-a-comment)
* [[!UICONTROL Watch Comment Updated]](#watch-comment-updated)
* [[!UICONTROL Watch New Comment]](#watch-new-comment)

#### [!UICONTROL Create a Comment]

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
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selecteer of u een opmerking wilt maken of op een opmerking wilt reageren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team in kaart dat het project bezit dat de activa bevat u een commentaar aan wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project of wijs identiteitskaart van het project toe dat de activa bevat u een commentaar aan wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map of wijs de id toe van de map met het element waaraan u een opmerking wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer of wijs het element toe waaraan u een opmerking wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Selecteer of wijs de commentaar toe u een antwoord aan wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Voer de tekstinhoud van de opmerking of het antwoord in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Voer het framenummer in de video in waarnaar de opmerking moet worden gekoppeld.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Comment]

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
   <td role="rowheader">[!UICONTROL Team ID]</td> 
   <td> <p> Selecteer of wijs het team toe dat het project bezit dat de activa bevat u een commentaar van wilt schrappen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Selecteer het project of wijs identiteitskaart van het project toe dat de activa bevat u een commentaar van wilt schrappen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p> Selecteer de map met het element waaruit u een opmerking wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Voer de id in van het element dat de opmerking bevat die u wilt verwijderen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Voer de id in van de opmerking die u wilt verwijderen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Comment]

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
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team toe dat het project bezit dat de omslag bevat u activa van wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project dat de map bevat waarvan u elementen wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map waarvan u elementen wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer het element dat de opmerking bevat die u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Selecteer de opmerking waarover u details wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Comments]

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
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team toe dat het project bezit dat de omslag bevat u commentaren van wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project dat de map bevat waarvan u de opmerkingen wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map met het element waaruit u de opmerkingen wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer het item waarvoor u opmerkingen wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Voer het maximum aantal opmerkingen in of wijs het toe dat u wilt dat de module retourneert tijdens elke uitvoeringscyclus van het scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Comment]

Deze actiemodule bewerkt een bestaande opmerking.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Verbinding [!DNL Frame.io] maken met [!DNL Frame.io][!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of wijs het team toe dat eigenaar is van het project dat het item bevat waarop u een opmerking wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Selecteer het project dat het element bevat waarop u een opmerking wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Selecteer de map met het item waarvoor u een opmerking wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Selecteer het item waarvoor u een opmerking wilt bijwerken.</p> </td> 
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
   <td> <p>Voer het framenummer in de video in waarnaar de reactie is gelinkt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comment Updated]

Deze triggermodule start een scenario wanneer een opmerking wordt bewerkt.

Omdat dit een directe trigger is, moet u een webhaak selecteren of maken die de module kan gebruiken.

Als u een webhaak toevoegt, voert u de volgende informatie in.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Voer de naam van de webhaak in, bijvoorbeeld Opmerking bewerkt.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer het team waarvoor deze webhook is gemaakt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Comment]

Deze triggermodule start een scenario wanneer een nieuwe opmerking of antwoord wordt gemaakt.

Omdat dit een directe trigger is, moet u een webhaak selecteren of maken die de module kan gebruiken.

Als u een webhaak toevoegt, voert u de volgende informatie in.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Voer de naam van de webhaak in, bijvoorbeeld Nieuwe opmerking.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Zie <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Frame.io] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Frame.io] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer het team waarvoor deze webhaak is gemaakt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projecten

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
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Selecteer of kaart het team u projecten voor wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal projecten in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige

#### [!UICONTROL Make an API Call]

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
   <td> <p>Voer een pad in dat relatief is ten opzichte van <code>https://api.frame.io</code> . Voorbeeld: <code> /v2/teams</code></p> <p>Opmerking: raadpleeg de [!DNL Frame.io] API-naslaggids voor de lijst met beschikbare eindpunten.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Query String] </td> 
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
