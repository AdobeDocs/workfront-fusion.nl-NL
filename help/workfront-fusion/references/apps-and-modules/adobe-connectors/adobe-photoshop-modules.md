---
title: Adobe Photoshop-modules
description: Met de Adobe Photoshop-modules kunt u een Adobe Workfront Fusion-scenario starten op basis van gebeurtenissen in uw Adobe Photoshop-account, overeenkomsten en andere records maken, lezen of bijwerken, records zoeken aan de hand van criteria die u hebt ingesteld en documenten uploaden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
source-git-commit: 95d52f8227c8a40c0db165eea9d2877e60446de9
workflow-type: tm+mt
source-wordcount: '4716'
ht-degree: 0%

---

# [!DNL Adobe Photoshop] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Adobe Photoshop] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.


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

Voordat u de [!DNL Adobe Photoshop] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!DNL Adobe Photoshop] account hebben.
* U moet een Firefly Services-licentie hebben.
* U moet een client-id en een clientgeheim hebben. U kunt deze aankopen op de Adobe Developer Console.

## Adobe Photoshop API-informatie

De Adobe Photoshop-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken met [!DNL Adobe Photoshop]

Verbinding maken voor uw [!DNL Adobe Photoshop] -modules:

1. Klik in een willekeurige module op **[!UICONTROL Add]** naast het vak Verbinding.

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
          <p>Selecteer of u een JWT-verbinding of een server-naar-server verbinding wilt gebruiken.</p>
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
        <td>Voer uw [!UICONTROL Adobe] [!UICONTROL Client ID] in. Dit vindt u in het gedeelte [!UICONTROL Credentials] Details van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in het gedeelte [!UICONTROL Credentials] Details van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Als u een JWT-verbinding gebruikt, voert u uw [!DNL Adobe] [!UICONTROL Technical account ID] in. Dit vindt u in het gedeelte [!UICONTROL Credentials] Details van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Als u een JWT-verbinding gebruikt, voert u uw [!DNL Adobe] [!UICONTROL Organization ID] in. Dit vindt u in het gedeelte [!UICONTROL Credentials] Details van het dialoogvenster [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Als u een JWT-verbinding gebruikt, voert u de persoonlijke sleutel in die is gegenereerd toen uw referenties werden gemaakt in de [!DNL Adobe Developer Console] . </p>
          <p>Uw persoonlijke sleutel of certificaat uitnemen:</p>
          <ol>
            <li value="1">
              <p>Klik op <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecteer het type bestand dat u extraheert.</p>
            </li>
            <li value="3">
              <p>Selecteer het bestand dat de persoonlijke sleutel of het certificaat bevat.</p>
            </li>
            <li value="4">
              <p>Voer het wachtwoord voor het bestand in.</p>
            </li>
            <li value="5">
              <p>Klik <b> sparen </b> om het dossier te halen en aan de verbindingsopstelling terug te keren.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## [!DNL Adobe Photoshop] modules en hun velden

Wanneer u [!DNL Adobe Photoshop] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Photoshop] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [PSD-bewerkingen toepassen](#apply-psd-edits)
* [Automatische kleuren corrigeren een afbeelding](#auto-color-correct-an-image)
* [Afbeeldingsindeling omzetten](#convert-image-format)
* [Een masker maken](#create-a-mask)
* [Een nieuwe PSD maken](#create-a-new-psd)
* [Tekstlagen bewerken](#edit-text-layers)
* [Tekstlagen bewerken (verouderd)](#edit-text-layers-legacy)
* [Een handeling uitvoeren JSON](#execute-an-action-json)
* [Diepte vervagen uitvoeren](#execute-depth-blur)
* [Photoshop-handelingen uitvoeren](#execute-photoshop-actions)
* [Uitsnijden van product uitvoeren](#execute-product-crop)
* [Laaginfo ophalen](#get-layer-info)
* [Een aangepaste API-aanroep maken](#make-a-custom-api-call)
* [Achtergrond verwijderen](#remove-background)
* [Een slim object vervangen](#replace-a-smart-object)
* [Een slim object vervangen (verouderd)](#replace-a-smart-object-legacy)
* [De grootte van een afbeelding wijzigen](#resize-an-image)
* [Watermerk toepassen op een afbeelding](#watermark-an-image)

### PSD-bewerkingen toepassen

In deze actiemodule worden diverse bewerkingen op document- en laagniveau toegepast.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand dat u wilt bewerken is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt bewerken. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Height]</p>
      </td>
      <td> Voer de hoogte van de afbeelding in pixels in of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Width]</p>
      </td>
      <td> Voer de breedte van de afbeelding in pixels in of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Top]</p>
      </td>
   <td> Voer in pixels de y-coördinaat in van de linkerbovenhoek van het document. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Bottom]</p>
      </td>
   <td> Voer in pixels de y-coördinaat in van de rechterbenedenhoek van het document. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Left]</p>
      </td>
   <td> Voer in pixels de x-coördinaat van de linkerbovenhoek van het document in of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Canvas size) Right]</p>
      </td>
   <td> Voer in pixels de x-coördinaat in van de rechterbenedenhoek van het document. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Trim]</p>
      </td>
   <td> Selecteer Transparante pixels om het bijsnijden te baseren op transparante pixels in de afbeelding. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Default font]</p>
      </td>
   <td> Voer de volledige postscriptnaam in van het lettertype dat als algemene standaardinstelling voor het document moet worden gebruikt. Dit lettertype wordt gebruikt voor alle tekstlagen met een ontbrekend lettertype en er is geen specifiek lettertype voor die laag opgegeven. Als dit lettertype ontbreekt, wordt de optie voor het beheren van ontbrekende lettertypen van kracht. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Voor elk lettertype dat het document nodig heeft, klikt u op Item toevoegen en geeft u de opslaglocatie en bestandslocatie van het lettertype op. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Manage missing fonts]</p>
      </td>
   <td> Selecteer de actie die u wilt uitvoeren als het document een of meer ontbrekende lettertypen bevat. <ul><li><code>fail</code>: De taak wordt niet uitgevoerd en de status wordt ingesteld op mislukt. De details van de fout worden weergegeven in de sectie Details in de status.</li><li><code>useDefault</code>: De taak wordt uitgevoerd en alle ontbrekende lettertypen worden vervangen door ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Layers]</p>
      </td>
   <td> Voor elke laag die u wilt toevoegen, klikt u op Item toevoegen en vult u de laagdetails in. <p>Voor details over laagopties, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/modifyDocumentAsync"> PSD uitgeven </a> in de documentatie van Adobe Photoshop toepassen.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Voor elk bewerkt bestand dat u wilt maken, klikt u op Item toevoegen en voert u de opslag, locatie en het type in zoals in deze tabel.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen. Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selecteer het bestandstype waarnaar u het bestand wilt converteren. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Trim to Canvas]</p>
      </td>
   <td>Selecteer of de uitvoeringen Canvasgrootte moeten hebben. De rendities worden op ware wijze bijgesneden tot de grootte van het canvas, terwijl bij False de laaggrootte van rendities wordt gemaakt</td> 
    </tr>
    </tbody>
</table>

### Automatische kleuren corrigeren een afbeelding

Met deze handelingsmodule corrigeert u de opgegeven afbeelding automatisch.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand is opgeslagen dat u wilt corrigeren.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt corrigeren. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen. Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selecteer het bestandstype waarnaar u het bestand wilt converteren. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tr>
    </tbody>
</table>

### Afbeeldingsindeling omzetten

Deze actiemodule zet een bestand om in JPEG, PNG, PSD of TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bestand is opgeslagen waaruit u de achtergrond wilt verwijderen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Typ of wijs de URL of het pad toe van het bestand waaruit u de achtergrond wilt verwijderen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Voor elk omgezet dossier wilt u tot stand brengen, voegt het punt toe en gaat de opslag, de plaats in, en typt zoals vermeld in deze lijst.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen. Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selecteer het bestandstype waarnaar u het bestand wilt converteren. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tr>
    </tbody>
</table>

### Een masker maken

Deze actiemodule retourneert een PNG-bestand waarop een masker is toegepast om het onderwerp.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice op de plaats waar het bestand is opgeslagen waarvan u een masker wilt maken.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Typ of wijs de URL of het pad toe van het bestand waaruit u een masker wilt maken. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het maskerbestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het maskerbestand wordt opgeslagen. Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Color space]</p>
      </td>
   <td>Selecteer of de uitvoerafbeelding RGB- of RGBA-kleur gebruikt. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>Selecteer of het masker zacht (doezeld) of binair moet zijn. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>Selecteer Prestaties om voor snelheid te optimaliseren, of Batch om wachttijd toe te staan. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Selecteer of naverwerking moet worden ingeschakeld.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Standaard is 4.0</td> 
    </tr> 
    </tbody>
</table>

### Een nieuwe PSD maken

Deze actiemodule maakt een nieuwe PSD met optionele lagen en genereert uitvoeringen of slaat op als een PSD.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Height]</p>
      </td>
      <td> Voer de hoogte van de afbeelding in pixels in of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document > Image size) Width]</p>
      </td>
      <td> Voer de breedte van de afbeelding in pixels in of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Resolution]</p>
      </td>
   <td> Voer de resolutie voor de afbeelding in in pixels per inch of wijs deze toe. Dit moet tussen 72 en 300 liggen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Mode]</p>
      </td>
   <td> Selecteer de modus voor de afbeelding. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Fill]</p>
      </td>
   <td> Selecteer of u de opvulling voor de achtergrondlaag transparant, wit of de achtergrondkleur van de afbeelding wilt maken. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options > Document) Depth]</p>
      </td>
   <td> Selecteer de bitdiepte van de afbeelding. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Layers]</p>
      </td>
   <td> Voor elke laag die u wilt toevoegen, klikt u op Item toevoegen en vult u de laagdetails in. <p>Voor details over laagopties, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync"> PSD </a> in de documentatie van Adobe Photoshop creëren.  </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Global font]</p>
      </td>
   <td> Voer de volledige postscriptnaam in van het lettertype dat als algemene standaardinstelling voor het document moet worden gebruikt. Dit lettertype wordt gebruikt voor alle tekstlagen met een ontbrekend lettertype en er is geen specifiek lettertype voor die laag opgegeven. Als dit lettertype ontbreekt, wordt de optie voor het beheren van ontbrekende lettertypen van kracht. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Voor elk lettertype dat het document nodig heeft, klikt u op Item toevoegen en geeft u de opslaglocatie en bestandslocatie van het lettertype op. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Manage missing fonts]</p>
      </td>
   <td> Selecteer de actie die u wilt uitvoeren als het document een of meer ontbrekende lettertypen bevat. <ul><li><code>fail</code>: De taak wordt niet uitgevoerd en de status wordt ingesteld op mislukt. De details van de fout worden weergegeven in de sectie Details in de status.</li><li><code>useDefault</code>: De taak wordt uitgevoerd en alle ontbrekende lettertypen worden vervangen door ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Klik voor elk bestand dat u wilt maken op Item toevoegen en voer de opslag, locatie en het type in zoals vermeld in deze tabel.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen. Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selecteer het bestandstype waarnaar u het bestand wilt converteren. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Other fields]</td>
      <td>
        <p><p>Voor details over outputopties, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/createDocumentAsync"> PSD </a> in de documentatie van Adobe Photoshop creëren.  </p>
      </td>
    </tr>
    </tbody>
</table>

### Tekstlagen bewerken

In deze actiemodule worden tekstlagen bewerkt in een Photoshop-bestand. U kunt afzonderlijke bewerkingsdetails voor meerdere lagen in hetzelfde bestand invoeren.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand dat u wilt bewerken is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt bewerken. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Manage missing fonts]</td>
      <td>
        <p>Selecteer de actie die u wilt uitvoeren als het document een of meer ontbrekende lettertypen bevat. Als het lettertype niet wordt opgegeven, gebruikt de module het standaardlettertype.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Voer de volledige postscriptnaam in van het lettertype dat als algemene standaardinstelling voor het document moet worden gebruikt. Dit lettertype wordt gebruikt voor alle tekstlagen met een ontbrekend lettertype en er is geen specifiek lettertype voor die laag opgegeven. Als dit lettertype ontbreekt, wordt de optie voor het beheren van ontbrekende lettertypen van kracht.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Geef de opslaglocatie en de bestandslocatie van het lettertype op. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Layers]</td>
   <td> <p>Voor elke tekstlaag die u wilt uitgeven, <b> toevoegen punt </b> en ga de laagopties in.<p>Voor details over laagopties, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync"> tekst </a> in de documentatie van Adobe Photoshop uitgeven.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bewerkte bestand moet worden opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het bewerkte bestand wordt opgeslagen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selecteer het bestandstype voor het bewerkte bestand. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan.</p>
      </td>
    </tr>
  </tbody>
</table>

### Tekstlagen bewerken (verouderd)

Deze actiemodule bewerkt een tekstlaag in een Photoshop-bestand.

Om veelvoudige lagen uit te geven, gebruik [ tekstlagen ](#edit-text-layers) module uitgeven.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand dat u wilt bewerken is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt bewerken. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Manage missing fonts]</td>
      <td>
        <p>Selecteer de actie die u wilt uitvoeren als het document een of meer ontbrekende lettertypen bevat. Als het lettertype niet wordt opgegeven, gebruikt de module het standaardlettertype.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Voer de volledige postscriptnaam in van het lettertype dat als algemene standaardinstelling voor het document moet worden gebruikt. Dit lettertype wordt gebruikt voor alle tekstlagen met een ontbrekend lettertype en er is geen specifiek lettertype voor die laag opgegeven. Als dit lettertype ontbreekt, wordt de optie voor het beheren van ontbrekende lettertypen van kracht.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Geef de opslaglocatie en de bestandslocatie van het lettertype op. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Layers]</td>
   <td> <p>Voor details over laagopties, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/editTextLayerAsync"> tekstlaag </a> in de documentatie van Adobe Photoshop uitgeven.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bewerkte bestand moet worden opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bewerkte bestand moet worden opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het bewerkte bestand wordt opgeslagen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Selecteer het bestandstype voor het bewerkte bestand. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan.</p>
      </td>
    </tr>
  </tbody>
</table>


### Een handeling uitvoeren JSON

Deze handelingsmodule voert Photoshop-handelingen uit met behulp van JSON-opdrachten.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand dat u wilt bewerken is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt bewerken. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action JSON]</td>
      <td>
        <p>Voer de JSON-opdracht in voor de handeling die u wilt uitvoeren.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Fonts / Patterns / Brushes / Additional images]</td>
      <td>
        <p>Voor elk lettertype, patroon, penseel of andere afbeelding die u in deze handeling wilt gebruiken, klikt u op Item toevoegen en voert u de opslag- en bestandslocatie van het item in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt gebruiken. </td> 
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Klik voor elk bestand dat u wilt maken op Item toevoegen en voer de optie voor opslag, locatie, type en overschrijven in die in deze tabel wordt vermeld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bewerkte bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het bewerkte bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Selecteer het bestandstype voor het bewerkte bestand. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan.</p>
      </td>
    </tr>
      </tbody>
</table>

### Diepte vervagen uitvoeren

Deze actiemodule voert Diepte vervagen op het geselecteerde bestand uit.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand dat u wilt bewerken is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt bewerken. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bewerkte bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het bewerkte bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Selecteer het bestandstype voor het bewerkte bestand. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>Voor details over andere opties van het Onduidelijke beeld van de Diepte, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync"> Uitvoeren Vervaging van de Diepte </a> in de documentatie van Adobe Photoshop API.</p>
      </td>
    </tr>
  </tbody>
</table>

### Photoshop-handelingen uitvoeren

Deze actiemodule voert een Photoshop-actie uit op de geselecteerde afbeelding.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand dat u wilt bewerken is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt bewerken. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Actions file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het actiebestand is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Actions file URL]</p>
      </td>
   <td> Voer de URL of het pad van het actiebestand in of wijs deze toe. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Action name]</p>
      </td>
   <td> Als u alleen een bepaalde handeling wilt uitvoeren, kunt u opgeven welke handeling in de ActionSet moet worden afgespeeld. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Font / Pattern / Brush storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bestand dat u wilt gebruiken, is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt gebruiken. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bewerkte bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het bewerkte bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Selecteer het bestandstype voor het bewerkte bestand. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>Voor details over andere opties van het Onduidelijke beeld van de Diepte, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync"> Uitvoeren Vervaging van de Diepte </a> in de documentatie van Adobe Photoshop API.</p>
      </td>
    </tr>
  </tbody>
</table>

### Uitsnijden van product uitvoeren

Deze actiemodule voert het Uitsnijden van het Product op het geselecteerde beeld uit.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bestand dat u wilt uitsnijden, is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand dat u wilt uitsnijden. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Unit]</p>
      </td>
   <td> Selecteer of u de hoogte- en breedteaanpassing wilt beschrijven in pixels of als een percentage. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> Voer de hoeveelheid breedte-opvulling in die u wilt toevoegen of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Height]</p>
      </td>
   <td> Voer de hoeveelheid opvulling voor de hoogte in die u wilt toevoegen of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bewerkte bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) File URL]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het bewerkte bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Selecteer het bestandstype voor het bewerkte bestand. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Outputs) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>Voor details over andere opties van het Onduidelijke beeld van de Diepte, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/applyDepthBlurAsync"> Uitvoeren Vervaging van de Diepte </a> in de documentatie van Adobe Photoshop API.</p>
      </td>
    </tr>
  </tbody>
</table>

### Laaginfo ophalen

Deze actiemodule wint laaginformatie van het gespecificeerde dossier van PSD terug.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bestand waarvan u laaggegevens wilt ophalen, is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Typ of wijs de URL of het pad toe van het bestand waaruit u laaggegevens wilt ophalen. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Thumbnails]</p>
      </td>
   <td> Selecteer het type bestand dat u wilt instellen als miniaturen. Miniaturen zijn kleine voorvertoningen voor elke renderbare laag.</td> 
    </tr>
  </tbody>
</table>

### Een aangepaste API-aanroep maken

Deze actiemodule maakt een aangepaste aanroep naar de Photoshop API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Voer een pad in dat relatief is ten opzichte van <code>https://image.adobe.io/pie/psdService</code> . Voorbeeld: <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion voegt automatisch machtigingsheaders toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Voer de queryreeks voor de aanvraag in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### Achtergrond verwijderen

Deze actiemodule identificeert het hoofdonderwerp van uw afbeelding en verwijdert de achtergrond.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bestand is opgeslagen waaruit u de achtergrond wilt verwijderen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Typ of wijs de URL of het pad toe van het bestand waaruit u de achtergrond wilt verwijderen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Color space]</p>
      </td>
   <td>Selecteer of de uitvoerafbeelding RGB- of RGBA-kleur gebruikt. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>Geef op of de randen van de afbeelding zacht (doezeld) of binair moeten zijn. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>Selecteer Prestaties om voor snelheid te optimaliseren, of Batch om wachttijd toe te staan. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Selecteer of naverwerking moet worden ingeschakeld.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>Standaard is 4.0</td> 
    </tr> 
    </tbody>
</table>

### Een slim object vervangen

Deze actiemodule vervangt een slim object in een PSD-laag en genereert nieuwe uitvoeringen.

Deze module gebruikt versie 2 van de API voor slimme objecten.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het slimme object is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Voer de URL of het pad van het slimme object in of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layers]</p>
      </td>
   <td>Klik voor elke laag die u aan het slimme object wilt toevoegen op Item toevoegen en voer de naam of id van het object in, de bestandsservice waar het slimme object is opgeslagen en de URL of het pad van de laag.<p>Voor beschrijvingen van de geavanceerde montages op dit gebied, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync"> een Slim Voorwerp </a> in de documentatie van Photoshop API vervangen </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resize image during place]</p>
      </td>
   <td> Selecteer of u het formaat van de afbeelding wilt wijzigen.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Voor elke nieuwe vertoning die u in de module wilt maken, klikt u op Item toevoegen en vult u de volgende velden in. U kunt maximaal 25 uitvoerbestanden hebben.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Outputs) Type]</p>
      </td>
   <td> Selecteer het bestandstype voor het bewerkte bestand. </td> 
    </tr>
     </tbody>
</table>

### Een slim object vervangen (verouderd)

Deze actiemodule vervangt een slim object in een PSD-laag en genereert nieuwe uitvoeringen.

In deze module wordt de oudere versie van slimme objecten gebruikt.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het slimme object is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Voer de URL of het pad van het slimme object in of wijs deze toe. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layers]</p>
      </td>
   <td>Klik voor elke laag die u aan het slimme object wilt toevoegen op Item toevoegen en voer de naam of id van het object in, de bestandsservice waar het slimme object is opgeslagen en de URL of het pad van de laag.<p>Voor beschrijvingen van de geavanceerde montages op dit gebied, zie <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/#operation/replaceSmartObjectAsync"> een Slim Voorwerp </a> in de documentatie van Photoshop API vervangen </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Voor elke nieuwe vertoning die u in de module wilt maken, klikt u op Item toevoegen en vult u de volgende velden in. U kunt maximaal 25 uitvoerbestanden hebben.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> De breedte, in pixels, van het uitvoerbestand. De oorspronkelijke hoogte-breedteverhouding blijft behouden in de module. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tbody>
</table>

### De grootte van een afbeelding wijzigen

Met deze actie wijzigt u de grootte van een afbeelding en gebruikt u dezelfde hoogte-breedteverhouding.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bestand waarvan u het formaat wilt wijzigen, is opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe aan het bestand waarvan u het formaat wilt wijzigen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Voor elk omgezet dossier wilt u tot stand brengen, voegt het punt toe en gaat de opslag, de plaats, en andere opties in zoals die in deze lijst worden vermeld.</p>
      </td>
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het nieuwe bestand moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het nieuwe bestand wordt opgeslagen.  Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> De breedte, in pixels, van het uitvoerbestand. De oorspronkelijke hoogte-breedteverhouding blijft behouden in de module. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Max width]</p>
      </td>
   <td>Wanneer de breedte 0 is, kan Max met worden verstrekt om de grootte te krijgen. Maximale breedte heeft voorrang, maar is kleiner dan de documentbreedte.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Trim to canvas]</p>
      </td>
   <td>Selecteer Ja als u de uitvoeringen wilt bijsnijden naar de canvasgrootte of Nee als u de rendities wilt vergroten naar de laaggrootte.</td> 
    </tr>
    </tbody>
</table>

### Watermerk toepassen op een afbeelding

Met deze actiemodule voegt u een watermerk toe aan de geselecteerde afbeelding.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Photoshop] Verbinding maken met <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Photoshop]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Base > Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waarin het bestand is opgeslagen waaraan u een watermerk wilt toevoegen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Base > Input) File location]</p>
      </td>
   <td> Typ of wijs de URL of het pad toe van het bestand waaraan u een watermerk wilt toevoegen. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Watermark > Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het watermerk dat u wilt toevoegen, is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Watermark > Input) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het watermerk dat u wilt toevoegen, is opgeslagen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Height]</p>
      </td>
   <td>Voer de gewenste hoogte van het watermerk in pixels in of wijs deze toe.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Width]</p>
      </td>
   <td> Voer de gewenste breedte van het watermerk in pixels in of wijs deze toe. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Left]</p>
      </td>
   <td> Voer de afstand in pixels in van de linkerzijde van de afbeelding die het watermerk moet hebben.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Watermark > Bounds) Top]</p>
      </td>
   <td> Voer de afstand in pixels in van de bovenkant van de afbeelding die het watermerk moet hebben.</td> 
    </tr>  
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Selecteer de bestandsservice waar het bestand met watermerken moet worden opgeslagen.</p><p>Als u interne Fusion-opslag selecteert, wordt het bestand beschikbaar voor latere modules, maar wordt het bestand niet buiten het scenario beschikbaar gesteld.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Voer de URL of het pad in of wijs deze toe waar het bestand met watermerken wordt opgeslagen. Dit is alleen nodig als u geen interne Fusion-opslag hebt gekozen voor de uitvoeropslag.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Selecteer het bestandstype waarnaar u het bestand wilt converteren. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Width]</p>
      </td>
   <td> De breedte, in pixels, van het uitvoerbestand. De oorspronkelijke hoogte-breedteverhouding blijft behouden in de module. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Selecteer of het zojuist bewerkte bestand alle uitvoerbestanden overschrijft die al bestaan. Dit geldt alleen voor bestanden in Adobe-opslag.</p>
      </td>
    </tbody>
</table>
