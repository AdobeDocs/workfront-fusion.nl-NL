---
title: Werken met grote bestanden
description: Er is momenteel ondersteuning voor grote bestanden beschikbaar voor de Workfront- en HTTP-connectors.
author: Becky
feature: Workfront Fusion
exl-id: 6df81943-e70c-42b3-aa44-d82343598a51
source-git-commit: a5a98d2e0b246d46389d4574e29f91c74f053472
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Werken met grote bestanden

>[!IMPORTANT]
>
>Grote bestandsmogelijkheden zijn alleen beschikbaar voor organisaties in het Workfront Ultimate-pakket.

De verbeterde mogelijkheden voor gegevensoverdracht zijn nu beschikbaar in Workfront Fusion, waardoor scenario&#39;s aanzienlijk grotere bestanden kunnen verwerken.

Voor het verwerken van grotere bestanden moeten uw scenario&#39;s worden bijgewerkt.

## Connectors die grote bestanden ondersteunen

Momenteel, steunen de volgende schakelaars grote dossiers.

>[!NOTE]
>
>* Als een bestand wordt gedownload met een module die grote bestanden ondersteunt en vervolgens wordt doorgegeven aan een module die geen grote bestanden ondersteunt, wordt het bestand niet verwerkt. Grote bestanden moeten tijdens de gehele workflow uitsluitend met ondersteunde modules worden afgehandeld.
>* Modules die geen ondersteuning bieden voor grote bestanden kunnen bestanden van maximaal 200 MB verwerken.

* Workfront
   * Document uploaden
   * Document downloaden
* Adobe Experience Manager Assets
   * Document uploaden
* Workfront Proof
   * Bestand uploaden
   * Proef downloaden
* Adobe Authenticator
   * Aangepaste API-aanroep maken
* SharePoint
   * Een bestand maken
   * Een bestand ophalen
* Salesforce
   * Bestand uploaden
* AWS S3
   * Bestand uploaden
   * Bestand ophalen
* HTTP

Andere schakelaars zullen in toekomstige versies worden gesteund.

## Uw scenario&#39;s bijwerken om grote bestanden af te handelen

De module Workfront > Document uploaden is gewijzigd voor het verwerken van grotere bestanden. In de vorige versie van deze module wordt nu `(Legacy)` weergegeven die aan de naam van de module is toegevoegd. In de meeste gevallen zal de oudere module blijven functioneren.

Als u met grotere bestanden wilt werken, raden wij u aan de oudere module te vervangen door de nieuwe module Document uploaden. Met de nieuwe module Document uploaden voorkomt u time-outs en andere fouten.

![ uploadt document ](assets/new-upload-document.png)

## Veelgestelde vragen

### Wat is de nieuwe maximale bestandsgrootte?

Gebruikers kunnen nu bestanden verwerken die de vorige limiet van 1 GB overschrijden, wat de efficiëntie en productiviteit verhoogt.  Hoewel het platform afzonderlijke bestanden tot 15 GB voor één actie kan ondersteunen (zoals het uploaden van een bestand), zijn er andere factoren die van invloed zijn op de gegevensoverdracht. De maximale bestandsgrootte van één actie is uiteindelijk afhankelijk van de webservice waarmee Fusion verbinding maakt. Gegevensoverdracht is de totale verwerking voor één uitvoering. Dit betekent dat meerdere acties in één uitvoering bijdragen aan de totale gegevensoverdracht.

Fusion verwerkt bestanden totdat de uitvoerlimiet van 40 minuten is bereikt. Het kan enige tijd duren om grote bestanden te uploaden, te downloaden of te verwerken in uw Fusion-scenario. Hoewel er geen limiet is voor de afzonderlijke bestandsgrootte, geldt er een limiet van 40 minuten voor de uitvoeringstijd van scenario&#39;s. Als grote bestanden ertoe leiden dat de uitvoering meer dan 40 minuten in beslag neemt, mislukt het scenario. De de uitvoeringstijd van het scenario kan ook door scenario grootte, moduleingewikkeldheid, en netwerksnelheid worden beïnvloed. Daarom adviseren wij dat u deze aspecten van uw scenario&#39;s wanneer het gebruiken van grote dossiers in overweging neemt.

### Hoe werkt de nieuwe bestandsoverdracht van Fusion?

Als Fusion bestanden verwerkt, worden grotere bestanden toegevoegd aan permanente opslag (S3 Bucket of Azure Blob Storage). Wanneer een Fusion-module een bestandshandeling uitvoert, zoals het uploaden of downloaden, gebruikt Fusion het bestand in permanente opslag als bron in plaats van als actief geheugen.

### Kan ik met grotere bestanden werken met onvolledige uitvoeringen?

Ja, Fusion ondersteunt onvolledige uitvoeringen met grotere bestanden. Onvolledige uitvoeringen zijn beperkt in omvang voor een organisatie en moeten actief worden beheerd.

### Kan ik grotere bestanden gebruiken met een aansluiting?

Elke Fusion-connector moet worden bijgewerkt om grotere bestanden te ondersteunen. Tot de ondersteunde connectors behoren Workfront, HTTP en AEM Assets. Fusion-connectors worden nog steeds beperkt door de bestandsgrootte die door de webservice wordt ondersteund. Bestandsgroottelimieten worden doorgaans opgenomen in de API-documentatie voor eindpunten van webservices die bestanden downloaden en uploaden.

### Heeft dit gevolgen voor de activiteiten?

Nee, het aantal bewerkingen dat door een module wordt uitgevoerd, is hetzelfde.

### Wanneer wordt de gebruikersinterface van Fusion bijgewerkt om gegevens over bestandsoverdracht weer te geven?

Deze functie is al voltooid en geïmplementeerd voor productie.

### Wat zijn sommige manieren om over de nieuwe grenzen van de dossierverwerking te denken die me ontwerpscenario&#39;s zullen helpen?

Het ontwerpen van een scenario om binnen de uitvoeringsgrens van 40 minuten te werken kan gecompliceerd lijken. Wij adviseren het volgende in mening te houden wanneer het ontwerpen van een scenario:

* **begrijp uw bedrijfsvereisten voor uitvoeringstijd**: De het platformgrens van Fusion voor uitvoeringstijd is 40 minuten, maar de meeste bedrijfsprocesautomatiseringen worden verwacht om veel sneller uit te voeren. Bijvoorbeeld, gebruiker-in werking gestelde automatiseringen met resultaat-afhankelijke voortzetting zouden naar verwachting goed onder de 40 minieme grens voltooien.
* **overweeg uitvoeringstijd wanneer het ontwerpen van**: Wanneer het ontwerpen van uw scenario, is het essentieel om de tijd van de moduleuitvoering voor individuele dossieracties, zoals uploads en downloads te begrijpen. Deze kennis helpt u scenario&#39;s te plannen die veelvoudige dossieracties impliceren.  Om nauwkeurigheid in uw ontwerp te verzekeren, adviseren wij ronding van de uitvoeringstijd van de module tot een buffer.
Als Fusion bijvoorbeeld een document in 144 seconden (2,4 minuten) downloadt, kunt u verwachten dat één uitvoering meerdere keren vergelijkbare handelingen kan uitvoeren. In dit voorbeeld duurt het uitvoeren van de module 144 seconden en u moet 3 minuten wachten voordat de module is gedownload. Als uw vereisten zowel een upload als een download omvatten, zou de verwachte uitvoeringstijd ongeveer 6 minuten zijn. Merk op dat de uitvoeringstijden van de Fusie beperkt zijn tot 40 minuten.

* **consolideer dossieracties**: het gemeenschappelijkste voorbeeld van dossieracties in een scenario van de Fusie is één download en één upload. De meeste scenario&#39;s met alleen deze twee acties worden binnen een paar minuten uitgevoerd. Indien mogelijk moeten Fusion-ontwerpers hun scenario&#39;s beperken tot één download en één upload.

* **berekent grootte gebruikend het kaartpaneel**: Workfront en andere Webdiensten omvatten de dossiergrootte van een dossier in de output van de downloadmodule. Met deze gegevens kunt u bestanden uitfilteren die te groot zijn voor een module die wordt geüpload of die te groot zijn voor de uitvoeringstijd van het scenario.

* **Isoleer dossieracties in hun eigen scenario wanneer het werken met veelvoudige dossiers**: De ontwerpers van de fusie zouden moeten nadenken isolerend dossieracties in afzonderlijke scenario&#39;s. Een Fusion-scenario dat bijvoorbeeld wordt geactiveerd door een nieuwe Workfront-aanvraag met meerdere gekoppelde bestanden, moet mogelijk maximaal 30 bestanden bevatten. Aangezien het uploaden en downloaden van elk bestand maximaal 3 minuten in beslag kan nemen, zou het verwerken van alle bestanden in één uitvoering de uitvoerlimiet van 40 minuten van Fusion overschrijden. De oplossing is om een scenario van dossieracties te creëren gewijd aan de behandeling van het uploaden en het downloaden van individuele dossiers. Het verzoek-teweeggebrachte scenario zou door de in bijlage dossiers herhalen, die het scenario van de dossieracties voor elk dossier aanhalen gebruikend de module van HTTP. Deze benadering zorgt ervoor dat elk dossier binnen de uitvoeringstermijnen wordt verwerkt.

<!--
## Connectors that do not support large files

Some Fusion connectors do not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

The following connectors do **not** support large files. 

* Archive
* Box
* Convert
* CSV
* Datastores
* Flow control
* FTP
* JSON
* JWT
* Markdown
* Math
* Microsoft Word templates
* MIME
* Microsoft SQL
* SFTP
* Adobe Acrobat Sign
* SOAP
* Tools
* XML

If a connector is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.-->






<!--## Connectors that support large files

The following connectors support large files.

Workfront
HTTP
Webhooks
Salesforce
Microsoft Email
Workfront Proof
AEM Assets
Email
Slack
Jira
Microsoft Excel
SharePoint
Frame.io
Adobe PDF Services
Marketo
Azure Devops 
Google Email
Jira Server
Google Sheets
Microsoft OneDrive
ServiceNow 
AWS S3
Bynder
OneDrive Business
Adobe Authenticator
Google Drive
Microsoft Dynamics
Google Docs
NetSuite
Airtable
Azure AD
QuickBase 
Adobe Target
Adobe Campaign Classic
Microsoft Calendar
Workfront Planning
HubSpot CRM  
DropBox
Cloud Convert
Egnyte
Adobe Firefly
OpenAI / Chat GPT
Allocadia
Cvent
GitLab 
Google Team Drive
Google Calendar
Workfront SDL Managed Translation
Widen
Workfront Boards
Google Slides
Qualtrics
Microsoft Power BI
Adobe Photoshop
Anaplan
DocuSign 
MariaDB
Adobe Creative Cloud Libraries
Figma
AEM Forms
Datadog
GitHub 
Google Forms
Adobe I/O Events
Trello
Workday
Adobe Journey Optimizer
Adobe Lightroom


If a file is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

-->
