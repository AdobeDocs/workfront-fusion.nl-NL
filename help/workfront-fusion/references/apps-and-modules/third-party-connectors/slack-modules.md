---
title: Slack-modules
description: In een [!DNL Adobe Workfront Fusion] scenario kunt u workflows automatiseren die gebruikmaken van Slack en deze verbinden met meerdere applicaties en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: eb0518ba0d1a0c758cb547e362c722f4be3674c7
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 0%

---

# [!DNL Slack] Modules

In een [!DNL Adobe Workfront Fusion] scenario kunt u werkstromen automatiseren die gebruikmaken van [!DNL Slack], en deze verbinden met meerdere toepassingen en services van derden.

Zie de artikelen onder [Scenario&#39;s maken: artikelindex](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md) voor instructies over het maken van een scenario.

Voor informatie over modules, zie de artikelen onder [Modules: artikelindex](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Uitvouwen om de toegangsvereisten voor de functionaliteit in dit artikel weer te geven.

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
   <p>Huidig: Geen Workfront Fusion-licentievereiste</p>
   <p>Of</p>
   <p>Legacy: Workfront Fusion voor werkautomatisering en -integratie </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Selecteer of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultiem Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>Of</p>
   <p>Current: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Zie [Toegangsvereisten in documentatie](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md) voor meer informatie over de informatie in deze tabel.

Zie licenties voor[&#128279;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md) informatie over [!DNL Adobe Workfront Fusion] licenties[!DNL Adobe Workfront Fusion] .

+++

## Vereisten

Als u [!DNL Slack] -modules wilt gebruiken, moet u een [!DNL Slack] -account hebben.

## Slack API-informatie

De Slack-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>&lbrace;{fempty(parameters.domain, 'https://slack.com/api/')}</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack] modules en hun vakgebieden

Wanneer u modules configureert [!DNL Slack] , [!DNL Workfront Fusion] worden de onderstaande velden weergegeven. Daarnaast kunnen extra [!DNL Slack] velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een vetgedrukte titel in een module geeft een verplicht veld aan.

Als u de kaartknop boven een veld of functie ziet, kunt u deze gebruiken om variabelen en functies voor dat veld in te stellen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Berichten](#messages)
* [Gesprek](#channels)
* [Overige](#other)

### Berichten

* [Een bericht maken](#create-a-message)
* [Een bericht verwijderen](#delete-a-message)
* [Ontvang een privékanaalbericht](#get-a-private-channel-message)
* [Een bericht op een openbaar kanaal ophalen](#get-a-public-channel-message)
* [Een bericht bijwerken](#update-a-message)
* [Privékanaalberichten bekijken](#watch-private-channel-messages)
* [Openbare kanaalberichten bekijken](#watch-public-channel-messages)

### [!UICONTROL Create a Message]

Deze actiemodule maakt een nieuw bericht aan.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Een verbinding maken met [!DNL Adobe Workfront Fusion] - Basisinstructies</a> voor instructies over het koppelen van uw [!DNL Slack] account aan[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Kies hoe je het kanaal wilt selecteren waar je een bericht wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het <strong>[!UICONTROL Channel ID or name]</strong> veld de kanaal-ID of de naam in van het kanaal waar je het bericht wilt plaatsen.</p> <p>Opmerking: de kanaal-id kan worden opgehaald met de module [!UICONTROL List Channels] .</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer het type kanaal en selecteer vervolgens het kanaal.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Voer de tekstinhoud in van het bericht dat u wilt maken.</p> <p>Opmerking: Zie <a href="https://api.slack.com/reference/surfaces/formatting">Tekst opmaken voor app-weergaven</a> in de [!DNL Slack] documentatie voor gedetailleerde informatie over tekstopmaak.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As user]</td> 
   <td>Schakel deze optie in om het bericht te posten als de gebruiker die eigenaar is van de referenties die door de verbinding voor deze module worden gebruikt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread message ID (time stamp)]</td> 
   <td>Als het nieuwe bericht een antwoord is, voert u het tijdstempel in van het bericht dat u wilt beantwoorden. Voer niet het tijdstempel in van een bericht dat al een antwoord is.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply broadcast]</td> 
   <td> <p>Selecteer <strong>[!UICONTROL Yes]</strong> of beide van de volgende situaties van toepassing zijn:</p> 
    <ul> 
     <li> <p>Het nieuwe bericht is een antwoord op een ander bericht</p> </li> 
     <li> <p>Je wilt dat het nieuwe bericht zichtbaar is voor iedereen in het kanaal</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachments]</td> 
   <td>Klik voor elk item dat u aan het bericht wilt toevoegen op <b>Item</b> toevoegen en vul de gegevens van het item in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon emoji]</td> 
   <td>Voer de emoji in of wijs deze toe die u wilt gebruiken als het pictogram voor dit bericht, in de indeling <code>:icon-name:</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon URL]</td> 
   <td>Voer de URL van de afbeelding in of wijs deze toe die u als pictogram voor dit bericht wilt gebruiken. </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link names]</p> </td> 
   <td> <p>Schakel deze optie in om namen en kanalen toe te staan te gebruiken <code>@username</code> of <code>#channel</code> op te maken. </p> <p>Zie <a href="https://api.slack.com/docs/formatting">Tekst opmaken voor app-oppervlakken</a> in de [!DNL Slack] documentatie voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse message text]</p> </td> 
   <td> <p>Schakel deze optie in als u automatisch parseren wilt toestaan. </p> <p>Voor meer informatie, zie <a href="https://api.slack.com/docs/formatting"> Formatterende tekst voor toepassingsoppervlakten </a> in de [!DNL Slack] documentatie.</p> <p>Opmerking: als u [!UICONTROL Link names] - of [!UICONTROL Parse message text] -opties hebt gebruikt in het oorspronkelijke bericht, moet u deze ook opgeven wanneer u de module [!UICONTROL Update a Message] uitvoert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use markdown]</p> </td> 
   <td> <p>Schakel deze optie in om het gebruik van markdown in de tekst toe te staan [!DNL Slack] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Unfurl primarily text-based content]</p> </td> 
   <td> <p>Schakel deze optie in om het ontvouwen van voornamelijk op tekst gebaseerde inhoud mogelijk te maken. </p> <p>Zie Koppelingen in berichten</a> in de documentatie voor meer informatie over ontvouwen[!DNL Slack][!DNL Slack].<a href="https://api.slack.com/reference/messaging/link-unfurling"></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Unfurl media content]</p> </td> 
   <td> <p>Schakel deze optie in om het ontvouwen van media-inhoud mogelijk te maken. </p> <p>Voor meer informatie over het ontrafelen in [!DNL Slack], zie <a href="https://api.slack.com/reference/messaging/link-unfurling"> het Onthullen van verbindingen in berichten </a> in de [!DNL Slack] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User name]</td> 
   <td>Geef de gebruikersnaam op die is gebruikt om het bericht te posten. Als er geen gebruikersnaam is opgegeven, wordt de naam "Bot" gebruikt.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Delete a Message]

Met deze actiemodule wordt een opgegeven bericht verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Een verbinding maken met [!DNL Adobe Workfront Fusion] - Basisinstructies</a> voor instructies over het koppelen van uw [!DNL Slack] account aan[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Voer de kanaalid in of wijs deze toe.</p> <p>Opmerking: de kanaal-id kan worden opgehaald met de module [!UICONTROL List Channels] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Voer de tijdstempel in of wijs deze toe van het bericht dat u wilt verwijderen.</p> <p>Nota: De tijdstempel kan worden teruggewonnen gebruikend een andere module, zoals de Module van de Berichten van het Kanaal van het Controle Privé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As user]</td> 
   <td> <p> Schakel deze optie in om het bericht te verwijderen als de gebruiker met de referenties die in de verbinding worden gebruikt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Private Channel Message]

Deze actiemodule wint de details van een bericht van een geselecteerd kanaal terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Slack] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Voer de kanaalid in (kaart).</p> <p>Opmerking: De kanaal-ID kan worden opgehaald met behulp van de [!UICONTROL List Channels] module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Time stamp)]</p> </td> 
   <td> <p> Voer de tijdstempel van het bericht in of wijs deze toe van het bericht waarover u informatie wilt ophalen.</p> <p>Opmerking: De tijdstempel kan worden opgehaald met behulp van een andere module, zoals de [!UICONTROL Watch Private Channel Messages] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Public Channel Message]**

Deze actiemodule keert een bericht met bepaalde identiteitskaart van een gespecificeerd openbaar kanaal terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Een verbinding maken met [!DNL Adobe Workfront Fusion] - Basisinstructies</a> voor instructies over het koppelen van uw [!DNL Slack] account aan[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Voer de kanaal-ID in of wijs deze toe.</p> <p>Opmerking: De kanaal-ID kan worden opgehaald met behulp van de [!UICONTROL List Channels] module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Time stamp)]</td> 
   <td> <p> Voer de tijdstempel van het bericht in of wijs deze toe van het bericht waarover u informatie wilt ophalen.</p> <p>Opmerking: De tijdstempel kan worden opgehaald met behulp van een andere module, zoals de [!UICONTROL Watch Public Channel Messages] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Message]

Met deze actiemodule kunt u een bestaand bericht bewerken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Slack] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Voer de id in van het kanaal dat het bericht bevat dat u wilt bijwerken of wijs deze toe.</p> <p>Opmerking: de kanaal-id kan worden opgehaald met de module [!UICONTROL List Channels] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Time stamp)]</p> </td> 
   <td> <p> Ga of kaart de stempel van de berichttijd van het bericht in u informatie over wilt terugwinnen.</p> <p>Opmerking: de tijdstempel kan worden opgehaald met een andere module, zoals de module [!UICONTROL Watch Public Channel Messages] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Voer de nieuwe tekstinhoud in van het bericht dat u wilt bijwerken.</p> <p>Voor meer informatie, zie <a href="https://api.slack.com/docs/formatting"> Formatterende tekst voor toepassingsoppervlakten </a> in de [!DNL Slack] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As user]</td> 
   <td>Schakel deze optie in om het bericht bij te werken als de gebruiker die eigenaar is van de referenties die door de verbinding voor deze module worden gebruikt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachments]</td> 
   <td>Voor elk punt dat u aan het bericht wilt vastmaken, klik <b> toevoegen punt </b> en vul de details van het punt in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link names]</p> </td> 
   <td> <p>Schakel deze optie in als u namen en kanalen de <code>@username</code> - of <code>#channel</code> -indeling wilt laten gebruiken. </p> <p>Voor meer informatie, zie <a href="https://api.slack.com/docs/formatting"> Formatterende tekst voor toepassingsoppervlakten </a> in de [!DNL Slack] documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse message text]</p> </td> 
   <td> <p>Schakel deze optie in als u automatisch parseren wilt toestaan. </p> <p> Zie <a href="https://api.slack.com/docs/formatting">Tekst opmaken voor app-oppervlakken</a> in de [!DNL Slack] documentatie voor meer informatie.</p> <p>Opmerking: Als u of [!UICONTROL Parse message text] opties in het oorspronkelijke bericht hebt gebruikt[!UICONTROL Link names], moet u deze ook opgeven bij het uitvoeren van de module Een bericht bijwerken.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Watch Private Channel Messages]

Deze triggermodule start het scenario wanneer een nieuw bericht wordt toegevoegd aan een privékanaal (groep).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Een verbinding maken met [!DNL Adobe Workfront Fusion] - Basisinstructies</a> voor instructies over het koppelen van uw [!DNL Slack] account aan[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Selecteer het privékanaal dat je wilt bekijken voor nieuwe berichten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Stel het maximum aantal berichten [!DNL Workfront Fusion] in dat tijdens één uitvoeringscyclus wordt geretourneerd.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Public Channel Messages]

Deze triggermodule start het scenario wanneer een nieuw bericht wordt toegevoegd aan een openbaar kanaal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Een verbinding maken met [!DNL Adobe Workfront Fusion] - Basisinstructies</a> voor instructies over het koppelen van uw [!DNL Slack] account aan[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Selecteer het openbare kanaal dat je wilt bekijken voor nieuwe berichten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Stel het maximum aantal berichten [!DNL Workfront Fusion] in dat tijdens één uitvoeringscyclus wordt geretourneerd.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Gesprekken

* [Een kanaal ophalen](#get-a-channel)
* [Kanalen weergeven](#list-channels)
* [Leden in kanaal weergeven](#list-members-in-channel)

#### [!UICONTROL Get a Channel]

Deze actiemodule retourneert informatie over een werkruimtekanaal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Slack] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Voer de ID in of wijs deze toe van het kanaal waarover u informatie wilt ophalen.</p> <p>Opmerking: De kanaal-ID kan worden opgehaald met behulp van de [!UICONTROL List Channels] module.</p> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL List Channels]

Deze zoekmodule geeft een lijst met alle kanalen in een werkruimte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Een verbinding maken met [!DNL Adobe Workfront Fusion] - Basisinstructies</a> voor instructies over het koppelen van uw [!DNL Slack] account aan[!DNL Workfront Fusion].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Exclude archived]</p> </td> 
   <td> <p>Selecteer deze optie [!UICONTROL Yes] om gearchiveerde kanalen uit te sluiten in de resultaten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Selecteer het type kanalen dat u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Stel het maximumaantal kanalen in dat [!DNL Workfront Fusion] tijdens één uitvoeringscyclus retourneert.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL List Members in Channel]

Deze zoekmodule geeft een lijst met gebruikers in het geselecteerde kanaal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Een verbinding maken met [!DNL Adobe Workfront Fusion] - Basisinstructies</a> voor instructies over het koppelen van uw [!DNL Slack] account aan[!DNL Workfront Fusion].</p> </td> 
  </tr> 
<tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Kies hoe u het bericht wilt selecteren dat u wilt .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Typ of wijs in het veld <strong>[!UICONTROL Channel ID or name]</strong> de kanaalid of het kanaal in waarvan u de gebruikers wilt weergeven.</p> <p>Opmerking: de kanaal-id kan worden opgehaald met de module [!UICONTROL List Channels] .</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Selecteer het type kanaal en selecteer vervolgens het kanaal.</p> </li> 
    </ul> </td> 
  </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Stel het maximumaantal leden dat [!DNL Workfront Fusion] retourneert tijdens één uitvoeringscyclus in.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Overige

#### [!UICONTROL Make an API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Slack] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Slack] -modules kan worden uitgevoerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Slack] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in ten opzichte van <code>https://slack.com/api/</code>. Voorbeeld: <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   TD&gt; <p>Selecteer de HTTP-aanvraagmethode die u nodig hebt om de API-aanroep te configureren. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP-aanvraagmethoden</a> voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de headers van de aanvraag toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] Voegt de autorisatieheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de body-inhoud voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Base URL]</td> 
   <td>Selecteer de basis-URL die u voor de API-aanroep wilt gebruiken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Send access token]</td> 
   <td>Selecteer of u het toegangstoken als kopbal of als vraagparameter wilt verzenden.</td> 
  </tr> 
 </tbody> 
</table>

## Terminologie

De volgende terminologie kan nuttig zijn bij het configureren van [!DNL Slack] modules:

* **DM**: [!UICONTROL Direct Message]
* **IM**: [!UICONTROL Instant Message]
* **Privé Kanaal**: vroeger [!UICONTROL Group]
* **Direct Message**: voorheen [!UICONTROL IM]
* **Kanaal**: [!UICONTROL Conversation] in de API-documentatie, [!UICONTROL channel] in de [!DNL Slack] app.
