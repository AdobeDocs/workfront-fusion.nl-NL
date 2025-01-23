---
title: Microsoft Dynamics 365-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Microsoft Dynamics 365 gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: 16ae173b-10ce-481d-8f6c-1df0e65f7c0e
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 modules]

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Microsoft Dynamics 365] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

>[!NOTE]
>
>De [!DNL Microsoft Dynamics 365] -connector biedt geen ondersteuning voor [!DNL Dynamics Finance and Operations] .

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Als u [!DNL Microsoft Dynamics] 365 wilt gebruiken, moet u een [!DNL Microsoft Dynamics 365] -account hebben.

## Microsoft Dynamics 365 verbinden met Workfront Fusion

U kunt rechtstreeks vanuit een [!DNL Microsoft Dynamics 365] -module verbinding maken met uw [!DNL Microsoft Dynamics 365] -account.

>[!NOTE]
>
>Sommige Microsoft-toepassingen gebruiken dezelfde verbinding, die is gekoppeld aan individuele gebruikersmachtigingen. Daarom bij het creëren van een verbinding, toont het scherm van de toestemmingstoestemming om het even welke toestemmingen die eerder aan de verbinding van deze gebruiker werden verleend, naast om het even welke nieuwe toestemmingen nodig voor de huidige toepassing.
>
>Bijvoorbeeld, als een gebruiker &quot;Gelezen lijst&quot;toestemmingen heeft die via de schakelaar van Excel worden verleend en dan een verbinding in de schakelaar van Vooruitzichten creeert om e-mails te lezen, zal het scherm van de toestemmingstoestemming zowel de reeds verleende &quot;Gelezen lijst&quot;toestemming en de onlangs vereiste &quot;Schrijf e-mail&quot;toestemming tonen.

1. Klik in een willekeurige [!DNL Microsoft Dynamics 365] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Voer een naam in voor de verbinding.
1. Voer in het veld **[!UICONTROL Resource]** het adres van uw [!DNL Dynamics 365] -account in, zonder `https://` .
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

>[!NOTE]
>
>Wanneer u [!DNL Workfront Fusion] registreert op uw [!DNL Microsoft Azure] -portal, gebruikt u de volgende URI voor omleiding:
>
>* `https://app.workfrontfusion.com/oauth/cb/workfront-microsoft-dynamics2`


## [!DNL Microsoft Dynamics 365] modules en hun velden

Wanneer u [!DNL Microsoft Dynamics 365] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Microsoft Dynamics 365] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Watch Records (Scheduled)]](#watch-records-scheduled)
* [[!UICONTROL Watch Records (Real Time)]](#watch-records-real-time)
* [[!UICONTROL Create Record]](#create-record)
* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Delete Record]](#delete-record)
* [[!UICONTROL Read Records]](#read-records)
* [[!UICONTROL Update Record]](#update-record)
* [[!UICONTROL Search Records]](#search-records)

### [!UICONTROL Watch Records (Scheduled)]

Deze geplande triggermodule voert een scenario uit wanneer een record in het opgegeven object wordt gemaakt of bijgewerkt na de laatste geplande run in [!DNL Dynamics 365] .

De output van de module wijst erop of het verslag dat het vond nieuw of bijgewerkt is (als het zowel in de tijdspanne werd toegevoegd en bijgewerkt, is het duidelijk als nieuw). U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Dit gebeurt op een regelmatig gepland interval dat u specificeert.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include]</td> 
   <td>Geef op of u de module <strong>[!UICONTROL Only new records]</strong> , <strong>[!UICONTROL Updated records only]</strong> of <strong>[!UICONTROL New records and all changes]</strong> wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Kies het [!UICONTROL Microsoft Dynamics 365] recordtype dat u het scenario wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max Records]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Watch Records (Real Time)]

Deze instant trigger-module voert een scenario uit wanneer een record (object) die u opgeeft, wordt gemaakt of bijgewerkt in [!DNL Dynamics 365] .

In deze module is een webhaak vereist.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer de webhaak die u voor deze module wilt gebruiken. </p> <p>Een nieuwe webhaak toevoegen:</p> 
    <ol> 
     <li value="1"> <p>Klik op <strong>[!UICONTROL Add]</strong> rechts van het veld Webhaak</p> </li> 
     <li value="2"> <p>Typ in het naamveld <strong>[!UICONTROL Webhook]</strong> een beschrijvende naam voor de webhaak.</p> </li> 
     <li value="3"> <p>Selecteer in het veld <strong>[!UICONTROL Connection]</strong> de gewenste verbinding</p> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </li> 
     <li value="4"> <p>Klik op <strong>[!UICONTROL Save]</strong> om de webhaak op te slaan en terug te keren naar de module.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create Record]

Deze actiemodule leidt tot een entiteit, zoals een benoeming of een taak,.

U geeft informatie op over de entiteit die u wilt maken.

De module retourneert de id van de nieuwe entiteit en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer het type entiteit dat de module moet maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select Fields to Map]</td> 
   <td>Selecteer de velden waarvoor u waarden wilt opnemen wanneer de record wordt gemaakt. Beschikbare velden zijn afhankelijk van het type entiteit.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Property fields]</td> 
   <td> Dit zijn de velden die u hebt geselecteerd. Voer de waarde in die de record voor een bepaalde eigenschap moet hebben. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Make an API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Microsoft Dynamics 365] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Microsoft Dynamics 365] -modules kan worden uitgevoerd.

De module keert informatie over de statuscode, kopballen, en lichaam terug. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Raadpleeg de documentatie van [!DNL Microsoft] over het gebruik van [!DNL Dynamics 365 Customer Engagement Web API] voor meer informatie.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Voer een pad in dat relatief is ten opzichte van <code>&lt;Instance URL>/api/data/v9.1/</code> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> <p>Voor meer in</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Hiermee voegt u de machtigingsheaders voor u toe.</p> </td> 
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

### [!UICONTROL Delete Record]

Met deze actiemodule verwijdert u een entiteit.

U geeft de id van de entiteit op.

De module retourneert de id van de entiteit en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td> <p>Selecteer het type entiteit dat de module moet verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Voer de unieke [!DNL Microsoft Dynamics 365] -id in of wijs deze toe aan de record die u wilt verwijderen door de module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Read Records]

Deze actiemodule leest gegevens van één entiteit in [!DNL Microsoft Dynamics 365] .

U geeft de id van de entiteit op.

De module retourneert de id van de entiteit en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer het type entiteit dat de module moet lezen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de unieke [!DNL Microsoft Dynamics 365] -id in of wijs deze toe aan de record die u wilt lezen in de module.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update Record]

Deze actiemodule werkt een entiteit bij.

U geeft de id van de entiteit op.

De module retourneert de id van de bijgewerkte record en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer het type entiteit dat de module moet bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select Fields to Map]</td> 
   <td>Selecteer de velden waarvoor u waarden wilt opnemen wanneer de record wordt gemaakt. Beschikbare velden zijn afhankelijk van het type entiteit.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Property fields]</td> 
   <td>Dit zijn de velden die u hebt geselecteerd. Voer de waarde in die de record voor een bepaalde eigenschap moet hebben.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de unieke [!DNL Microsoft Dynamics] 365-id in of wijs deze toe aan de record die u wilt bijwerken in de module.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search Records]

Deze zoekmodule zoekt naar records in een object in [!DNL Microsoft Dynamics 365] dat overeenkomt met de zoekquery die u opgeeft. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Zie <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Microsoft Dynamics 365] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Microsoft Dynamics 365] -account met [!DNL Workfront Fusion] . </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Selecteer het type entiteit dat de module moet bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filters]</td> 
   <td> <p>Selecteer het filter dat u voor deze zoekopdracht wilt gebruiken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Standard Filters]</strong> </p> <p>Stel het filter in door een veld en een operator te selecteren en de waarde die u wilt zoeken in te voeren of toe te wijzen. U kunt EN of OF regels aan uw filter gebruiken.</p> </li> 
     <li> <p><strong>[!UICONTROL Query Functions]</strong> </p> <p>Voer de API-queryfunctie van [!DNL Dynamics 365] in die u wilt gebruiken om te zoeken. </p> <p>Voor meer informatie over vraagfuncties, zie {de Verwijzing van de Functie van de Vraag van 0} Web API </a> in de [!DNL Microsoft] documentatie.<a href="https://docs.microsoft.com/en-us/dynamics365/customer-engagement/web-api/queryfunctions?view=dynamics-ce-odata-9"></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>Geef de volgorde op waarin de items worden geretourneerd. U kunt meerdere soorten toevoegen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>Geef het veld op waarin u de resultaten wilt sorteren.</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Geef de richting van de sortering op (oplopend of aflopend).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max Records]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
 </tbody> 
</table>
