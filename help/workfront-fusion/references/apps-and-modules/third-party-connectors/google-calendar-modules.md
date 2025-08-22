---
title: Google-kalendermodules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die gebruikmaken van Google Calendar, en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---

# [!DNL Google Calendar] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!UICONTROL Google Calendar] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-abonnement*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidige vergunningsvereiste: geen Workfront Fusion-vergunningsvereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] Adobe Workfront-abonnement hebt, moet uw organisatie zowel Adobe Workfront Fusion als Adobe Workfront aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. Workfront Fusion is opgenomen in het Workfront-plan van [!UICONTROL Ultimate] .</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet Adobe Workfront Fusion en Adobe Workfront aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met uw Workfront-beheerder om te weten te komen welk plan, licentietype of toegang u hebt.

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Als u [!DNL Google Calendar] -modules wilt gebruiken, moet u een [!DNL Google] -account hebben.

## Google Calendar API-informatie

De Google Calendar-aansluiting gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Calendar] modules en hun velden

Wanneer u [!DNL Google Calendar] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Google Calendar] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Triggers](#triggers)
* [Handelingen](#actions)
* [Iteratoren](#iterators)

### Triggers

* [Gebeurtenissen van Let](#watch-events)
* [Controlegebeurtenissen (onmiddellijk)](#watch-events-instant)

#### Gebeurtenissen van Let

Deze triggermodule voert een scenario uit wanneer een nieuwe gebeurtenis wordt toegevoegd, bijgewerkt, verwijderd, gestart of beëindigd in de kalender die u opgeeft. De module retourneert alle standaardvelden die zijn gekoppeld aan de record of records, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google Calendar] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Selecteer de kalender waarmee de module moet werken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Kies of u alleen nieuwe gebeurtenissen of nieuwe gebeurtenissen en alle wijzigingen wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Schakel deze optie in om gebeurtenissen op te nemen die zijn verwijderd.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Voer de tekst in waarvoor u resultaten wilt retourneren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Stel het maximumaantal gebeurtenissen in waarmee Workfront Fusion tijdens één cyclus werkt (het aantal herhalingen per uitgevoerde scenario). Als de waarde te hoog is ingesteld, kan de verbinding aan de kant van de opgegeven service van derden (timeout) worden onderbroken. Workfront Fusion heeft daar geen invloed op. Wij adviseren dat u een lagere waarde plaatst en of een hogere waarde voor het maximumaantal cycli bepaalt of het scenario vaker in werking stelt.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Controlegebeurtenissen (onmiddellijk)

Deze triggermodule gebruikt een mailhaak om een e-mailadres te maken dat u kunt gebruiken als een genodigde van gebeurtenissen. De module begint een scenario dat op gebeurtenissen wordt gebaseerd dat het e-mailadres wordt uitgenodigd aan.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>Selecteer de brievenhaak die u voor deze module wilt gebruiken. Om een nieuwe brievenbus tot stand te brengen, voegt de klik <b> </b> toe en gaat de verbinding in u voor de brievenhaak wilt gebruiken.</p><p>Voor instructies over het aansluiten van uw [!DNL Google Calendar] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> Stel het maximumaantal gebeurtenissen in waarmee Workfront Fusion tijdens één cyclus werkt (het aantal herhalingen per uitgevoerde scenario). Als de waarde te hoog is ingesteld, kan de verbinding aan de kant van de opgegeven service van derden (timeout) worden onderbroken. Workfront Fusion heeft daar geen invloed op. Wij adviseren dat u een lagere waarde plaatst en of een hogere waarde voor het maximumaantal cycli bepaalt of het scenario vaker in werking stelt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [Een kalender maken](#create-a-calendar)
* [Een gebeurtenis maken](#create-an-event)
* [Een gebeurtenis verwijderen](#delete-an-event)
* [Gebeurtenissen ophalen](#get-events)
* [Een gebeurtenis bijwerken](#update-an-event)

#### Een kalender maken

Deze actiemodule maakt een kalender die aan de account is gekoppeld.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google Calendar] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Selecteer de kleur die u aan de kalender wilt koppelen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>Voer een naam voor de nieuwe kalender in of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

Deze actiemodule maakt een gebeurtenis.

U geeft de kalender en de parameters voor de gebeurtenis op.

De module retourneert de id van de gebeurtenis en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Voor instructies over het aansluiten van uw [!DNL Google Calendar] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selecteer de kalender waarin u de gebeurtenis wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Selecteer de kleur die de gebeurtenis in de kalender weergeeft.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Voer een naam voor de gebeurtenis in of wijs een naam toe. </p> <p>Opmerking: als u [!UICONTROL Quick add] in het veld [!UICONTROL Create an event] hebt geselecteerd, kunt u de datum en tijd van de gebeurtenis opnemen en maakt Workfront Fusion de gebeurtenis voor die datum en tijd. Voorbeeld: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code> . Als u [!UICONTROL Quick add] hebt geselecteerd maar geen datum en tijd in de naam van de gebeurtenis hebt opgenomen, wordt de gebeurtenis gemaakt op basis van de huidige tijd en duurt deze een uur.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Schakel deze optie in als de gebeurtenis een alledaagse gebeurtenis is (geen begin- en eindtijd nodig).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Voer de begindatum en -tijd van de gebeurtenis in of wijs deze toe. </p> <p>Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Voer de einddatum en -tijd van de gebeurtenis in of wijs deze toe. </p> <p>Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Voer een beschrijving van de gebeurtenis in of wijs deze toe. Dit veld ondersteunt HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Voer een locatie voor de gebeurtenis in het tekstformulier in.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Schakel deze optie in als u de standaardinstellingen voor herinneringen wilt gebruiken. Als u een aangepaste herinnering instelt in het veld [!UICONTROL Reminder] , wordt deze waarde ingesteld op Nee.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Herinnering toevoegen voor de gebeurtenis. Voor elke herinnering wilt u toevoegen, <b> toevoegen punt </b>, dan selecteren de methode u met moet worden herinnerd en bepalen hoe lang (in notulen) vóór de gebeurtenis wilt worden herinnerd u.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Voeg de deelnemers aan de gebeurtenis toe. Voor elke aanwezige, klik <b> een aanwezige </b> toevoegen, dan ingaan of hun naam en e-mailadres in kaart brengen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Selecteer of u wilt dat mensen die uw kalender bekijken u als Bezig of Beschikbaar tijdens deze gebeurtenis zien.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Selecteer de zichtbaarheid van deze gebeurtenis. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>De gebeurtenis heeft de zichtbaarheid die u hebt ingesteld in uw kalenderinstellingen.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Iedereen met wie de kalender wordt gedeeld kan deze gebeurtenis zien.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Alleen deelnemers kunnen deze gebeurtenis zien.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Geef op of u meldingen over het maken van een nieuwe gebeurtenis wilt verzenden naar alle gasten, niet- [!DNL Google Calendar] gasten of naar niemand.</p> <p>Tip: we raden u aan de optie [!UICONTROL None] alleen te gebruiken voor gevallen waarin migratie wordt gebruikt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Schakel deze optie in als u gasten in staat wilt stellen deze gebeurtenis te wijzigen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Voeg terugkerende regels toe die u op deze gebeurtenis wilt toepassen. Elke regel vereist een lijst met [!UICONTROL RRULE]-, [!UICONTROL EXRULE] -, [!UICONTROL RDATE] - en [!UICONTROL EXDATE] -regels voor een terugkerende gebeurtenis. [!UICONTROL DTSTART] en [!UICONTROL DTEND] regels zijn niet toegestaan in dit veld. De begin- en eindtijd van gebeurtenissen worden opgegeven in de begin- en eindvelden. Dit veld wordt weggelaten voor enkele gebeurtenissen of voor terugkerende gebeurtenissen. Voor meer informatie, zie <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5"> RFC5545 </a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an event]

Deze actiemodule verwijdert een gebeurtenis.

U geeft de kalender en gebeurtenis-id op.

De module retourneert de id van de gebeurtenis en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google Calendar] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selecteer de kalender die de gebeurtenis bevat die u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Voer de gebeurtenis-id in uit een eerder gemaakte [!DNL Google Calendar] -gebeurtenis die u wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get events]

Deze module haalt informatie over gebeurtenissen in de geselecteerde kalender op op basis van criteria u specificeert.

U geeft de kalender en de parameters van de zoekopdracht op.

De module retourneert de id van de gebeurtenissen en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Voor instructies over het aansluiten van uw [!DNL Google Calendar] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Selecteer de kalender waarvoor u gebeurtenissen wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Voer de datum in waarop de gebeurtenis begint of wijs de datum toe. Deze module wint ook gebeurtenissen terug die vóór deze datum beginnen, die nog op de ingegaan begindatum voorkomen. </p> <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Voer de datum in of wijs de datum toe waarop de gebeurtenis eindigt. </p> <p> Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> Schakel deze optie in om terugkerende gebeurtenissen als één instantie te behandelen. Als u bijvoorbeeld een wekelijkse vergadering hebt en deze optie is ingeschakeld, retourneert de module de vergadering van elke week als een aparte gebeurtenis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Voer de zoekterm in of wijs deze toe waarop u wilt zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>Selecteer de volgorde van de gebeurtenissen die in het resultaat worden geretourneerd.</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong>: Volgorde op de begindatum en -tijd (oplopend). Dit is alleen beschikbaar bij het opvragen van afzonderlijke gebeurtenissen.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: Volgorde bij laatste wijzigingstijd (oplopend).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mazimum number of returned events]</td> 
   <td> <p>Stel het maximumaantal gebeurtenissen in dat Workfront Fusion retourneert tijdens één uitvoeringscyclus.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event]

Deze actiemodule wijzigt een bestaande gebeurtenis.

U geeft de kalender en gebeurtenis-id op.

De module retourneert de id van de gebeurtenis en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Google Calendar] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Selecteer de kalender waarmee u wilt werken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Voer de gebeurtenis-id in uit de eerder gemaakte gebeurtenis [!DNL Google Calendar] die u wilt bijwerken.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Voer een naam voor de gebeurtenis in of wijs een naam toe. </p> <p>Opmerking: als u [!UICONTROL Quick add] in het veld [!UICONTROL Create an event] hebt geselecteerd, kunt u de datum en tijd van de gebeurtenis opnemen en maakt Workfront Fusion de gebeurtenis voor die datum en tijd. Voorbeeld: <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code> . Als u [!UICONTROL Quick add] hebt geselecteerd maar geen datum en tijd in de naam van de gebeurtenis hebt opgenomen, wordt de gebeurtenis gemaakt op basis van de huidige tijd en duurt deze een uur.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Schakel deze optie in als de gebeurtenis een alledaagse gebeurtenis is (geen begin- en eindtijd nodig).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Voer de begindatum en -tijd van de gebeurtenis in of wijs deze toe. </p> <p>Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Voer de einddatum en -tijd van de gebeurtenis in of wijs deze toe. </p> <p>Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Voer een beschrijving van de gebeurtenis in of wijs deze toe. Dit veld ondersteunt HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Voer een locatie voor de gebeurtenis in het tekstformulier in.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Schakel deze optie in als u de standaardinstellingen voor herinneringen wilt gebruiken. Als u een aangepaste herinnering instelt in het veld [!UICONTROL Reminder] , wordt deze waarde ingesteld op Nee.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Herinnering toevoegen voor de gebeurtenis. Voor elke herinnering wilt u toevoegen, <b> toevoegen punt </b>, dan selecteren de methode u met moet worden herinnerd en bepalen hoe lang (in notulen) vóór de gebeurtenis wilt worden herinnerd u.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Voeg de deelnemers aan de gebeurtenis toe. Voor elke aanwezige, klik <b> een aanwezige </b> toevoegen, dan ingaan of hun naam en e-mailadres in kaart brengen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Selecteer of u wilt dat mensen die uw kalender bekijken u als Bezig of Beschikbaar tijdens deze gebeurtenis zien.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Selecteer de zichtbaarheid van deze gebeurtenis. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>De gebeurtenis heeft de zichtbaarheid die u hebt ingesteld in uw kalenderinstellingen.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Iedereen met wie de kalender wordt gedeeld kan deze gebeurtenis zien.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Alleen deelnemers kunnen deze gebeurtenis zien.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Geef op of u meldingen over het maken van een nieuwe gebeurtenis wilt verzenden naar alle gasten, niet- [!DNL Google Calendar] gasten of naar niemand.</p> <p>Tip: we raden u aan de optie [!UICONTROL None] alleen te gebruiken voor gevallen waarin migratie wordt gebruikt.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Schakel deze optie in als u gasten in staat wilt stellen deze gebeurtenis te wijzigen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Voeg terugkerende regels toe die u op deze gebeurtenis wilt toepassen. Elke regel vereist een lijst met [!UICONTROL RRULE]-, [!UICONTROL EXRULE] -, [!UICONTROL RDATE] - en [!UICONTROL EXDATE] -regels voor een terugkerende gebeurtenis. [!UICONTROL DTSTART] en [!UICONTROL DTEND] regels zijn niet toegestaan in dit veld. De begin- en eindtijd van gebeurtenissen worden opgegeven in de begin- en eindvelden. Dit veld wordt weggelaten voor enkele gebeurtenissen of voor terugkerende gebeurtenissen. Voor meer informatie, zie <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5"> RFC5545 </a>.</td> 
  </tr>

</tbody> 
</table>

### Iteratoren

#### Bijlagen herhalen

Deze actiemodules doorlopen gehechtheid aan een gebeurtenis, en output elke gehechtheid in een afzonderlijke bundel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Selecteer de module in dit scenario die de gebeurtenis uitvoert die de gehechtheid bevat die u wilt herhalen. </td> 
  </tr> 
 </tbody> 
</table>

#### Deelnemers itereren

Deze actiemodules doorlopen de deelnemers voor een gebeurtenis en voeren elke deelnemer uit in een aparte bundel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Selecteer in dit scenario de module die de gebeurtenis uitvoert die de deelnemers bevat die u wilt herhalen. </td> 
  </tr> 
 </tbody> 
</table>





## Een scenario activeren vóór een gebeurtenis

U kunt een scenario een gespecificeerde tijd vóór een gebeurtenis met de hulp van standaard [!DNL Google Calendar] e-mailherinneringen en de [!UICONTROL Webhooks] > [!UICONTROL Custom mailhook] module teweegbrengen.

1. Met de module [!UICONTROL Google Calendar] > [!UICONTROL Update an event] kunt u een e-mailherinnering aan de gebeurtenis toevoegen:

   ![ het scenario van de Trekker vóór gebeurtenis ](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Creeer een nieuw scenario dat met [!UICONTROL Webhooks] > [!UICONTROL Custom mailhook] module begint.

   1. Kopieer het e-mailadres van de mailhaak.
   1. Sla het scenario op en voer het uit.

1. Lijn in [!DNL Gmail] de [!DNL Google Calendar] -e-mailherinneringen om naar het e-mailadres van de mailhaak:

   1. Open uw **[!UICONTROL [!DNL Gmail] settings]**.
   1. Open de tab **[!UICONTROL Forwarding and POP/IMAP]** .
   1. Klik op **[!UICONTROL Add a forwarding address].**
   1. Plak het e-mailadres van de gekopieerde e-mail, klik op &#x200B; **[!UICONTROL Next]**, bevestig door op **[!UICONTROL Proceed]** in het pop-upvenster te drukken en klik vervolgens op **[!UICONTROL OK]** .

   1. Schakel in Workfront Fusion over naar het nieuwe scenario dat de uitvoering moet voltooien door het bevestigingsbericht te ontvangen.
   1. Klik de bel boven de module om de output van de module te inspecteren.
   1. Vouw het item `Text` uit en kopieer de bevestigingscode:

      ![ Bevestigingscode ](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. Plak in Gmail de bevestigingscode in het bewerkingsvak en klik op &#x200B;**[!UICONTROL Verify]** :

      ![ de code van het Deeg ](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Open de tab **[!UICONTROL Filters and Blocked Addresses]** .
   1. Klik op **[!UICONTROL Create a new filter]**.
   1. Stel een filter in voor alle e-mails die uit `     calendar-notification@google.com` komen en klik op &#x200B; **[!UICONTROL Create a filter]** :
   1. Selecteer **[!UICONTROL Forward it to]** en kies in de lijst het e-mailadres van de e-mail.
   1. Klik op **[!UICONTROL Create filter]** om het filter te maken.

1. (Optioneel) Voeg in Workfront Fusion de module [!UICONTROL Text parser] > [!UICONTROL Match pattern] toe na de module [!UICONTROL Webhooks] > [!UICONTROL Custom mailhook] om de HTML-code van de e-mail te parseren voor alle informatie die u nodig hebt.

   U kunt de module bijvoorbeeld als volgt configureren om de id van de gebeurtenis op te halen:

   *Patroon*: `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Tekst*: Het `HTML content` punt dat van [!UICONTROL Webhooks] wordt uitgevoerd > [!UICONTROL Custom mailhook] module.
