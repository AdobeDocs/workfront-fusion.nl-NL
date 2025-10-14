---
title: Microsoft Teams-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Teams gebruiken en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
source-git-commit: f5b49cca308fad01167aed27e4716a3d630cb026
workflow-type: tm+mt
source-wordcount: '3629'
ht-degree: 0%

---

# Microsoft Teams-modules

<!-- ADD REDIRECTS -->

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Microsoft Teams gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

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

Als u Microsoft Teams-modules wilt gebruiken, moet u een Microsoft Teams-account hebben die de handeling in de module kan uitvoeren.

## De Microsoft Teams-service verbinden met Workfront Fusion

Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie [&#x200B; een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies &#x200B;](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
>
>Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.

## Microsoft Teams-modules en hun velden

Wanneer u Microsoft Teams-modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er aanvullende Microsoft Teams-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Team](#team)
* [Kanaal](#channel)
* [Bericht](#message)
* [Lid](#member)
* [Online vergadering](#online-meeting)
* [Overige](#other)

### Team

* [Een team maken van een groep](#create-a-team-from-a-group)
* [Een Office 365-groep maken](#create-an-office-365-group)
* [Een team of groep verwijderen](#delete-a-team-or-group)
* [Een team ophalen](#get-a-team)
* [Alle teams en groepen weergeven](#list-all-teams-and-groups)
* [Deelnemers aan teams tonen](#list-joined-teams)
* [Een team bijwerken](#update-a-team)
* [Controleteams](#watch-teams)

#### Een team maken van een groep

Deze actiemodule leidt tot een team van een bestaande Microsoft Office 365 groep en vormt montages voor het nieuwe team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groep-id</td> 
   <td> <p>Selecteer de groep waarvan u een team wilt maken.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Leden toestaan kanalen te maken en bij te werken</td> 
   <td>Selecteer of u leden wilt toestaan om kanalen tot stand te brengen en bij te werken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Leden toestaan kanalen te verwijderen</td> 
   <td>Selecteer of u leden wilt toestaan om kanalen te schrappen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Leden toestaan apps toe te voegen en te verwijderen</td> 
   <td>Selecteer of u leden wilt toestaan apps toe te voegen en te verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Leden toestaan tabbladen te maken, bij te werken en te verwijderen</td> 
   <td>Selecteer of u leden wilt toestaan om lusjes tot stand te brengen, bij te werken en te verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Leden toestaan connectors te maken en te verwijderen</td> 
   <td>Selecteer of u leden wilt toestaan om schakelaars tot stand te brengen en te verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruikers toestaan hun berichten te bewerken</td> 
   <td>Selecteer of u gebruikers wilt toestaan om hun berichten uit te geven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebruikers toestaan hun berichten te verwijderen</td> 
   <td>Selecteer of u gebruikers wilt toestaan om hun berichten te schrappen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eigenaars toestaan om berichten te verwijderen</td> 
   <td>Selecteer of u eigenaars wilt toestaan om het even welk bericht te schrappen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">@teamopmerkingen toestaan</td> 
   <td>Selecteer of u @team-aantekeningen wilt toestaan.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">@channel-opmerkingen toestaan</td> 
   <td>Selecteer of u @channel-aanhalingstekens wilt toestaan.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gidrukken toestaan</td> 
   <td>Selecteer of u het gebruik van Giphy voor dit Team wilt toestaan.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Toestaan dat stickers en memen</td> 
   <td>Selecteer of u gebruikers wilt toestaan om stickers en memen op te nemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aangepaste memes toestaan</td> 
   <td>Selecteer of u gebruikers wilt toestaan om douanememen op te nemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gasten kanalen maken en bijwerken</td> 
   <td>Selecteer of u gasten wilt toestaan om kanalen te maken en bij te werken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gasten toestaan kanalen te verwijderen</td> 
   <td>Selecteer of u gasten wilt toestaan om kanalen te verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

#### Een Office 365-groep maken

Deze actiemodule leidt tot een groep in Microsoft Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Weergavenaam</td> 
   <td> <p>Ga of kaart de naam in die deze groep in zijn adresboek toont.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias voor groep</td> 
   <td>Voer de e-mailalias voor deze groep in of wijs deze toe. U kunt kleine letters, cijfers, en onderstrepingstekens omvatten. Voor het groepstype Office 365 is dit de e-mailalias van de groep ([Alias]@[Uw domein].onmicrosoft.com). Voor het type van de Groep van de Veiligheid, functioneert de alias als bijnaam.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groepstype</td> 
   <td>Selecteer of u een Bureau 365 groep of een groep van de Veiligheid creeert.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschrijving</td> 
   <td>Voer een beschrijving voor deze groep in of wijs een beschrijving toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beveiliging ingeschakeld</td> 
   <td>Schakel deze optie in als u de beveiliging van de groep wilt inschakelen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Eigenaars</td> 
   <td>Selecteer de eigenaars voor deze groep.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Leden</td> 
   <td>Selecteer de leden voor deze groep.</td> 
  </tr> 
 </tbody> 
</table>

#### Een team of groep verwijderen

Deze actiemodule verwijdert het opgegeven team of de opgegeven groep.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groep-id</td> 
   <td> <p>Voer de id in van de groep die u wilt verwijderen of wijs deze toe.</p> 
   </tr> 
 </tbody> 
</table>

#### Team ophalen

Deze module wint eigenschappen en verhoudingen voor het gespecificeerde team van Microsoft of de groep van Office 365 terug.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groep-id</td> 
   <td> <p>Voer de id in van de groep waarvoor u details wilt ophalen of wijs deze toe.</p> 
   </tr> 
 </tbody> 
</table>

#### Alle teams en groepen weergeven

Deze module maakt een lijst van alle teams in Microsoft Teams en Bureau 365 groepen verbonden aan de organisatie. U kunt filteren om alleen resultaten te retourneren die aan door u opgegeven criteria voldoen.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>U kunt een filter instellen om alleen teams en groepen te retourneren die voldoen aan de criteria die u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN of OF regels toe te voegen.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximum aantal geretourneerde resultaten</td> 
   <td>Stel het maximumaantal teams of groepen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>


#### Teams toevoegen aan lijst

Deze actiemodule maakt een lijst van de teams die bij door de gebruiker verbonden aan de verbinding zijn aangesloten die in deze module wordt gebruikt.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td>Maximum aantal geretourneerde resultaten</td> 
   <td>Stel het maximumaantal teams of groepen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>

#### Een team bijwerken

Deze actiemodule werkt de eigenschappen van de gespecificeerde teams in Microsoft Teams of Bureau 365 groep bij.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Weergavenaam</td> 
   <td> <p>Ga of kaart de naam in die deze groep in zijn adresboek toont.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias voor groep</td> 
   <td>Voer de e-mailalias voor deze groep in of wijs deze toe. U kunt kleine letters, cijfers, en onderstrepingstekens omvatten. Voor het groepstype Office 365 is dit de e-mailalias van de groep ([Alias]@[Uw domein].onmicrosoft.com). Voor het groepstype van de Veiligheid, functioneert de alias als bijnaam.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beschrijving</td> 
   <td>Voer een beschrijving voor deze groep in of wijs een beschrijving toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Beveiliging ingeschakeld</td> 
   <td>Schakel deze optie in als u de beveiliging van de groep wilt inschakelen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Zichtbaarheid</td> 
   <td>Specificeer de zichtbaarheid van de Office 365-groep.</td> 
  </tr> 
 </tbody> 
</table>

#### Controleteams

Deze trekkermodule begint een scenario wanneer een team wordt gecreeerd.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>U kunt een filter instellen om alleen te controleren op teams en groepen die voldoen aan de criteria die u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN of OF regels toe te voegen.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximum aantal geretourneerde resultaten</td> 
   <td>Stel het maximumaantal teams of groepen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>

### Kanaal

* [Een kanaal maken](#create-a-channel)
* [Een kanaal verwijderen](#delete-a-channel)
* [Een kanaal ophalen](#get-a-channel)
* [Kanalen weergeven](#list-channels)
* [Een kanaal bijwerken](#update-a-channel)

#### Een kanaal maken

Deze actiemodule leidt tot een nieuw kanaal voor het gespecificeerde team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Selecteer het team in Microsoft Teams waarvoor u een kanaal wilt maken.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaalnaam</td> 
   <td>Voer een naam voor het nieuwe kanaal in of wijs een naam toe.</td> 
  </tr> 
  <tr> 
   <td>Description</td> 
   <td>Voer een beschrijving voor het nieuwe kanaal in of wijs een beschrijving toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Een kanaal verwijderen

Deze actiemodule verwijdert het opgegeven kanaal uit een Microsoft-team.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Voer de id in van het team in Microsoft Teams waaruit u een kanaal wilt verwijderen of wijs deze toe.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaal-id</td> 
   <td>Voer de id in van het kanaal dat u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
  </tbody> 
</table>

#### Een kanaal ophalen

Deze module wint de eigenschappen en de verhoudingen van een kanaal terug.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Ga of kaart identiteitskaart van het team in Microsoft Teams in die het kanaal bezit u details voor wilt terugwinnen.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaal-id</td> 
   <td>Voer de id in van het kanaal waarvoor u details wilt ophalen of wijs deze toe.</td> 
  </tr> 
  </tbody> 
</table>

#### Kanalen weergeven

Deze modules maakt een lijst van kanalen die door het gespecificeerde team in de Teams van Microsoft worden bezeten.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Selecteer het team in Microsoft Teams waarvoor u kanalen wilt weergeven.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximum aantal geretourneerde resultaten</td> 
   <td>Stel het maximumaantal kanalen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
  </tbody> 
</table>

#### Een kanaal bijwerken

Deze actiemodule werkt de beschrijving van het opgegeven kanaal bij.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Selecteer het team in Microsoft Teams dat eigenaar is van het kanaal dat u wilt bijwerken.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaalnaam</td> 
   <td>Voer de naam in van het kanaal dat u wilt bijwerken of wijs de naam ervan toe.</td> 
  </tr> 
  <tr> 
   <td>Beschrijving</td> 
   <td>Voer de nieuwe beschrijving voor het kanaal in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

### Bericht

* [Een kanaalbericht beantwoorden](#reply-to-a-channel-message)
* [Een bericht verzenden](#send-a-message)
* [Controleren op berichten](#watch-messages)
* [Nieuwe reacties bekijken](#watch-new-replies)

#### Een kanaalbericht beantwoorden

Deze actiemodule leidt tot een antwoord op een bericht in het gespecificeerde kanaal.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Selecteer het team in Microsoft Teams dat eigenaar is van het kanaal dat het bericht bevat waarop u wilt reageren.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaal-id</td> 
   <td>Selecteer het kanaal dat het bericht bevat waarop u wilt reageren.</td> 
  </tr> 
  <tr> 
   <td>Bericht-id</td> 
   <td>Ga of kaart identiteitskaart van het bericht in u wilt antwoorden aan.</td> 
  </tr> 
  <tr> 
   <td>Inhoudstype</td> 
   <td>Selecteer of u het bericht in normale tekst of in HTML-indeling wilt verzenden.</td> 
  </tr> 
  <tr> 
   <td>Reactiebericht</td> 
   <td>Voer de hoofdtekst in van het antwoordbericht dat u wilt verzenden of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Een bericht verzenden

Deze actiemodule verzendt een bericht naar het kanaal van een team of naar een praatje.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Berichttype/td&gt; 
   <td> <p>Selecteer of u een kanaalbericht of een praatjebericht verzendt.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Als u een bericht naar een kanaal verzendt, ga of kaart identiteitskaart van het team in Microsoft Teams in die het kanaal bezit dat u een bericht naar wilt verzenden.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaal-id</td> 
   <td>Als u een bericht naar een kanaal verzendt, ga identiteitskaart van het kanaal in of kaart die u een bericht naar wilt verzenden.</td> 
  </tr> 
  <tr> 
   <td>Een nieuwe chat maken</td> 
   <td>Als u een praatjebericht verzendt, selecteer of u een nieuwe praatje wilt tot stand brengen.
   <ul><li><b>Ja</b><p>Selecteer of u een één-op-één praatje of een groepspraatje wilt, en selecteer het lid dat u in de praatje wilt omvatten. U moet de gebruiker selecteren verbonden aan de verbinding deze module gebruikt, en een één-op-één praatje moet slechts die gebruiker en één andere gebruiker bevatten.</p><p>Als u een groepspraatje creeert, kunt u een onderwerp op het gebied van het Onderwerp plaatsen.</p>
   <li><b>Nee</b><p>Ga of kaart identiteitskaart van het team in dat het kanaal bezit u een bericht naar wilt verzenden, dan ingaan of identiteitskaart van het kanaal in kaart brengen.</td> 
  </tr> 
  <tr> 
   <td>Bericht</td> 
   <td>Ga of kaart het lichaam van het bericht in u wilt verzenden.</td> 
  </tr> 
  <tr> 
   <td>Inhoudstype</td> 
   <td>Selecteer of u het bericht in normale tekst of in HTML-indeling wilt verzenden.</td> 
  </tr> 
 </tbody> 
</table>

#### Controleren op berichten

Deze trekkermodule begint een scenario wanneer een bericht wordt verzonden naar het kanaal van een team of naar een praatje.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type berichten dat moet worden gecontroleerd</td> 
   <td> <p>Selecteer of u kanaalberichten of chatberichten wilt bekijken.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Als u naar kanaalberichten kijkt, selecteert u het team in Microsoft Teams dat eigenaar is van het kanaal dat u voor berichten controleert.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaal-id</td> 
   <td>Als u naar kanaalberichten kijkt, selecteer het kanaal dat u op berichten wilt letten.</td> 
  </tr> 
  <tr> 
   <td>Chat-id</td> 
   <td>Als u chatberichten bekijkt, selecteert u de chat die u voor berichten wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td>Maximum aantal geretourneerde berichten</td> 
   <td>Stel het maximumaantal berichten in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>

#### Nieuwe reacties bekijken

Deze trekkermodule begint een scenario wanneer een nieuw antwoord door het gespecificeerde bericht wordt ontvangen.

Deze module is niet beschikbaar voor persoonlijke accounts.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Team-id</td> 
   <td> <p>Selecteer het team in Microsoft Teams dat eigenaar is van het kanaal dat u controleert op antwoorden.</p> </td> 
   </tr> 
  <tr> 
   <td>Kanaal-id</td> 
   <td>Selecteer het kanaal dat u voor reacties wilt letten.</td> 
  </tr> 
  <tr> 
   <td>Bericht-id</td> 
   <td>Selecteer de chat waar u op wilt letten voor reacties.</td> 
  </tr> 
  <tr> 
   <td>Maximum aantal geretourneerde antwoorden</td> 
   <td>Stel het maximumaantal antwoorden in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>

### Lid

* [Een lid toevoegen](#add-a-member)
* [Een lid toevoegen aan een groep](#add-a-member-to-a-group)

#### Een lid toevoegen

In deze actiemodule wordt een lid toegevoegd aan Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Lidnaam</td> 
   <td> <p>Voer de naam in of wijs de naam toe van het lid dat u aan Microsoft Teams wilt toevoegen.</p> </td> 
   </tr> 
  <tr> 
   <td>Wachtwoord</td> 
   <td>Ga of kaart het wachtwoord voor het lid in.</td> 
  </tr> 
 </tbody> 
</table>

#### Een lid toevoegen aan een groep

Deze actiemodule voegt een lid aan een Bureau 365 Groep toe.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Groep-id</td> 
   <td> <p>Selecteer de groep waaraan u een lid wilt toevoegen.</p> </td> 
   </tr> 
  <tr> 
   <td>Lid-id</td> 
   <td>Selecteer het lid dat u aan de groep wilt toevoegen.</td> 
  </tr> 
 </tbody> 
</table>

### Online vergadering

* [Een online vergadering maken](#create-an-online-meeting)
* [Een online vergadering verwijderen](#delete-an-online-meeting)
* [Een online vergadering ophalen](#get-an-online-meeting)
* [Een online vergadering bijwerken](#update-an-online-meeting)

#### Een online vergadering maken

Deze actiemodule maakt een zelfstandige vergadering die niet is gekoppeld aan een gebeurtenis in de agenda van de gebruiker. Deze vergadering wordt niet weergegeven in de agenda van de gebruiker.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Onderwerp</td> 
   <td>Ga of kaart een onderwerp voor deze vergadering in.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Begindatum en -tijd</td> 
   <td>Ga of kaart de datum en de tijd in dat u de vergadering wilt beginnen. Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Einddatum en -tijd</td> 
   <td>Ga of kaart de datum en de tijd in dat u de vergadering wilt beëindigen. Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Toegestane presentatoren</td> 
   <td>Selecteer de groep die in deze vergadering mag worden weergegeven.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Aanwezigen</td> 
   <td>Voor elke aanwezige die u aan de vergadering wilt toevoegen, klik <b> toevoegen punt </b> en selecteer de naam en de rol van de aanwezige.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Deelnemers toestaan hun camera's in te schakelen</td> 
   <td>Selecteer of deelnemers hun eigen camera's mogen inschakelen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Deelnemers toestaan hun microfoons in te schakelen</td> 
   <td>Selecteer of deelnemers hun eigen microfoons mogen inschakelen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Vergaderingchat toestaan</td> 
   <td>Selecteer of u wilt dat de vergaderingchat wordt toegelaten, onbruikbaar gemaakt, of beperkt tot de duur van de vergaderingsvraag</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teamreacties toestaan</td> 
   <td>Selecteer of u de reacties van Teams voor deze vergadering wilt toelaten.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Thread-id</td> 
   <td>Ga of kaart identiteitskaart van een draad in verbonden aan deze vergadering.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Bericht-id</td> 
   <td>Voer de id in of wijs deze toe aan een bericht dat aan deze vergadering is gekoppeld.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Bericht-ID antwoordketen</td> 
   <td>Ga of kaart identiteitskaart van de antwoordketen verbonden aan deze vergadering in.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Ingang en uitgang aankondigen</td> 
   <td>Selecteer of u wilt dat de vergadering aankondigt wanneer de aanwezigen binnenkomen of weggaan.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Toepassingsgebied</td> 
   <td>Selecteer de groep aanwezigen die de wachttijd in de lobby kan omzeilen. Deze deelnemers nemen rechtstreeks deel aan de vergadering.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Inbelgebruikers toestaan lobby te omzeilen</td> 
   <td>Selecteer of inbelgebruikers de lobby mogen omzeilen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Automatisch opnemen</td> 
   <td>Selecteer of u de vergadering automatisch wilt opnemen.</td> 
   </tr> 
   </tbody> 
</table>

#### Een online vergadering verwijderen

In deze actiemodule wordt de onlinevergadering met de opgegeven id verwijderd.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Vergadering-id</td> 
   <td> <p>Ga of kaart identiteitskaart van de vergadering in die u wilt schrappen.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Een online vergadering ophalen

Deze actiemodule wint details van de online vergadering met gespecificeerde identiteitskaart terug

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Vergadering-id</td> 
   <td> <p>Ga of kaart identiteitskaart van de vergadering in die u details voor wilt terugwinnen.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Een online vergadering bijwerken

Deze actiemodule werkt de online vergadering bij met de opgegeven id.



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Vergadering-id</td> 
   <td>Ga of kaart identiteitskaart van de vergadering in die u wilt bijwerken.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Onderwerp</td> 
   <td>Ga of kaart een onderwerp voor deze vergadering in.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Begindatum en -tijd</td> 
   <td>Ga of kaart de datum en de tijd in dat u de vergadering wilt beginnen. Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Einddatum en -tijd</td> 
   <td>Ga of kaart de datum en de tijd in dat u de vergadering wilt beëindigen. Voor een lijst van gesteunde datumformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Toegestane presentatoren</td> 
   <td>Selecteer de groep die in deze vergadering mag worden weergegeven.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Aanwezigen</td> 
   <td>Voor elke aanwezige die u aan de vergadering wilt toevoegen, klik <b> toevoegen punt </b> en selecteer de naam en de rol van de aanwezige.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Deelnemers toestaan hun camera's in te schakelen</td> 
   <td>Selecteer of deelnemers hun eigen camera's mogen inschakelen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Deelnemers toestaan hun microfoons in te schakelen</td> 
   <td>Selecteer of deelnemers hun eigen microfoons mogen inschakelen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Vergaderingchat toestaan</td> 
   <td>Selecteer of u wilt dat de vergaderingchat wordt toegelaten, onbruikbaar gemaakt, of beperkt tot de duur van de vergaderingsvraag</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Teamreacties toestaan</td> 
   <td>Selecteer of u de reacties van Teams voor deze vergadering wilt toelaten.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Thread-id</td> 
   <td>Ga of kaart identiteitskaart van een draad in verbonden aan deze vergadering.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Bericht-id</td> 
   <td>Voer de id in of wijs deze toe aan een bericht dat aan deze vergadering is gekoppeld.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Bericht-ID antwoordketen</td> 
   <td>Ga of kaart identiteitskaart van de antwoordketen verbonden aan deze vergadering in.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Ingang en uitgang aankondigen</td> 
   <td>Selecteer of u wilt dat de vergadering aankondigt wanneer de aanwezigen binnenkomen of weggaan.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Toepassingsgebied</td> 
   <td>Selecteer de groep aanwezigen die de wachttijd in de lobby kan omzeilen. Deze deelnemers nemen rechtstreeks deel aan de vergadering.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Inbelgebruikers toestaan lobby te omzeilen</td> 
   <td>Selecteer of inbelgebruikers de lobby mogen omzeilen.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Automatisch opnemen</td> 
   <td>Selecteer of u de vergadering automatisch wilt opnemen.</td> 
   </tr> 
   </tbody> 
</table>

### Overige

* [De aanwezigheid van gebruikers controleren](#check-presence-of-users)
* [Een aangepaste API-aanroep maken](#make-a-custom-api-call)
* [Gebruikers zoeken](#search-users)

#### De aanwezigheid van gebruikers controleren

Deze actiemodules controleren of de geselecteerde gebruikers aanwezig zijn op Microsoft Teams.

Deze module ondersteunt geen persoonlijke accounts.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Gebruikersnamen</td> 
   <td> <p>Selecteer de gebruikers waarvoor u de aanwezigheid wilt controleren.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Een aangepaste API-aanroep maken

Deze actiemodule doet een aangepaste aanvraag voor de Microsoft Teams API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://graph.microsoft.com</code> . Voorbeeld:<code> /v1.0/groups</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
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
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Gebruikers zoeken

Deze module zoekt naar gebruikers die criteria gebruiken u specificeert.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Microsoft Teams aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding creëren - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filter</td> 
   <td> <p>U kunt een filter instellen om alleen gebruikers te retourneren die voldoen aan de criteria die u selecteert.</p> <p>Voer voor elk filter het veld in dat door het filter moet worden geëvalueerd, de operator en de waarde die door het filter moet worden toegestaan. U kunt meer dan één filter gebruiken door EN of OF regels toe te voegen.</p> </td> 
   </tr> 
  <tr> 
   <td>Maximum aantal geretourneerde resultaten</td> 
   <td>Stel het maximumaantal teams of groepen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
 </tbody> 
</table>



