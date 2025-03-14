---
title: Microsoft Office 365 Excel-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Microsoft 365 Excel gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 059bc82b-f1bc-4b92-a44b-51c1daf14f08
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2260'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Excel] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Microsoft 365 Excel] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u [!DNL Microsoft office 365 Excel] wilt gebruiken, moet u een Microsoft-account hebben.

## Microsoft Office 365 Excel API-informatie

De Microsoft Office 365 Excel-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v2.0.16</td> 
  </tr>
 </tbody> 
 </table>



## De service [!DNL Office 365 Excel] verbinden met [!DNL Workfront Fusion]

Voor instructies over het aansluiten van uw [!DNL Office 365 Excel] rekening aan [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
>
>Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.

## [!DNL Microsoft Office 365 Excel] modules en hun velden

Wanneer u [!DNL Microsoft 365 Excel] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Microsoft 365 Excel] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Werkboek](#workbook)
* [Werkblad](#worksheet)
* [Tabel](#table)
* [Overige](#other)

### Werkboek

* [Een werkboek downloaden](#download-a-workbook)
* [Werkboeken zoeken](#search-workbooks)
* [Werkboeken controleren](#watch-workbooks)

#### [!UICONTROL Download a Workbook]

Deze actiemodule downloadt de inhoud van het gespecificeerde werkboek van Excel.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a workbook]</td> 
   <td> <p>Selecteer hoe u het werkboek voor de module wilt identificeren om te downloaden.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By entering an ID manually]</strong> </p> <p>Op het [!UICONTROL Workbook ID] gebied, ga of kaart identiteitskaart van het specifieke werkboek in dat u de module wilt downloaden.</p> </li> 
     <li> <p><strong>[!UICONTROL By selecting from the path]</strong> </p> <p>Op het [!UICONTROL Workbook] gebied, selecteer het werkboek dat u de module, met inbegrip van zijn weg wilt downloaden als het niet in de wortelomslag is.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL Search Workbooks]

Deze actiemodule zoekt naar [!DNL Excel] werkboeken.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selecteer de map die u wilt zoeken naar werkboeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>U kunt een filter plaatsen om naar slechts werkboeken te zoeken die aan criteria voldoen u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN of OF regels toe te voegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal aantekenvellen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Watch Workbooks]

Deze trekkermodule begint een scenario wanneer een werkboek wordt gecreeerd.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Selecteer de map die u wilt controleren voor nieuwe werkboeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>U kunt een filter instellen om alleen te controleren op werkboeken die voldoen aan de criteria die u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN of OF regels toe te voegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal werkboeken in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Werkblad

* [[!UICONTROL Add a Worksheet]](#add-a-worksheet)
* [[!UICONTROL Add a Worksheet Row]](#add-a-worksheet-row)
* [[!UICONTROL Delete a Worksheet Row]](#delete-a-worksheet-row)
* [[!UICONTROL List Worksheet Rows]](#list-worksheet-rows)
* [[!UICONTROL List Worksheets]](#list-worksheets)
* [[!UICONTROL Update a Worksheet Row]](#update-a-worksheet-row)
* [[!UICONTROL Watch Worksheet Rows]](#watch-worksheet-rows)

#### [!UICONTROL Add a Worksheet]

Deze actiemodule leidt tot een nieuw aantekenvel binnen het geselecteerde werkboek.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek waar u een aantekenvel, met inbegrip van de weg wilt toevoegen als het werkboek niet in de wortelfolder is.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Name] </td>
   <td> <p>Voer een naam in voor het nieuwe werkblad of wijs een naam toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add a Worksheet Row]

Deze actiemodule voegt een nieuwe rij toe aan het geselecteerde werkblad.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat het aantekenvel bevat waar u een rij, met inbegrip van de weg wilt toevoegen als het werkboek niet in de wortelfolder is.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selecteer het werkblad waaraan u een rij wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Type of values being entered]</p> </td> 
   <td> <p>Selecteer het type waarde dat u in het werkblad wilt invoeren. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formulas]</strong> </p> <p> Excel probeert de opgegeven expressie te evalueren. De namen van functies in een formule zijn in het Engels. Voorbeeld: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formulas local]</strong> </p> <p>Excel probeert de opgegeven expressie te evalueren. De functienamen zijn in de taal van uw toepassing van Excel. Voorbeeld: <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Excel evalueert de waarde niet. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Row]</td>
    <td>Voer voor elke kolom de waarde in die de kolom in de nieuwe rij moet hebben.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Worksheet Row]

Met deze actiemodule verwijdert u een rij uit een werkblad.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat het aantekenvel bevat dat de rij omvat u wilt schrappen.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet]</td>
   <td> <p> Selecteer het werkblad dat de rij bevat die u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Row ID]</td>
   <td>Voer de id in van de rij die u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Worksheet Rows]

Deze actiemodule wint een lijst van rijen in het gespecificeerde aantekenvel terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat het aantekenvel bevat dat de rijen omvat u, met inbegrip van de weg wilt een lijst maken als het werkboek niet in de wortelfolder is.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selecteer het werkblad met de rijen die u wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Ga of kaart het maximumaantal aantekenvelrijen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Worksheets]

Deze actiemodule wint een lijst van aantekenvellen in het gespecificeerde werkboek terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat de aantekenvellen bevat die u de module aan lijst wilt.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Ga of kaart het maximumaantal aantekenvellen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Worksheet Row]

Deze actiemodule werkt een bestaande werkbladrij bij.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat het aantekenvel bevat dat de rij omvat u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selecteer het werkblad dat de rij bevat die u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Type of values being entered]</p> </td> 
   <td> <p>Selecteer het type waarde dat u in het werkblad wilt invoeren. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formulas]</strong> </p> <p> Excel probeert de opgegeven expressie te evalueren. De namen van functies in een formule zijn in het Engels. Voorbeeld: <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formulas local]</strong> </p> <p>Excel probeert de opgegeven expressie te evalueren. De functienamen zijn in de taal van uw toepassing van Excel. Voorbeeld: <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Excel evalueert de waarde niet. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row ID]</td> 
   <td>Selecteer het nummer van de rij dat u wilt bijwerken.</td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Row]</td>
    <td>Voer voor elke kolom de waarde in die de kolom in de nieuwe rij moet hebben.</td>
    </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Worksheet Rows]

Deze triggermodule start een scenario wanneer een nieuwe rij aan het werkblad wordt toegevoegd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat het aantekenvel bevat u op nieuwe rijen wilt letten.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selecteer het Excel-werkblad waarop u nieuwe rijen wilt controleren.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Skip Empty Rows] </td>
   <td> <p>Schakel deze optie in als u geen bundels wilt retourneren voor lege rijen in het werkblad.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Ga of kaart het maximumaantal aantekenvelrijen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Tabel

* [[!UICONTROL Add a table]](#add-a-table)
* [[!UICONTROL Add a table row]](#add-a-table-row)
* [[!UICONTROL Delete a table]](#delete-a-table)
* [[!UICONTROL Get a Table]](#get-a-table)
* [[!UICONTROL List table rows]](#list-table-rows)
* [[!UICONTROL List tables]](#list-tables)
* [[!UICONTROL Update a table]](#update-a-table)
* [[!UICONTROL Watch table rows]](#watch-table-rows)

#### [!UICONTROL Add a table]

Deze actiemodule leidt tot een lijstelement binnen het aantekenvel van Excel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workbook] </td> 
   <td> <p>Selecteer het werkboek dat het aantekenvel bevat waar u een lijst wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Worksheet] </td> 
   <td> <p>Selecteer het werkblad waaraan u een tabel wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Has headers]</td> 
   <td> <p>Schakel deze optie in om de eerste rij als tabelkoppen te definiëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Address]</p> </td> 
   <td> <p>Stel de grootte van de tabel in door de cellen linksboven en rechtsonder aan te geven. Voorbeeld: <code>A1:C10</code> maakt een tabel met 3 kolommen en 10 rijen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add a table row]

Deze actiemodule wijzigt een bestaande tabel.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat de lijst bevat waar u een rij wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selecteer het werkblad dat de tabel bevat waarin u een rij wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Table]</td>
   <td>Selecteer de tabel waaraan u een rij wilt toevoegen.</td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Row]</td>
    <td>Voer voor elke kolom de waarde in die de kolom in de nieuwe rij moet hebben.</td>
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row ID]</p> </td> 
   <td> <p>Als u een rij wilt toevoegen op een specifieke locatie in de tabel, voert u een rijnummer in of wijst u dit toe. De module neemt de nieuwe rij na deze rij op.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a table]

Met deze actiemodule verwijdert u de opgegeven tabel uit een [!DNL Excel] -werkblad.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Delete a table]</td> 
   <td> <p>Selecteer hoe u de tabel wilt identificeren die u wilt verwijderen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Ga of kaart identiteitskaart van het werkboek in dat de lijst bevat u wilt schrappen, dan ingaan of identiteitskaart van het aantekenvel in kaart brengen dat de lijst bevat.</p> <p>Voer in het veld [!UICONTROL Table Name] de naam in van de tabel die u wilt verwijderen of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer het werkboek en het aantekenvel die de lijst bevatten u wilt schrappen, dan de lijst selecteren.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Table]

Deze actiemodule wint meta-gegevens voor de gespecificeerde lijst terug.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> 
     <p >[!UICONTROL Connection]</p>
   </td> 
   <td> 
     <p>Voor instructies over het aansluiten van uw Bureau 365 rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p>
    —&gt; </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a table]</td> 
   <td> <p>Selecteer hoe u de tabel wilt identificeren die u wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Ga of kaart identiteitskaart van het werkboek in dat de lijst bevat u wilt terugwinnen, dan ingaan of identiteitskaart van het aantekenvel in kaart brengen dat de lijst bevat.</p> <p>Voer in het veld [!UICONTROL Table Name] de naam in van de tabel die u wilt ophalen of wijs deze naam toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer het werkboek en het aantekenvel die de lijst bevatten u wilt terugwinnen, dan de lijst selecteren.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List table rows]

Deze onderzoeksmodule wint een lijst van alle lijstrijen in een werkboek terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat de lijst bevat die de rijen omvat u wilt een lijst maken.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selecteer het werkblad dat de tabel bevat met de rijen die u wilt weergeven</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Table] </td>
   <td> <p>Selecteer de tabel die de rijen bevat die u wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Ga of kaart het maximumaantal lijstrijen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List tables]

Deze zoekmodule haalt een lijst met alle tabelobjecten op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Selecteer het werkboek dat de lijsten bevat u wilt een lijst maken.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Selecteer het werkblad dat de tabellen bevat die u wilt weergeven</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Ga of kaart het maximumaantal lijsten in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a table]

Deze actiemodule werkt een bestaande tabel bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update a table]</td> 
   <td> <p>Selecteer hoe u de tabel wilt identificeren die u wilt bijwerken.</p> 
    <ul> 
     <li> <p><strong> ga manueel binnen </strong> </p> <p>Op het [!UICONTROL Workbook ID] gebied, ga of kaart identiteitskaart van het werkboek in dat de lijst bevat u wilt bijwerken.</p> <p>Voer in het veld [!UICONTROL Table Name] de naam in van de tabel die u wilt bijwerken of wijs deze naam toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer het werkboek en het aantekenvel die de lijst bevatten u wilt bijwerken, dan de lijst selecteren.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Als u de naam van de tabel wilt wijzigen, voert u een nieuwe naam voor de tabel in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Headers]</td> 
   <td> <p>Schakel deze optie in om de koppen van de bijgewerkte tabel weer te geven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show totals]</td> 
   <td>Schakel deze optie in om de totale waarden van de tabel weer te geven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style]</td> 
   <td>Kies een stijl voor de nieuwe tabel.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch table rows]

Deze trigger start een scenario wanneer een nieuwe rij aan een tabel wordt toegevoegd.

>[!NOTE]
>
>De tabel verwijst hier naar het ingesloten tabelelement in het werkboek. Niet de volledige tabel (werkboek/werkblad).

![ Ingebedde lijst ](/help/workfront-fusion/references/apps-and-modules/assets/embedded-table-350x420.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Workbook]</p> </td> 
   <td> <p>Selecteer het werkboek dat de lijst bevat u wilt letten op.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p> Selecteer het werkblad dat de tabel bevat die u wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Table]</p> </td> 
   <td> <p>Selecteer de tabel die u wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Ga of kaart het maximumaantal rijen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Retrieve data]](#retrieve-data)

#### [!UICONTROL Make an API Call]

Met deze actiemodule kunt u een aangepaste API-aanroep maken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://graph.microsoft.com</code> . Voorbeeld:<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
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

#### [!UICONTROL Retrieve data]

Deze actie wint gegevens van de bepaalde aantekenvelwaaier terug, en keert een bundel voor elke rij terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Office 365] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workbook] </td> 
   <td> <p>Selecteer het werkboek dat de gegevens bevat u wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Worksheet] </td> 
   <td> <p>Selecteer het werkblad met de gegevens die u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Range] </td> 
   <td> <p>Geef het gebied van het blad op waarvan u de gegevens wilt ophalen door de cellen linksboven en rechtsonder aan te geven. Voorbeeld: <code>A1:D10</code></p> </td> 
  </tr> 
 </tbody> 
</table>
