---
title: GitHub-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die GitHub gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# [!DNL GitHub] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!UICONTROL GitHub] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Als u [!DNL GitHub] modules wilt gebruiken, hebt u een [!DNL GitHub] account nodig.

## Verbinden [!DNL GitHub] met [!DNL Workfront Fusion]

Voor instructies over het aansluiten van uw [!DNL GitHub] rekening aan [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen [!UICONTROL Adobe Workfront Fusion] - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL GitHub] -modules en de bijbehorende velden.

Wanneer u [!DNL GitHub] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL GitHub] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)

### Triggers

* [[!UICONTROL Watch Issues]](#watch-issues)
* [[!UICONTROL Watch Repositories]](#watch-repositories)
* [[!UICONTROL Watch Forks]](#watch-forks)
* [[!UICONTROL Watch Comments]](#watch-comments)
* [[!UICONTROL Watch Pull Requests]](#watch-pull-requests)

#### [!UICONTROL Watch Issues]

Deze module activeert wanneer een nieuwe uitgave wordt toegevoegd of een bestaande kwestie wordt gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to watch]</td> 
   <td>Selecteer of u alle opslagruimten wilt bekijken, of slechts één opslagplaats.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Als u ervoor hebt gekozen om problemen in slechts één opslagplaats te bekijken, selecteert u de opslagplaats die u wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt. </td> 
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
   <td>Voeg een tag toe. De module controleert op problemen met deze tag.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Repositories]

Deze module activeert wanneer een opslagplaats wordt gemaakt of gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned repositories]</td> 
   <td>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Selecteer of u wilt controleren op nieuwe opslagruimten en alle wijzigingen, of alleen op nieuwe opslagruimten.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Forks]

Deze module activeert wanneer een nieuwe vork wordt gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die u voor vorken wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned forks]</td> 
   <td>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comments]

Deze module activeert wanneer een nieuwe opmerking wordt toegevoegd of een bestaande opmerking wordt gewijzigd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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
   <td>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Selecteer of u alleen wilt letten op nieuwe opmerkingen of op opmerkingen en alle wijzigingen.</td> 
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
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Selecteer de opslagplaats die u wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned pull requests]</td> 
   <td>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt. </td> 
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

### Handelingen

* [[!UICONTROL Search for an issue]](#search-for-an-issue)
* [[!UICONTROL Create an issue]](#create-an-issue)
* [[!UICONTROL Update an issue]](#update-an-issue)
* [[!UICONTROL Get an issue]](#get-an-issue)
* [[!UICONTROL Add assignees]](#add-assignees)
* [[!UICONTROL Remove assignees]](#remove-assignees)
* [[!UICONTROL Add labels to an issue]](#add-labels-to-an-issue)
* [[!UICONTROL Remove a label from an issue]](#remove-a-label-from-an-issue)
* [[!UICONTROL Create a comment]](#create-a-comment)
* [[!UICONTROL List comments]](#list-comments)

#### [!UICONTROL Search for an issue]

Deze module zoekt naar problemen die voldoen aan uw zoekcriteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt (het aantal herhalingen per uitgevoerde scenario). </td> 
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

#### [!UICONTROL Create an issue]

Deze module maakt een nieuwe uitgave in de geselecteerde repository.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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

#### [!UICONTROL Update an issue]

Deze module werkt een bestaand [!DNL GitHub] -probleem bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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
   <td>Voer een titel voor de uitgave in of wijs deze toe.</td> 
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
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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

#### [!UICONTROL Add assignees]

Deze module voegt toewijzingen toe aan de opgegeven uitgave

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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

#### [!UICONTROL Remove assignees]

Deze module verwijdert toewijzingen uit de opgegeven uitgave.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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

#### [!UICONTROL Add labels to an issue]

Deze module voegt labels toe aan een uitgave. Labels worden gedefinieerd op het niveau van de gegevensopslagruimte en kunnen alleen worden gemaakt door iemand met schrijftoegang tot de gegevensopslagruimte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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

#### [!UICONTROL Remove a label from an issue]

Deze module verwijdert één label uit een uitgave.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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

#### [!UICONTROL Create a comment]

In deze module wordt een opmerking over het opgegeven probleem gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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

#### [!UICONTROL List comments]

In deze module worden alle opmerkingen over het opgegeven probleem weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL GitHub] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
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
   <td>De module retourneert opmerkingen die na deze datum zijn gemaakt. Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td>Stel het maximale aantal resultaten in waarmee [!DNL Workfront Fusion] gedurende één cyclus werkt. </td> 
  </tr> 
 </tbody> 
</table>

<!--
<h2>Troubleshooting</h2>
-->

<!--
<h3>Module does not receive any events</h3>
-->

<!--
<p>If a module does not receive any events, check the webhook settings in Github and make sure that:</p>
-->

<!--
  <p>You have set the correct type of event that the chosen module should receive</p>
  -->

<!--
  <p>You have entered the correct Payload URL</p>
  -->
