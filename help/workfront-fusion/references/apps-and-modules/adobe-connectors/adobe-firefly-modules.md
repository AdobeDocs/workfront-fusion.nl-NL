---
title: Adobe Firefly
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL Adobe Firefly] gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 1219642306c03cb0aa6037493ce2f02ced80b99d
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 0%

---

# [!DNL Adobe Firefly] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Adobe Firefly] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Voordat u de [!DNL Adobe Firefly] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!DNL Adobe Firefly] account hebben.

## API-informatie voor Adobe Firefly

De verbindingslijn van de Adobe Firefly gebruikt het volgende:

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

Wanneer u [!DNL Adobe Firefly] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Firefly] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Een afbeelding uitbreiden

Deze actiemodule breidt een afbeelding uit, optioneel met inhoud van een vraag die u opgeeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > Verbinding maken met [!DNL Adobe Firefly]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
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
   <td role="rowheader">[!UICONTROL Expanded image format]</td> 
   <td>Selecteer de bestandsindeling waarin de uitgevouwen afbeelding wordt opgeslagen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>  <p>Selecteer een bronbestand uit een vorige module of wijs de naam en het afbeeldingsbestand (gegevens) van het bronbestand toe.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de grootte van de uitgevouwen afbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>Voor elk zaad wilt u gebruiken, <b> toevoegen punt </b> en ingaan of een geheel in kaart brengen. U kunt dit zelfde zaad in een andere gebruiken breid een beeldmodule uit om een gelijkaardige beeld met verschillende stijlen te produceren. </td> 
  </tr> 
 </tbody> 
</table>

## Een afbeelding vullen

Deze actiemodule vult het gemaskeerde gebied van een afbeelding, optioneel met inhoud van een vraag die u opgeeft.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > Verbinding maken met [!DNL Adobe Firefly]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Image]</td> 
   <td>  <p> Voor elk beeld wilt u vullen, <b> een beeld </b> toevoegen, dan een brondossier van een vorige module selecteren of de het dossiernaam en gegevens van het Beeld van het brondossier in kaart brengen.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask]</td> 
   <td>  <p>  Voor elk masker wilt u gebruiken, <b> toevoegen een masker </b>. Selecteer een bronbestand uit een vorige module of wijs de naam en het masker van het bronbestand toe. Het maskerbestand vertegenwoordigt het aangepaste masker dat wordt gevuld met gegenereerde inhoud.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de grootte van de gevulde afbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Voor elk beeld dat de module zal produceren, <b> toevoegt punt <b> en gaat of een geheel in kaart brengt. U kunt dit zelfde zaad in een andere gebruiken breid een beeldmodule uit om een gelijkaardige beeld met verschillende stijlen te produceren. Het aantal zaden dat u toevoegt, moet gelijk zijn aan het veld Aantal variaties.</td> 
  </tr> 
 </tbody> 
</table>

## Een afbeelding genereren

Deze actiemodule genereert een afbeelding op basis van een vraag die u opgeeft. U kunt ook een optionele referentieafbeelding opgeven en de gegenereerde afbeelding komt overeen met de stijl van de referentieafbeelding.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Zie <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > Verbinding maken met [!DNL Adobe Firefly]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Campaign] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Voer een vraag in of wijs een vraag toe aan de afbeelding die u wilt maken. Als u meer details opgeeft in de vraag, hebt u meer controle over wat er in de afbeelding wordt weergegeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Voer een getal in tussen 1 en 4. De module genereert dit aantal afbeeldingsvariaties.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Selecteer de bestandsindeling waarin de uitgevouwen afbeelding wordt opgeslagen. Als u de standaardinstelling selecteert, wordt de bestandsindeling JPEG als er geen referentieafbeelding is opgegeven. Als een referentieafbeelding wordt opgegeven, is de bestandsindeling van de gegenereerde afbeelding dezelfde als die van de referentieafbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>  <p>Selecteer een bronbestand uit een vorige module of wijs de naam van het referentiebestand en het referentieafbeeldingsbestand (gegevens) van het bronbestand toe. De gegenereerde afbeelding wordt zo gemaakt dat deze overeenkomt met de stijl van de referentieafbeelding.</p> </td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presets]</td> 
   <td>Als u een vooraf ingestelde stijl wilt gebruiken, voegt de klik punt toe en gaat of kaart de stijl in die u wilt gebruiken.<p>Voor een lijst van vooraf ingestelde stijlen, zie <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" > ModelStijlen van het Beeld </a> in de documentatie van de ontwikkelaar van de Adobe.</td> 
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
   <td>Voer een geheel getal in of wijs een geheel getal toe. U kunt dit zelfde zaad in een andere gebruiken breid een beeldmodule uit om een gelijkaardige beeld met verschillende stijlen te produceren. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Selecteer de grootte van de gegenereerde afbeelding.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strength]</td> 
   <td>Voer een geheel getal in of wijs een geheel getal toe dat de intensiteit aangeeft waarmee de gegenereerde afbeelding overeenkomt met de stijl van de vooraf ingestelde stijl of de referentieafbeelding. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visual intensity]</td> 
   <td>Voer een geheel getal in of wijs een geheel getal toe dat de algemene intensiteit van de bestaande visuele kenmerken van de foto vertegenwoordigt. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Als een landinstelling wordt opgegeven, genereert de module inhoud die relevanter is voor de opgegeven landinstelling. <p>De landinstelling moet worden vermeld in ISO 639-1 taalcode en ISO 3166-1 regio.</p><p> Voorbeeld: <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>



### Een aangepaste API-aanroep maken

Deze actiemodule doet een douanevraag aan de Firefly API.

Voor specifieke beschikbare APIs, zie [ Adobe Firefly API ](https://developer.adobe.com/firefly-services/docs/firefly-api/) in de documentatie van Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Zie <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" > Verbinding maken met [!DNL Adobe Firefly]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe Firefly] .</td>
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
        <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p>
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

