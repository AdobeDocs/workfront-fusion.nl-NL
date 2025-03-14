---
title: Google Slides-modules
description: Met de Adobe Workfront Fusion Google Slides-modules kunt u presentaties maken, bijwerken, weergeven en/of verwijderen en afbeeldingen uploaden naar presentaties in uw Google Slides-account.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 0%

---

# [!DNL Google Slides] modules

Met de modules [!DNL Adobe Workfront Fusion] [!DNL Google Slides] kunt u presentaties maken, bijwerken, weergeven en/of verwijderen en afbeeldingen uploaden naar presentaties in uw [!DNL Google Slides] -account.

Als u [!DNL Google Slides] met [!DNL Workfront Fusion] wilt gebruiken, hebt u een [!DNL Google] -account nodig. Als u nog geen [!DNL Google] -account hebt, kunt u er een maken op de pagina [!DNL Google] Account Help.

U hebt ook [!DNL Google Slides] in uw [!DNL Google Drive] nodig.

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

Als u [!DNL Google Slides] -modules wilt gebruiken, moet u een [!DNL Google] -account hebben.

## Informatie over de Google-API voor dia&#39;s

De aansluiting Google Slides gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://slides.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.5.9</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Slides] modules en hun velden

Wanneer u [!DNL Google Slides] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Google Slides] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [ Presentatie ](#presentation)
* [Overige](#other)

### Presentatie

* [[!UICONTROL Add/Delete a Slide]](#adddelete-a-slide)
* [[!UICONTROL Create a Presentation From a Template]](#create-a-presentation-from-a-template)
* [[!UICONTROL Get a Page/Thumbnail]](#get-a-pagethumbnail)
* [[!UICONTROL Get a Presentation]](#get-a-presentation)
* [[!UICONTROL List Presentations]](#list-presentations)
* [[!UICONTROL Refresh a Chart]](#refresh-a-chart)
* [[!UICONTROL Upload an Image To a Presentation]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Watch Presentations]](#watch-presentations)

#### [!UICONTROL Add/Delete a Slide]

In deze actiemodule wordt een dia gemaakt of wordt een bestaande dia uit de opgegeven presentatie verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the method]</td> 
   <td> <p>Kies of u een nieuwe dia wilt toevoegen of een dia wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Enter a Slide ID]</td> 
   <td> <p>Als u een dia verwijdert, selecteert u of u de dia-id handmatig wilt invoeren of de dia in een lijst wilt selecteren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Selecteer de presentatie of wijs de presentatie-id van de presentatie toe waarvoor u een dia wilt toevoegen of verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Slide Object ID]</td> 
   <td> <p>Als u een dia verwijdert en de dia handmatig wilt invoeren, voert u de dia-id in of wijst u deze toe. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Predefined layout type]</td> 
   <td> <p> Selecteer de vooraf gedefinieerde dialay-out waarvan u de toegevoegde dia wilt gebruiken. Geef waarden op voor aanvullende velden (zoals [!UICONTROL Title] ).</p> 
    <ul> 
     <li>[!UICONTROL Blank layout, with no placeholders]</li> 
     <li>[!UICONTROL Layout with a caption at the bottom]</li> 
     <li>[!UICONTROL Layout with a title and subtitle]</li> 
     <li>[!UICONTROL Layout with a title and body]</li> 
     <li>[!UICONTROL Layout with a title and two columns]</li> 
     <li>[!UICONTROL Layout with only a title]</li> 
     <li>[!UICONTROL Layout with a section title]</li> 
     <li>[!UICONTROL Layout with a title and subtitle on one side and description on the other]</li> 
     <li>[!UICONTROL Layout with one title and one body, arranged in a single column]</li> 
     <li>[!UICONTROL Layout with a main point]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Dit veld is beschikbaar als u een dia wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>Voer de tekstinhoud voor de dia in of wijs deze toe. De velden zijn beschikbaar op basis van de geselecteerde sjabloon.</p> <p>Dit veld is beschikbaar als u een dia wilt toevoegen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Presentation From a Template]

Met deze actiemodule maakt u een nieuwe presentatie door een presentatie te kopiëren en alle tags, zoals `{{Name}}` `{{Email}}` in te vullen met de verschafte gegevens.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Voer een naam in voor de nieuwe presentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy a Presentation]</td> 
   <td> <p> Selecteer de optie als u een bestaande presentatie wilt kopiëren:</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy of Existing Presentation ID]</td> 
   <td> <p> Voer het pad of de presentatie-id in van een bestaande presentatie die u wilt kopiëren. Dit veld wordt weergegeven als u de presentatie maakt [!UICONTROL By Mapping] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selecteer de locatie van de [!DNL Google Drive] presentaties die u wilt weergeven:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Gedeeld station]</li> 
    </ul> <p>Dit veld wordt weergegeven als u de presentatie maakt [!UICONTROL By Dropdown] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecteer de presentatie of voer de presentatie-id in of wijs deze toe aan de presentatie die u als sjabloon wilt gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Voeg de waarden toe:</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: Voer in de presentatie het label in dat u wilt vervangen. Bijvoorbeeld: <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: Voer de waarde in waarmee de bestaande tag moet worden vervangen. Als bijvoorbeeld een tekenreeks <code>&#123;&#123;Name&#125;&#125;</code> in de presentatie en de vervangen waarde Sample is, wordt <code>&#123;&#123;Name&#125;&#125;</code> vervangen door <code>Sample</code> .</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Drive Location]</td> 
   <td> <p>Selecteer de locatie [!DNL Google Drive] waar u de nieuwe presentatie wilt opslaan of toevoegen:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Gedeeld station]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Document's Location]</p> </td> 
   <td> <p>Selecteer de map waarin u de presentatie wilt opslaan of toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>Selecteer deze optie als u de presentatie wilt delen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sharing with Other's Email Address]</td> 
   <td> <p> Voer het e-mailadres in waarmee u de presentatie wilt delen. Als u de optie Gedeeld inschakelt zonder een e-mail in te voeren in dit veld, kan de presentatie door iedereen worden gedeeld.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Page/Thumbnail]

Deze actiemodule krijgt de recentste versie van de gespecificeerde pagina of van de duimnagel van een pagina in de presentatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Presentation and Page ID]</td> 
   <td> <p> Kies of u een presentatie- en pagina-id handmatig wilt invoeren of selecteer deze in een lijst.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecteer de presentatie-id die u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page Object ID]</td> 
   <td> <p> Selecteer de dia waarvoor u de details van het paginaobject wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Page Thumbnail]</td> 
   <td> <p> Schakel het selectievakje in als u de paginaminiatuurgegevens wilt weergeven.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Presentation]

Deze actiemodule krijgt de recentste versie van een gespecificeerde presentatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selecteer de locatie van de [!DNL Google Drive] presentaties die u wilt weergeven:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Gedeeld station]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecteer de presentatie die u wilt ophalen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Presentations]

Deze module wint een lijst van alle presentaties in de bepaalde plaats terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive location]</td> 
   <td> <p>Selecteer de locatie van de [!DNL Google Drive] presentaties die u wilt weergeven:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Gedeeld station]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p>Kies de maplocatie van de presentaties die u wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal presentaties in dat u de module tijdens één cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Refresh a Chart]

De actiemodule THis vernieuwt de diagramgegevens die zijn opgeslagen in een presentatie die is opgegeven met de id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Presentation ID]</td> 
   <td> <p> Kies of u een presentatie-id handmatig wilt invoeren of selecteer deze in een lijst.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Als u de presentatie in een lijst selecteert, selecteert u de [!DNL Google Drive] locatie waar de presentaties die u wilt weergeven zich bevinden:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Gedeeld station]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Selecteer de presentatie of voer de presentatie-id in of wijs deze toe aan de presentatie met het diagram dat u wilt vernieuwen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chart Object ID]</td> 
   <td> <p> Als u handmatig gegevens invoert, voert u de id in van het diagram dat u wilt vernieuwen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an Image To a Presentation]

Uploadt een afbeelding met de verschafte gegevens.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Kies hoe u de presentatie wilt selecteren waarnaar u een afbeelding uploadt.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Als u een keuze maakt in een vervolgkeuzelijst, selecteert u de [!DNL Google Drive] locatie waar de presentatie waaraan u een afbeelding wilt toevoegen zich bevindt:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Gedeeld station]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Selecteer de presentatie-id van de presentatie waarnaar u een afbeelding uploadt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the Method]</td> 
   <td> <p> Selecteer hoe u de afbeelding wilt vervangen.</p>
   <ul>
   <li><p><b>Een afbeelding uploaden door tekstcode te vervangen</b></p><p>Op het gebied van Waarden, voor elk beeld wilt u uploaden, <b> toevoegen punt </b> en ga de markering van het beeld en URL van het nieuwe beeld in.</p></li>
   <li><p><b>Upload een afbeelding door deze te vervangen</b></p><p>Op het gebied van Waarden, voor elk beeld wilt u uploaden, <b> toevoegen punt </b> en ingaan het objecten identiteitskaart van het beeld, vervangen methode, en URL van het nieuwe beeld.</p></li>
   </ul>
  <p>Opmerking: de afbeeldingen moeten kleiner zijn dan 50 MB, mogen niet groter zijn dan 25 megapixels en moeten de PNG-, JPEG- of GIF-indeling hebben.</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Presentations]

Deze triggermodule start een scenario wanneer een nieuwe presentatie wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch] </td> 
   <td> <p>Selecteer de optie om de presentaties te bekijken:</p> 
    <ul> 
     <li> <p>[!UICONTROL Created Date]</p> </li> 
     <li> <p>[!UICONTROL Modified Date]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Typ of wijs het maximumaantal presentaties toe dat Workfront Fusion tijdens de uitvoeringscyclus van één scenario moet retourneren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Overige

* [[!UICONTROL Insert Links in a Presentation]](#insert-links-in-a-presentation)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Insert Links in a Presentation]

In deze module worden alle koppelingen in een presentatie aanklikbaar gemaakt of wordt een koppeling ingevoegd in alle overeenkomende invoerteksten.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Kies hoe u de presentatie wilt selecteren waarnaar u een afbeelding uploadt.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Selecteer de locatie van de [!DNL Google Drive] presentaties die u wilt weergeven:</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Gedeeld station]</li> 
    </ul> <p>Dit veld wordt weergegeven als u de presentatie maakt [!UICONTROL By Dropdown] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Kies de maplocatie van de presentaties die u wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select]</td> 
   <td> <p>Selecteer of u alle koppelingen in een presentatie klikbaar wilt maken of dat u een koppeling wilt invoegen in alle overeenkomende invoerteksten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text Inputs]</td> 
   <td>Als u een verbinding, voor elk tekstpunt opneemt dat u een verbinding voor wilt toevoegen, <b> toevoegen punt </b> en gaat de tekst en zijn bijbehorende verbinding in. Telkens wanneer het item in de presentatie wordt weergegeven, wordt het automatisch gekoppeld aan de opgegeven site.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Voert een willekeurige geautoriseerde API-aanroep uit.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Google Slides] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van <code>https://developers.google.com/slides/</code> . Bijvoorbeeld presentatie.</p> <p>Raadpleeg de <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides] API-documentatie </a> voor de lijst met beschikbare eindpunten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voer de gewenste aanvraagheaders in. U hoeft geen machtigingsheaders toe te voegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Voer de queryreeks voor de aanvraag in.</p> </td> 
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

>[!BEGINSHADEBOX]

**Voorbeeld:** Gebruikend een API vraag kunt u de presentatiedetails voor presentatieidentiteitskaart krijgen u bent ingegaan. U kunt de presentatie-id in de URL vinden wanneer u de presentatie opent in [!DNL Google Slides] .

![ API vraagvoorbeeld ](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

De volgende API-aanroep retourneert de presentatiedetails:

![ de details van de Presentatie ](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

Overeenkomsten met de zoekopdracht vindt u in de sectie Uitvoer van de module onder [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL presentationId] .

In ons voorbeeld zijn de gevraagde presentatiegegevens geretourneerd:

![ Presentatiedetails ](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
