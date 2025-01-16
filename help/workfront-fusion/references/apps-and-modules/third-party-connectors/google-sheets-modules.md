---
title: Google Sheets-modules
description: Om  [!DNL Google Sheets]  met  [!DNL Adobe Workfront Fusion],you need the [!UICONTROL Workfront Fusion Google Sheets]  (facultatieve, maar vereist voor onmiddellijke trekkers) te gebruiken uitbreiding.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 80965570-2937-4ac8-97c0-54f7a813ec50
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3367'
ht-degree: 0%

---

# [!DNL Google Sheets] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Google Sheets] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie [ een verbinding tot stand brengen  [!DNL Adobe Workfront Fusion]  - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Als u [!UICONTROL Google Sheets] -modules wilt gebruiken, moet u een [!UICONTROL Google] -account hebben.

## Informatie over Google Sheets API

De Google Sheets-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://sheets.googleapis.com/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v2.5.7</td> 
  </tr>
 </tbody> 
 </table>

## Triggers

### [!UICONTROL Watch Rows]

Haalt waarden op van elke nieuwe rij die is toegevoegd aan het werkblad.

De module wint slechts nieuwe rijen terug die niet eerder zijn ingevuld. De trigger verwerkt geen overschreven rij.

>[!IMPORTANT]
>
>Als het werkblad een lege rij bevat, worden er geen rijen na de lege rij verwerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer het werkblad dat het werkblad bevat dat u wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het werkblad dat u wilt controleren voor een nieuwe rij.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table contains headers]</td> 
   <td> <p> Selecteer of het spreadsheet de kopbalrij bevat.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>De module haalt de koptekstrij niet op als uitvoergegevens. </p> <p>De namen van variabelen in de uitvoer worden aangeroepen door de kopteksten.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>De module wint ook de eerste lijstrij terug</p> <p>De namen van variabelen in de uitvoer worden A, B, C, D enzovoort genoemd.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers] </td> 
   <td> <p>Voer het bereik van de koptekstrij in. Bijvoorbeeld <code>A1:F1</code> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First table row]</td> 
   <td> <p>Voer het bereik van de eerste rij van de tabel in. Bijvoorbeeld <code>A1:F1</code> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Value render option]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>De waarden worden berekend en opgemaakt in de reactie volgens de opmaak van de cel. Opmaak is gebaseerd op de landinstelling van het werkblad, niet op de landinstelling van de gebruiker die het verzoek indient. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"$1.23"</code> .</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>De waarden worden berekend, maar niet opgemaakt in de reactie. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld het getal <code>"1.23"</code> .</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>De waarden worden niet berekend. Het antwoord zal ook de formules bevatten. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"=A1"</code> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Date and time render option]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Geeft velden voor datum, tijd, datumtijd en tijdsduur de opdracht om te worden uitgevoerd als dubbele gegevens in de indeling "serienummer", zoals deze worden gevuld door Lotus 1-2-3. Het gehele getalgedeelte van de waarde (links van het decimaalteken) telt de dagen sinds 30 december 1899. Het fractionele gedeelte (rechts van het decimaalteken) telt de tijd als een fractie van de dag. Bijvoorbeeld, zou 1 januari 1900 om 12.00 uur 2.5 zijn, 2 omdat het 2 dagen na 30 december 1899 is, en 0.5 omdat 12.00 uur een halve dag is. 1 februari 1900 om 15.625 uur. Dit is een goede manier om het jaar 1900 te beschouwen als geen schrikkeljaar.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Hiermee worden datum-, tijd-, datum- en duurvelden geïnstrueerd als tekenreeksen in de opgegeven getalnotatie (die afhankelijk is van de landinstelling van het werkblad).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] werkt tijdens één uitvoeringscyclus.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Handelingen

* [[!UICONTROL Add a Row]](#add-a-row)
* [[!UICONTROL Update a Row]](#update-a-row)
* [[!UICONTROL Clear a Row]](#clear-a-row)
* [[!UICONTROL Delete a Row]](#delete-a-row)
* [[!UICONTROL Get a Cell]](#get-a-cell)
* [[!UICONTROL Update a Cell]](#update-a-cell)
* [[!UICONTROL Clear a Cell]](#clear-a-cell)
* [[!UICONTROL Add a Sheet]](#add-a-sheet)
* [[!UICONTROL Create a Spreadsheet]](#create-a-spreadsheet)
* [[!UICONTROL Delete a Sheet]](#delete-a-sheet)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

### [!UICONTROL Add a Row]

Met deze module voegt u een rij toe aan een vel.

Wanneer u [!DNL Google Sheets] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Google Sheets] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mode]</td> 
   <td> <p>Selecteer of u de spreadsheet en het blad handmatig of door toewijzing wilt selecteren.</p> <p>Opmerking: handmatige toewijzing is bijvoorbeeld handig wanneer een nieuw spreadsheet wordt gemaakt in een [!DNL Workfront Fusion] -scenario en u gegevens rechtstreeks in het nieuwe spreadsheet wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de spreadsheet van [!DNL Google] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het blad waaraan u een rij wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column Range]</td> 
   <td>Selecteer het kolombereik waarmee u wilt werken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Selecteer of het spreadsheet de kopbalrij bevat.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>De module haalt de koptekstrij niet op als uitvoergegevens. </p> <p>De namen van variabelen in de uitvoer worden aangeroepen door de kopteksten.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>De module wint ook de eerste lijstrij terug</p> <p>De namen van variabelen in de uitvoer worden A, B, C, D enzovoort genoemd.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Values] </td> 
   <td> <p>Voer de gewenste cellen in van de rij die u wilt toevoegen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>De waarden worden geparseerd alsof de gebruiker hen in UI typt. Getallen blijven getallen, maar tekenreeksen kunnen in getallen, datums of andere indelingen worden omgezet volgens dezelfde regels die worden toegepast bij het invoeren van tekst in een cel via de gebruikersinterface van [!DNL Google Sheets] .</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> De waarden die de gebruiker invoert, worden niet geparseerd en worden als zodanig opgeslagen. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Insert data option]</td> 
   <td> <p>Geef op hoe bestaande gegevens moeten worden gewijzigd wanneer nieuwe gegevens worden ingevoerd. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>De rijen worden opgenomen voor de nieuwe gegevens.</p> </li> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>De nieuwe gegevens overschrijven bestaande gegevens in de gebieden waar ze zijn geschreven. Als u gegevens toevoegt aan het einde van het blad, worden nieuwe rijen of kolommen ingevoegd, zodat de gegevens kunnen worden geschreven.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Row]

In deze module kunt u de celinhoud in een geselecteerde rij wijzigen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mode]</td> 
   <td> <p>Selecteer of u de spreadsheet en het blad handmatig of door toewijzing wilt selecteren.</p> <p>Opmerking: handmatige toewijzing is bijvoorbeeld handig wanneer een nieuw spreadsheet wordt gemaakt in het [!UICONTROL Workfront Fusion] -scenario en u gegevens rechtstreeks in het scenario wilt toevoegen aan het nieuwe spreadsheet.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de spreadsheet van [!DNL Google] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het blad waarin u een rij wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row number]</td> 
   <td> <p> Voer het nummer in van de rij die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Selecteer of het spreadsheet de kopbalrij bevat.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Yes]</strong> </p> <p>De module haalt de koptekstrij niet op als uitvoergegevens. </p> <p>De namen van variabelen in de uitvoer worden aangeroepen door de kopteksten.</p> </li> 
     <li> <p><strong>[!UICONTROL No]</strong> </p> <p>De module wint ook de eerste lijstrij terug</p> <p>De namen van variabelen in de uitvoer worden A, B, C, D enzovoort genoemd.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Values] </td> 
   <td> <p>Voer de waarden in of wijs deze toe aan de gewenste cellen van de rij die u wilt wijzigen (bijwerken).</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>De waarden worden geparseerd alsof de gebruiker hen in UI typt. Getallen blijven getallen, maar tekenreeksen kunnen in getallen, datums of andere indelingen worden omgezet volgens dezelfde regels die worden toegepast bij het invoeren van tekst in een cel via de gebruikersinterface van [!DNL Google Sheets] .</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> De waarden die de gebruiker invoert, worden niet geparseerd en worden als zodanig opgeslagen. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Clear a Row]

Hiermee verwijdert u waarden uit een opgegeven rij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer het werkblad van [!DNL Google] dat het blad bevat waarvan u een rij wilt wissen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p> Selecteer het blad waarvan u gegevens wilt wissen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row number]</td> 
   <td> <p>Voer het nummer in van de rij waaruit u gegevens wilt wissen. Bijvoorbeeld <code> 23</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Row]

Hiermee verwijdert u een opgegeven rij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de Google-spreadsheet met het blad waaruit u een rij wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>Werkblad </td> 
   <td> <p>Selecteer het blad waarvan u een rij wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>Rijnummer</td> 
   <td> <p>Voer het nummer in van de rij die u wilt verwijderen. Voorbeeld: <code>23</code></p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a Cell]

Hiermee wordt een waarde uit een geselecteerde cel opgehaald.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de spreadsheet van [!DNL Google] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het werkblad met de cel waaruit u de gegevens wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Voer de id in van de cel waarvan u de gegevens wilt ophalen. Voorbeeld: <code>A6</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>De waarden worden berekend en opgemaakt in de reactie volgens de opmaak van de cel. Opmaak is gebaseerd op de landinstelling van het werkblad, niet op de landinstelling van de gebruiker die het verzoek indient. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"$1.23"</code> .</p> <p style="font-weight: bold;">[!DNL Unformatted value]</p> <p>De waarden worden berekend, maar niet opgemaakt in de reactie. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld het getal <code>"1.23"</code> .</p> <p style="font-weight: bold;">[!DNL Formula]</p> <p>De waarden worden niet berekend. Het antwoord zal ook de formules bevatten. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"=A1"</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!DNL Serial number]</p> <p>Geeft velden voor datum, tijd, datumtijd en tijdsduur de opdracht om te worden uitgevoerd als dubbele gegevens in de indeling "serienummer", zoals deze worden gevuld door Lotus 1-2-3. Het gehele getalgedeelte van de waarde (links van het decimaalteken) telt de dagen sinds 30 december 1899. Het fractionele gedeelte (rechts van het decimaalteken) telt de tijd als een fractie van de dag. Bijvoorbeeld, zou 1 januari 1900 om 12.00 uur 2.5 zijn, 2 omdat het 2 dagen na 30 december 1899 is, en 0.5 omdat 12.00 uur een halve dag is. 1 februari 1900 om 15.625 uur. Dit is een goede manier om het jaar 1900 te beschouwen als geen schrikkeljaar.</p> <p style="font-weight: bold;">[!DNL Formatted string]</p> <p>Hiermee worden datum-, tijd-, datum- en duurvelden geïnstrueerd als tekenreeksen in de opgegeven getalnotatie (die afhankelijk is van de landinstelling van het werkblad).</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Cell]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de spreadsheet van [!DNL Google] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Voer de id in van de cel die u wilt bijwerken. Voorbeeld: <code>A5</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value]</td> 
   <td> <p>Voer de nieuwe waarde voor de cel in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>De waarden worden geparseerd alsof de gebruiker hen in UI typt. Getallen blijven getallen, maar tekenreeksen kunnen in getallen, datums of andere indelingen worden omgezet volgens dezelfde regels die worden toegepast bij het invoeren van tekst in een cel via de gebruikersinterface van [!DNL Google Sheets] .</p> </li> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> De waarden die de gebruiker invoert, worden niet geparseerd en worden als zodanig opgeslagen. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Clear a Cell]

Hiermee wordt een waarde uit een opgegeven cel verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de Google-spreadsheet met het vel waaruit u een cel wilt wissen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het blad waarvan u een cel wilt wissen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cell] </td> 
   <td> <p>Voer de id in van de cel die u wilt wissen. Voorbeeld: <code>A5</code> .</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Add a Sheet]

Hiermee maakt u een nieuw blad in een geselecteerde spreadsheet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de Google-spreadsheet waar u een vel wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Properties]</td> 
   <td> 
    <ul> 
     <li> <p style="font-weight: bold;">[!UICONTROL Title]</p> <p>Voer de naam van het nieuwe blad in.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Index]</p> <p>Voer de positie van het blad in. De standaardwaarde is 0 (het blad wordt op de eerste plaats geplaatst)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create a Spreadsheet]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>Voer de naam van een nieuw spreadsheet in.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Locale]</td> 
   <td> <p>Voer de landinstelling van het werkblad in een van de volgende notaties in:</p> 
    <ul> 
     <li>een ISO 639-1 taalcode zoals <code>en</code></li> 
     <li>een ISO 639-2-taalcode, zoals <code>haw</code>, als er geen 639-1 code bestaat</li> 
     <li>een combinatie van de ISO-taalcode en de landcode, zoals <code>en_US</code></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recalculation interval]</td> 
   <td> <p>De hoeveelheid tijd die moet worden gewacht voordat vluchtige functies opnieuw worden berekend:</p> <p style="font-weight: bold;">[!UICONTROL On change]</p> <p>Vluchtige functies worden bij elke wijziging bijgewerkt.</p> <p style="font-weight: bold;">[!UICONTROL On change and every minute]</p> <p>Vluchtige functies worden bij elke wijziging en elke minuut bijgewerkt.</p> <p style="font-weight: bold;">[!UICONTROL On change and hourly]</p> <p>Vluchtige functies worden bij elke verandering en per uur bijgewerkt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Time zone]</td> 
   <td> <p> Selecteer de tijdzone van het spreadsheet.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Number format]</td> 
   <td> <p>Selecteer de standaardindeling van alle cellen in het werkblad.</p> <p><strong>[!UICONTROL Text]</strong>: Tekstopmaak. Voorbeeld: <code>1000. 12</code></p> <p><strong>[!UICONTROL Number]</strong>: Number-opmaak. Voorbeeld: <code>1,000.12</code></p> <p><strong>[!UICONTROL Percent]</strong>: Percentage van opmaak. Voorbeeld: <code>10. 12%</code></p> <p><strong>[!UICONTROL Currency]</strong>: Opmaak van valuta. Voorbeeld: <code>$1,000.12</code></p> <p><strong>[!UICONTROL Date]</strong>: Datum-opmaak. Voorbeeld: <code>9/26/2008</code></p> <p><strong>[!UICONTROL Time]</strong>: Tijdnotatie. Voorbeeld: <code>3:59:00 PM</code></p> <p><strong>[!UICONTROL Date time]</strong>: Datum- en tijdnotatie. Voorbeeld: <code>9/26/08 15:59:00</code> </p> <p><strong>[!UICONTROL Scientific]</strong>Wetenschappelijke getalnotatie. Voorbeeld: <code>1. 01E+03</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheets] </td> 
   <td> <p>Klik op <strong>[!UICONTROL Add]</strong> om een werkblad aan het werkblad toe te voegen. Voer voor elk blad een titel voor het blad en de index van het blad in of wijs deze toe. Een index van 0 staat voor het eerste blad.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Sheet]

Hiermee verwijdert u een specifiek blad.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de spreadsheet van [!DNL Google] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het blad dat u wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Make an API Call]

Met deze actiemodule kunt u een aangepaste API-aanroep uitvoeren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [Fusion App] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan [!DNL Adobe Workfront Fusion] tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://sheets.googleapis.com/v4/</code> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP-aanvraagmethoden in [!DNL Adobe Workfront Fusion]</a> voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van de aanvraag toe in de vorm van een standaard JSON-object. Bijvoorbeeld <code>{"Content-type":"application/json"}</code> . [!DNL Workfront Fusion] voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:   <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zoekopdrachten

* [[!UICONTROL Search Rows]](#search-rows)
* [[!UICONTROL Search Rows (Advanced)]](#search-rows-advanced)
* [[!UICONTROL Get Range Values]](#get-range-values)
* [[!UICONTROL List Sheets]](#list-sheets)

### [!UICONTROL Search Rows]

Hiermee doorzoekt u rijen met de filteropties.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [Fusion App] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan [!DNL Adobe Workfront Fusion] tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de spreadsheet van [!DNL Google] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het blad waarin u de rijen wilt doorzoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p> Selecteer of het spreadsheet de kopbalrij bevat. Als de optie [!UICONTROL Yes] is geselecteerd, haalt de module de koptekstrij niet op als uitvoergegevens en worden de namen van variabelen in de uitvoer vervolgens aangeroepen door de koppen. Als de optie [!UICONTROL No] is geselecteerd, haalt de module ook de eerste tabelrij op en worden de namen van variabelen in de uitvoer vervolgens gewoon A, B, C, D enzovoort genoemd.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column range]</td> 
   <td>Selecteer het kolombereik waarmee u wilt werken. Voorbeeld: <code>A-F</code></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter]</td> 
   <td> <p>Stel het filter in voor de rij waarop moet worden gezocht.</p> <!--<p>For more information about filters, see <a href="/help/workfront-fusion/create-scenarios/add-modules/" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort order]</td> 
   <td>Selecteer of u oplopend of aflopend wilt sorteren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td>Kies de kolom waarop u wilt sorteren.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>De waarden worden berekend en opgemaakt in de reactie volgens de opmaak van de cel. Opmaak is gebaseerd op de landinstelling van het werkblad, niet op de landinstelling van de gebruiker die het verzoek indient. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"$1.23"</code> .</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>De waarden worden berekend, maar niet opgemaakt in de reactie. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld het getal <code>"1.23"</code> .</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>De waarden worden niet berekend. Het antwoord zal ook de formules bevatten. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"=A1"</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Geeft velden voor datum, tijd, datum en tijd de opdracht om te worden uitgevoerd als dubbele cijfers in de notatie "serienummer", zoals gevuld door Lotus 1-2-3. Het gehele getalgedeelte van de waarde (links van het decimaalteken) telt de dagen sinds 30 december 1899. Het fractionele gedeelte (rechts van het decimaalteken) telt de tijd als een fractie van de dag. Bijvoorbeeld, zou 1 januari 1900 om 12.00 uur 2.5 zijn, 2 omdat het 2 dagen na 30 december 1899 is, en 0.5 omdat 12.00 uur een halve dag is. 1 februari 1900 om 15.625 uur. Dit is een goede manier om het jaar 1900 te beschouwen als geen schrikkeljaar.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Hiermee worden datum-, tijd-, datum- en duurvelden geïnstrueerd als tekenreeksen in de opgegeven getalnotatie (die afhankelijk is van de landinstelling van het werkblad).</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned rows]</td> 
   <td>Stel het maximumaantal rijen in dat [!DNL Workfront Fusion] tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search Rows (Advanced)]

Geeft resultaten die overeenkomen met de opgegeven criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de Google-spreadsheet die het vel bevat dat u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het blad met de rijen die u wilt doorzoeken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Gebruik de lus [!DNL Google Charts Query Language] . Voorbeeld: <code>select * where B = "John"</code></p> <p>Voor meer informatie over [!DNL Google Charts Query Language], zie {de Verwijzing van de Taal van 1} Vraag </a> in de [!DNL Google] documentatie.<a href="https://developers.google.com/chart/interactive/docs/querylanguage"></p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get Range Values]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer de spreadsheet van [!DNL Google] .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sheet] </td> 
   <td> <p>Selecteer het blad waarvan u de bereikinhoud wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Range] </td> 
   <td> <p>Voer het bereik in dat u wilt ophalen. Voorbeeld: <code>A1:D25</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Table contains headers]</td> 
   <td> <p>Schakel dit vakje in als het blad een koptekstrij heeft</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Row with headers]</td> 
   <td>Voer het bereik van de tabelkoppen in. Voorbeeld <code>A1:F1</code> . Als u het veld leeg laat, veronderstelt [!DNL Workfront Fusion] dat de koptekst zich in de eerste rij van het opgegeven bereik bevindt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Formatted value]</p> <p>De waarden worden berekend en opgemaakt in de reactie volgens de opmaak van de cel. Opmaak is gebaseerd op de landinstelling van het werkblad, niet op de landinstelling van de gebruiker die het verzoek indient. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"$1.23"</code> .</p> <p style="font-weight: bold;">[!UICONTROL Unformatted value]</p> <p>De waarden worden berekend, maar niet opgemaakt in de reactie. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld het getal <code>"1.23"</code> .</p> <p style="font-weight: bold;">[!UICONTROL Formula]</p> <p>De waarden worden niet berekend. Het antwoord zal ook de formules bevatten. Als <code>A1</code> is <code>1.23</code> en <code>A2</code> is <code>=A1</code> en is opgemaakt als valuta, retourneert <code>A2</code> bijvoorbeeld <code>"=A1"</code> .</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Date and time render option]</td> 
   <td> <p style="font-weight: bold;">[!UICONTROL Serial number]</p> <p>Geeft velden voor datum, tijd, datum en tijd de opdracht om te worden uitgevoerd als dubbele cijfers in de notatie "serienummer", zoals gevuld door Lotus 1-2-3. Het gehele getalgedeelte van de waarde (links van het decimaalteken) telt de dagen sinds 30 december 1899. Het fractionele gedeelte (rechts van het decimaalteken) telt de tijd als een fractie van de dag. Bijvoorbeeld, zou 1 januari 1900 om 12.00 uur 2.5 zijn, 2 omdat het 2 dagen na 30 december 1899 is, en 0.5 omdat 12.00 uur een halve dag is. 1 februari 1900 om 15.625 uur. Dit is een goede manier om het jaar 1900 te beschouwen als geen schrikkeljaar.</p> <p style="font-weight: bold;">[!UICONTROL Formatted string]</p> <p>Hiermee worden datum-, tijd-, datum- en duurvelden geïnstrueerd als tekenreeksen in de opgegeven getalnotatie (die afhankelijk is van de landinstelling van het werkblad).</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL List Sheets]

Deze module retourneert een lijst met alle bladen in een spreadsheet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Sheets] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Spreadsheet] </td> 
   <td> <p>Selecteer het [!DNL Google] -werkblad dat de bladen bevat die u wilt weergeven.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Gebruiksbeperkingen

Als de fout `429: RESOURCE_EXHAUSTED` optreedt, hebt u de limiet van de API-snelheid overschreden.

De [!DNL Google Sheets] API heeft een grens van 500 verzoeken per 100 seconden per project, en 100 verzoeken per 100 seconden per gebruiker. Limieten voor lezen en schrijven worden afzonderlijk bijgehouden. Er is geen dagelijkse gebruikslimiet.

Zie meer details in [ developers.google.com/sheets/api/limits ](https://developers.google.com/sheets/api/limits).

## Tips en trucs

* [Hoe te om Lege Cellen van a  [!DNL Google]  Blad te krijgen](#how-to-get-empty-cells-from-a-google-sheet)
* [Voeg een knoop in een blad toe om een scenario in werking te stellen](#add-a-button-in-a-sheet-to-run-a-scenario)

### Lege cellen ophalen van een [!DNL Google Sheet]

Gebruik de module [!UICONTROL Search Rows (Advanced)] en gebruik deze formule om de kolommen op te halen die leeg zijn.
<pre>select * waarbij E null is</pre>Hier is "E"de kolom &amp; "is ongeldig"de voorwaarde. U kunt een geavanceerdere query maken met [Google Query Lang] (https://developers.google.com/chart/interactive/docs/querylanguage).

### Voeg een knoop in een blad toe om een scenario in werking te stellen

1. In [!DNL Workfront Fusion], neem **[!UICONTROL Webhook]** > **[!UICONTROL Custom webhooks]** module/trekker in het scenario op en vorm het (zie [ Webhooks ](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)).

1. Kopieer de URL van de website.
1. Voer het scenario uit.
1. Kies in Google Sheets **[!UICONTROL Insert]** > **[!UICONTROL Drawing]** ... in de hoofdmenubalk.

1. Klik in het [!UICONTROL Drawing] -venster op het **[!UICONTROL Text box]** pictogram ![](/help/workfront-fusion/references/apps-and-modules/assets/text-box.png) boven in het venster.
1. Ontwerp een knop en klik op de knop **[!UICONTROL Save and Close]** in de rechterbovenhoek:
1. De knop wordt in uw werkblad geplaatst. Klik op de drie verticale stippen in de rechterbovenhoek van de knop:
1. Kies **[!UICONTROL Assign script..].** in het menu.
1. Voer de naam van het script (functie) in, bijvoorbeeld `runScenario` en klik op **[!UICONTROL OK]** :
1. Kies **[!UICONTROL Tools]** > **[!UICONTROL Script editor]** in de hoofdmenubalk.

1. Voeg de volgende code in:

   * De naam van de functie moet overeenkomen met de naam die u in stap 9 hebt opgegeven.
   * Vervang de URL door de URL van de webhaak die u in stap 2 hebt gekopieerd.

     <pre>function runScenario() {</pre><pre>UrlFetchApp.fetch("&lt;webhaak u hebt gekopieerd&gt;");</pre><pre>}</pre>

1. Druk op **[!UICONTROL Ctrl+S]** om het scriptbestand op te slaan, voer een projectnaam in en klik op **[!UICONTROL OK]** .

1. Ga terug naar [!DNL Google Sheets] en klik op de nieuwe knop.
1. Verleen de vereiste toestemming aan het manuscript:
1. Controleer in [!DNL Workfront Fusion] of het scenario is uitgevoerd.

## Datums opslaan in een spreadsheet

Als u een Date-waarde opslaat in een spreadsheet zonder opmaak, wordt deze waarde in de spreadsheet weergegeven als tekst in de ISO 8601-indeling. In [!DNL Google Sheets] echter worden formules of functies die werken met datums die deze tekst niet begrijpen (bijvoorbeeld: formule `=A1+10` ) de volgende fout weergegeven:

![](/help/workfront-fusion/references/apps-and-modules/assets/mceclip6-350x87.png)

Om [!DNL Google Sheets] toe te staan om de datum te begrijpen, formatteer het met de [[!UICONTROL formatDate] (datum; formaat; [timezone]) ](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md#formatda) functie. De juiste indeling die als het tweede argument aan de functie wordt doorgegeven, is afhankelijk van de landinstellingen van het werkblad.

U kunt als volgt de juiste indeling bepalen:

1. Kies **[!UICONTROL File]** > **[!UICONTROL Spreadsheet]** -instellingen in het hoofdmenu om de landinstelling te controleren of in te stellen.

1. Nadat u de juiste landinstelling hebt gecontroleerd of ingesteld, bepaalt u de corresponderende datum- en tijdnotatie door **[!UICONTROL Format]** > **[!UICONTROL Number]** in het hoofdmenu te kiezen. De notatie wordt weergegeven naast de menuoptie Datum en tijd:

1. Om het correcte formaat samen te stellen dat tot de [!UICONTROL formatDate()] functie zou moeten worden overgegaan, verwijs naar de lijst van [ Tokens voor datum en tijd het formatteren ](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md).

**Voorbeeld:** het gebruik van `MM/DD/YYYY HH:mm:ss` formaat voor de scène van de Verenigde Staten:

![](/help/workfront-fusion/references/apps-and-modules/assets/locale-time-350x83.png)

## [!DNL Google Sheets] -functies gebruiken

Als u een ingebouwde functie mist, maar het wordt voorzien door [!DNL Google Sheets], kunt u het exploiteren. Voor meer informatie, zie  [!DNL Google Sheets]  functies van het Gebruik ](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md#exploiti) in [ punten van de Kaart gebruikend functies in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).[

## [!DNL Google Sheets] niet wijzigen in datums

Een tekenreeks met getallen die u als tekst gebruikt, wordt wellicht geïnterpreteerd als een datum in een [!DNL Google] -werkblad. U typt bijvoorbeeld 1-2019, waarbij u het als tekst wilt gebruiken, maar Google interpreteert het als een datum. U kunt het nummer vooraf opmaken als normale tekst om dit te voorkomen.

1. Markeer in [!DNL Google Sheets] de kolom of cel met het nummer of de nummers.
1. Klik op **[!UICONTROL Format]** > **[!UICONTROL Number]** > **[!UICONTROL Plain text]**.

Een andere oplossing in [!DNL Workfront Fusion] is het typen van een apostrof (&#39;) vóór een getal, bijvoorbeeld &#39;1-2019 of &#39;1/47. De apostrof wordt niet in de cel weergegeven nadat de gegevens vanuit [!DNL Workfront Fusion] zijn verzonden.
