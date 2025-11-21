---
title: Adobe-onderdelenmodules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Adobe Substance] gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.
author: Becky
feature: Workfront Fusion
source-git-commit: 2e44c89d487100b3245b40f6927185a0ff12ef2f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Adobe Substance] Modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Adobe Substance] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Als u instructies bij het creëren van een scenario nodig hebt, zie de artikelen onder [ een scenario creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Voordat u de [!DNL Adobe Substance] -connector kunt gebruiken, moet u controleren of aan de volgende voorwaarden is voldaan:

* U moet een actieve [!DNL Adobe Substance] account hebben.



## [!DNL Adobe Substance] modules en hun velden

Wanneer u [!DNL Adobe Substance] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Substance] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een sterretje naast de veldnaam in een module geeft een verplicht veld aan.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Samenstellingen](#composites)
* [Scènes](#scenes)
* [Spaties](#spaces)

### Samenstellingen

#### 3D-objectsamenstelling genereren

Deze actiemodule genereert inhoud voor een 3D-samenstelling die het geselecteerde hoofdelement bevat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Adobe Substance] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overige velden</td> 
   <td>Configureer desgewenst andere velden. Voor details van gebieden, zie de <a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose"> Substance API documentatie van Adobe </a>.</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### Scènes

* [3D-bestanden converteren](#convert-3d-files)
* [3D-scène maken](#create-3d-scene)
* [3D-scène beschrijven](#describe-3d-scene)
* [3D-object renderen](#render-3d-object)
* [3D-object renderen (basisversie)](#render-3d-object-basic-version)

#### 3D-bestanden converteren

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Adobe Substance] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Indeling</td> 
   <td>Selecteer de indeling waarnaar u het bestand converteert.</td> 
  </tr> 
<tr> 
   <td role="rowheader">Invoerpunt model</td> 
   <td>Voor conversie wordt meestal het eerste bestand gebruikt dat als een geldig 3D-model wordt beschouwd. Definieer dit ingangspunt voor doorverwijzen wanneer er meerdere opties zijn.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bronnen</td> 
   <td>Voor elk bestand dat u wilt converteren, klikt u op <b> Item toevoegen </b> en voert u de bestandsinformatie in.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-scène maken

In deze actiemodule wordt een scène gemaakt met de elementen die u opgeeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Adobe Substance] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
   <td role="rowheader">Codering</td> 
   <td>Selecteer het bestandstype voor de scène.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Basisnaam bestand</td> 
   <td>Voer een naam voor het uitvoerbestand in of wijs een naam toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overige velden</td> 
   <td>Configureer desgewenst andere velden. Voor details van gebieden, zie de <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble"> Substance API documentatie van Adobe </a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Bronnen</td> 
   <td>Voor elk bestand dat u wilt gebruiken, klikt u op <b> Item toevoegen </b> en voert u de bestandsinformatie in.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-scène beschrijven

Deze actiemodule haalt informatie op over inhoud van een 3D-scène.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Adobe Substance] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
   <td role="rowheader">Scènebestand</td> 
   <td>Voer het pad in of wijs het toe aan het scènebestand dat u wilt beschrijven.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Bronnen</td> 
   <td>Voor elk dossier dat u wilt beschrijven, <b> voeg punt </b> toe en ga de dossierinformatie in.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-object renderen

In deze actiemodule wordt een afbeelding van een scène weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Adobe Substance] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td role="rowheader">Overige velden</td> 
   <td>Configureer desgewenst andere velden. Voor details van gebieden, zie de <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render"> Substance API documentatie van Adobe </a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Bronnen</td> 
   <td>Voor elk bestand dat u wilt gebruiken, klikt u op <b> Item toevoegen </b> en voert u de bestandsinformatie in.</td> 
  </tr> 
 </tbody> 
</table>

#### 3D-object renderen (basisversie)

Deze actiemodule rendert een afbeelding van een scène, maar heeft minder opties dan de module 3D-object renderen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Adobe Substance] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
   <td role="rowheader">Overige velden</td> 
   <td>Configureer desgewenst andere velden. Voor details van gebieden, zie de <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render-basic"> Substance API documentatie van Adobe </a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Bronnen</td> 
   <td>Voor elk bestand dat u wilt gebruiken, klikt u op <b> Item toevoegen </b> en voert u de bestandsinformatie in.</td> 
  </tr> 
 </tbody> 
</table>

### Spaties

#### Ruimte maken

Met deze actiemodule kunt u bestanden uploaden en tijdelijk opslaan.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Adobe Substance] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
   <td role="rowheader">Bestandsnaam</td> 
   <td>Voer de naam in of wijs de naam toe van het bestand dat wordt geüpload.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Bestandsgegevens</td> 
   <td>Voer de binaire gegevens van het bestand in of wijs deze toe.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Naam</td> 
   <td>Voer een naam in of wijs een naam toe aan de formulierwaarde met meerdere onderdelen.</td> 
  </tr> 
 </tbody> 
</table>
