---
title: Jira-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die gebruikmaken van Jira-software en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
source-git-commit: e65d868dc2165cbe800600f271f6b03d0a906cb4
workflow-type: tm+mt
source-wordcount: '2345'
ht-degree: 0%

---

# Jira-modules

>[!NOTE]
>
>Deze instructies gelden voor de nieuwe versie van de Jira-connector, die alleen Jira heet. Voor instructies over de erfenisJira Cloud en de schakelaars van de Server van Jira, zie [&#x200B; Jira softwaremodules &#x200B;](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die gebruikmaken van Jira en deze koppelen aan meerdere toepassingen en services van derden.

De Jira-connector kan worden gebruikt voor zowel Jira Cloud- als Jira Data Server.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

* Als u Jira-modules wilt gebruiken, moet u een Jira-account hebben.
* U moet toegang hebben tot de Jira Developer Console om een OAuth2-toepassing te maken in Jira.

## Jira verbinden met Workfront Fusion

De procedure voor het maken van een verbinding met Jira is afhankelijk van het feit of u een basisverbinding of een OAuth2-verbinding maakt.

* [Een OAuth2-verbinding met Jira maken](#create-an-oauth2-connection-to-jira)
* [Een basisverbinding met Jira maken](#create-a-basic-connection-to-jira)

### Een OAuth2-verbinding met Jira maken

Als u een OAuth2-verbinding met Jira wilt maken, moet u een toepassing maken in Jira voordat u de verbinding kunt configureren in Fusion.

* [Een OAuth2-toepassing maken in Jira](#create-an-oauth2-application-in-jira)
* [De OAuth2-verbinding in Fusion configureren](#configure-the-oauth2-connection-in-fusion)

#### Een OAuth2-toepassing maken in Jira

>[!IMPORTANT]
>
>U moet toegang hebben tot de Jira Developer Console om een OAuth2-toepassing te maken en configureren voor uw Jira-verbinding.

1. Ga naar [&#x200B; Developer Console van Jira &#x200B;](https://developer.atlassian.com/console.myapps/).
1. In het Mijn gebied van apps, creeer **&#x200B;**, dan uitgezochte **OAuth 2.0 integratie**.
1. Ga een naam voor de integratie in, ga met de ontwikkelaarstermijnen akkoord, en klik **creeer**.

   De toepassing wordt gecreeerd, en u wordt genomen aan het gebied van de toepassingsconfiguratie.
1. Klik **Toestemmingen** in het linkernavigatievenster.
1. In het gebied van Toestemmingen, bepaal de plaats van de **Jira API** lijn.
1. Klik **toevoegen** in Jira API lijn, dan klik **&#x200B;**&#x200B;in de zelfde lijn verdergaan.
1. Schakel het volgende bereik in:

   * Jira-uitgiftegegevens weergeven (`read:jira-work`)
   * Gebruikersprofielen weergeven (`read:jira-user`)
   * Problemen maken en beheren (`write:jira-work`)

1. In de linkernavigatie, klik **Vergunning**.
1. Klik **toevoegen** in de lijn voor de vergunning OAuth 2.0.
1. Op het **Callback URL** gebied, ga één van de volgende URLs in, die op uw het gegevenscentrum van de Fusie van Workfront wordt gebaseerd:

   | Fusion-datacenter | URL voor terugbellen |
   |---|---|
   | VS | `https://app.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | EU | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira2` |

1. In de linkernavigatie, klik **Montages**.
1. (Facultatief) ga een beschrijving in het gebied van de Beschrijving in, en klik **sparen veranderingen** onder dat gebied.
1. Kopieer de client-id en het clientgeheim van het gebied Instellingen naar een beveiligde locatie of laat deze pagina open terwijl u de verbinding configureert in Fusion.
1. Ga aan [&#x200B; verder vormen de verbinding OAutt2 in Fusion &#x200B;](#configure-the-oauth2-connection-in-fusion)

#### De OAuth2-verbinding in Fusion configureren

1. In om het even welke module van Jira, voegt de klik **naast het gebied van de Verbinding toe.**
1. Configureer de volgende velden:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Verbindingstype</p> </td> 
      <td> <p>Selecteer <b> OAuth 2 </b>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Verbindingsnaam</p> </td> 
      <td> <p>Voer een naam in voor de nieuwe verbinding.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">Service-URL</td>
      <td>Voer de URL van uw Jira-instantie in. Dit is de URL die u gebruikt om toegang te krijgen tot Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira-accounttype</td>
       <td>Selecteer of u verbinding maakt met Jira Cloud of Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">Client-id</td> 
      <td> <p>Ga identiteitskaart van de Cliënt van de toepassing van Jira in u in <a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override=""> creeerde tot een toepassing OAuth2 in Jira </a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Clientgeheim</td> 
      <td> <p>Ga het Geheim van de Cliënt van de toepassing van Jira in u in <a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override=""> creeerde tot een toepassing OAuth2 in Jira </a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Extra bereik</td> 
      <td>Voer eventueel extra bereik in dat u aan deze verbinding wilt toevoegen.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-versie</td> 
      <td>Selecteer de Jira API-versie waarmee u verbinding wilt maken.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

### Een basisverbinding met Jira maken

Het maken van een basisverbinding met Jira hangt af van het feit of u een verbinding met Jira Cloud of Jira Data Center maakt.

* [Een basisverbinding met Jira Cloud maken](#create-a-basic-connection-to-jira-cloud)
* [Een basisverbinding maken met Jira Data Center](#create-a-basic-connection-to-jira-data-center)

#### Een basisverbinding met Jira Cloud maken

>[!IMPORTANT]
>
> Als u een basisverbinding met Jira Cloud wilt maken, hebt u een Jira API-token nodig.
>Voor instructies bij het verwerven van een teken van Jira API, zie [&#x200B; API tokens voor uw Atlassian rekening &#x200B;](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account) in de Atlassiaanse documentatie beheren.


1. In om het even welke module van Jira, voegt de klik **naast het gebied van de Verbinding toe.**
1. Configureer de volgende velden:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Verbindingstype</p> </td> 
      <td> <p>Selecteer of u een basisverbinding of een OAuth 2-verbinding maakt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Verbindingsnaam</p> </td> 
      <td> <p>Voer een naam in voor de nieuwe verbinding.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">Service-URL</td>
      <td>Voer de URL van uw Jira-instantie in. Dit is de URL die u gebruikt om toegang te krijgen tot Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira-accounttype</td>
       <td>Selecteer of u verbinding maakt met Jira Cloud of Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">E-mail</td> 
      <td>Voer uw e-mailadres in.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-token</td> 
      <td>Voer uw API-token in.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-versie</td> 
      <td>Selecteer de Jira API-versie waarmee u verbinding wilt maken.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

#### Een basisverbinding maken met Jira Data Center

>[!IMPORTANT]
>
> Om een basisverbinding aan het Centrum van Gegevens van Jira tot stand te brengen, moet u een persoonlijk toegangstoken van Jira (PAT) hebben.
>Voor instructies bij het verwerven van een persoonlijk toegangstoken van Jira, zie [&#x200B; API tokens voor uw Atlassian rekening &#x200B;](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) in de Atlassiaanse documentatie beheren.
>Voor overwegingen wanneer het creëren van het KLOPJE, zie [&#x200B; uw KLOPJE &#x200B;](#configure-your-pat) in dit artikel vormen.

1. In om het even welke module van Jira, voegt de klik **naast het gebied van de Verbinding toe.**
1. Configureer de volgende velden:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Verbindingstype</p> </td> 
      <td> <p>Selecteer of u een basisverbinding of een OAuth 2-verbinding maakt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Verbindingsnaam</p> </td> 
      <td> <p>Voer een naam in voor de nieuwe verbinding.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">Service-URL</td>
      <td>Voer de URL van uw Jira-instantie in. Dit is de URL die u gebruikt om toegang te krijgen tot Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Jira-accounttype</td>
       <td>Selecteer of u verbinding maakt met Jira Cloud of Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">PAT (Persoonlijk toegangstoken)</td> 
      <td>Voer uw persoonlijke toegangstoken voor Jira in.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API-versie</td> 
      <td>Selecteer de Jira API-versie waarmee u verbinding wilt maken.</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

##### Uw PAT configureren

Om een basisverbinding aan het Centrum van Gegevens van Jira tot stand te brengen, moet u een persoonlijk toegangstoken van Jira (PAT) hebben.

Voor instructies bij het verwerven van een persoonlijk toegangstoken van Jira, zie [&#x200B; API tokens voor uw Atlassian rekening &#x200B;](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) in de Atlassiaanse documentatie beheren.

Mogelijk hebt u de volgende informatie nodig wanneer u uw PAT configureert

* URL&#39;s omleiden

  | Fusion-datacenter | URL omleiden |
  |---|---|
  | VS | `https://app.workfrontfusion.com/oauth/cb/workfront-jira` |
  | EU | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira` |

* Bestandsconfiguraties

Als u een PAT wilt gebruiken, moet u het volgende inschakelen in de bestanden `jira/bin/WEB-INF/classes` in het bestand `jira-config.properties` :

* `jira.rest.auth.allow.basic = true`
* `jira.rest.csrf.disabled = true`

Als dit bestand niet bestaat, moet u het maken.

## Jira-modules en hun velden

Wanneer u Jira-modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er aanvullende Jira-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

#### Controleren op records

Deze triggermodule start een scenario wanneer een record wordt toegevoegd, bijgewerkt of verwijderd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhaak</td> 
   <td> <p>Selecteer de webhaak die u wilt gebruiken om te controleren op records of maak een nieuwe webhaak. </p> <p>Een nieuwe webhaak maken:</p> 
    <ol> 
     <li>Klik <strong> toevoegen </strong></li> 
     <li>Voer een naam in voor de webhaak.</li> 
     <li> Selecteer de verbinding die u voor uw webhaak wilt gebruiken. <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </li> 
     <li> <p>Selecteer het recordtype waarop u de software wilt letten:</p> 
      <ul> 
       <li>Probleem</li> 
       <li>Opmerking </li> 
       <li>Worklog </li> 
       <li>Project </li> 
       <li>Sprint</li> 
       <li>Bijlage </li> 
      </ul> </li> 
     <li>Selecteer een of meer gebeurtenistypen die dit scenario activeren.</li> 
     <li>Voer een Jira Query Language-filter in voor deze module.<p>Voor meer informatie over JQL, zie <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers."> JQL </a> bij de Atlassiaanse hulpplaats. </p></li>
     <li>Klik <b> sparen </b> om webhaak te bewaren. 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [Uitgave toevoegen aan sprint](#add-issue-to-sprint)
* [Een record maken](#create-a-record)
* [Aangepaste API-aanroep](#custom-api-call)
* [Een record verwijderen](#delete-a-record)
* [Een bijlage downloaden](#download-an-attachment)
* [Een record lezen](#read-a-record)
* [Een record bijwerken](#update-a-record)

#### Uitgave toevoegen aan sprint

Deze actiemodule voegt een of meer uitgaven aan een sprint toe.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Afdruk-id</td> 
   <td>Voer de Sprint-id in van de sprint waaraan u een uitgave wilt toevoegen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Uitgave-id of -sleutels</td> 
   <td>Voor elke kwestie of sleutel die u aan sprint wilt toevoegen, <b> toevoegen punt </b> en gaat uitgeeft identiteitskaart of sleutel in. U kunt maximaal 50 invoeren in één module.</td> 
  </tr> 
 </tbody> 
</table>

#### Een record maken

Deze actiemodule maakt een nieuwe record in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer het type record dat de module moet maken.</p> 
    <ul> 
     <li>Bijlage</li> 
     <li>Opmerking</li> 
     <li>Probleem</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Worklog</li> 
     <li>Gebruiker</li> 
     <li>Raad</li> 
     <li>Categorie</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Overige velden</td> 
   <td> Vul de andere velden in. De velden zijn afhankelijk van het geselecteerde recordtype beschikbaar. </td> 
  </tr> 
 </tbody> 
</table>

#### Aangepaste API-aanroep

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de Jira API maken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Een pad invoeren ten opzichte van<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Methode</td> 
   td&gt; <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kopteksten</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tekenreeks query</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lichaam</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### Een record verwijderen

Deze actiemodule verwijdert de opgegeven record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer het type record dat de module moet verwijderen. </p> 
    <ul> 
     <li>Opmerking</li> 
     <li>Probleem</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Worklog</li> 
     <li>Bijlage</li> 
     <li>Raad</li> 
     <li>Categorie</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Type record)ID</td> 
   <td>Voer de id of sleutel in van de record die u wilt verwijderen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Een bijlage downloaden

Deze actiemodule downloadt de opgegeven bijlage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>Voer de id in van de bijlage die u wilt downloaden of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### Een record lezen

Deze actiemodule leest gegevens uit de opgegeven record in Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer het type Jira-record dat de module moet lezen.</p> 
    <ul> 
     <li>Bijlage</li> 
     <li>Opmerking</li> 
     <li>Probleem</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Worklog</li> 
     <li>Gebruiker</li> 
     <li>Raad</li> 
     <li>Categorie</li> 
     <li>Filter</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Uitvoer</td> 
   <td>Selecteer de uitvoer die u wilt ontvangen. Uitvoeropties zijn beschikbaar op basis van het type record dat is geselecteerd in het veld Recordtype.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Type record)-id</td> 
   <td> <p>Voer de unieke Jira-id in of wijs deze toe aan de record die u wilt lezen in de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een record bijwerken

Deze actiemodule werkt een bestaand record bij, zoals een uitgave of project.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer het type record dat de module moet bijwerken. Wanneer u een recordtype selecteert, worden andere velden die specifiek zijn voor dat recordtype, weergegeven in de module.</p> 
    <ul> 
     <li>Opmerking</li> 
     <li>Probleem</li> 
     <li>Project</li> 
     <li>Sprint </li> 
     <li>Overgangskwestie</li> 
     <li>Categorie </li> 
     <li>Filter </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID of sleutel</td> 
   <td>Voer de id of sleutel in van de record die u wilt bijwerken.</td> 
  <tr> 
   <td role="rowheader">Overige velden</td> 
   <td> Vul de andere velden in. De velden zijn afhankelijk van het geselecteerde recordtype beschikbaar. </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

>[!IMPORTANT]
>
>De zoekmodule die door de verouderde Jira-connector wordt gebruikt, kan de volgende fout opleveren:
>
>`[410] The requested API has been removed. Please migrate to the /rest/api/3/search/jql API. A full migration guideline is available at https://developer.atlassian.com/changelog/#CHANGE-2046`
>
>Dit is te wijten aan een afkeer aan de zijde van Jira.
>
>Als deze fout optreedt, kunt u de zoekmodule van de verouderde Jira-connector vervangen door de zoekmodule van de nieuwe connector. Met de nieuwe connector kunt u de gebruikte API-versie selecteren. Zorg ervoor dat u V3 selecteert wanneer u de verbinding maakt.
>
> ![&#x200B; API versieoptie in nieuwe schakelaar van Jira &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/jira-version-option.png)
>
>Let op:
>
>* Dit heeft alleen invloed op de module Zoeken. Op dit moment worden andere Jira API-eindpunten die door de Fusion-connector worden gebruikt, niet beïnvloed door deze afleiding.
>
>* Geografische rollout kan inconsistenties veroorzaken. Atlassian voert deze verandering regionaal uit, wat betekent sommige instanties van de Wolk van Jira nog kunnen oudere eindpunten tijdelijk steunen. Dit kan leiden tot inconsequent gedrag in verschillende omgevingen.

#### Zoeken naar records

Deze zoekmodule zoekt naar records in een object in Jira die overeenkomen met de zoekquery die u opgeeft.

U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw rekening van Jira aan de Fusie van Workfront, zie <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override=""> Verbinding Jira aan de Fusie van Workfront </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Recordtype</td> 
   <td> <p>Selecteer het type record waarnaar de module moet zoeken. Wanneer u een recordtype selecteert, worden andere velden die specifiek zijn voor dat recordtype, weergegeven in de module.</p> 
    <ul> 
     <li>Probleem</li> 
     <li>Project</li> 
     <li>Gebruiker</li> 
     <li>Sprint</li> 
     <li>Raad</li> 
     <li>Worklog</li> 
     <li>Opmerking</li> 
     <li>Overgangsprobleem</li> 
     <li>Categorie</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>Max. resultaten</p> </td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugwinnen.</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Verschuiven</td> 
    <td> Voer de id in of wijs de id toe van het eerste item waarvoor u details wilt ophalen. Dit is een manier om de records te pagineren. Als u het 5000ste punt als compensatie ingaat, zou de module punten 5000-9999 terugkeren.</td> 
   </tr>
  <tr> 
   <td role="rowheader">Overige velden</td> 
   <td> Vul de andere velden in. De velden zijn afhankelijk van het geselecteerde recordtype beschikbaar. </td> 
  </tr> 
 </tbody> 
</table>
