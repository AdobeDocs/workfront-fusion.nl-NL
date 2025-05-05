---
title: Adobe Lightroom-modules
description: Met de Adobe Lightroom-modules kunt u een Adobe Workfront Fusion-scenario starten op basis van gebeurtenissen in uw Adobe Lightroom-account.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '2376'
ht-degree: 0%

---

# [!DNL Adobe Lightroom] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Adobe Lightroom] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [ een scenario creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
      <td>
        <p>[!UICONTROL Pro] of hoger</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td>
      <td >
        <p>[!UICONTROL Workfront Fusion for Work Automation and Integration]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Product</td>
      <td>Uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</td>
    </tr>
    </tr>
  </tbody>
</table>


&#42; om te weten te komen welk plan, vergunningstype, of toegang u hebt, contacteer uw [!DNL Workfront] beheerder.

&#42;&#42; Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL [Adobe Workfront Fusion] licenses]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Voordat u de [!DNL Adobe Lightroom] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!DNL Adobe Lightroom] account hebben.

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

Verbinding maken voor uw [!DNL Adobe Lightroom] -modules:

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
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL -omgeving]</td>
        <td>Selecteer of u verbinding maakt met een productie- of niet-productieomgeving.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL -type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!UICONTROL Adobe] [!UICONTROL Client ID] in. Dit vindt u in het detailgedeelte [!UICONTROL Credentials] van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in het detailgedeelte [!UICONTROL Credentials] van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. Klik **[!UICONTROL verdergaan]** om de verbinding te bewaren en aan de module terug te keren.




## Adobe Lightroom-modules en hun velden

Wanneer u [!DNL Adobe Lightroom] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Lightroom] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Als u specifieke referenties wilt opgeven om ervoor te zorgen dat een specifieke server wordt uitgevoerd, klikt u op Item toevoegen en voert u de referenties in.</p><p>Autorisatiekoppen worden automatisch toegevoegd.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Metagegevens uit gebruikerscatalogus ophalen

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
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

* [Origineel elementbestand maken](#create-an-asset-external-xmp-develop-setting-file)
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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
      <td role="rowheader">[!UICONTROL -bytebereik]</td>
      <td>
        <p>Ga of kaart de bytewaaier voor het verzoek in, met inbegrip van eerste en laatste bytes en entiteitlengte zoals bepaald in RFC 2616. Moet alleen worden opgenomen wanneer de gegevens te groot zijn om in één aanroep te worden geüpload.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -inhoudstype]</td>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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
      <td role="rowheader">[!UICONTROL -elementtype]</td>
      <td>
        <p>Selecteer of het element een afbeelding of een video is.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -gebruiker datumtime gemaakt]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -gebruiker Datetime bijgewerkt]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -datum vastgelegd]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00</code> .</p>
      </td>
    </tr>
  </tbody>
</table>

#### Externe XMP-ontwikkelinstellingsbestand voor middelen maken

Deze actiemodule ondersteunt twee workflows. De eerste workflow bestaat uit het uploaden van het externe XMP-bestand met ontwikkelinstellingen voor het element. De tweede workflow bestaat uit het maken van een extern XMP-bestand voor ontwikkelinstellingen door te kopiëren van het externe XMP-instellingenbestand van een ander element.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Length of content in bytes]</td>
      <td>
        <p>Voer de lengte van de inhoud in bytes in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Upload nieuw of kopieer XMP/develop-bestand]</td>
      <td>
        <p>Selecteer of u een nieuw bestand uploadt of een bestand uit een bestaand element kopieert.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rendition Type(s) (puntkomma gescheiden)]</td>
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
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
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

#### De nieuwste uitvoering van elementen ophalen

Deze actiemodule wint de recentste elementenvertoning van het gespecificeerde type terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Voer de id in of wijs deze toe aan het element dat is gekoppeld aan het XMP-instellingsbestand voor ontwikkeling.</p>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
      <td>
        <p>Voer de id in van de catalogus die het element bevat of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starttijdstempel]</td>
      <td>
        <p>Voer een tijdstempel in of wijs deze toe. De module keert verslagen terug die na dit tijdstempel zijn bijgewerkt.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Return-middelen die eerder zijn vastgelegd]</td>
      <td>
        <p>Voer een datum in met de notatie <code>YYYY-MM-DDT00:00:00</code> . De module retourneert resultaten die vóór deze datum zijn vastgelegd.</p><p> Dit veld kan niet worden gebruikt met het veld <code>Return assets captured after</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum aantal geretourneerde elementen]</td>
      <td>
        <p>Ga het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256 Hash-waarde van oorspronkelijk bestand]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Elementen verbergen die zich in stapels bevinden?"]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset subtype values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -id's van element]</td>
      <td>
        <p>Voer maximaal 100 id's van elementen in of wijs deze toe, gescheiden door komma's.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types van activa om uit te sluiten]</td>
      <td>
        <p>Selecteer deze optie als u volledige of onvolledige elementen wilt uitsluiten. Laat dit veld leeg als u alle elementen wilt opnemen.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL -groepswaarden]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -naamwaarden]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Favoriete status]</td>
      <td>
        <p></p>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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
      <td role="rowheader">[!UICONTROL Is dit element een albumhoes?]</td>
      <td>
        <p>Selecteer of u dit element wilt weergeven als de afbeelding die het album vertegenwoordigt.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Order]</td>
      <td>
        <p></p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL -metagegevens]</td>
      <td>
        <p>Voer metagegevens in of wijs deze toe aan het element dat u wilt opnemen. Dit moet één tekstreeks zijn met een maximale lengte van 1-24 tekens.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL -externe id]</td>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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
      <td role="rowheader">[!UICONTROL -subtype]</td>
      <td>
        <p>Selecteer het subtype voor het album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL API-sleutel]</td>
      <td>
        <p>Voer de API-sleutel in van de service die het album maakt.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL -gebruiker datumtime gemaakt]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -gebruiker Datetime bijgewerkt]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album name]</td>
      <td>
        <p>Voer een naam in voor het nieuwe album of wijs een naam toe.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Cover ID]</td>
      <td>
        <p>Voer de id in van een element dat u als voorblad van dit album wilt gebruiken of wijs deze toe.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL -externe id]</td>
      <td>
        <p>Voer een id in voor het element.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL , aanmaakdatum]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL bijgewerkte datum]</td>
      <td>
        <p>Voer een datum in of wijs een datum toe met de notatie <code>YYYY-MM-DDT00:00:00-00:00Z</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Is het album verwijderd?]</td>
      <td>
        <p>Schakel deze optie in als de extern gekoppelde inhoud is verwijderd.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL van locatie om gekoppelde inhoud te bewerken]</td>
      <td>
        <p>Als er een URL is waar gebruikers inhoud van dit album kunnen bewerken, voert u hier de URL in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL van locatie om verwante inhoud te bekijken]</td>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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
      <td role="rowheader">[!UICONTROL onderliggende albums verwijderen?]</td>
      <td>
        <p>Selecteer of u onderliggende albums van het verwijderde album wilt verwijderen.</p>
      </td>
    </tr>
  </tbody>
</table>

### Een album ophalen

Deze actiemodule wint het gespecificeerde album terug

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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



#### Albums ophalen

Deze actiemodule wint een lijst van albums in de gespecificeerde catalogus terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
      <td>
        <p>Voer de id in of wijs deze toe aan de catalogus met albums die u wilt ophalen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -subtypen]</td>
      <td>
        <p>Voer de id in van het album dat u wilt ophalen of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Naam van album om huidige resultaten voor te gaan]</td>
      <td>
        <p>Als u paginering toepast op de resultaten, typt of wijst u de naam van het laatste album op de voorafgaande pagina toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Maximum aantal geretourneerde albums]</td>
      <td>
        <p>Stel het maximumaantal elementen in dat [!DNL Workfront Fusion] tijdens één uitvoeringscyclus retourneert. De standaardwaarde voor dit veld is 100. Deze module retourneert mogelijk meer albums dan deze limiet als meerdere albums aan de limietgrens dezelfde <code>name_after</code> -waarde hebben.</p>
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
      <td role="rowheader">[!UICONTROL -verbinding]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" > Verbinding maken met [!DNL Adobe Lightroom]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Lightroom] .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL -catalogus-ID]</td>
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
