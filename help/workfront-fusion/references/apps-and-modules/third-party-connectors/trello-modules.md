---
title: Trello-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Trello gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: 899fc717f5107433d6f1aea31c4d079243a85822
workflow-type: tm+mt
source-wordcount: '4366'
ht-degree: 0%

---

# [!UICONTROL Trello] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!UICONTROL Trello] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Als u [!DNL Trello] -modules wilt gebruiken, moet u een [!UICONTROL Trello] -account hebben.

## Trello API-informatie

De Trello-aansluiting gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!UICONTROL Trello] met [!DNL Workfront Fusion]

Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie [ een verbinding tot stand brengen  [!DNL Adobe Workfront Fusion]  - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Trello] modules en hun velden

Wanneer u [!UICONTROL Trello] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!UICONTROL Trello] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Borden](#boards)
* [Lijsten](#lists)
* [Kaarten](#cards)
* [Leden](#members)
* [Controlelijsten](#checklists)
* [Labels](#labels)
* [Opmerkingen](#comments)

### Borden

+++ **[!UICONTROL Archive or Unarchive a Board]**

In deze actiemodule wordt een door u opgegeven board gesloten (archieven) of opnieuw geopend (unarchives).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Voer de id in van het board dat u wilt sluiten of opnieuw openen, of wijs deze id toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Selecteer of u het bord wilt sluiten (archiveren) of opnieuw openen (archiveren).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

Deze actiemodule wijst een lid toe aan een raad die u specificeert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Selecteer de raad waar u een lid wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email address]</td> 
   <td> <p> Voer het e-mailadres in of wijs het e-mailadres toe van het lid dat u aan de lijst wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Member type]</p> </td> 
   <td> <p>Selecteer het type lid dat het nieuwe lid moet zijn.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: Een beheerder van het toetsenbord kan elke willekeurige bordactie op het bord uitvoeren.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: Een normaal lid is gewoon lid van de raad van bestuur.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: Een waarnemer is lid met alleen-lezen toegang tot de raad. <br> de Waarnemers zijn slechts beschikbaar aan teams met [!UICONTROL Trello Business Class].</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Full name]</td> 
   <td> <p> Voer de volledige naam in of wijs de volledige naam toe van de gebruiker die u aan de kaart wilt toevoegen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Board]**

In deze actiemodule wordt een nieuw board met de geselecteerde instellingen gemaakt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer een naam in voor het nieuwe bord of wijs een naam toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Voer zo nodig de beschrijving van de kaart in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Voer de id van de organisatie in of wijs deze toe. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>De raden hebben verschillende stem en commentaarregels voor elk toestemmingsniveau. Als uw board bijvoorbeeld [!UICONTROL Private] is en u de regels voor stemmen en opmerkingen instelt als [!UICONTROL All] , ontvangt u een fout. </p> <p>Stemmen en opmerkingen zijn beperkt tot de volgende groepen voor elk machtigingsniveau:</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      Leden, leden en waarnemers</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      Leden, leden en waarnemers, leden van de organisatie</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      Leden, leden en waarnemers, organisatieleden, alle</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Selecteer een optie om aan te geven wie op dit bord kan stemmen. Zie het veld [!UICONTROL Permission level] voor stembeperkingen op machtigingsniveaus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Selecteer een optie om op te geven wie opmerkingen kan plaatsen op de kaarten voor dit bord. Zie het veld [!UICONTROL Permission level] voor opmerkingen over beperkingen op machtigingsniveaus.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Invitations]</p> </td> 
   <td> <p>Selecteer wie andere personen kan uitnodigen voor dit bord.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-join]</p> </td> 
   <td> <p>Selecteer of teamleden zich bij de raad van bestuur kunnen aansluiten of zij moeten worden uitgenodigd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default labels]</p> </td> 
   <td> <p>Selecteer of u de standaardset labels voor het nieuwe bord wilt gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default lists]</p> </td> 
   <td> <p>Selecteer of u de standaardset lijsten aan het board wilt toevoegen ([!UICONTROL To Do], [!UICONTROL Doing], [!UICONTROL Done]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board source ID]</p> </td> 
   <td> <p>Selecteer of wijs identiteitskaart van de raad toe die u in de nieuwe raad wilt kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card Covers]</p> </td> 
   <td> <p>Selecteer <strong>[!UICONTROL Yes]</strong> als u kaartomslagen voor het bord wilt inschakelen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Background]</p> </td> 
   <td> <p>Selecteer de kleur van de achtergrond of de aangepaste achtergrond.</p> <p>Opmerking: aangepaste achtergronden zijn alleen beschikbaar voor abonnees van [!UICONTROL Trello Gold and Business Class] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> Als u een aangepaste achtergrond wilt gebruiken in het veld [!UICONTROL Background] , voert u de id van de achtergrond die u wilt gebruiken in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Selecteer een optie tussen twee manieren voor kaartveroudering. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: Kaarten scheuren, geel en kraken als een oude piratenkaart terwijl ze ouder worden.</li> 
     <li><strong>[!UICONTROL Regular mode &#x200B;]</strong>: Kaarten worden steeds transparanter naarmate ze ouder worden. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Board]**

In deze actiemodule worden de instellingen van een bestaande board bewerkt.

>[!SUCCESS]
>
><table style="table-layout:auto">
><col> 
> <col> 
> <tbody> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Connection] </td> 
>   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
>   <td> <p>Voer de unieke [!UICONTROL Trello] -id in of wijs deze toe aan het bord dat u met de module wilt maken. U kunt de kaart-id ophalen met behulp van een andere module, zoals de module Controlebord</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL New name]</td> 
>   <td> <p> Voer een nieuwe naam voor het bord in of wijs deze toe.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL New description]</td> 
>   <td> <p> Voer een nieuwe beschrijving van het bord in of wijs deze toe.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
>   <td> <p>Voer de unieke [!UICONTROL Trello] -id in of wijs deze toe aan het bord dat u wilt bewerken in de module.  </p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Subscribe] </td> 
>   <td> <p>Selecteer een optie om op te geven of de gebruiker die eigenaar is van de verbinding die door deze module wordt gebruikt, is geabonneerd op de kaart.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
>   <td> <p>De raden hebben verschillende stem en commentaarregels voor elk toestemmingsniveau. Bijvoorbeeld: als uw board [!UICONTROL Private] is en u de regels voor stemmen en opmerkingen instelt als [!UICONTROL All] , ontvangt u een fout. </p> <p>Stemmen en opmerkingen zijn beperkt tot de volgende groepen voor elk machtigingsniveau:</p> 
>    <ul> 
>     <li><strong>[!UICONTROL Private]</strong>: 
>      Leden, leden en waarnemers</li> 
>     <li><strong>[!UICONTROL For organization]</strong>: 
>      Leden, leden en waarnemers, leden van de organisatie</li> 
>     <li><strong>[!UICONTROL Public]</strong>: 
>      Leden, leden en waarnemers, organisatieleden, alle</li> 
>    </ul> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
>   <td> <p>Selecteer een optie om aan te geven wie op dit bord kan stemmen. Zie het veld [!UICONTROL Permission level] voor stembeperkingen op machtigingsniveaus.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
>   <td> <p>Selecteer een optie om op te geven wie opmerkingen kan plaatsen op de kaarten voor dit bord. Zie het veld [!UICONTROL Permission level] voor opmerkingen over beperkingen op machtigingsniveaus.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Invitations] </td> 
>   <td> <p>Selecteer wie personen kan uitnodigen voor dit bord.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Self-join]</td> 
>   <td> <p> Selecteer of teamleden zich bij de raad van bestuur kunnen aansluiten of zij moeten worden uitgenodigd.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Card covers]</td> 
>   <td> <p> Selecteer of de kaartomslagen op dit bord zouden moeten worden getoond.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Background] </td> 
>   <td> <p>Selecteer de kleur van de achtergrond of de aangepaste achtergrond.</p> <p>Opmerking: aangepaste achtergronden zijn alleen beschikbaar voor abonnees van [!UICONTROL Trello Gold and Business Class] .</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Background ID]</td> 
>   <td> <p> Als u een aangepaste achtergrond wilt gebruiken in het veld [!UICONTROL Background] , voert u de id van de achtergrond die u wilt gebruiken in of wijst u deze toe.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
>   <td> <p>Selecteer een optie tussen twee manieren voor kaartveroudering. </p> 
>    <ul> 
>     <li><strong>[!UICONTROL Pirate mode]</strong>: Kaarten scheuren, geel en kraken als een oude piratenkaart terwijl ze ouder worden.</li> 
>     <li><strong>[!UICONTROL Regular mode]</strong>: Kaarten worden steeds transparanter naarmate ze ouder worden. </li> 
>    </ul> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Calendar feed enabled]</td> 
>   <td> <p> Selecteer of de kalenderfeed is ingeschakeld.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL &lt;Color> label name]</td> 
>   <td> <p> Wijs een naam toe aan het gewenste kleurlabel.</p> </td> 
>  </tr> 
>  <tr> 
>   <td role="rowheader">[!UICONTROL Archive] </td> 
>   <td> <p>Selecteer een optie om aan te geven of u het board wilt archiveren (sluiten). </p> </td> 
>  </tr> 
> </tbody> 
></table>


+++

+++ **[!UICONTROL Get a Board]**

Deze actiemodule wint de details van een board terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Ga of kaart identiteitskaart van de raad in u informatie over wilt terugwinnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

Deze zoekmodule haalt informatie op over een board dat u opgeeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Typ of wijs de naam (of een deel van de naam) van het bord toe waarover u informatie wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned boards]</td> 
   <td> <p> Voer het maximumaantal tekengebieden in dat [!DNL Workfront Fusion] tijdens één uitvoeringscyclus retourneert. Deze waarde moet kleiner zijn dan of gelijk zijn aan 1000.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partial] </p> </td> 
   <td> <p>Standaard zoekt deze module naar lidinhoud voor exacte overeenkomsten van elk woord in uw query. Wanneer [!UICONTROL Partial] wordt toegelaten, zoekt de module inhoud die met om het even welk woord in uw vraag begint.</p> <p> Bijvoorbeeld als u het woord "ontwikkeling"gebruikt om een raad te zoeken getiteld "Mijn Rapport van de Status van de Ontwikkeling,"door gebrek, zou u naar het volledige woord moeten zoeken. Als u [!UICONTROL Partial] hebt ingeschakeld, kunt u wel zoeken naar 'dev', maar niet naar 'development'.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Boards] </td> 
   <td> <p>Voer "mijn" in of wijs een door komma's gescheiden lijst met kaart-id's toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Deze actiemodule verwijdert een lid uit een raad.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Voer de id in van het bord waarvan u de gebruiker wilt verwijderen (kaart maken of selecteren).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Member] </td> 
   <td> <p>Selecteer het lid dat u uit de raad wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Boards]**

Deze triggermodule begint met een scenario wanneer een nieuw bord wordt toegevoegd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal raad in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Lijsten

+++ **[!UICONTROL Create a List]**

Deze actiemodule maakt een lijst op een bord dat u opgeeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Voer de id van het bord in of wijs deze toe op de plaats waar u een lijst wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer een naam voor de nieuwe lijst in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecteer of u de lijst aan de bovenkant wilt toevoegen of het aan de bodem van de kaart wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy list]</td> 
   <td> <p> Als u een lijst kopieert, selecteert u hoe u identiteitskaart van de lijst wilt ingaan u wilt kopiëren.</p> 
    <ul> 
     <li> <p><strong> ga manueel binnen </strong> </p> <p>Voer in het veld <strong>[!UICONTROL List ID]</strong> de id in van de lijst die u wilt kopiëren of wijs deze toe.<br></p> </li> 
     <li> <p><strong> Uitgezocht </strong> </p> <p>Selecteer het bord met de lijst die u wilt kopiëren en selecteer vervolgens de lijst.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a List]**

Deze actiemodule bewerkt een bestaande lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td> <p> Voer de id in van de lijst die u wilt bijwerken of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer een nieuwe naam voor de lijst in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Wijs of selecteer het bord toe waar u de lijst wilt verplaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecteer of u de lijst aan de bovenkant wilt toevoegen of het aan de bodem van de kaart wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribed]</td> 
   <td> <p>Schakel deze optie in als u het actieve lid in de lijst wilt opnemen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a List]**

Deze actiemodule wint details over een specifieke lijst terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL List ID]</p> </td> 
   <td> <p>Ga of kaart identiteitskaart van de lijst in u informatie over wilt terugwinnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards moved to a list]**

Deze activeringsmodule wordt geactiveerd wanneer een kaart naar een specifieke lijst wordt verplaatst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>Selecteer het bord dat de lijst bevat die u voor kaarten wilt controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List]</td> 
   <td>Selecteer de lijst die u wilt bekijken voor kaarten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Kaarten

+++ **[!UICONTROL Add an Attachment]**

Deze actiemodule voegt een bijlage toe aan de geselecteerde kaart.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Selecteer hoe u de id wilt invoeren van de kaart waaraan u een bijlage wilt toevoegen.</p> 
    <ul> 
     <li> <p><strong> ga manueel binnen </strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id in van de kaart waaraan u een bijlage wilt toevoegen of wijs deze toe.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een bijlage wilt toevoegen, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment type]</p> </td> 
   <td> <p>Selecteer of u het bestand rechtstreeks wilt uploaden of een URL naar het bestand wilt opgeven.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Voer de URL naar het bestand in en geef een naam op voor de bijlage.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Card]**

Deze actiemodule archiveert of stuurt een kaart terug naar het bord.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card ID]</td> 
   <td> <p> Voer de id in van de kaart die u wilt archiveren of terugsturen naar de kaart of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Selecteer of u de kaart wilt sluiten (archiveren) of terugsturen naar de kaart (unarchive).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a card]**

Deze actiemodule maakt een kaart in een geselecteerde lijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a list ID]</td> 
   <td> <p> Selecteer hoe u de id wilt invoeren in de lijst waar u een kaart wilt toevoegen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL List ID]</strong> de id van de lijst in of wijs deze toe op de plaats waar u een kaart wilt toevoegen.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de lijst waaraan u een kaart wilt toevoegen en selecteer vervolgens de lijst.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Voor elk etiket dat u aan de kaart wilt toevoegen, klik <b> toevoegen punt </b> en ga identiteitskaart van het etiket in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members]</td> 
   <td>Voor elk lid dat u aan de kaart wilt toevoegen, klik <b> toevoegen punt </b> en ga identiteitskaart van het lid in. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer een naam in voor de nieuwe kaart.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Description]</p> </td> 
   <td> <p>Voer de beschrijving van de kaart in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecteer of u de kaart aan de bovenkant wilt toevoegen of de kaart aan de bodem van de lijst toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Voer een vervaldatum in voor de kaart. Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Schakel deze optie in om de kaart op de juiste datum als volledig te markeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td> <p>Typ of wijs de URL toe van een bestand dat u als bijlage aan de kaart wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source file]</p> </td> 
   <td> <p>Voer gegevens in of wijs deze toe aan een bestand dat u als bijlage aan de kaart wilt toevoegen. Selecteer een bestand uit een vorige module of wijs de naam en gegevens van het bestand toe</p> 
     <p>Opmerking: per bijlage geldt een uploadlimiet van 10 MB. Leden van [!UICONTROL Business Class] en [!UICONTROL Trello Gold] hebben echter een uploadlimiet van 250 MB per bijlage.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy card]</td> 
   <td> <p> Als u een nieuwe kaart maakt als een kopie van een bestaande kaart, selecteert u hoe u de id wilt invoeren van de kaart die u wilt kopiëren.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id in van de kaart die u wilt kopiëren of wijs deze toe.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart die u wilt kopiëren, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Card]**

In deze actiemodule wordt een bestaande kaart bewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Card ID]</td> 
   <td> <p> Selecteer hoe u de id wilt invoeren van de kaart die u wilt bewerken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id in van de kaart die u wilt bewerken.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart die u wilt bewerken, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p>Voer een nieuwe naam voor de kaart in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New description]</p> </td> 
   <td> <p>Voer een nieuwe beschrijving voor de kaart in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Move a card]</p> </td> 
   <td> <p>Selecteer het bord of het bord en geef aan waar u de kaart wilt verplaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Voor elk etiket dat u aan de kaart wilt toevoegen, klik <b> toevoegen punt </b> en ga identiteitskaart van het etiket in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecteer of u de kaart bovenaan wilt plaatsen of [!UICONTROL append] de kaart onderaan in de lijst.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Voer een vervaldatum in voor de kaart. Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Schakel deze optie in om de kaart op de juiste datum als volledig te markeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members] </td> 
   <td> <p>Voor elk lid dat u aan de kaart wilt toevoegen, <b> klik toevoegen punt </b> en ga of kaart identiteitskaart van het lid in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment cover ID]</p> </td> 
   <td> <p>Voer de id in van de afbeeldingsbijlage die u als omslag van de kaart wilt gebruiken of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Selecteer of het lid op de kaart moet worden geabonneerd.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Selecteer een optie om aan te geven of u de kaart wilt archiveren (sluiten). </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Card]**

Deze actiemodule haalt de gegevens van een geselecteerde kaart op.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p>Voer de id in van het bord met de kaart waarover u gegevens wilt ophalen. Op deze manier kunt u namen van aangepaste velden van de board zien.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Selecteer hoe u de id wilt invoeren van de kaart waarover u gegevens wilt ophalen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id in van de kaart waarover u gegevens wilt ophalen of wijs deze toe.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waarover u gegevens wilt ophalen, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Cards]**

Deze actiemodule retourneert kaarten die overeenkomen met de zoekquery.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>Selecteer de gebieden die u wilt doorzoeken. Als er geen board is geselecteerd, worden alle borden doorzocht.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Query]</p> </td> 
   <td> <p>Voer de zoekquery in. U kunt uw zoekopdracht verfijnen met de volgende zoekoperatoren:</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>U kunt "-" aan om het even welke exploitant toevoegen om een negatieve onderzoek, zoals <code>[!UICONTROL -has:members]</code> te doen naar kaarten zonder enige toegewezen leden te zoeken.</p> </li> 
     <li><code><strong>@name</strong></code> <p>Keert kaarten terug die aan een lid worden toegewezen. U kunt ook <code>member:</code> gebruiken. Gebruik <code>@me</code> als u alleen uw kaarten wilt opnemen.</p> </li> 
     <li><code><strong>#label</strong></code> <p>Retourneert gelabelde kaarten. U kunt ook <code>label:</code> gebruiken. <code>label:"FIX IT"</code> retourneert bijvoorbeeld kaarten met het label "FIX IT".</p> </li> 
     <li><code><strong>board:id</strong></code> <p>Keert kaarten binnen een specifieke raad terug. <code>board:Trello</code> retourneert bijvoorbeeld kaarten op borden met [!UICONTROL Trello] in de naam van het tekengebied.</p> </li> 
     <li><code><strong>list:name</strong></code> <p>Retourneert kaarten in de lijst met de naam "name".</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>Retourneert kaarten met bijlagen. De operator <code>has</code>: kan ook worden gebruikt met andere kenmerken, zoals <code>has:description</code> , <code>has:cover</code> , <code>has:members</code> of <code>has:stickers</code> .</p> </li> 
     <li><code><strong>due:day</strong></code> <p>Retourneert kaarten die binnen 24 uur verschuldigd zijn. De operator <code>due:</code> kan ook worden gebruikt met andere tijdframes, zoals <code>due:week</code> , <code>due:month</code> of <code>due:overdue</code> . U kunt ook zoeken naar een specifiek dagbereik. Als u bijvoorbeeld <code>due:14</code> toevoegt aan de zoekopdracht, worden kaarten opgenomen die in de komende 14 dagen verschuldigd zijn.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>Retourneert kaarten die in de laatste 24 uur zijn gemaakt. De operator <code> created:</code> kan ook worden gebruikt met andere tijdframes, zoals <code>created:week</code> of <code>created:month</code> . U kunt ook zoeken naar een specifiek dagbereik. Als u bijvoorbeeld <code>created:14</code> aan de zoekopdracht toevoegt, worden kaarten opgenomen die in de afgelopen 14 dagen zijn gemaakt.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>Retourneert kaarten die in de laatste 24 uur zijn bewerkt. De operator <code>edited:</code> kan ook worden gebruikt met andere tijdframes, zoals <code>edited:week</code> of <code>edited:month</code> . U kunt ook zoeken naar een specifiek dagbereik. Als u bijvoorbeeld <code>edited:21</code> aan de zoekopdracht toevoegt, bevat dit kaarten die in de afgelopen 21 dagen zijn bewerkt.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Retourneert kaarten die overeenkomen met de tekst van kaartbeschrijvingen, checklists, opmerkingen of namen. <code>comment:"FIX IT"</code> retourneert bijvoorbeeld kaarten met "FIX IT" in een opmerking.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Retourneert kaarten die zijn geopend of gearchiveerd. Als geen van beide is opgegeven, retourneert [!UICONTROL Trello] beide typen.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>Alleen kaarten op starred boards.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned cards]</td> 
   <td> <p> Voer het maximumaantal kaarten in dat [!DNL Workfront Fusion] tijdens één uitvoeringscyclus mag retourneren of wijs het maximumaantal kaarten toe. Deze waarde moet kleiner zijn dan of gelijk zijn aan 1000.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Standaard zoekt deze module naar lidinhoud voor exacte overeenkomsten van elk woord in uw query. Wanneer [!UICONTROL Partial] wordt toegelaten, zoekt de module inhoud die met om het even welk woord in uw vraag begint.</p> <p> Bijvoorbeeld als u het woord "ontwikkeling"gebruikt om een raad te zoeken getiteld "Mijn Rapport van de Status van de Ontwikkeling,"door gebrek, zou u naar het volledige woord moeten zoeken. Als u [!UICONTROL Partial] hebt ingeschakeld, kunt u wel zoeken naar 'dev', maar niet naar 'development'.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cards] </td> 
   <td> <p>Om specifieke kaarten te zoeken, <b> voeg punt </b> toe en voeg identiteitskaart van de kaart toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards]**

Deze triggermodule start een scenario wanneer een nieuwe kaart wordt toegevoegd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Selecteer de locatie die u voor kaarten wilt controleren.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards]</strong> </li> 
     <li> <p><strong> Kaarten op specifieke raad </strong> </p> <p>Selecteer de kaart die u wilt controleren voor kaarten</p> </li> 
     <li> <p><strong>[!UICONTROL Cards on specific list]</strong> </p> <p>Selecteer het bord dat de lijst bevat die u voor kaarten wilt controleren, en selecteer dan de lijst.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Leden

+++ **[!UICONTROL Add a Member to a Card]**

Deze actiemodule voegt het opgegeven lid toe aan de opgegeven kaart.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter card ID and member ID]</p> </td> 
   <td> <p>Kies hoe u de kaart-id en de lid-id wilt invoeren.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer de <strong>[!UICONTROL Card ID]</strong> en de <strong>[!UICONTROL Member ID]</strong> in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een lid wilt toevoegen en selecteer vervolgens de lijst met de kaart, de kaart zelf en het lid dat u aan de kaart wilt toevoegen.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

Zie &quot;[!UICONTROL Assign a Member to a Board]&quot;onder [ Boards ](#boards).

+++

+++ **[!UICONTROL Search for Members]**

Deze actiemodule haalt informatie op over [!UICONTROL Trello] leden.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Voer de naam of gebruikersnaam in van de gebruiker die u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Standaard zoekt deze module naar lidinhoud voor exacte overeenkomsten van elk woord in uw query. Wanneer [!UICONTROL Partial] wordt toegelaten, zoekt de module inhoud die met om het even welk woord in uw vraag begint.</p> <p> Bijvoorbeeld als u het woord "ontwikkeling"gebruikt om een raad te zoeken getiteld "Mijn Rapport van de Status van de Ontwikkeling,"door gebrek, zou u naar het volledige woord moeten zoeken. Als u [!UICONTROL Partial] hebt ingeschakeld, kunt u wel zoeken naar 'dev', maar niet naar 'development'.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned members]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Zie &quot;[!UICONTROL Unassign a Member from a Board]&quot;onder [ Boards ](#boards).

+++

### Controlelijsten

+++ **[!UICONTROL Create a Checklist]**

Deze actiemodule maakt een controlelijst op de geselecteerde kaart.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Selecteer hoe u de id van de kaart wilt invoeren waaraan u een controlelijst wilt toevoegen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id van de kaart in of wijs deze toe waar u een controlelijst wilt toevoegen.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een controlelijst wilt toevoegen, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Voer een naam in of wijs een naam toe aan de controlelijst.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Selecteer of u de checklist aan de bovenkant wilt toevoegen of de controlelijst aan de bodem van de kaart wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter checklist ID]</p> </td> 
   <td> <p>Als u de controlelijst maakt door een bestaande controlelijst te kopiëren, voert u de id in van een broncontrolelijst die u naar de nieuwe wilt kopiëren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Checklist Item]**

Deze actiemodule voegt een item toe aan een specifieke controlelijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter checklist ID]</td> 
   <td> <p> Als u een nieuwe controlelijst maakt door een bestaande controlelijst te kopiëren, selecteert u hoe u de id van de controlelijst wilt invoeren waaraan u een item wilt toevoegen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Checklist ID]</strong> de id van de kaart in of wijs deze toe waar u een controlelijst wilt toevoegen.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een controlelijst wilt toevoegen, selecteer vervolgens de lijst met de kaart, selecteer vervolgens de kaart en selecteer vervolgens de controlelijst.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Voer een naam voor het nieuwe item in of wijs een naam toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Selecteer of u het item bovenaan of [!UICONTROL append] onderaan de controlelijst wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Checked]</p> </td> 
   <td> <p>Schakel deze optie in als u het item wilt toevoegen zoals het al is ingeschakeld.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Checklist Item]**

Deze actiemodule bewerkt een bestaande controlelijst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Card ID and Checklist Item ID]</td> 
   <td> <p> Selecteer hoe u de id van de kaart wilt invoeren en checklist waar u een item wilt bewerken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Checklist ID]</strong> de id van de kaart in of wijs deze toe waar u een controlelijst wilt toevoegen.</p> <p>Voer in het veld <strong>[!UICONTROL Checklist Item ID]</strong> de id van de controlelijst in of wijs deze toe.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een controlelijst wilt toevoegen, selecteer vervolgens de lijst met de kaart, selecteer vervolgens de kaart en selecteer vervolgens de controlelijst.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklist ID]</td> 
   <td>Selecteer of wijs de controlelijst toe waarnaar u het item in de controlelijst wilt verplaatsen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Voer een naam voor het nieuwe item in of wijs een naam toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Selecteer of u het item bovenaan of onderaan de controlelijst wilt plaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL State]</p> </td> 
   <td> <p>Selecteer of het item in de controlelijst compleet of onvolledig is.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Labels

+++ **[!UICONTROL Add a Label to a Card]**

Deze actiemodule voegt een label toe aan een geselecteerde kaart.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Selecteer hoe u de id van de kaart wilt invoeren waaraan u een controlelijst wilt toevoegen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id van de kaart in of wijs deze toe waar u een controlelijst wilt toevoegen. Op het <strong>[!UICONTROL Label ID]</strong> gebied, ga of kaart identiteitskaart van het etiket in dat u wilt toevoegen.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een controlelijst wilt toevoegen, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart. </p> <p>Selecteer het label dat u aan de kaart wilt toevoegen.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Opmerkingen

+++ **[!UICONTROL Create a Comment in a Card]**

Deze actiemodule voegt een opmerking toe aan een geselecteerde kaart.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Selecteer hoe u de id van de kaart wilt invoeren waaraan u een opmerking wilt toevoegen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id van de kaart in of wijs deze toe waar u een opmerking wilt toevoegen.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een opmerking wilt toevoegen, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment] </td> 
   <td> <p>Typ of wijs de opmerking toe die u aan de geselecteerde kaart wilt toevoegen.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Comments in a Card]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Selecteer hoe u de id van de kaart wilt invoeren waaraan u een opmerking wilt toevoegen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Voer in het veld <strong>[!UICONTROL Card ID]</strong> de id van de kaart in of wijs deze toe waar u een opmerking wilt toevoegen.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Selecteer het bord met de kaart waaraan u een opmerking wilt toevoegen, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> Voer het maximumaantal opmerkingen in dat [!DNL Workfront Fusion] tijdens één uitvoeringscyclus retourneert.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since] </td> 
   <td> <p>Stel de begindatum in van de periode waarin de opmerking is gemaakt. Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before] </td> 
   <td> <p>Stel de einddatum in van de periode waarin de opmerking is gemaakt. Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Comments]**

Deze triggermodule start een scenario wanneer een opmerking wordt toegevoegd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies over het verbinden van uw [!UICONTROL Trello] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Selecteer de locatie waar u de opmerkingen wilt bekijken.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards] Overal </strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>Selecteer het bord dat u wilt controleren voor opmerkingen</p> </li> 
     <li> <p><strong>[!UICONTROL List]</strong> </p> <p>Selecteer het bord met de lijst die u wilt controleren voor opmerkingen en selecteer vervolgens de lijst.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>Selecteer het bord met de kaart die u wilt controleren voor opmerkingen, selecteer vervolgens de lijst met de kaart en selecteer vervolgens de kaart.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Ga of kaart het maximumaantal commentaren in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL Trello] Object-id&#39;s

* [Hoe te om identiteitskaart of de kortere weg van een kaart in te vinden  [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [Hoe te om IDs van andere voorwerpen in te vinden  [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### De id of de snelkoppeling van een kaart vinden in [!DNL Trello]

Als u een kaart wilt bewerken of een nieuwe opmerking wilt maken, moet u de id van de kaart of de bijbehorende snelkoppeling weten. U kunt deze informatie ophalen uit de uitvoer van de trigger [!UICONTROL New Card] . U kunt de snelkoppeling voor een kaart ook verkrijgen door de kaart te openen en op de knop [!UICONTROL Share] te klikken. De snelkoppeling vindt u in het vak [!UICONTROL Link to this card] aan het einde van de URL na `https://trello.com/c/` .

![ Aandeel en meer ](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### Id&#39;s van andere objecten zoeken in [!DNL Trello]

ID&#39;s voor toetsenbord, lijst en opmerking kunnen alleen worden verkregen met behulp van triggers. Deze id&#39;s worden niet weergegeven op de [!DNL `trello.com`] -website.
