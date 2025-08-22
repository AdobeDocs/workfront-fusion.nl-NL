---
title: Adobe Lightroom-modules
description: Met de Adobe Lightroom-modules kunt u een Adobe Workfront Fusion-scenario starten op basis van gebeurtenissen in uw Adobe Lightroom-account.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2738'
ht-degree: 0%

---

# [!DNL Adobe Lightroom] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Adobe Lightroom] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [ een scenario creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Voordat u de [!DNL Adobe Lightroom] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!DNL Adobe Lightroom] account hebben.
* U moet een OAuth Web App hebben die in Adobe Admin Console wordt gevormd. Voor details zie [ een toepassing OAuth in Adobe Admin Console ](#configure-an-oauth-application-in-the-adobe-admin-console) in dit artikel vormen.

## Adobe Lightroom API-informatie

De Adobe Lightroom-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://lr.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.17.128</td> 
  </tr>
 </tbody> 
 </table>



## Verbinding maken met Adobe Lightroom

Als u verbinding wilt maken met Adobe Lightroom, moet u eerst een OAuth-app configureren in de Adobe Admin Console. Nadat deze app is geconfigureerd, kunt u verbindingen maken met Workfront Fusion.

### Een OAuth-toepassing configureren in de Adobe Admin Console

1. Beginnen met het configureren van een OAuth Web App in de Adobe Admin Console.

   Voor instructies, zie {de Gids van de Implementatie van de Authentificatie van 0} Gebruiker [ in de de ontwikkelaarsdocumentatie van Adobe.](https://developer.adobe.com/developer-console/docs/guides/authentication/UserAuthentication/implementation)
1. Wanneer het vormen van OAuth Web App, ga de volgende waarden in:

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>
          <ul>
            <li>AdobeID</li>
            <li>lr_partner_rendition_apis</li>
            <li>openhartig</li>
            <li>offline_access</li>
            <li>lr_partner_apis</li>
          </ul>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Redirect URI]</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Redirect URI pattern]</td>
        <td><code>https://app\.workfrontfusion\.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
      </tbody>
    </table>

### Verbinding maken met Adobe Lightroom vanuit Workfront Fusion

Verbinding maken voor uw [!DNL Adobe Lightroom] -modules:

1. Klik in een willekeurige Adobe Lightroom-module op **[!UICONTROL Add]** naast het vak Verbinding.

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
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!UICONTROL Adobe] [!UICONTROL Client ID] in. Dit vindt u in het gedeelte [!UICONTROL Credentials] Details van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in het gedeelte [!UICONTROL Credentials] Details van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.


## Adobe Lightroom-modules en hun velden

Wanneer u [!DNL Adobe Lightroom] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Lightroom] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Overige](#other)
* [Assets](#assets)
* [Albums](#albums)

### Overige

* [Health check](#health-check)
* [Metagegevens uit gebruikerscatalogus ophalen](#retrieve-user-catalog-metadata)

#### Health check

Deze actiemodule haalt een versie-id van de Lightroom-server op, om aan te tonen of de Lightroom-service momenteel wordt uitgevoerd.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Als u specifieke geloofsbrieven wilt leveren om ervoor te zorgen dat een specifieke server loopt, klik <b> toevoegen punt </b> en ga de geloofsbrieven in.</p><p>Autorisatiekoppen worden automatisch toegevoegd.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Metagegevens uit gebruikerscatalogus ophalen

Deze actiemodule wint meta-gegevens van een catalogus in Adobe Lightroom terug. Een catalogus bevat elementen, albums of andere bronnen.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Als u specifieke referenties wilt opgeven om ervoor te zorgen dat u toegang hebt tot de juiste gebruikersaccount, klikt u op Item toevoegen en voert u de referenties in.</p><p>Autorisatiekoppen worden automatisch toegevoegd.</p>
      </td>
    </tr>
  </tbody>
</table>

### Assets

* [Origineel elementbestand maken](#create-an-asset-original-file)
* [Een element maken](#create-an-asset)
* [Externe XMP-ontwikkelinstellingsbestand voor middelen maken](#create-an-asset-external-xmp-develop-setting-file)
* [Uitvoeringen genereren voor een origineel bestand](#generate-renditions-for-an-original-file)
* [Een cataloguselement ophalen](#get-a-catalog-asset)
* [De nieuwste middelen voor externe XMP-ontwikkelinstellingen ophalen](#get-the-latest-asset-external-xmp-develop-setting-file)
* [De nieuwste uitvoering van elementen ophalen](#get-the-latest-asset-rendition)
* [Elementen ophalen](#retrieve-assets)

#### Origineel elementbestand maken

Met deze actiemodule maakt en uploadt u een origineel bestand voor een element.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in van het element waarvoor u een bestand wilt maken of upload er een.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Voer de lengte van de inhoud in bytes in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Byte range]</td>
      <td>
        <p>Ga of kaart de bytewaaier voor het verzoek in, met inbegrip van eerste en laatste bytes en entiteitlengte zoals bepaald in RFC 2616. Deze informatie zou slechts moeten worden omvat wanneer de gegevens te groot zijn om in één enkele vraag te worden geupload.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content type]</td>
      <td>
        <p>Selecteer het inhoudstype voor het nieuwe bestand.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Een element maken

In deze actiemodule wordt een nieuw element gemaakt met initiële metagegevens en importgegevens.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id van de catalogus in of wijs deze toe waar het element wordt gemaakt.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id van het nieuwe element in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset type]</td>
      <td>
        <p>Selecteer of het element een afbeelding of een video is.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Date captured]</td>
      <td>
        <p>Voer de vastlegdatum van het element in of wijs deze toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00</code> . Deze wordt door de server ingesteld als de vastgelegde datum is ingesteld op <code>0000-00-00T00:00:00</code> . </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL File name]</td>
      <td>
        <p>Voer de bestandsnaam in of wijs de naam toe van het element dat u in Lightroom importeert.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name of Device Imported On]</td>
      <td>
        <p>Voer de naam in of wijs de naam toe van het apparaat dat het element importeert.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Account ID of User Who Imported]</td>
      <td>
        <p>Voer de id in of wijs deze toe aan de gebruiker die het element importeert.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Import Timestamp]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00</code> .</p>
      </td>
    </tr>
  </tbody>
</table>

#### Externe XMP-ontwikkelinstellingsbestand voor middelen maken

Deze handelingsmodule ondersteunt twee workflows: het uploaden van het externe XMP-bestand voor ontwikkelinstellingen voor het element of het maken van een extern XMP-bestand voor ontwikkelinstellingen door het kopiëren van het externe XMP-instellingenbestand van een ander element.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content Length in Bytes]</td>
      <td>
        <p>Voer de lengte van de inhoud in bytes in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Upload new or copy XMP/develop file]</td>
      <td>
        <p>Selecteer of u een nieuw bestand uploadt of een bestand uit een bestaand element kopieert.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id van de catalogus in of wijs deze toe op de plaats waar u het element wilt maken.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in van het element waarnaar u een bestand wilt uploaden of waarnaar u een bestand wilt kopiëren, of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Link to XMP/develop file]</td>
      <td>
        <p>Voer een koppeling in of wijs een koppeling toe aan het bestand dat u wilt uploaden of kopiëren.</p><p>Dit bestand moet JSON zijn bij het kopiëren van een bestand, of XML bij het uploaden van een bestand.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Uitvoeringen genereren voor een origineel bestand

Deze actiemodule genereert asynchroon uitvoeringen voor een origineel bestand.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition Type(s) (semi-colon separated)]</td>
      <td>
        <p>Voer het weergavetype in voor de vertoning die u wilt maken. Als u meer dan één type invoert, scheidt u deze met een puntkomma (;). <p>Mogelijke typen:</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Voer de lengte van de inhoud in bytes in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id van de catalogus in of wijs deze toe op de plaats waar u de uitvoeringen wilt genereren.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in van het element waarvoor u een uitvoering van een bestand wilt maken of wijs deze toe.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Een cataloguselement ophalen

Deze actiemodule wint informatie over één enkel middel in een catalogus terug. De catalogus moet eigendom zijn van de gebruiker wiens referenties worden weergegeven in de verbinding die in deze module wordt gebruikt.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in van het element waarvoor u informatie wilt ophalen of wijs deze toe.</p>
      </td>
    </tr>
  </tbody>
</table>


#### De nieuwste middelen van het externe XMP-instellingenbestand voor ontwikkeling ophalen

Met deze actiemodule haalt u het meest recente externe XMP-instellingsbestand voor elementen op.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat dat is gekoppeld aan het instellingsbestand voor XMP-ontwikkeling of wijs deze id toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in of wijs deze toe aan het element dat is gekoppeld aan het XMP-instellingsbestand voor ontwikkeling.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Nieuwste uitvoering van element ophalen

Deze actiemodule wint de recentste elementenvertoning van het gespecificeerde type terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat waarvoor u een vertoning wilt ophalen of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in van het element waarvoor u een vertoning wilt ophalen of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition type]</td>
      <td>
        <p>Selecteer het type vertoning dat u wilt ophalen.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Elementen ophalen

Deze actiemodule wint activa terug die door de gebruiker worden bezeten waarvan geloofsbrieven in de verbinding worden vertegenwoordigd die in deze module wordt gebruikt.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starting timestamp]</td>
      <td>
        <p>Voer een tijdstempel in of wijs deze toe. De module keert verslagen terug die na dit tijdstempel zijn bijgewerkt.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Return assets captured before given time]</td>
      <td>
        <p>Voer een datum in met de notatie <code>YYYY-MM-DDT00:00:00</code> . De module retourneert resultaten die vóór deze datum zijn vastgelegd.</p><p> Dit veld kan niet worden gebruikt met het veld <code>Return assets captured after given time</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Return assets captured after given time]</td>
      <td>
        <p>Voer een datum in met de notatie <code>YYYY-MM-DDT00:00:00</code> . De module retourneert resultaten die vóór deze datum zijn vastgelegd.</p><p> Dit veld kan niet worden gebruikt met het veld <code>Return assets captured before given time</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum number of returned assets]</td>
      <td>
        <p>Ga het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256 Hash value of original file]</td>
      <td>
        <p>Voer de hashwaarde van het oorspronkelijke bestand in of wijs deze toe. Assets met een overeenkomende hash wordt geretourneerd.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Hide assets that are inside stacks?"]</td>
      <td>
        <p>Selecteer Ja om elementen in stapels te verbergen (elementen in stapels worden niet geretourneerd). Selecteer Nee als u elementen in stapels in de resultaten wilt opnemen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset subtype values]</td>
      <td>
        <p>Voer een lijst in met subtypen die door puntkomma's worden gescheiden en wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset IDs]</td>
      <td>
        <p>Voer maximaal 100 id's van elementen in of wijs deze toe, gescheiden door komma's.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types of assets to exclude]</td>
      <td>
        <p>Selecteer deze optie als u volledige of onvolledige elementen wilt uitsluiten. Laat dit veld leeg als u alle elementen wilt opnemen.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Group values]</td>
      <td>
        <p>Voer een lijst met groepswaarden in of wijs deze toe aan een lijst met door puntkomma's gescheiden waarden.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name values]</td>
      <td>
        <p>Voer een lijst met naamwaarden in of wijs deze toe aan een lijst met door puntkomma's gescheiden waarden.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Favorite status]</td>
      <td>
        <p>Voer de favoriete status in of wijs deze toe waarvoor u resultaten wilt retourneren.</p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>

### Albums

* [Elementen toevoegen aan een album](#add-assets-to-an-album)
* [Een album maken](#create-an-album)
* [Een album verwijderen](#delete-an-album)
* [Een album ophalen](#get-an-album)
* [Elementen van een album weergeven](#list-assets-of-an-album)
* [Albums ophalen](#retrieve-albums)
* [Een album bijwerken](#update-album)

#### Elementen toevoegen aan een album

Deze actiemodule voegt een of meer elementen toe aan het opgegeven album. U kunt maximaal 50 elementen in één uitvoeringscyclus toevoegen.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het album bevat waaraan u elementen wilt toevoegen of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Voer de id in van het album waaraan u elementen wilt toevoegen of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Assets]</td>
      <td>
        <p>Voor elk element dat u aan het album wilt toevoegen, klik <b> toevoegen punt </b> en ga de volgende gebieden in.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in van het element dat u aan het album wilt toevoegen of wijs deze toe</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Is this asset an album cover?]</td>
      <td>
        <p>Selecteer of u dit element wilt weergeven als de afbeelding die het album vertegenwoordigt.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Order]</td>
      <td>
        <p>Geef de volgorde van het element op.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Service Payload]</td>
      <td>
        <p>Voer metagegevens in of wijs deze toe aan het element dat u wilt opnemen. Dit moet één tekstreeks zijn met een maximale lengte van 1-24 tekens.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
      <td>
        <p>Voer een id in voor het element.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Een album maken

Deze actiemodule maakt een nieuw album in Lightroom.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id van de catalogus in of wijs deze toe op de plaats waar u een album wilt maken.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Voer een id voor het nieuwe album in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype]</td>
      <td>
        <p>Selecteer het subtype voor het album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Service ID]</td>
      <td>
        <p>Voer de API-sleutel in van de service die het album maakt.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Date User Created]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Date User Updated]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album Name]</td>
      <td>
        <p>Voer een naam in voor het nieuwe album of wijs een naam toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Cover ID]</td>
      <td>
        <p>Voer de id in van een element dat u als voorblad van dit album wilt gebruiken of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Parent ID]</td>
      <td>
        <p>Voer de id van het bovenliggende element voor dit album in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Service Payload]</td>
      <td>
        <p>Voer de metagegevens van een album in of wijs deze toe als een tekenreeks.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Remote ID]</td>
      <td>
        <p>Voer een id in voor het element.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Created date]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Updated date]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Is the album deleted?]</td>
      <td>
        <p>Schakel deze optie in als de extern gekoppelde inhoud is verwijderd.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to edit affiliated content]</td>
      <td>
        <p>Als er een URL is waar gebruikers inhoud van dit album kunnen bewerken, voert u hier de URL in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to view affiliated content]</td>
      <td>
        <p>Als er een URL is waar gebruikers de inhoud van dit album kunnen bekijken, ga hier URL in.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Een album verwijderen

Met deze actiemodule verwijdert u een album.

Het verwijderde album moet zijn gemaakt door dezelfde clienttoepassing die het album nu verwijdert en moet van het subtype `project` of `project_set` zijn.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het album bevat dat u wilt verwijderen of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Voer de id in van het album dat u wilt verwijderen of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Delete child albums?]</td>
      <td>
        <p>Selecteer of u onderliggende albums van het verwijderde album wilt verwijderen.</p>
      </td>
    </tr>
  </tbody>
</table>

### Een album ophalen

Deze actiemodule wint het gespecificeerde album terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het album bevat dat u wilt ophalen of wijs deze id toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Voer de id in van het album dat u wilt ophalen of wijs deze toe.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Elementen van een album weergeven

Deze actiemodule wint een lijst van activa in het gespecificeerde album terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het album bevat of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Voer de id in van het album waarvan u elementen wilt weergeven of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Capture Assets Before Time]</td>
      <td>
        <p>Voer een datum in met de notatie <code>YYYY-MM-DDT00:00:00</code> . De module retourneert resultaten die vóór deze datum zijn vastgelegd.</p><p> Dit veld kan niet worden gebruikt met het veld <code>Return assets captured after given time</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Capture Assets After Time]</td>
      <td>
        <p>Voer een datum in met de notatie <code>YYYY-MM-DDT00:00:00</code> . De module retourneert resultaten die vóór deze datum zijn vastgelegd.</p><p> Dit veld kan niet worden gebruikt met het veld <code>Return assets captured before given time</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ending Asset Order Value]</td>
      <td>
        <p>Voer de orderwaarde van het laatste element in of wijs deze toe.</p><p> Dit veld kan alleen worden gebruikt met het veld <code>Capture Assets After Time</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starting Asset Order Value]</td>
      <td>
        <p>Voer de orderwaarde van het beginelement in of wijs deze toe.</p><p> Dit veld kan alleen worden gebruikt met het veld <code>Capture Assets BEfore Time</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Number of Assets to Return (1-500)]</td>
      <td>
        <p>Ga het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren. Dit getal moet tussen 1 en 500 liggen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Hide assets that are inside stacks?"]</td>
      <td>
        <p>Selecteer Ja om elementen in stapels te verbergen (elementen in stapels worden niet geretourneerd). Selecteer Nee als u elementen in stapels in de resultaten wilt opnemen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype Values (semi-colon separated)]</td>
      <td>
        <p>Voer een lijst in met subtypen die door puntkomma's worden gescheiden en wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Flag Values (semi-colon separated)]</td>
      <td>
        <p>Voer een lijst met door puntkomma's gescheiden waarden in die u wilt retourneren of wijs deze lijst toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Additional Data Fields to Include (semi-colon separated)]</td>
      <td>
        <p>Als een element is opgenomen, worden alle velden opgenomen, anders worden alleen de id- en zelfhref-koppeling geretourneerd.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types of assets to exclude]</td>
      <td>
        <p>Selecteer deze optie als u volledige of onvolledige elementen wilt uitsluiten. Laat dit veld leeg als u alle elementen wilt opnemen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset IDs]</td>
      <td>
        <p>Voer maximaal 100 id's van elementen in of wijs deze toe, gescheiden door komma's.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Filter out album assets based on presentation filters]</td>
      <td>
        <p>Wanneer dit veld is ingesteld op 'true', worden alle albumelementen gefilterd op basis van de presentatiefilters die in het album zijn ingesteld. Met deze parameter worden afgewezen elementen altijd uitgefilterd, ongeacht de instellingen in presentatiefilters. Presentatiefilters worden niet toegepast wanneer een andere waarde dan 'true' wordt ingesteld voor album_filters. Standaard worden alle elementen weergegeven. Deze parameter kan niet samen met de parameter flag worden gebruikt. </p>
      </td>
    </tr>
  </tbody>
</table>

#### Albums ophalen

Deze actiemodule wint een lijst van albums in de gespecificeerde catalogus terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in of wijs deze toe aan de catalogus met albums die u wilt ophalen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtypes]</td>
      <td>
        <p>Voer een lijst in met subtypen die door puntkomma's worden gescheiden en wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name of album to precede current results]</td>
      <td>
        <p>Als u paginering toepast op de resultaten, typt of wijst u de naam van het laatste album op de voorafgaande pagina toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Number of Albums to Return]</td>
      <td>
        <p>Stel het maximumaantal elementen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert. De standaardwaarde voor dit veld is 100. Deze module retourneert mogelijk meer albums dan deze limiet als meerdere albums aan de limietgrens dezelfde <code>name_after</code> -waarde hebben.</p>
      </td>
    </tr>
  </tbody>
</table>

#### album bijwerken

Deze actiemodule werkt het opgegeven album bij.

Het bijgewerkte album moet zijn gemaakt door dezelfde clienttoepassing die het nu bijwerkt en moet van het subtype `project` of `project_set` zijn.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Lightroom] Verbinding maken met <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het album bevat dat u wilt bijwerken of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Voer de id in van het album dat u wilt bijwerken of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Overige velden</td>
      <td>
      <td>Voor beschrijvingen van andere gebieden in deze module, zie <a href="#create-an-album" class="MCXref xref" > een album </a> in dit artikel creëren.</td>
      </td>
    </tr>
  </tbody>
</table>
