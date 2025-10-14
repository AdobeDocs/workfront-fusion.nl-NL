---
title: Google Forms-modules
description: De  [!DNL Adobe Workfront Fusion Google Forms]  modules staan u toe om reacties op uw Google Forms te controleren, te selecteren, toe te voegen, bij te werken of te schrappen.
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%

---

# [!DNL Google Forms] modules

Met de Adobe Workfront Fusion [!DNL Google Forms] -modules kunt u reacties op uw [!DNL Google Forms] controleren, selecteren, toevoegen, bijwerken of verwijderen.

Als u [!DNL Google Docs] wilt gebruiken met Adobe Workfront Fusion, hebt u een [!DNL Google] -account nodig. Als u nog geen [!DNL Google] -account hebt, kunt u er een maken op de pagina [!DNL Google] Account Help.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u [!DNL Google Forms] -modules wilt gebruiken, moet u een [!DNL Google] -account hebben.

## Google Forms API-informatie

De Google Forms-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>2.0.10.</td> 
  </tr>
 </tbody> 
 </table>

## Een werkblad maken op basis van het formulier

Als u met reacties op formulieren wilt werken, moet u eerst het werkblad met reacties maken.

1. Open het formulier.
1. Ga naar de tab **[!UICONTROL Responses]** .
1. Klik het **[!UICONTROL Create Spreadsheet]** pictogram ![&#x200B; pictogram van de Spreadsheet &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png).

1. Selecteer of u een nieuw spreadsheet of een bestaand spreadsheet wilt creëren
1. Klik op **[!UICONTROL Create]**.

## [!DNL Google Forms] modules en hun velden

Wanneer u [!DNL Google Forms] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Google Forms] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

#### [!UICONTROL Watch Responses]

Hiermee controleert u het formulier op nieuwe reacties.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecteer het werkblad met de reacties van het formulier waarop u nieuwe reacties wilt controleren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecteer het blad met de formulierreacties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers]</td> 
   <td>Geef de koptekstrij van de tabel op. De standaardrij is <code>A1:Z1</code> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Geef op hoe de waarden in de uitvoer moeten worden weergegeven.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong> </p> <p>Waarden worden berekend en opgemaakt in de reactie op basis van de opmaak van de cel. Opmaak is gebaseerd op de landinstelling van het werkblad, niet op de landinstelling van de gebruiker die het verzoek indient. Als <code>A1</code> bijvoorbeeld <code>1. 23</code> is en <code>A2 </code> <code>=A1</code> is en als valuta is opgemaakt, retourneert <code>A2</code> <code>$1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Waarden worden berekend, maar niet opgemaakt in de reactie. Als <code>A1</code> bijvoorbeeld <code>1. 23</code> is en <code>A2 </code> <code>=A1</code> is en als valuta is opgemaakt, retourneert <code>A2</code> het getal <code>1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Waarden worden niet berekend. Het antwoord bevat de formules. Als <code>A1</code> bijvoorbeeld <code>1. 23</code> is en <code>A2 </code> <code>=A1</code> is en als valuta is opgemaakt, retourneert <code>A2</code> <code>=A1</code> .</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date and time render option]</td> 
   <td>Selecteer hoe u datums, tijden en duur wilt weergeven in de uitvoer. Dit veld wordt genegeerd als [!UICONTROL Value Render Option] is ingesteld op [!UICONTROL Formatted Value] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p> Stel het maximumaantal reacties in waarmee Workfront Fusion tijdens één cyclus werkt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Add a Response]](#add-a-response)
* [[!UICONTROL Delete a Response]](#delete-a-response)
* [[!UICONTROL Update a Response]](#update-a-response)

#### [!UICONTROL Add a Response]

Deze module voegt een nieuw antwoord toe aan de onderkant van het spreadsheet van het formulier.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecteer het werkblad dat het werkblad bevat waarop u een reactie wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecteer het blad met de formulierreacties.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Voer de gewenste waarden in voor de bladkolommen. Kolommen zijn beschikbaar op basis van het blad.</p> <p>Gebruik voor de kolom [!UICONTROL Timestamp] de volgende waarde:</p><pre>formatDate(now;DD/MM/YYYY HH:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> De waarden die de gebruiker invoert, worden niet geparseerd en worden als zodanig opgeslagen. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>De waarden worden geparseerd alsof de gebruiker hen in UI typt. Getallen blijven getallen, maar tekenreeksen kunnen in getallen, datums of andere indelingen worden omgezet volgens dezelfde regels die worden toegepast bij het invoeren van tekst in een cel via de gebruikersinterface van [!DNL Google Sheets] .</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Insert data option]</td> 
   <td> <p>Geef op hoe bestaande gegevens moeten worden gewijzigd wanneer nieuwe gegevens worden ingevoerd. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>De nieuwe gegevens overschrijven bestaande gegevens in de gebieden waar ze zijn geschreven. Als u gegevens toevoegt aan het einde van het blad, worden nieuwe rijen of kolommen ingevoegd, zodat de gegevens kunnen worden geschreven.</p> </li> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>De rijen worden opgenomen voor de nieuwe gegevens.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Response]

In deze module wordt een geselecteerde reactie verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecteer het werkblad dat het werkblad bevat waarop u een reactie wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecteer het blad met de formulierreacties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Voer het nummer in of wijs het nummer toe van de rij die u wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Response]

Deze module werkt de geselecteerde reactie bij.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Selecteer het werkblad met het werkblad waarop u een reactie wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Selecteer het blad met de formulierreacties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Voer het nummer in van de rij die u wilt bijwerken of wijs dit toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Voer de nieuwe waarden in voor de gewenste kolommen. Kolommen zijn beschikbaar op basis van het blad.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> De waarden die de gebruiker invoert, worden niet geparseerd en worden als zodanig opgeslagen. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>De waarden worden geparseerd alsof de gebruiker hen in UI typt. Getallen blijven getallen, maar tekenreeksen kunnen in getallen, datums of andere indelingen worden omgezet volgens dezelfde regels die worden toegepast bij het invoeren van tekst in een cel via de gebruikersinterface van [!DNL Google Sheets] .</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

* [[!UICONTROL Search Responses]](#search-responses)
* [[!UICONTROL Search Responses (Advanced])](#search-responses-advanced)

#### [!UICONTROL Search Responses]

Deze module retourneert antwoorden die voldoen aan de opgegeven criteria.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>Verbinding</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Selecteer het formulier waarin u wilt zoeken.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>Selecteer het blad met de formulierreacties.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Column range]</td>
   <td> <p> Selecteer het kolombereik dat u wilt zoeken.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Definieer het filter waarop u reacties wilt zoeken.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sort Order] </td>
   <td> <p>Selecteer of geretourneerde reacties in oplopende of aflopende volgorde moeten worden gesorteerd.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> Selecteer de kolom waarop u de geretourneerde reacties wilt sorteren.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Geef op hoe de waarden in de uitvoer moeten worden weergegeven.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong></p> <p>Waarden worden berekend en opgemaakt in de reactie op basis van de opmaak van de cel. Opmaak is gebaseerd op de landinstelling van het werkblad, niet op de landinstelling van de gebruiker die het verzoek indient. Als <code>A1</code> bijvoorbeeld <code>1. 23</code> is en <code>A2 </code> <code>=A1</code> is en als valuta is opgemaakt, retourneert <code>A2</code> <code>$1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Waarden worden berekend, maar niet opgemaakt in de reactie. Als <code>A1</code> bijvoorbeeld <code>1. 23</code> is en <code>A2 </code> <code>=A1</code> is en als valuta is opgemaakt, retourneert <code>A2</code> het getal <code>1. 23</code> .</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Waarden worden niet berekend. Het antwoord bevat de formules. Als <code>A1</code> bijvoorbeeld <code>1. 23</code> is en <code>A2 </code> <code>=A1</code> is en als valuta is opgemaakt, retourneert <code>A2</code> <code>=A1</code> .</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Date and time render option]</td>
    <td>Selecteer hoe u datums, tijden en duur wilt weergeven in de uitvoer. Dit veld wordt genegeerd als [!UICONTROL Value Render] Optie is ingesteld op Opgemaakte waarde. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Maximum number of returned responses]</td>
   <td> <p> Stel het maximumaantal reacties in dat Workfront Fusion tijdens één cyclus retourneert.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Responses (Advanced)]

Deze module voert een onderzoek uit gebruikend [[!DNL Google Charts Query Language] &#x200B;](https://developers.google.com/chart/interactive/docs/querylanguage). Deze module retourneert geen rijnummer.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Selecteer de spreadsheet die het blad bevat u wilt zoeken.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> Selecteer het blad met de formulierreacties.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Definieer de zoekquery met de <a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a> .</p> <p>Voorbeeld: <code>select * where C = "John"</code> haalt alle waarden op voor de rij waarin de kolom C "John" is.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Maximum number of returned rows]</td>
   <td> <p> Stel het maximumaantal reacties in dat Workfront Fusion tijdens één cyclus retourneert.</p> </td> 
  </tr> 
 </tbody> 
</table>
