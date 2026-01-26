---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gebruik sjablonen om Adobe Workfront Fusion en Jira te verbinden
description: Gebruik deze sjablonen om workflows tussen Adobe Workfront Fusion en Jira te automatiseren.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ede5c7a75725a6540d6a8ff9cd056e6147d5c55
workflow-type: tm+mt
source-wordcount: '4171'
ht-degree: 0%

---

# Gebruik sjablonen om Adobe Workfront Fusion en Jira te verbinden

Adobe Workfront Fusion biedt sjablonen die algemene workflows tussen Fusion en Jira kunnen automatiseren.

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
   <td role="rowheader">Product</td> 
   <td>
   <p>Workfront: als uw organisatie een Select- of Prime Workfront-pakket heeft dat Workfront Automation and Integration niet bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</p><p>Jira: U moet een licentie hebben voor Jira Cloud</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Configuraties op toegangsniveau</td> 
   <td> <p>Workfront: machtiging om gebruikers, aangepaste formulieren en aangepaste velden te maken.</p> <p>Jira: Machtigingen om gebruikers en aangepaste velden te maken en schermen en webhaken te wijzigen.</td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Vereisten

### Workfront

* Je moet een technische rekening hebben op de Adobe Developer Console.

  Voor informatie en instructies, zie [ Technische rekeningsopstelling ](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup) in de documentatie van Adobe.
* U moet de toestemmingen van de Beheerder van het Systeem op de technische rekening in het gebied van de Profielen van het Product van Adobe Admin Console toepassen.

  Voor informatie en instructies, zie [ systeembeheerders in Workfront met Adobe Admin Console ](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console) creëren

### Jira

Als u (geadviseerde) vergunning OAuth2 voor Jira gebruikt, moet u opstelling een toepassing OAuth2 in [ https://developer.atlassian.com/console ](https://developer.atlassian.com/console). Voor informatie en instructies, zie [ een verbinding OAuth2 aan Jira ](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#create-an-oauth2-connection-to-jira) in de modules van artikelJira creëren.

<!--

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

-->

## Veronderstellingen

Bij deze modules wordt uitgegaan van het volgende:

* Workfront is de bron van de waarheid van het algemene marketingcampagneproject
* Jira wordt gebruikt door technische teams, die een deel van een project uitvoeren dat in Workfront is gestart.
* Niet alle Jira-gebruikers hebben toegang tot Workfront of vice versa.
* Workfront en Jira worden gehost in de cloud.

## Gegevensmodel (veldtoewijzingen)


| Workfront | Jira | Richting | Notities |
|---|---|---|---|
| ObjId | WF-ID * | WF → Jira | Bij Jira Issue Creation |
| Jira Key * | Issue Key | Jira → WF | Bij Jira Issue Creation |
| URL van jira * | - | Jira → WF | Door gebruiker aanklikbare koppeling in SWF naar Jira |
| - | WF-koppeling * | WF → Jira | Door gebruiker aanklikbare koppeling in Jira naar WF |
| Naam | Samenvatting | WF → Jira |  |
| Beschrijving | Beschrijving | WF → Jira |  |
| Status | WF-status | WF → Jira | WF-status |
| Status van jira * | Status | Jira → WF | Jira-status |
| Geplande afsluitdatum | Vervaldatum | WF → Jira | Geplande afsluitdatum |
| Notities | Opmerkingen | WF ↔ Jira | Bidirectionele kopie |
| Document | Bijlage | WF → Jira | Als bijlagen bij het maken van uitgaven en opmerkingen bij nieuwe documenten na het maken. |

\* Deze velden zijn geconfigureerd als onderdeel van deze integratie-instelling. Voor instructies, zie [ eerste vereisten in Workfront, Jira, en de Fusie van Workfront ](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion) vormen.

## Voorwaarden configureren in Workfront, Jira en Workfront Fusion

Als u de Jira-integratiesjablonen wilt gebruiken, moet u de volgende configuraties uitvoeren:

* [Jira configureren](#configure-jira)
* [Workfront configureren](#configure-workfront)
* [Verbindingen configureren in Workfront Fusion](#configure-connections-in-workfront-fusion)

### Jira configureren

Als u deze modules wilt gebruiken, moet u in Jira het volgende maken:

* Een gebruiker voor systeemintegratie
* Drie specifieke aangepaste velden

#### Een gebruiker voor systeemintegratie in Jira maken

1. In Jira, creeer een specifieke gebruiker genoemd de Gebruiker van de Integratie van het Systeem. Deze gebruiker mag alleen worden gebruikt door Workfront Fusion en mag geen menselijke gebruiker vertegenwoordigen. De gebruikersgegevens van deze gebruiker worden gebruikt door Workfront Fusion-verbindingen.

#### De benodigde aangepaste velden maken in Jira

Deze integratie verwacht drie specifieke gebieden in de rekening van Jira het met verbindt. Zonder deze gebieden zal de integratie mislukken

1. In Jira, ga naar **Montages** (tandwielpictogram) en selecteer **Punten van het Werk**.
1. In de linkernavigatie, uitgezochte **gebieden van de Douane**.
1. In de hoger-juiste hoek van het scherm, klik **creeer douanegebied.**
1. Maak de volgende velden:

   | Veldnaam | Veldtype |
   |---|---|
   | WF-id | Tekstveld (één regel) |
   | WF-status | Tekstveld (één regel) |
   | WF-koppeling | URL-veld |

   Raadpleeg de documentatie van Jira over het maken van velden voor informatie over het maken van koppelingen in Jira.
1. Voeg de zojuist gemaakte velden toe aan het scherm dat aan uw Jira-project is gekoppeld.

   Raadpleeg de documentatie van Jira over het instellen van werkitemschermen voor informatie over schermen in Jira.


### Workfront configureren

Als u deze modules wilt gebruiken, moet u het volgende maken in Workfront:

* Een gebruiker voor systeemintegratie
* Een specifiek aangepast formulier

#### Een gebruiker voor systeemintegratie in Workfront maken

1. In Workfront, creeer een gebruiker van de Integratie van het Systeem. Deze gebruiker wordt alleen gebruikt door Workfront Fusion en vertegenwoordigt geen menselijke gebruiker. Taken die aan deze gebruiker zijn toegewezen, activeren het scenario dat Workfront synchroniseert met Jira.

   Voor instructies, zie [ gebruikers ](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users) in de documentatie van Workfront toevoegen.

#### Een aangepast formulier maken in Workfront

1. Maak in Workfront een aangepast formulier.

   Voor instructies, zie [ een douaneformulier ](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form) in de documentatie van Workfront creëren.
1. Noem de vorm &quot;**Velden JIRA**&quot;.
1. Voeg de volgende velden toe aan het aangepaste formulier:

| Veldnaam | Veldtype |
|---|---|
| Jira Key | Tekstveld met één regel |
| Jira URL | Tekstveld met één regel |
| Jira-status | Tekstveld met één regel |

1. Voeg aanvullende velden toe die u wilt toewijzen tussen Jira en Workfront.
1. Sla het aangepaste formulier op.

>[!NOTE]
>
>We raden u aan dit formulier te beperken tot bewerkingen door andere gebruikers. U kunt dit bereiken door ervoor te zorgen dat gebruikers die aan het aangepaste formulier worden toegevoegd, alleen toegang tot de weergave hebben.
>
>Voor instructies, zie [ een douanevorm ](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form) in de documentatie van Workfront delen.

### Verbindingen configureren in Workfront Fusion

U moet de gebruikers van de Integratie van het Systeem in Jira en Workfront hebben gecreeerd alvorens u verbindingen kunt tot stand brengen.

Wanneer het creëren van deze verbindingen, ben zeker om de geloofsbrieven van de gecreeerde gebruikers van de Integratie van het Systeem te gebruiken.

Indien gewenst, kunt u deze verbindingen als deel van het vormen van de malplaatjes tot stand brengen.

* Voor instructies bij het creëren van een verbinding aan Workfront, zie [ Workfront met de Fusie van Workfront ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion) in de modules van artikelWorkfront verbinden.
* Voor instructies bij het creëren van een verbinding aan Jira, zie [ Verbinding Jira aan de Fusie van Workfront ](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) in de modules van de artikelJira Software.


## Scenarios

Acht gebruiksklare sjablonen voor Jira moeten helpen algemene workflows te repliceren en de implementatie te versnellen. De malplaatjes zijn volledig aanpasbaar om aan specifieke bedrijfsbehoeften te voldoen en kunnen worden uitgebreid aangezien de vereisten evolueren.

U hoeft niet alle scenario&#39;s uit te voeren. Voor de minimale implementatie zou scenario 1 nodig zijn, wat zou leiden tot een eenrichtingsintegratie in een JIRA-kwestie vanuit een toewijzing in Workfront.  U kunt de extra scenario&#39;s toevoegen om robuustheid en meer bidirectionele interconnectiviteit tussen Workfront en JIRA toe te voegen.  U kunt ook aanvullende scenario&#39;s maken voor het afhandelen van gevallen zoals projecten voor epische integratie of JIRA-problemen voor Workfront-uitgaven of -taken.

Om het even welk gebruik van deze malplaatjes of uitbreidingen van deze malplaatjes wordt beschouwd als douaneconfiguratie, en wij adviseren gebruikend Adobe Professional Services of een partner van Adobe voor steun en implementatie.

* **[Workfront aan Jira: Creeer JIRA kwestie van de taak van Workfront of geef taak](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)** uit
* [JIRA naar Workfront: JIRA naar Workfront: stuur updates over problemen en opmerkingen terug naar Workfront vanuit Jira](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront naar Jira: Veranderingen in de Workfront-taak naar JIRA-kwestie](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* [Workfront naar Jira: Wijzigingen in Workfront-kwestie naar JIRA-kwestie](#scenario-4-workfront-to-jira-changes-to-workfront-issue-to-jira-issue)
* [Workfront naar Jira: Maak opmerkingen in JIRA wanneer u een nieuwe notitie maakt over Workfront-taak of -uitgave](#scenario-5-workfront-to-jira-create-comment-in-jira-when-new-note-on-workfront-task-or-issue)
* [Workfront naar Jira: Maak in JIRA opmerkingen over verwijderde notitie over Workfront-taak of -uitgave](#scenario-6-workfront-to-jira-create-comment-in-jira-on-deleted-note-on-workfront-task-or-issue)
* [Workfront naar Jira: Opmerking maken in JIRA wanneer nieuw document wordt gemaakt over Workfront-taak of -uitgave](#scenario-7-workfront-to-jira-create-comment-in-jira-when-new-document-on-workfront-task-or-issue)
* [Workfront naar Jira: Maak in JIRA opmerkingen over verwijderd document over Workfront-taak of -uitgave](#scenario-8-workfront-to-jira-create-comment-in-jira-on-deleted-document-on-workfront-task-or-issue)

### Algemene parameters

Wanneer het vormen van deze malplaatjes, gebruik de volgende algemene parameters:

* **JiraBaseURL**: De basisURL voor de instantie van Jira. Voorbeeld: `https://myjira.atlassian.net/`
* **wfBaseURL**: De basis URL voor de instantie van Workfront.  Doorgaans: `https://<domain>.my.workfront.com` waarbij `<domain>` uw specifieke Workfront-domeinnaam is.
* **defaultJIRAReporterID**: Identiteitskaart voor de gebruiker in JIRA die tot kwesties leidt. (Voorbeeld: `557058:5aedf933-2312-40bc-b328-0c21314167f0`)
U kunt deze id op een van de volgende manieren ophalen:
   * Klik op het profiel van de gebruiker in JIRA en controleer de URL in uw browser.
(Voorbeeld `https://myjira.atlassian.net/jira/people/<JiraUserID>`)
   * Voer de volgende API-aanroep uit op uw JIRA-instantie om de id voor de specifieke account in JIRA op te halen:
     `GET /rest/api/3/user/search?query=email@example.com`


### Scenario 1: Workfront naar Jira: Maak een JIRA-uitgave van Workfront-taak of geef een toewijzing uit

Dit scenario leidt tot een kwestie van Jira wanneer een Taak of een Kwestie van Workfront aan de Gebruiker van de Integratie van het Systeem wordt toegewezen. Het scenario vult de Summiere, Beschrijving, Vervaldatum, Status WF en identiteitskaart WF in gebieden. Nadat de uitgave is gemaakt, uploadt dit scenario ook de lijst met bijlagen en de geschiedenis van notities die betrekking hebben op de oorspronkelijke taak of uitgave in Workfront.

Als een Workfront-taak is toegewezen, is het probleem in Jira een taak. Als er een Workfront-probleem is toegewezen, is het Jira-probleem een probleem.

+++**breid zich aan meningsinstructies voor het vormen Scenario 1 :Workfront aan Jira uit: Creeer JIRA kwestie van de taak van Workfront of geef taak** uit

#### De triggermodule configureren

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Workfront aan Jira: Creeer JIRA kwestie van de taak van Workfront of geef taak** malplaatje uit.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer de verbinding van Workfront die u in [ creeerde vormt verbindingen in de Fusie van Workfront ](#configure-connections-in-workfront-fusion).
1. Op het **gebied van het Type van Verslag**, uitgezochte `Assignment`.
1. Op het **gebied van de Staat**, uitgezochte `New state`.
1. Vorm de filter met de volgende verrichtingen, gebruikend **en** optie:

   | Veld | Operator | Waarde |
   |---|---|---|
   | assignedToID | Gelijk | (Voer de Workfront-id van de gebruiker System Integration in) |
   | TaskID | Exists |  |
   | projectID | Gelijk | (Voer de id in van het project of de projecten die de webhaak moet controleren) |

1. Laat de **updates van de Uitsluiting toe die door deze verbinding** optie worden gemaakt.
1. Op het **gebied van de Oorsprong van het Verslag**, uitgezochte Nieuwe slechts Verslag.
1. Klik **sparen** om Webhaak te bewaren, dan klik O.K. **** om de trekkermodule te bewaren.
1. Ga aan [ Connect malplaatjemodules aan Workfront en Jira ](#connect-template-modules-to-workfront-and-jira) verder

#### Sjabloonmodules verbinden met Workfront en Jira

1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die u in [ creeerde vormt verbindingen in de Fusie van Workfront ](#configure-connections-in-workfront-fusion), dan klik O.K. **** om de verbinding aan die module te bewaren.
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Workfront die u in [ creeerde vormt verbindingen in de Fusie van Workfront ](#configure-connections-in-workfront-fusion), dan klik O.K. **** om de verbinding aan die module te bewaren.
1. Ga aan [ bij Werk de Algemene module van Parameters ](#update-the-general-parameters-module).

#### De module Algemene parameters bijwerken

1. In de tweede module van het malplaatje (de Details van het Milieu van de Reeks), voor elk van de volgende variabelen, klik **toevoegen punt** en ga de naam en de waarde van de variabele in

   | Naam variabele | Waarde variabele |
   |---|---|
   | defaultJiraReporterID | Voer de id van de standaardgebruiker in wanneer de Maker-gebruiker niet bestaat in Jira. U vindt deze gebruikersnaam door op het profiel van de gebruiker te klikken en de URL van de browser te controleren. Voorbeeld: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Voer de basis-URL in van de Jira-account waarmee u verbinding maakt. |
   | wfBaseURL | Voer de basis-URL in van de Workfront-account waarmee u verbinding maakt. |

1. Ga aan [ aangepaste gebieden van de Kaart in Jira ](#map-custom-fields-in-jira) verder

<!--#### Map custom fields in Jira. 

Awaiting feedback-->

+++

### Scenario 2: JIRA naar Workfront: stuur updates over problemen en opmerkingen terug naar Workfront vanuit Jira

Dit scenario leidt tot een taak of een kwestie van Workfront wanneer een kwestie in Jira wordt gecreeerd.

>[!NOTE]
>
>Voor dit scenario is een OAuth2-verbinding voor Jira vereist.
>Om OAuth2 vergunning voor Jira te gebruiken, moet u opstelling een toepassing OAuth2 in [ https://developer.atlassian.com/console ](https://developer.atlassian.com/console). Raadpleeg de documentatie bij Jira voor meer informatie en instructies.

+++**breid aan meningsinstructies voor het vormen Scenario 2 uit: JIRA aan Workfront: Verzend updates over kwesties en commentaren terug naar Workfront van Jira**

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Deel 2: JIRA aan Workfront: Verzend updates over kwesties en commentaren terug naar Workfront van Jira** malplaatje.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer een verbinding die de geloofsbrieven voor de gebruiker van de Integratie van het Systeem gebruikt, of creeer een verbinding aan Jira met de geloofsbrieven van de Integratie van het Systeem.

* Voor instructies bij het creëren van een verbinding aan Jira, zie [ Verbinding Jira aan de Fusie van Workfront ](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) in de modules van de artikelJira Software.

1. Het webhaakfilter configureren

1. Ga aan [ verder vormen een webhaak in Jira ](#configure-a-webhook-in-jira)

#### Webhaak configureren in Jira

1. Maak een webhaak in Jira.

   Voor instructies zie [ Webhooks ](https://developer.atlassian.com/server/jira/platform/webhooks/) in de documentatie van Jira.

1. Gebruik de volgende waarden wanneer u de webhaak configureert:

   * **JQL**: project = &quot;yourProjectName&quot; (waar yourProjectName = de naam van uw JIRA-project)
   * **Uitgave**: gecreeerd, bijgewerkt
   * **Commentaar**: gecreeerd, geschrapt


1. Ga aan [ Connect malplaatjemodules aan Workfront en Jira (Module 2) ](#connect-template-modules-to-workfront-and-jira-module-2) verder

#### Sjabloonmodules verbinden met Workfront en Jira (module 2)

1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die u in [ creeerde vormt verbindingen in de Fusie van Workfront ](#configure-connections-in-workfront-fusion), dan klik O.K. **** om de verbinding aan die module te bewaren.
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Workfront die u in [ creeerde vormt verbindingen in de Fusie van Workfront ](#configure-connections-in-workfront-fusion), dan klik O.K. **** om de verbinding aan die module te bewaren.
   <!--#### Map custom fields-->

+++

### Scenario 3: Workfront naar Jira: Verandering van Workfront-taak naar JIRA-kwestie

+++**breid aan meningsinstructies voor het vormen Scenario 3 uit: De Veranderingen van WF-aan-Jira (Taken)**

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Deel 3: Workfront aan Jira: Veranderingen in de taak van Workfront aan JIRA uitgiftesjabloon**.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.

1. Klik op de sjabloon om de editor in te voeren.
1. Selecteer de organisatie en het team die dit scenario zullen bezitten.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer in het veld Verbinding de Workfront-verbinding die de referenties voor systeemintegratie gebruikt.
1. Op het **gebied van het Type van Verslag**, uitgezochte `Task`.
1. Op het **gebied van de Staat**, uitgezochte `New state`.
1. Vorm de filter met de volgende verrichtingen, gebruikend **en** optie:

   | Veld | Operator | Waarde |
   |---|---|---|
   | assignedToID | Gelijk | Voer de Workfront-id van de gebruiker System Integration in |
   | projectID | Gelijk | Voer de id in van het project of de projecten die de webhaak moet bekijken. |
   | DE: Jira Key | Exists |  |

1. Laat de **updates van de Uitsluiting toe die door deze verbinding** optie worden gemaakt.
1. Op het **gebied van de Oorsprong van het 0} Verslag, uitgezochte**.`Updated record only`
1. Klik **sparen** om Webhaak te bewaren, dan klik O.K. **** om de trekkermodule te bewaren.
1. In de **Reeks JIRA Variabelen** module, plaats de volgende variabelen, dan klik O.K. **** om de module te bewaren.

   | Naam variabele | Waarde variabele |
   |---|---|
   | defaultJiraReporterID | Dit is de id van de standaardgebruiker wanneer de Maker-gebruiker niet bestaat in Jira. U vindt deze gebruikersnaam door op het profiel van de gebruiker te klikken en de URL van de browser te controleren. Voorbeeld: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | De basis-URL van de Jira-account waarmee u verbinding maakt. |
   | wfBaseURL | De basis-URL van de Workfront-account waarmee u verbinding maakt. |

1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Jira die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**

+++

### Scenario 4: Workfront naar Jira: Wijzigingen in Workfront-kwestie in JIRA-kwestie

In dit scenario worden updates van Workfront-problemen verzonden naar eerder verwante JIRA-problemen.

+++**breid zich aan meningsinstructies voor het vormen Scenario 4 uit: Workfront aan Jira: De veranderingen in de kwestie van Workfront aan JIRA**

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Scenario 4: De Veranderingen van WF-aan-Jira (Kwesties)** malplaatje.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.

1. Klik op de sjabloon om de editor in te voeren.
1. Selecteer de organisatie en het team die dit scenario zullen bezitten.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer in het veld Verbinding de Workfront-verbinding die de referenties voor systeemintegratie gebruikt.
1. Op het **gebied van het Type van Verslag**, uitgezochte `Issues`.
1. Op het **gebied van de Staat**, uitgezochte `New state`.
1. Vorm de filter met de volgende verrichtingen, gebruikend **en** optie:

   | Veld | Operator | Waarde |
   |---|---|---|
   | assignedToID | Gelijk | Voer de Workfront-id van de gebruiker System Integration in |
   | projectID | Gelijk | Voer de id in van het project of de projecten die de webhaak moet bekijken. |
   | DE: Jira Key | Exists |  |

1. Laat de **updates van de Uitsluiting toe die door deze verbinding** optie worden gemaakt.
1. Op het **gebied van de Oorsprong van het 0} Verslag, uitgezochte**.`Updated record only`
1. Klik **sparen** om Webhaak te bewaren, dan klik O.K. **** om de trekkermodule te bewaren.
1. In de **Reeks JIRA Variabelen** module, plaats de volgende variabelen, dan klik O.K. **** om de module te bewaren.

   | Naam variabele | Waarde variabele |
   |---|---|
   | defaultJiraReporterID | Dit is de id van de standaardgebruiker wanneer de Maker-gebruiker niet bestaat in Jira. U vindt deze gebruikersnaam door op het profiel van de gebruiker te klikken en de URL van de browser te controleren. Voorbeeld: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | De basis-URL van de Jira-account waarmee u verbinding maakt. |
   | wfBaseURL | De basis-URL van de Workfront-account waarmee u verbinding maakt. |

1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Jira die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**

+++

### Scenario 5: Workfront naar Jira: Maak opmerkingen in JIRA wanneer u een nieuwe notitie maakt over de Workfront-taak of -kwestie

+++**breid aan meningsinstructies voor het vormen Scenario 5 uit: Workfront aan Jira: Creeer commentaar in JIRA wanneer nieuwe nota over de taak of de kwestie van Workfront**

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Scenario 5: WF-aan-Jira Nieuwe nota&#39;s (Taken en Kwesties)** malplaatje.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer in het veld Verbinding de Workfront-verbinding die de referenties voor systeemintegratie gebruikt.
1. Op het **gebied van het Type van Verslag**, uitgezochte `Note`.
1. Op het **gebied van de Staat**, uitgezochte `New state`.
1. Configureer het filter met de volgende bewerkingen:

   | Veld | Operator | Waarde |
   |---|---|---|
   | projectID <br> EN <br> TaskID | Gelijk <br><br> bestaat | Voer de id in van het project of de projecten die de webhaak moet bekijken. |
   | OF |  |  |
   | projectID <br> EN <br> OpTaskID | Gelijk <br><br> bestaat | Voer de id in van het project of de projecten die de webhaak moet bekijken. |

1. Laat de **updates van de Uitsluiting toe die door deze verbinding** optie worden gemaakt.
1. Op het **gebied van de Oorsprong van het 0} Verslag, uitgezochte**.`New record only`
1. Klik **sparen** om Webhaak te bewaren, dan klik O.K. **** om de trekkermodule te bewaren.
1. In de **Vastgestelde variabelen** module, plaats de volgende variabelen, dan klik O.K. **** om de module te bewaren.

   | Naam variabele | Waarde variabele |
   |---|---|
   | defaultJiraReporterID | Dit is de id van de standaardgebruiker wanneer de Maker-gebruiker niet bestaat in Jira. U vindt deze gebruikersnaam door op het profiel van de gebruiker te klikken en de URL van de browser te controleren. Voorbeeld: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | De basis-URL van de Jira-account waarmee u verbinding maakt. |
   | wfBaseURL | De basis-URL van de Workfront-account waarmee u verbinding maakt. |

1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Jira die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**

+++

### Scenario 6: Workfront naar Jira: Maak in JIRA opmerkingen over verwijderde notitie over de Workfront-taak of -kwestie

+++**breid aan meningsinstructies voor het vormen Scenario 6 uit: Workfront aan Jira: Creeer commentaar in JIRA op geschrapte nota over de taak of de kwestie van Workfront**

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Scenario 6: WF-aan-Jira verwijdert nota&#39;s (Taken en Kwesties)** malplaatje.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer in het veld Verbinding de Workfront-verbinding die de referenties voor systeemintegratie gebruikt.
1. Op het **gebied van het Type van Verslag**, uitgezochte `Note`.
1. Op het **gebied van de Staat**, uitgezochte `New state`.
1. Configureer het filter met de volgende bewerkingen:

   | Veld | Operator | Waarde |
   |---|---|---|
   | projectID <br> EN <br> TaskID | Gelijk <br><br> bestaat | Voer de id in van het project of de projecten die de webhaak moet bekijken. |
   | OF |  |  |
   | projectID <br> EN <br> OpTaskID | Gelijk <br><br> bestaat | Voer de id in van het project of de projecten die de webhaak moet bekijken. |

1. Laat de **updates van de Uitsluiting toe die door deze verbinding** optie worden gemaakt.
1. Op het **gebied van de Oorsprong van het 0} Verslag, uitgezochte**.`Deleted record only`
1. Klik **sparen** om Webhaak te bewaren, dan klik O.K. **** om de trekkermodule te bewaren.
1. In de tweede module, plaats de volgende variabelen, dan klik O.K. **** om de module te bewaren.

   | Naam variabele | Waarde variabele |
   |---|---|
   | defaultJiraReporterID | Dit is de id van de standaardgebruiker wanneer de Maker-gebruiker niet bestaat in Jira. U vindt deze gebruikersnaam door op het profiel van de gebruiker te klikken en de URL van de browser te controleren. Voorbeeld: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | De basis-URL van de Jira-account waarmee u verbinding maakt. |
   | wfBaseURL | De basis-URL van de Workfront-account waarmee u verbinding maakt. |

1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Jira die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**

+++

### Scenario 7: Workfront naar Jira: Maak opmerkingen in JIRA wanneer een nieuw document over de Workfront-taak of -kwestie wordt gepubliceerd

+++**breid aan meningsinstructies voor het vormen Scenario 7 uit: Workfront aan Jira: Creeer commentaar in JIRA wanneer het nieuwe document op de taak of de kwestie van Workfront**

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Scenario 7: WF-aan-Jira Nieuwe Gehechtheid (Taken en Kwesties)** malplaatje.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer in het veld Verbinding de Workfront-verbinding die de referenties voor systeemintegratie gebruikt.
1. Op het **gebied van het Type van Verslag**, uitgezochte `Document`.
1. Op het **gebied van de Staat**, uitgezochte `New state`.
1. Vorm de filter met de volgende verrichtingen, gebruikend **en** optie:

   | Veld | Operator | Waarde |
   |---|---|---|
   | assignedToID | Gelijk | Voer de Workfront-id van de gebruiker System Integration in |
   | projectID | Gelijk | Voer de id in van het project of de projecten die de webhaak moet bekijken. |

1. Stel in de tweede module de volgende variabelen in.

   | Naam variabele | Waarde variabele |
   |---|---|
   | defaultJiraReporterID | Dit is de id van de standaardgebruiker wanneer de Maker-gebruiker niet bestaat in Jira. U vindt deze gebruikersnaam door op het profiel van de gebruiker te klikken en de URL van de browser te controleren. Voorbeeld: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | De basis-URL van de Jira-account waarmee u verbinding maakt. |
   | wfBaseURL | De basis-URL van de Workfront-account waarmee u verbinding maakt. |

1. Laat de **updates van de Uitsluiting toe die door deze verbinding** optie worden gemaakt.
1. Op het **gebied van de Oorsprong van het 0} Verslag, uitgezochte**.`New record only`
1. Klik **sparen** om Webhaak te bewaren, dan klik O.K. **** om de trekkermodule te bewaren.
1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Jira die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**

+++

### Scenario 8: Workfront naar Jira: Maak in JIRA opmerkingen over verwijderd document over Workfront-taak of -uitgave

+++**breid aan meningsinstructies voor het vormen Scenario 8 uit: Workfront aan Jira: Creeer commentaar in JIRA op geschrapt document op de taak of de kwestie van Workfront**

1. Klik het **lusje** pictogram van Malplaatjes 1} van Malplaatjes ![ in het linkernavigatievenster.](assets/templates-icon.png)
1. Zoek naar het malplaatje door de onderzoeksbar dichtbij de upper-left hoek van het scherm te gebruiken. U kunt zoeken op sjabloonnaam of opgenomen toepassingen.
1. Klik **Scenario 8: WF-aan-Jira verwijder Gehechtheid (Taken en Kwesties)** malplaatje.

   Er wordt een weergave van de sjabloon geopend met informatie en een animatie van de gegevensstroom.
1. Voeg in de eerste module een webhaak toe.
1. Selecteer in het veld Verbinding de Workfront-verbinding die de referenties voor systeemintegratie gebruikt.
1. Op het **gebied van het Type van Verslag**, uitgezochte `Document`.
1. Op het **gebied van de Staat**, uitgezochte `New state`.
1. Configureer het filter met de volgende bewerkingen:

   | Veld | Operator | Waarde |
   |---|---|---|
   | projectID <br> EN <br> TaskID | Gelijk <br><br> bestaat | Voer de id in van het project of de projecten die de webhaak moet bekijken. |
   | OF |  |  |
   | projectID <br> EN <br> OpTaskID | Gelijk <br><br> bestaat | Voer de id in van het project of de projecten die de webhaak moet bekijken. |

1. In de **Vastgestelde variabelen** module, plaats de volgende variabelen.

   | Naam variabele | Waarde variabele |
   |---|---|
   | defaultJiraReporterID | Dit is de id van de standaardgebruiker wanneer de Maker-gebruiker niet bestaat in Jira. U vindt deze gebruikersnaam door op het profiel van de gebruiker te klikken en de URL van de browser te controleren. Voorbeeld: `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | De basis-URL van de Jira-account waarmee u verbinding maakt. |
   | wfBaseURL | De basis-URL van de Workfront-account waarmee u verbinding maakt. |

1. Laat de **updates van de Uitsluiting toe die door deze verbinding** optie worden gemaakt.
1. Op het **gebied van de Oorsprong van het 0} Verslag, uitgezochte**.`Deleted record only`
1. Klik **sparen** om Webhaak te bewaren, dan klik O.K. **** om de trekkermodule te bewaren.
1. In **elke** module van Workfront, op het gebied van de Verbinding, selecteer de verbinding van Workfront die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**
1. In **elke** module van Jira, op het gebied van de Verbinding, selecteer de verbinding van Jira die de geloofsbrieven van de Integratie van het Systeem gebruikt, dan klik O.K. **om de module te bewaren.**


+++

