---
title: GitHub-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die GitHub gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 0%

---

# [!DNL GitHub] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!UICONTROL GitHub] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Als u [!DNL GitHub] modules wilt gebruiken, hebt u een [!DNL GitHub] account nodig.

## Verbinden [!DNL GitHub] met Workfront Fusion

Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan [!UICONTROL Workfront Fusion], zie [&#x200B; een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies &#x200B;](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL GitHub] -modules en de bijbehorende velden.

Wanneer u [!DNL GitHub] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL GitHub] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

* [[!UICONTROL Watch Comments]](#watch-comments)
* [[!UICONTROL Watch Forks]](#watch-forks)
* [[!UICONTROL Watch Issues]](#watch-issues)
* [[!UICONTROL Watch Pull Requests]](#watch-pull-requests)
* [[!UICONTROL Watch Repositories]](#watch-repositories)

#### [!UICONTROL Watch Comments]

Deze triggermodule start een scenario wanneer een nieuwe opmerking wordt toegevoegd of een bestaande opmerking wordt gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die u wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue number]</td> 
   <td>Als u de zoekopdracht wilt beperken door alleen te zoeken naar nieuwe opmerkingen over een bepaald onderwerp, voert u het nummer van de uitgave in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td> <p> Stel het maximumaantal opmerkingen in dat Workfront Fusion tijdens één cyclus retourneert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Selecteer of u alleen wilt letten op nieuwe opmerkingen of op opmerkingen en alle wijzigingen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Forks]

Deze triggermodule start een scenario wanneer een nieuwe vork wordt gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die u voor vorken wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned forks]</td> 
    <td>Ga of kaart het maximumaantal vorken in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Issues]

Deze triggermodule start een scenario wanneer een nieuwe uitgave wordt toegevoegd of een bestaande uitgave wordt gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to watch]</td> 
   <td>Selecteer of u alle aan dit account gekoppelde opslagplaatsen wilt bekijken, of slechts één opslagplaats.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Als u ervoor hebt gekozen om problemen in slechts één opslagplaats te bekijken, selecteert u de opslagplaats die u wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td> <p> Stel het maximumaantal problemen in dat Workfront Fusion tijdens één cyclus retourneert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Selecteer of u alleen wilt letten op nieuwe uitgaven of op nieuwe uitgaven en alle wijzigingen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>U kunt de kwesties filtreren u wilt letten op door hoe u met hen wordt geassocieerd.</p> 
    <ul> 
     <li>[!UICONTROL All issues]</li> 
     <li>[!UICONTROL Only issues assigned to me]</li> 
     <li>[!UICONTROL Only issues created by me]</li> 
     <li>[!UICONTROL Only issues mentioning me]</li> 
     <li>[!UICONTROL Only issues I'm subscribed to updates for]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Selecteer of u alleen openstaande kwesties wilt bekijken of alleen gesloten kwesties. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Voor elke markering die u wilt toevoegen, <b> toevoegen punt </b> klikken en de markering ingaan. De module zoekt naar problemen met deze tags.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Pull Requests]

Deze module activeert wanneer een nieuwe pull-aanvraag wordt toegevoegd of een bestaande pull-aanvraag wordt gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die u wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned pull requests]</td> 
   <td> <p> Stel het maximumaantal pull-aanvragen in dat Workfront Fusion gedurende één cyclus retourneert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Selecteer of u [!UICONTROL only open pull] aanvragen, [!UICONTROL only closed ones] of alle pull-aanvragen wilt bekijken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Selecteer of u alleen nieuwe pull-aanvragen of nieuwe pull-aanvragen en alle wijzigingen wilt controleren.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Repositories]

Deze triggermodule start een scenario wanneer een opslagplaats wordt gemaakt of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned repositories]</td> 
   <td> <p> Stel het maximumaantal opslagruimten in dat Workfront Fusion gedurende één cyclus retourneert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Selecteer of u wilt controleren op nieuwe opslagruimten en alle wijzigingen, of alleen op nieuwe opslagruimten.</td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Add assignees]](#add-assignees)
* [[!UICONTROL Add labels to an issue]](#add-labels-to-an-issue)
* [[!UICONTROL Create a comment]](#create-a-comment)
* [[!UICONTROL Create an issue]](#create-an-issue)
* [[!UICONTROL Get an issue]](#get-an-issue)
* [[!UICONTROL List comments]](#list-comments)
* [[!UICONTROL Remove a label from an issue]](#remove-a-label-from-an-issue)
* [[!UICONTROL Remove assignees]](#remove-assignees)
* [[!UICONTROL Search for an issue]](#search-for-an-issue)
* [[!UICONTROL Update an issue]](#update-an-issue)

#### [!UICONTROL Add assignees]

Deze module voegt toewijzingen toe aan de opgegeven uitgave

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die de uitgave bevat waaraan u toewijzingen wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Selecteer de personen die u aan het probleem wilt toewijzen. Tot de beschikbare toewijzingen behoren ook personen met schrijfmachtigingen voor de gegevensopslagruimte en leden van de organisatie met leesmachtigingen voor de gegevensopslagruimte. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in van de uitgave waaraan u toewijzingen wilt toevoegen of wijs dit nummer toe. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add labels to an issue]

Deze module voegt labels toe aan een uitgave. Labels worden gedefinieerd op het niveau van de gegevensopslagruimte en kunnen alleen worden gemaakt door iemand met schrijftoegang tot de gegevensopslagruimte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die de uitgave bevat waaraan u labels wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Selecteer de labels die u aan de uitgave wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in van de uitgave waaraan u labels wilt toevoegen of wijs dit nummer toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a comment]

In deze module wordt een opmerking over het opgegeven probleem gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die de uitgave bevat waarop u een opmerking wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in of wijs het nummer toe van de uitgave waarop u een opmerking wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Voer de inhoud van de opmerking in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an issue]

Deze module maakt een nieuwe uitgave in de geselecteerde repository.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats waarin u een uitgave wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Selecteer de personen die u aan het probleem wilt toewijzen. Tot de beschikbare toewijzingen behoren iedereen met schrijfmachtigingen voor de gegevensopslagruimte en leden van de organisatie met leesmachtigingen voor de gegevensopslagruimte. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Selecteer de mijlpaal die u aan de nieuwe kwestie wilt associëren. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Selecteer de labels die u op de nieuwe uitgave wilt toepassen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Voer een titel in of wijs een titel toe voor de nieuwe uitgave.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Typ of wijs de hoofdtekst van de uitgave aan, zoals een beschrijving of aanvullende informatie</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an issue]

Deze module wint details over de gespecificeerde kwestie terug

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die de kwestie bevat waarover u details wilt terugwinnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in of wijs het nummer toe van de uitgave waarover u details wilt ophalen. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List comments]

In deze module worden alle opmerkingen over het opgegeven probleem weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die de uitgave bevat waaruit u opmerkingen wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in of wijs het nummer toe van de uitgave waaruit u opmerkingen wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>De module retourneert opmerkingen die na deze datum zijn gemaakt. Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> Stel het maximumaantal opmerkingen in dat Workfront Fusion tijdens één cyclus retourneert.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a label from an issue]

Deze module verwijdert één label uit een uitgave.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die de uitgave bevat waaruit u een label wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Selecteer het label dat u uit de uitgave wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in of wijs het nummer toe van de uitgave waaruit u een label wilt verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assignees]

Deze module verwijdert toewijzingen uit de opgegeven uitgave.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die de uitgave bevat waaruit u toewijzingen wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Selecteer de personen die u uit het probleem wilt verwijderen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in of wijs het nummer toe van de uitgave waaruit u toewijzingen wilt verwijderen. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for an issue]

Deze module zoekt naar problemen die voldoen aan uw zoekcriteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td> <p> Stel het maximumaantal problemen in dat Workfront Fusion tijdens één cyclus retourneert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Selecteer hoe u de resultaten van de zoekopdracht wilt sorteren.</p> 
    <ul> 
     <li> <p>[!UICONTROL Best match] </p> </li> 
     <li>[!UICONTROL Date created]</li> 
     <li>[!UICONTROL Date updated]</li> 
     <li>[!UICONTROL Number of comments]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort direction]</td> 
   <td> <p>Selecteer oplopend of aflopend. </p> <p>Als u voor datums selecteert, retourneert u eerst de meest recente datum. <strong>[!UICONTROL descending]</strong> </p> <p>Als u [!UICONTROL number of comments] selecteert, retourneert <strong>[!UICONTROL descending]</strong> het probleem met het hoogste aantal opmerkingen eerst.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Voer de zoekquery in of wijs deze toe. Voor een gedetailleerde beschrijving van onderzoeksopties, zie <a href="https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests"> zoekend kwesties en trekkingsverzoeken </a> op de [!DNL GitHub] hulpplaats.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an issue]

Deze module werkt een bestaand [!DNL GitHub] -probleem bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats waarin u een uitgave wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Selecteer de personen die u aan het probleem wilt toewijzen. Tot de beschikbare toewijzingen behoren ook personen met schrijfmachtigingen voor de gegevensopslagruimte en leden van de organisatie met leesmachtigingen voor de gegevensopslagruimte. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Selecteer de mijlpaal die u aan de kwestie wilt associëren. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Selecteer de labels die u op de uitgave wilt toepassen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Voer het nummer in of wijs het nummer toe van de uitgave die u wilt bijwerken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Selecteer de status waarnaar u de uitgave wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Voer een nieuwe titel voor de uitgave in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Voer een nieuwe hoofdtekst voor de uitgave in of wijs deze toe, zoals een beschrijving of aanvullende informatie</td> 
  </tr> 
 </tbody> 
</table>
