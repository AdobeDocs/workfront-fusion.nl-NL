---
title: Gegevenstypen item
description: Uw Adobe Workfront Fusion-scenario's kunnen de hieronder vermelde objecttypen in een bundel bevatten.
author: Becky
feature: Workfront Fusion
exl-id: 3ad65959-5c19-4727-bc9d-4ff1d238ad8b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Gegevenstypen item

U kunt de hieronder vermelde objecttypen in een bundel opnemen.

Voor informatie over welke types van punten de Fusie van Workfront voor omzetting tussen elkaar toestaat, zie [&#x200B; Druk van het Type &#x200B;](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Tekst</p> </td> 
   <td> <p>Het meest gangbare itemtype. Voor sommige tekstitems controleert Adobe Workfront Fusion of aan de maximum- of minimumlengte is voldaan of de indeling van het item is gevalideerd (e-mail, URL of bestandsnaam).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Getal</p> </td> 
   <td> <p>Voor sommige numerieke items kan Workfront Fusion de invoer voor een opgegeven bereik (de minimaal of maximaal toegestane waarde) valideren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Boolean (Ja/Nee)</p> </td> 
   <td> <p>Dit type wordt gebruikt voor items met slechts twee mogelijke waarden: true of false. </p> <p>Bij het instellen van modules kan het type Boolean in twee verschillende vormen worden weergegeven:</p> 
    <ul> 
     <li> <p>Het verplichte selectievakje wordt weergegeven als het veld verplicht is en moet worden ingevuld.</p> <p> <img src="assets/boolean-checkbox-350x158.jpg" style="width: 350;height: 158;"> </p> </li> 
     <li> <p>Optionele velden die leeg kunnen worden gelaten, worden weergegeven als een selectievak, zodat u ze kunt selecteren op basis van drie waarden: <code>Yes</code>, <code>No</code> en <code>Not defined</code> (standaard).</p> <p> <img src="assets/boolean-convert-file-350x129.jpg" style="width: 350;height: 129;"> </p> </li> 
    </ul> <p>U kunt <strong>[!UICONTROL Map]</strong> klikken als u de waarde aan een punt van een andere module moet in kaart brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Datum</p> </td> 
   <td> <p>Datums worden bijvoorbeeld ingevoerd in de datumnotatie ISO 8601. <code>2015-09-18T11:58Z</code> U kunt de tijdzone wijzigen in de profielinstellingen. </p> <p>Als u op een veld klikt waarvoor een datum is vereist, wordt een pop-upkalender weergegeven in de module-instellingen. Voor sommige items is de tijd niet vereist.</p> <p>Waarden van Date-items worden opgemaakt met de lokale tijdzone en de webtijdzone die in uw profiel zijn geselecteerd. U kunt de ISO 8601-versie van de waarde van een datumitem weergeven door de aanwijzer boven het item te plaatsen.</p> <p>Opmerking: als de ISO-waarde niet wordt weergegeven, is het item waarschijnlijk tekst, niet een datum.</p> <p>De tijd wordt ingegaan in het <code>hours:minutes:seconds</code> formaat, bijvoorbeeld, <code>14:03:52</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Buffer (binaire gegevens)</p> </td> 
   <td> <p>Bestandsinhoud wordt meestal verzonden als inhoud van het type Buffer (afbeeldingsinhoud, videobestand en andere). In sommige gevallen worden tekstgegevens in dit type opgenomen (bijvoorbeeld een tekstbestand). Workfront Fusion kan tekstgegevens in binaire code automatisch omzetten naar tekst en tekst naar tekstgegevens in binaire code. Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/map-data/map-files.md" class="MCXref xref"> dossiers van de Kaart </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Verzameling</p> </td> 
   <td> <p>Een verzameling is een item dat uit meerdere subitems bestaat. Het item Afzender in een e-mailbericht is een voorbeeld van een verzameling: het bevat de naam van de afzender (teksttype) en het e-mailadres van de afzender (teksttype).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Selecteren (menu)</p> </td> 
   <td> <p>Wanneer u de modulemontages vormt, kunt u uit verscheidene punten van het zelfde type selecteren. Een voorbeeld hiervan is het menu dat de map selecteert in de instellingen voor de modules [!DNL Dropbox] . </p> <p>Bij het instellen van modules kan het menu Selecteren in twee formulieren worden weergegeven:</p> <p> <p>Als meerdere selecties mogelijk zijn, worden meerdere items met selectievakjes weergegeven.</p> <p> <img src="assets/image-kb-type-list-multi-350x232.jpg" style="width: 350;height: 232;"> </p> </p> <p>Als er maar één optie mogelijk is, wordt een vervolgkeuzemenu weergegeven.</p> <p> <img src="assets/select-menu-dropdown-350x130.jpg" style="width: 350;height: 130;"> </p> <p>Als u een punt van een andere module moet in kaart brengen, gebruik de <strong> Kaart </strong> knoop. Met deze knop wordt een tekstveld geopend in plaats van het selectiemenu. Voor meer informatie bij afbeelding, zie <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md" class="MCXref xref"> Overzicht van de Afbeelding </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Array</p> </td> 
   <td> <p>U kunt het arraytype gebruiken om met verschillende waarden van hetzelfde type te werken, waaronder verzamelingen. Een voorbeeld hiervan zijn de [!UICONTROL Email] -modules: ze retourneren een array met bijlagen en elke bijlage bevat naam, inhoud, grootte enzovoort. Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/map-data/map-an-array.md" class="MCXref xref"> een serie of serieelement </a> in kaart brengen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Validatie</p> </td> 
   <td> <p>Workfront Fusion kan validatie uitvoeren voor elk type item. Als een item de validatie niet doorgeeft, stopt de module de verwerking vanwege een gegevensfout. Voor meer informatie, zie <a href="/help/workfront-fusion/references/errors/error-processing.md" class="MCXref xref"> types van Fout </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
