---
title: Tekstparser
description: U kunt het parserhulpmiddel van de Tekst gebruiken om tekst voor gebruik in andere  [!DNL Adobe Workfront Fusion]  scenariomodules te ontleden. Voor de tekstparser is geen verbinding vereist.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 885d714e-fc09-41a2-89dc-ebe29a355e43
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 0%

---

# [!UICONTROL Text parser]

Met de [!UICONTROL Text parser tool] kunt u tekst parseren voor gebruik in andere [!DNL Adobe Workfront Fusion] -scenario-modules. Voor [!UICONTROL Text parser] is geen verbinding vereist.

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
   <p>Geen Workfront Fusion-licentievereiste</p>
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

## API-informatie voor tekstparser

De schakelaar van de parser van de Tekst gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v2</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL Text parser] modules en hun velden

Wanneer u [!UICONTROL Text parser] modules configureert, geeft [!DNL Adobe Workfront Fusion] de onderstaande velden weer. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Transformatoren

* [[!UICONTROL Get Elements from HTML]](#get-elements-from-html)
* [[!UICONTROL Get Elements from text]](#get-elements-from-text)
* [[!UICONTROL HTML to Text]](#html-to-text)
* [[!UICONTROL Match Pattern]](#match-pattern)
* [[!UICONTROL Replace]](#replace)

#### [!UICONTROL Get Elements from HTML]

Haalt de gewenste elementen op uit de HTML-code.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module finds no matches]</td> 
   <td> <p>Schakel deze optie in om ervoor te zorgen dat de module het scenario niet stopt als er geen resultaten worden geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Element type]</td> 
   <td> <p> Selecteer het elementtype dat u wilt ophalen uit de HTML-code. </p> 
    <ul> 
     <li>[!UICONTROL Image]</li> 
     <li>[!UICONTROL Link]</li> 
     <li>[!UICONTROL iFrame element(s)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Voer de HTML-code in of wijs deze toe waaruit u de opgegeven elementtypen wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Elements from text]

Hiermee parseert u elementen van tekst op basis van het opgegeven patroon.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Input text]</td> 
   <td> <p>Typ of wijs de tekst toe die u wilt parseren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pattern]</td> 
   <td> <p>Selecteer het patroon dat de elementen weerspiegelt die u in de tekst wilt parseren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ignore Duplicate Occurrences]</td> 
   <td> <p>Schakel dit vakje in om dubbele instanties van een tekstelement te negeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL HTML to Text]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Voer de HTML-code in die u wilt omzetten in onbewerkte tekst.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Line break] </td> 
   <td> <p>Selecteer het type nieuwe regel (regeleinde).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Uppercase headings]</p> </td> 
   <td> <p>Schakel deze optie in om tekst tussen kopcodes (zoals &lt;h2&gt; &lt;/h2&gt;) om te zetten in hoofdletters.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Match Pattern]

In de module [!UICONTROL Match pattern] kunt u zoeken naar tekenreekselementen die overeenkomen met een zoekpatroon in een bepaalde tekst. Deze module gebruikt reguliere expressies (ook wel regex of regexp genoemd).

Een reguliere expressie is een reeks tekens waarin elk teken een metateken is met een speciale betekenis of een regulier teken met een letterlijke betekenis. Met deze teken- en metatekens wordt een patroon geïdentificeerd dat kan worden gebruikt voor het zoeken naar tekst. Als u bijvoorbeeld naar namen wilt zoeken, kunt u een reguliere expressie instellen om te zoeken naar een patroon dat bestaat uit twee opeenvolgende woorden die beginnen met hoofdletters. Reguliere expressies zijn een krachtig gereedschap voor het zoeken en bewerken van tekst.

Een discussie over reguliere expressies valt buiten het toepassingsgebied van dit artikel. Wij adviseren de volgende middelen:

* Voor de volledige lijst van metacharacters, zie [ Reguliere uitdrukkingen ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) in MDN Web docs.
* Voor een leerprogramma op hoe te om regelmatige uitdrukkingen tot stand te brengen, adviseren wij [ RegexOne ](https://regexone.com/).
* Voor het experimenteren met regelmatige uitdrukkingen, adviseren wij de [ Reguliere Uitdrukkingen 101 ](https://regex101.com/) website. Selecteer de ECMAScript-FLAVOR (JavaScript) in het linkerdeelvenster.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Pattern] </td> 
   <td> <p>Voer het reguliere-expressiepatroon in. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b> Voorbeeld: </b></span></span> <code>[+-]?(\d+(\.\d+)?|\.\d+)([eE][+-]?\d+)?</code> haalt alle cijfers in de verstrekte tekst uit.</p> <p>Opmerking:  <p>Het patroon moet ten minste één vastleggroep tussen haakjes <code>()</code> bevatten. Als het patroon geen vastleggingsgroepen bevat, is de uitvoerbundel leeg.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Global match]</td> 
   <td> <p>Schakel deze optie in om alle overeenkomsten in de tekst op te halen. Elke overeenkomst wordt uitgevoerd in een afzonderlijke bundel. Als deze optie is uitgeschakeld, haalt de module alleen het eerste item op.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Case sensitive]</td> 
   <td> <p> Schakel deze optie voor deze module in om tekst als hoofdlettergevoelig te behandelen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>Schakel deze optie in om ervoor te zorgen dat metatekens aan het begin en einde (<code>^</code> en <code>$</code> ) overeenkomen met het begin of einde van elke regel, en niet alleen met het uiterste begin of einde van de gehele invoertekenreeks.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Singleline]</td> 
   <td>Schakel deze optie in om ervoor te zorgen dat de punt (.) overeenkomt met nieuwe-regeltekens (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p>Schakel deze optie in om ervoor te zorgen dat de module het scenario niet stopt als er geen resultaten worden geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>Voer de tekst in of wijs de tekst toe die u aan het patroon wilt aanpassen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Replace]

Zoekt de ingevoerde tekst naar een opgegeven waarde of reguliere expressie en vervangt het resultaat door de nieuwe waarde.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Pattern] </td> 
   <td> <p>Voer de zoekterm in. U kunt ook een reguliere expressie gebruiken. Zie de module <a href="#match-pattern" class="MCXref xref">[!UICONTROL Match Pattern]</a> voor meer informatie over de reguliere expressie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New value]</td> 
   <td> <p> Voer de waarde in die u de zoekterm wilt vervangen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Global match]</td> 
   <td> <p>Schakel deze optie in om alle overeenkomsten in de tekst op te halen. Elke overeenkomst wordt uitgevoerd in een afzonderlijke bundel. Als deze optie is uitgeschakeld, haalt de module alleen het eerste item op.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Case sensitive]</td> 
   <td> <p> Schakel deze optie voor deze module in om tekst als hoofdlettergevoelig te behandelen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>Schakel deze optie in om ervoor te zorgen dat metatekens aan het begin en einde (<code>^</code> en <code>$</code> ) overeenkomen met het begin of einde van elke regel, en niet alleen met het uiterste begin of einde van de gehele invoertekenreeks.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Singleline]</td> 
   <td>Schakel deze optie in om ervoor te zorgen dat de punt (.) overeenkomt met nieuwe-regeltekens (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>Voer de tekst in die u wilt doorzoeken.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Gegevensovervulling

Het schrapen van gegevens, soms genoemd Webschrapping, gegevensextractie, of Web het oogsten, is het proces om gegevens van websites te verzamelen en het op te slaan in uw lokale gegevensbestand of spreadsheets. Als u gegevens van een website wilt verwijderen en u niet bekend bent met reguliere expressies, kunt u een gereedschap voor het verwijderen van gegevens gebruiken.

Als het hulpmiddel van de gegevensschrapping REST API verstrekt, kunt u met het via onze universele [[!UICONTROL HTTP] modules ](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors) en [ Webhooks ](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md) modules verbinden.

## Problemen met tekstparsering

Gebruik deze informatie als u geen tekstparser kunt krijgen om output te veroorzaken.

>[!BEGINSHADEBOX]

Voorbeeld:

De module moet het bestandstype van het bestandsdocument filename.docx parseren en de bestandsextensie varieert van DOCX tot PDF tot CSV.

De expressie die u in dit geval kunt gebruiken, is [!DNL \..+]

Deze reguliere expressie resulteert normaal gesproken in een volledige overeenkomst.

Het implementeren van deze expressie in uw tekstparser resulteert echter niet in een overeenkomst:

![ Geen gelijke ](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-you-dont-get-a-match-350x365.png)

De reden hiervoor is dat &quot;i&quot;slechts het aantal gelijken per gelijke toont zodat in dit geval, hebben wij 2 gelijken, daarom nadat &quot;i&quot;er een numerieke waarde 1 en 2 is. Het gebruik hiervan is dat als u ooit gegevens via een filter moet aanpassen of doorgeven, alleen de tweede overeenkomende waarde kan worden opgegeven welke waarde wordt vertegenwoordigd door de numerieke waarde.

![ Gelijke ](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-matches-350x355.png)

Als u de overeenkomende waarden wilt ophalen die u nodig hebt om haakjes toe te voegen aan het onderdeel dat u wilt parseren (bijvoorbeeld als u wilt extraheren uit &quot;filename.docx&quot; - alleen &quot;docx&quot;), moeten de haakjes volgens de regex-expressie die we in dit casescenario gebruiken, worden toegepast op \.(.+)

Hierdoor wordt de DOCX vastgelegd, in een groep geplaatst en de &quot;.&quot; van het.

![ krijgt gelijken ](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-get-matches-350x592.png)

In de uitvoer die in de onderstaande afbeelding wordt weergegeven, komt de vastgelegde groep overeen met elk willekeurig teken (behalve regeleinde).

![ Output ](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-output-350x389.png)

Een andere oplossing die ook regex opneemt, gebruikt de vervangingsfunctie

`{{replace("abcdefghijklmno pqr stuvw xyz.docx"; "/.\./"; ".")}}`

Vervang `abcdefghijklmno pqr stuvw xyz.docx` vervolgens door de werkelijke bestandsnaamvariabele.

>[!ENDSHADEBOX]
