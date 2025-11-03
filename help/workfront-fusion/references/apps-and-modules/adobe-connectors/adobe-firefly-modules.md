---
title: Adobe Firefly-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Adobe Firefly] gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '2301'
ht-degree: 0%

---

# [!DNL Adobe Firefly] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Adobe Firefly] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [&#x200B; een scenario creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk Adobe Workfront Workflow-pakket en elk Adobe Workfront Automation and Integration-pakket</p><p>Workfront Ultimate</p><p>Workfront Prime en Select packages, met extra aanschaf van Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p><p>Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie</td> 
   <td>
   <p>Exploitatie gebaseerd: geen Workfront Fusion-licentievereisten</p>
   <p>Connectorgebaseerde (verouderde): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Voordat u de [!DNL Adobe Firefly] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!DNL Adobe Firefly] account hebben.

## Adobe Firefly API-informatie

De Adobe Firefly-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken met [!DNL Adobe Firefly]

Verbinding maken voor uw [!DNL Adobe Firefly] -modules:

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
        <td>Voer uw [!UICONTROL Adobe] [!UICONTROL Client ID] in. Dit vindt u in de sectie [!UICONTROL Credentials] Details van [!DNL Adobe Developer Console] .</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] [!UICONTROL Client Secret] in. Dit vindt u in de sectie [!UICONTROL Credentials] Details van [!DNL Adobe Developer Console] .</td>
        </tr>
      </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## [!DNL Adobe Firefly] modules en hun velden

Wanneer u [!DNL Adobe Firefly] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Firefly] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Een afbeelding uitbreiden

Deze actiemodule breidt een afbeelding uit, optioneel met inhoud van een vraag die u opgeeft.

Deze module werkt met de Firefly API V3 Async. De vorige versie van deze module is vervangen en wordt in de nabije toekomst verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie [!DNL Adobe Campaign] Verbinding maken met <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Firefly]</a> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Voer een vraag in of wijs een vraag toe aan de inhoud waarmee u de afbeelding wilt uitvouwen. Als er geen vraag wordt weergegeven, wordt de afbeelding uitgebreid met inhoud die overeenkomt met de oorspronkelijke afbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Voer een getal in tussen 1 en 4. De module genereert dit aantal uitgebreide afbeeldingsvariaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source]</td> 
   <td>Selecteer hoe u het bronbestand opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expanded image format]</td> 
   <td>Selecteer de bestandsindeling waarin de uitgevouwen afbeelding wordt opgeslagen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand by]</td> 
   <td>  <p>Selecteer of u de afbeelding wilt uitvouwen door de afbeelding te plaatsen of door een masker te gebruiken.</p> 
   <ul>
   <li><b>Plaatsing</b><p>Voer de horizontale en verticale uitlijning in en de inzet van de geplaatste afbeelding vanaf de randen.</p></li>
   <li><b>Masker</b><p>Selecteer het bronbestand voor het masker en geef aan of het masker moet worden omgekeerd.</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de hoogte en breedte die u wilt instellen als de uitgevouwen afbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Voor elk beeld dat de module zal produceren, <b> toevoegt punt </b> en gaat of een geheel in kaart brengt. U kunt dit zelfde zaad in een andere gebruiken breid een beeldmodule uit om een gelijkaardige beeld met verschillende stijlen te produceren. Het aantal zaden dat u toevoegt, moet gelijk zijn aan het veld Aantal variaties.</td> 
  </tr> 
 </tbody> 
</table>

### Een afbeelding uitvouwen (afgekeurd)

Deze module is vervangen en wordt in de nabije toekomst verwijderd. Gebruik in plaats hiervan de module Een afbeelding uitbreiden.

### Een afbeelding vullen

Deze actiemodule vult het gemaskeerde gebied van een afbeelding, optioneel met inhoud van een vraag die u opgeeft.

Deze module werkt met de Firefly API V3 Async. De vorige versie van deze module is vervangen en wordt in de nabije toekomst verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie [!DNL Adobe Campaign] Verbinding maken met <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Firefly]</a> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
   <td>Selecteer hoe u het afbeeldingsbronbestand opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask > Source]</td> 
   <td>Selecteer hoe u het bronbestand van het masker oplevert:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Voer een vraag in of wijs een vraag toe aan de inhoud waarmee u de afbeelding wilt vullen. Als er geen vraag wordt weergegeven, wordt de afbeelding gevuld met inhoud die overeenkomt met de oorspronkelijke afbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Voer een getal in tussen 1 en 4. De module genereert dit aantal gevulde afbeeldingsvariaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filled image format]</td> 
   <td>Selecteer de bestandsindeling waarin de gevulde afbeelding wordt opgeslagen.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Voor elk beeld dat de module zal produceren, <b> toevoegt punt </b> en gaat of een geheel in kaart brengt. U kunt dit zelfde zaad in een andere gebruiken breid een beeldmodule uit om een gelijkaardige beeld met verschillende stijlen te produceren. Het aantal zaden dat u toevoegt, moet gelijk zijn aan het veld Aantal variaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de grootte van de gevulde afbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Als een landinstelling wordt opgegeven, genereert de module inhoud die relevanter is voor de opgegeven landinstelling. <p>De landinstelling moet worden vermeld in ISO 639-1 taalcode en ISO 3166-1 regio.</p><p> Voorbeeld: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### Een afbeelding vullen (afgekeurd)

Deze module is vervangen en wordt in de nabije toekomst verwijderd. Gebruik in plaats hiervan de module Een afbeelding vullen.

### Een afbeelding genereren

Deze actiemodule genereert een afbeelding op basis van een vraag die u opgeeft. U kunt ook een optionele referentieafbeelding opgeven en de gegenereerde afbeelding komt overeen met de stijl van de referentieafbeelding.

Deze module werkt met de Firefly API V3 Async. De vorige versie van deze module is vervangen en wordt in de nabije toekomst verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie [!DNL Adobe Campaign] Verbinding maken met <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Firefly]</a> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Voer een vraag in of wijs een vraag toe voor de afbeelding die u wilt genereren. Als u meer details opgeeft in de vraag, hebt u meer controle over wat er in de afbeelding wordt weergegeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Selecteer de Firefly-modelversie die u wilt gebruiken om de afbeelding te genereren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Voer een getal in tussen 1 en 4. De module genereert dit aantal afbeeldingsvariaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Selecteer de bestandsindeling waarin de uitgevouwen afbeelding wordt opgeslagen. Als u standaard selecteert, wordt de bestandsindeling JPEG als er geen referentieafbeelding is opgegeven. Als een referentieafbeelding wordt opgegeven, is de bestandsindeling van de gegenereerde afbeelding dezelfde als die van de referentieafbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Image reference]</td> 
    <td>Selecteer hoe u het bronbestand voor de structuur van de nieuwe afbeelding opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Voer een getal in tussen 0 en 100 om te bepalen hoe strikt Firefly de structuur van de bronafbeelding volgt. Hogere waarden betekenen dat Firefly de afbeelding strikter volgt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Selecteer hoe u het bronbestand voor de stijl van de nieuwe afbeelding opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Voer een getal in tussen 0 en 100 om te bepalen hoe strikt Firefly de stijl van de bronafbeelding volgt. Hogere waarden betekenen dat Firefly de afbeelding strikter volgt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Presets]</td> 
   <td>Als u een vooraf ingestelde stijl wilt gebruiken, voegt de klik punt toe en gaat of kaart de stijl in die u wilt gebruiken.<p>Voor een lijst van vooraf ingestelde stijlen, zie <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" > ModelStijlen van het Beeld </a> in de de ontwikkelaarsdocumentatie van Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Negative prompt]</td> 
   <td>Typ of wijs de woorden toe die u in de gegenereerde inhoud wilt vermijden. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content class]</td> 
   <td>Selecteer of u de gegenereerde afbeelding meer als een foto wilt weergeven, of meer als een gemaakte illustratie. <ul><li><b>Foto</b><p>Voer waarden in voor de lensopening, de sluitersnelheid (in seconden) en het gezichtsveld (in millimeters).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>Voor elk beeld dat de module zal produceren, <b> toevoegt punt </b> en gaat of een geheel in kaart brengt. U kunt dit zelfde zaad in een andere gebruiken breid een beeldmodule uit om een gelijkaardige beeld met verschillende stijlen te produceren. Het aantal zaden dat u toevoegt, moet gelijk zijn aan het veld Aantal variaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de grootte van de gegenereerde afbeelding.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Visual intensity]</td> 
   <td>Voer een geheel getal in of wijs een geheel getal toe dat de algemene intensiteit van de bestaande visuele kenmerken van de foto vertegenwoordigt. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Als een landinstelling wordt opgegeven, genereert de module inhoud die relevanter is voor de opgegeven landinstelling. <p>De landinstelling moet worden vermeld in ISO 639-1 taalcode en ISO 3166-1 regio.</p><p> Voorbeeld: <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>Schakel deze optie in om een afbeelding te genereren die oneindig in elke richting kan worden herhaald.</td> 
  </tr> 
 </tbody> 
</table>

### Een afbeelding genereren (afgekeurd)

Deze module is vervangen en wordt in de nabije toekomst verwijderd. Gebruik in plaats hiervan de module Een afbeelding genereren.

### Een objectsamenstelling genereren

Deze actiemodule combineert afbeeldingen die door Firefly zijn gegenereerd om een samengestelde afbeelding te maken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie [!DNL Adobe Campaign] Verbinding maken met <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Firefly]</a> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Voer een vraag in of wijs een vraag toe voor de afbeelding die u wilt genereren. Als u meer details opgeeft in de vraag, hebt u meer controle over wat er in de afbeelding wordt weergegeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Voer een getal in tussen 1 en 4. De module genereert dit aantal afbeeldingsvariaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content classs]</td> 
   <td>Selecteer of u de gegenereerde afbeelding meer wilt weergeven als een foto of als een soort illustratie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
    <td>Selecteer hoe u het bronbestand voor de structuur van de nieuwe afbeelding opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Selecteer de bestandsindeling waarin de uitgevouwen afbeelding wordt opgeslagen. Als u standaard selecteert, wordt de bestandsindeling JPEG als er geen referentieafbeelding is opgegeven. Als een referentieafbeelding wordt opgegeven, is de bestandsindeling van de gegenereerde afbeelding dezelfde als die van de referentieafbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Selecteer hoe u het bronbestand voor de stijl van de nieuwe afbeelding opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Voer een getal in tussen 0 en 100 om te bepalen hoe strikt Firefly de stijl van de bronafbeelding volgt. Hogere waarden betekenen dat Firefly de afbeelding strikter volgt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Presets]</td> 
   <td>Als u een vooraf ingestelde stijl wilt gebruiken, voegt de klik punt toe en gaat of kaart de stijl in die u wilt gebruiken.<p>Voor een lijst van vooraf ingestelde stijlen, zie <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" > ModelStijlen van het Beeld </a> in de de ontwikkelaarsdocumentatie van Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de grootte die de gegenereerde samenstelling moet hebben. </td> 
  </tr> 
 </tbody> 
</table>

### Vergelijkbare afbeeldingen genereren

Deze actiemodule genereert afbeeldingen die lijken op de bronafbeelding die u opgeeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie [!DNL Adobe Campaign] Verbinding maken met <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Firefly]</a> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Voer een getal in tussen 1 en 4. De module genereert dit aantal afbeeldingsvariaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Selecteer de Firefly-modelversie die u wilt gebruiken om de afbeeldingen te genereren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Selecteer de bestandsindeling waarin de uitgevouwen afbeelding wordt opgeslagen. Als u standaard selecteert, wordt de bestandsindeling JPEG als er geen referentieafbeelding is opgegeven. Als een referentieafbeelding wordt opgegeven, is de bestandsindeling van de gegenereerde afbeelding dezelfde als die van de referentieafbeelding.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
    <td>Selecteer hoe u het bronbestand voor de structuur van de nieuwe afbeelding opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Selecteer hoe u het bronbestand voor de stijl van de nieuwe afbeelding opgeeft:<ul><li><p><b>Bestand</b></p><p>Selecteer een bronbestand uit een vorige module of wijs de naam en het bestand met referentieafbeelding van het bronbestand toe.</p></li><li><p><b>Vooraf geplaatste URL</b></p><p>Voer de URL van de bronafbeelding in of wijs deze toe.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de grootte die de gegenereerde samenstelling moet hebben. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Voor elk beeld dat de module zal produceren, <b> toevoegt punt </b> en gaat of een geheel in kaart brengt. U kunt dit zelfde zaad in een andere gebruiken breid een beeldmodule uit om een gelijkaardige beeld met verschillende stijlen te produceren. Het aantal zaden dat u toevoegt, moet gelijk zijn aan het veld Aantal variaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>Schakel deze optie in om een afbeelding te genereren die oneindig in elke richting kan worden herhaald.</td> 
  </tr> 
 </tbody> 
</table>


### Een aangepaste API-aanroep maken

Deze actiemodule maakt een aangepaste aanroep naar de Firefly API.

Voor specifieke beschikbare APIs, zie [&#x200B; Adobe Firefly API &#x200B;](https://developer.adobe.com/firefly-services/docs/firefly-api/) in de documentatie van Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie [!DNL Adobe Firefly] Verbinding maken met <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Firefly]</a> .</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Voer een pad in dat relatief is ten opzichte van <code>https://firefly-api.adobe.io/</code> .</p>
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
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

