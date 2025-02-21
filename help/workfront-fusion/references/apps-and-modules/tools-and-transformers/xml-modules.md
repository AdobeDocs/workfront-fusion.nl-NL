---
title: XML
description: Met de XML-toepassing kunt u tekst met XML-opmaak parseren via XML &gt; XML-module parseren en omzetten in een bundel om de gegevens beschikbaar te maken voor andere modules. U kunt een bundel ook omzetten in een tekst met XML-indeling via de XML-&gt; XML-module maken
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: 5351c2386ed6f2d030df1df01fcf9ea0de7d813f
workflow-type: tm+mt
source-wordcount: '1292'
ht-degree: 1%

---

# XML

Met de app [!UICONTROL XML] kunt u tekst met XML-opmaak parseren via de module [!UICONTROL XML] > [!UICONTROL Parse XML] en deze converteren naar een bundel om de gegevens beschikbaar te maken voor andere modules. U kunt een bundel ook omzetten in tekst met XML-indeling via de module [!UICONTROL XML] > [!UICONTROL Create XML]

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
   <p>Geen Workfront Fusion-licentievereiste.</p>
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

## XML maken

De module [!UICONTROL XML] > [!UICONTROL Create XML] zet een bundel om in tekst met XML-indeling.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>De gegevensstructuur beschrijft de structuur van de resulterende XML. Als u een voorbeeld hebt van de XML die u wilt maken, kunt u deze gebruiken om de gegevensstructuur te genereren:</p> 
    <ol> 
     <li value="1">Klik op <strong>[!UICONTROL Add]</strong> .</li> 
     <li value="2">Klik op <strong>[!UICONTROL Generator]</strong> .</li> 
     <li value="3">Kopieer en plak het XML-voorbeeld in het veld Voorbeeldgegevens.</li> 
     <li value="4">Klik op <strong>[!UICONTROL Save]</strong> .</li> 
     <li value="5">Controleer of de gegevensstructuur is gegenereerd.</li> 
     <li value="6">Klik op <strong>[!UICONTROL Save]</strong> om de gegevensstructuur op te slaan.</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Root element name]</td> 
   <td>Voer de naam van het hoofdelement van de XML in. De standaardwaarde is <code>root</code> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype SYSTEM ID]</td> 
   <td>Voer de bestandsnaam in die u wilt gebruiken in de declaratie <code>!DOCTYPE SYSTEM</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype PUBLIC ID]</td> 
   <td>Voer de bestandsnaam in die u wilt gebruiken in de declaratie <code>!DOCTYPE PUBLIC</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strip Xml Declaration]</td> 
   <td>Schakel deze optie in om de declaratie XML <code>&lt;?xml ... ?&gt;</code> en <code>&lt;!DOCTYPE ... &gt;</code> te verwijderen en alleen het hoofdelement XML en de inhoud ervan te behouden.</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Voorbeeld:**

Doorgaans worden gegevens van een [!DNL Google] >spreadsheet getransformeerd naar XML.

1. Plaats de module [!DNL Google Sheets] > [!UICONTROL Select rows] in uw scenario om de gegevens op te halen. Stel de module in om rijen op te halen uit de [!DNL Google] -spreadsheet. Plaats de &#x200B; **[!UICONTROL Maximum number of returned rows]** aan een klein aantal, maar groter dan één voor het testen doeleinden (Voorbeeld, drie). Voer de module [!DNL Google Sheets] uit door er met de rechtermuisknop op te klikken en &quot;**[!UICONTROL Run this module only]**&quot; te kiezen. Controleer de uitvoer van de module.
1. Sluit de module [!UICONTROL Array Aggregator] aan na de module [!DNL Google Sheets] . Kies in de installatie van de module de module [!DNL Google Sheets] in het veld **[!UICONTROL Source node]** . Laat de andere velden op dit moment ongewijzigd.
1. Sluit de module [!UICONTROL XML] > [!UICONTROL Create XML] aan na de module [!UICONTROL Array Aggregator] .

   De opstelling van de module vereist een gegevensstructuur die de structuur van de output van XML beschrijft. Klik op de knop **[!UICONTROL Add]** om de gegevensstructuurinstellingen te openen. De eenvoudigste manier om deze gegevensstructuur te maken, is deze automatisch te genereren op basis van een XML-voorbeeld.

1. Klik op de knop **[!UICONTROL Generator]** en plak het XML-voorbeeld in het veld [!UICONTROL Sample data] :

   ![ het gegevensgebied van de Steekproef ](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)

1. Klik op **[!UICONTROL Save]**.

   Het veld Specificatie in de gegevensstructuur bevat nu de gegenereerde structuur.
1. Wijzig de naam van de gegevensstructuur in een specifiekere naam en klik op **[!UICONTROL Save]** .

   Een veld dat overeenkomt met het kenmerk van de hoofdarray wordt als een toewijzingsveld weergegeven in de instellingen van de JSON-module.
1. Klik op de knop **[!UICONTROL Map]** naast het veld en wijs het `Array[]` -item vanuit de [!UICONTROL Array aggregator] -uitvoer toe:
1. Klik op **[!UICONTROL OK]** om de instellingen van de XML-module te sluiten.
1. Open de instelling van de module [!UICONTROL Array Aggregator] . Wijzig **[!UICONTROL Target structure]** van Aangepast in het veld van een XML-module dat overeenkomt met de bovenliggende items XML element.Map van de module [!DNL Google Sheets] in de juiste velden.
1. Klik op **[!UICONTROL OK]** om de installatie van de Array Aggregator-module te sluiten.
1. Voer het scenario uit.

   De module XML geeft het juiste XML-bestand als uitvoer.

1. Open de instelling van de module [!DNL Google Sheets] en verhoog het getal [!UICONTROL Maximum number of returned rows] om groter te zijn dan het aantal rijen in het werkblad om alle gegevens te verwerken.

   De resulterende XML kan worden opgeslagen in [!DNL Dropbox] , als bijlage worden verzonden via e-mail, via FTP naar een server worden geüpload, enzovoort.

>[!ENDSHADEBOX]

### XML-kenmerken toevoegen

Als u kenmerken wilt toevoegen aan een complex knooppunt (een knooppunt dat andere knooppunten zal bevatten), moet u een verzameling met de naam `_attributes` toevoegen voor de complexe notitie in de aangepaste gegevensstructuur. Deze verzameling wordt toegewezen aan knooppuntkenmerken. Als u kenmerken wilt toevoegen aan een tekstknooppunt (bijvoorbeeld: `<node attr="1">abc</node>`), moet u een verzameling `_attributes` for attributes en een text eigenschap `_value` toevoegen voor de knoopwaarde voor dit knooppunt in de aangepaste gegevensstructuur.

```
{
   "name": "node",
   "type": "collection",
   "spec": [
      {
         "name": "_attributes",
         "type": "collection"
         "spec": [
            {
               "name": "attr1",
               "type": "text"
            }
         ]
      },
      {
         "name": "_value",
         "type": "text"
      }
   ]
}
```

## [!UICONTROL Parse XML]

De module [!UICONTROL XML] > [!UICONTROL Parse XML] parseert een tekst met XML-opmaak en voert een enkele bundel uit die alle informatie bevat die uit de XML is geëxtraheerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>De gegevensstructuur beschrijft de structuur van XML om de output van de module beschikbaar te maken in het toewijzingspaneel voor de volgende modules.</p> <p>Als u een voorbeeld hebt van de XML die u wilt parseren, kunt u deze gebruiken om de gegevensstructuur te genereren:</p> 
    <ol> 
     <li value="1">Klik op <strong>[!UICONTROL Add]</strong> .</li> 
     <li value="2">Klik op <strong>[!UICONTROL Generator]</strong> .</li> 
     <li value="3">Kopieer en plak het XML-voorbeeld in het veld <strong>[!UICONTROL Sample data]</strong> .</li> 
     <li value="4">Klik op <strong>[!UICONTROL Save]</strong>.</li> 
     <li value="5">Controleer of de gegevensstructuur is gegenereerd.</li> 
     <li value="6"> <p>Klik op <strong>[!UICONTROL Save]</strong> om de gegevensstructuur op te slaan.</p> <p>U kunt de stappen 2 tot en met 5 overslaan om een lege gegevensstructuur op te geven. Als de gegevensstructuur leeg is, is de uitvoer van de module niet beschikbaar in het deelvenster Toewijzing totdat de module ten minste één keer is uitgevoerd.</p> </li> 
    </ol> <p>Voor meer informatie, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref"> structuren van Gegevens </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve numbers as text]</td> 
   <td>Schakel deze optie in om ervoor te zorgen dat getallen behouden blijven als tekst (tekenreeks). Anders worden getallen naar getalwaarden gecast.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL XML]</p> </td> 
   <td> <p>Typ of wijs de XML-opgemaakte tekst toe die u wilt parseren.</p> <p>Als u een formule gebruikt, moet u ervoor zorgen dat het gegevenstype van de resultaatwaarde het gegevenstype [!UICONTROL Text] is (of dat dit automatisch kan worden toegepast). </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>Als het resultaatwaardetype [!UICONTROL Buffer] (binaire gegevens) is, gebruikt u de <code>toString()</code> functie om het in het gegevenstype van de Tekst om te zetten. Voor meer informatie, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> de dwang van het Type </a> en <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref"> de gegevenstypes van het Punt </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Voorbeeld:**

Een XML-bestand downloaden van een URL en de inhoud ervan parseren:

1. Maak een nieuw scenario.
1. Voeg de module [!UICONTROL HTTP] > [!UICONTROL Get a file] toe
1. Open de configuratie van de module en vorm het als volgt:

   **URL**: URL van het dossier van XML (b.v. `https://siftrss.com/f/rqLy05ayMBJ`)

   ![ URL van het dossier van XML voorbeeld ](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)

1. Klik **[!UICONTROL OK]** om de configuratie van de module te bewaren en te sluiten.
1. Voeg [!UICONTROL XML] > [!UICONTROL Parse XML] -module toe, sluit deze aan na de module [!UICONTROL HTTP] > [!UICONTROL Get a file] en configureer deze als volgt:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Data structure]</td> 
      <td> 
       <ol> 
        <li value="1">Klik op <strong>[!UICONTROL Add]</strong> .</li> 
        <li value="2">Klik op <strong>[!UICONTROL Generator]</strong> .</li> 
        <li value="3">Open een nieuw tabblad of venster in uw webbrowser.</li> 
        <li value="4">Plaats URL u in de derde stap in de adresbar gebruikte en haal het dossier van XML.</li> 
        <li value="5">Selecteer alle XML-tekst en kopieer deze naar het klembord.</li> 
        <li value="6">Sluit de tab of het venster en ga terug naar het scenario.</li> 
        <li value="7">Plak de gekopieerde XML-tekst in het veld Voorbeeldgegevens.</li> 
        <li value="8">Klik op <strong>[!UICONTROL Save]</strong>.</li> 
        <li value="9">Controleer of de gegevensstructuur is gegenereerd.</li> 
        <li value="10">Klik op <strong>[!UICONTROL Save]</strong> om de gegevensstructuur op te slaan.</li> 
       </ol> <p>U kunt stap 2 tot en met 9 overslaan om een lege gegevensstructuur op te geven. Als de gegevensstructuur leeg is, is de uitvoer van de module niet beschikbaar in het deelvenster Toewijzing totdat de module ten minste één keer is uitgevoerd.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL XML]</td> 
      <td> <p>Wijs het <code>Data </code> punt van de output van de [!UICONTROL HTTP] &gt; [!UICONTROL Get a file] module in het gebied toe. Gebruik de functie <code>toString()</code> om de waarde van het gegevenstype [!UICONTROL Buffer] (binaire gegevens) om te zetten in het gegevenstype [!UICONTROL Text] .</p> <p>U kunt de code van de formule kopiëren en in het gebied kleven: <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>Voor meer informatie zien de de gegevenstypes van de Buffer en van de Tekst, <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref"> gegevenstypes van het Punt </a>.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png"> </p> </td> 
     </tr> 
    </tbody> 
   </table>

>[!ENDSHADEBOX]

### [!UICONTROL Parsing XML attributes]

Standaard plaatst de module [!UICONTROL XML] > [!UICONTROL Parse XML] kenmerken in een speciale verzameling `_attributes` als een onderliggend element van het knooppunt met deze kenmerken. Als het knooppunt een tekstknooppunt is en kenmerken heeft, worden twee speciale eigenschappen toegevoegd: `_attributes` voor kenmerken en `_value` voor de tekstinhoud van het knooppunt.

>[!BEGINSHADEBOX]

**Voorbeeld:** Deze XML:

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

wordt omgezet in deze bundel:

![ XML die in bundel ](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png) wordt omgezet

>[!ENDSHADEBOX]

## Problemen oplossen: kan geen gegevens toewijzen vanuit de module [!UICONTROL Parse XML]

Zorg ervoor dat de gegevensstructuur correct is gedefinieerd. U kunt ook een lege gegevensstructuur gebruiken en de module ten minste één keer uitvoeren om een XML-invoer te verwerken.
