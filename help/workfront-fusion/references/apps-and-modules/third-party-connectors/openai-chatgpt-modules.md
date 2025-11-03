---
title: OpenAI-modules (ChatGPT)
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die OpenAIT (ChatGPT) gebruiken, en deze ook verbinden met meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: c8138d82-fa5a-4e69-b3cb-aa232099cb33
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1325'
ht-degree: 0%

---

# [!DNL OpenAI (ChatGPT & DALL-E)] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL OpenAI (ChatGPT & DALL-E)] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Als u [!DNL OpenAI (ChatGPT & DALL-E)] -modules wilt gebruiken, hebt u een [!DNL OpenAI] -account nodig, inclusief een API-sleutel en een organisatie-id.

## Informatie over de OpenAI-API (ChatGPT en DALL-E)

De OpenAI-connector (ChatGPT &amp; DALL-E) gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.11.1</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken [!DNL OpenAI (ChatGPT & DALL-E)] met Workfront Fusion

U kunt rechtstreeks vanuit een [!DNL OpenAI (ChatGPT & DALL-E)] -module verbinding maken met uw [!DNL OpenAI (ChatGPT & DALL-E)] -account.

1. Klik in een willekeurige [!DNL OpenAI (ChatGPT & DALL-E)] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Voer de volgende gegevens in:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Voer een naam in voor de nieuwe verbinding.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>U kunt de API-sleutel zoeken in uw OpenAI-gebruikersinstellingen.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organization ID] </td> 
      <td>U kunt uw organisatie-id vinden op de pagina Instellingen organisatie in OpenAI.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.


## [!DNL OpenAI (ChatGPT & DALL-E)] modules en hun velden

Wanneer u [!DNL OpenAI (ChatGPT & DALL-E)] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL OpenAI (ChatGPT & DALL-E)] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Voltooien maken

>[!IMPORTANT]
>
>Deze module is vervangen.

<!--

This action module creates a completion for the provided prompt or chat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Enter or map the ID of the model to use. You can use the Get models module to see all of your available models. </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Temperature]</td> 
   <td> This value must be between 0 and 2, and determines the randomness of the output. Higher values produce output that is more random, while lower values produce more focused output. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating completions in the <a href="https://platform.openai.com/docs/api-reference/completions/create" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Een moderatie maken

Deze actiemodule bepaalt of tekst het Inhoudsbeleid van OpenAI schendt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Voor elke steekproef van tekst die u wilt omvatten, klik <b> toevoegen punt </b> en ga of kaart de tekst in. Neem het volledige tekstvoorbeeld op.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Voer de id van het te gebruiken model in of wijs deze toe. U kunt de Get module van modellen gebruiken om al uw beschikbare modellen te zien. </td> 
  </tr> 
 </tbody> 
</table>

### Een bewerking maken

Deze actiemodule keert een uitgegeven versie van een herinnering terug u, na uw instructies verstrekt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Voer de id van het te gebruiken model in of wijs deze toe. U kunt de Get module van modellen gebruiken om al uw beschikbare modellen te zien. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Typ of wijs de tekst toe die u wilt bewerken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Instruction]</td> 
   <td> Voer de instructies voor de bewerking in of wijs deze toe. Voorbeeld: "Corrigeer de spelfouten." </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Voor informatie over de facultatieve geavanceerde montages in deze module, zie de informatie over het creëren van geeft in de <a href="https://platform.openai.com/docs/api-reference/edits/create" class="MCXref xref"> documentatie OpenAI API </a> uit.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Een insluiting maken

In deze actiemodule wordt een insluitvector gemaakt die de invoertekst vertegenwoordigt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Voer de id van het te gebruiken model in of wijs deze toe. U kunt de Get module van modellen gebruiken om al uw beschikbare modellen te zien. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input text to embed]</td> 
   <td> Typ of wijs de tekst toe die u wilt insluiten. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> Voer een unieke id in of wijs een unieke id toe die uw eindgebruiker vertegenwoordigt en die OpenAI kan helpen misbruik te controleren en op te sporen </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Ga of kaart het maximumaantal uitgeeft in u de module wilt werken met tijdens elke cyclus van de scenariouitvoering.</td> 
  </tr> 
 </tbody> 
</table>

### Chatvoltooiing maken

Gezien een lijst van berichten beschrijvend een gesprek, keert deze actiemodule een reactie terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Voer de id van het te gebruiken model in of wijs deze toe. U kunt de Get module van modellen gebruiken om al uw beschikbare modellen te zien. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>De berichten beschrijven het gesprek tot dusver. Voor elk bericht wilt u toevoegen, <b> toevoegen punt </b> en vullen het volgende in:
   <ul>
   <li> <b> Rol </b>: Selecteer de rol van de auteur van dit bericht.</li>
   <li> <b> Inhoud </b>: Ga of kaart de inhoud van dit bericht in.</li>
   <li> <b> Naam </b>: Ga of kaart de naam van de auteur van dit bericht in. De naam kan hoofdletters en kleine letters, cijfers en onderstrepingstekens bevatten. De naam mag maximaal 64 tekens lang zijn.</li>
   </ul>
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Voor informatie over de facultatieve geavanceerde montages in deze module, zie de informatie over het creëren van praatjevoltooiing in de <a href="https://platform.openai.com/docs/api-reference/chat/create" class="MCXref xref"> documentatie OpenAI API </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Edit image

This action module makes edits or creates variations of existing images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to create edits or variations of the image.
   <p>NOTE: Images must be a valid PNG file, less than 4MB, and square. If mask is not provided, the image must have transparency, which will be used as the mask.</p> 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Text description of desired image]</td> 
   <td> <p>If editing an image, enter or map a description of the edits you want to create. Maximum length is 1000 characters.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating image edits or variations in the <a href="https://platform.openai.com/docs/api-reference/images/createEdit" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Afbeeldingen genereren

Deze actiemodule genereert of manipuleert afbeeldingen met Dall-E-modellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text description of the desire image]</td> 
   <td> Voer een beschrijving van de gewenste afbeelding in of wijs deze toe. De maximale lengte van de beschrijving is 1000 tekens. 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Voor informatie over de facultatieve geavanceerde montages in deze module, zie de informatie over het creëren van beelden in de <a href="https://platform.openai.com/docs/api-reference/images/create" class="MCXref xref"> documentatie OpenAI API </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modellen ophalen

In deze module vindt u een overzicht en beschrijving van de verschillende modellen die beschikbaar zijn in de OpenAI API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> Selecteer of u een lijst van alle modellen wilt krijgen of een specifiek model terugwinnen.
    <ul>
    <li><p><b>Lijstmodellen </b></p><p>Deze actie maakt een lijst van de momenteel beschikbare modellen, en verstrekt basisinformatie over elk zoals de eigenaar en de beschikbaarheid.</p></li>
    <li><p><b>Model ophalen </b></p><p>Ga of kaart identiteitskaart van het model in u wilt terugwinnen. </p></li>
   </ul>
 </td> 
  </tr>
 </tbody> 
</table>

### Aangepaste API-aanroep maken

Deze actie module een aangepaste HTTP-aanvraag naar de OpenAI API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Een pad invoeren ten opzichte van <code>https://api.openai.com/v1/</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt de machtigingsheaders automatisch toe.</p> </td> 
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

<!--

### Manage Audio

This action modules converts audio to text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to transcribe the audio into the input language, or into English.
   <p>If transcribing into the input language, you can select the language in this module's advanced settings. </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Enter or map the maximum number of edits you want the module to work with during each scenario execution cycle.</td> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating transcriptions in the <a href="https://platform.openai.com/docs/api-reference/audio/createTranscription" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

-->

### Bestanden beheren

In deze actiemodule worden bestanden of bestandsinhoud weergegeven, verwijderd of opgehaald.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> Selecteer de handeling die u wilt uitvoeren. 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> Als u een bestand verwijdert of een bestand of bestandsinhoud ophaalt, voert u de id van het bestand in of wijst u deze toe. 
  </tr> 
</tbody>
</table>

### FineTunes beheren

U kunt fijnafstemmende taken beheren om een model af te stemmen op uw specifieke trainingsgegevens.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL OpenAI (ChatGPT & DALL-E)] rekening aan de Fusie van Workfront, zie <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref"> het Verbinden [!DNL OpenAI (ChatGPT & DALL-E)] met de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Selecteer de handeling die u wilt uitvoeren.
   <ul>
   <li><p>Een model nauwkeurig afstellen op basis van een gegevensset</p><p>Voer een beschrijving in of wijs een beschrijving toe voor de gewenste afbeelding.</p>
     <li><p>Informatie ophalen over een fijnafstemmingstaak</p><p>Voer de id van de taak in of wijs deze toe.</p>
   <li><p>Een verfijnde taak annuleren</p><p>Voer de id van de taak in of wijs deze toe.</p>
   <li><p>Een verfijnde taak annuleren</p><p>Voer de id van de taak in of wijs deze toe.</p>
   <li><p>Status-updates ophalen voor een fijnafstemmingstaak</p><p>Voer de id van de taak in of wijs deze toe en geef aan of u deze updates wilt streamen.</p>
   <li><p>Een verfijnd model verwijderen</p><p>Voer de id in van het model dat u wilt verwijderen of wijs deze toe.</p>
 </ul> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> Als u een bestand verwijdert of een bestand of bestandsinhoud ophaalt, voert u de id van het bestand in of wijst u deze toe. 
  </tr> 
</tbody>
