---
title: Veeva Vault-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Veeva Vault gebruiken en deze aansluiten op meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
source-git-commit: 37cb18a2e13a494c4174514539c0c7e43cdee011
workflow-type: tm+mt
source-wordcount: '1660'
ht-degree: 1%

---

# Veeva Vault-modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Veeva Vault gebruiken en deze aansluiten op meerdere toepassingen en services van derden.

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

Als u Veeva Vault-modules wilt gebruiken, hebt u een Veeva Vault-account nodig.

## Connect Veeva Vault naar Workfront Fusion

U kunt rechtstreeks vanuit een Veva Vault-module een verbinding maken met uw Veva Vault-account.

1. In om het even welke module van VevaVault, voegt de klik **naast het gebied van de Verbinding toe.**
1. Vul de volgende velden in.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Verbindingsnaam</td> 
       <td> <p>Voer een naam in voor de verbinding.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Omgeving</td>
        <td>
          <p>Selecteer of u verbinding maakt met een productieomgeving of niet.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Gebruikersnaam</td>
        <td>
          <p>Voer de gebruikersnaam in voor de Veva Vault-account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Wachtwoord</td>
        <td>
          <p>Voer het wachtwoord voor de Veva Vault-account in.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">Vault DNS</td> 
       <td>Voer uw Veva Vault DNS (domeinnaam) in.</p><p>Als u de Veva Vault DNS wilt zoeken, bekijkt u de URL die u gebruikt om toegang te krijgen tot Veeva Vault.</p>In de URL <code>https://my-dns.veevavault.com</code> is de DNS bijvoorbeeld <code>my-dns</code> . U hoeft niet de volledige URL in te voeren.</td> 
      </tr> 
     </tbody> 
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.



## Veeva Vault-modules en hun velden

Wanneer u Veeva Vault-modules configureert, geeft Workfront Fusion de onderstaande velden weer. Naast deze opties kunnen extra Vève Vault-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Document

* [Eén document maken](#create-a-single-document)
* [Meerdere documenten maken](#create-multiple-documents)
* [Eén document verwijderen](#delete-a-single-document)
* [Documenten exporteren](#export-documents)
* [Eén document ophalen](#get-a-single-document)
* [Gebruikersactie starten](#initiate-user-action)
* [Documenten weergeven](#list-documents)
* [Exportresultaten van document ophalen](#retrieve-document-export-results)
* [Meerdere documenten bijwerken](#update-multiple-documents)
* [Eén document bijwerken](#update-a-single-document)

#### Eén document maken

Deze module maakt één document, binder of sjabloon.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u een document, binder of sjabloon wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Velden selecteren</p> </td> 
   <td> <p>Selecteer de velden waarvoor u gegevens wilt invoeren en voer de gegevens in die velden in.</td> 
  </tr> 
 </tbody> 
</table>

#### Meerdere documenten maken

Deze module maakt meerdere documenten of sjablonen met behulp van een CSV-bestand.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u sjablonen of documenten wilt maken</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Bestandsgegevens</p> </td> 
   <td> <p>Wijs het CSV-bestand toe dat wordt gebruikt om de documenten te maken.</td> 
  </tr> 
 </tbody> 
</table>

#### Eén document verwijderen

Deze module verwijdert één document, binder of sjabloon.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u een document, binder of sjabloon wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document-id / Binder-id / Sjabloonnaam</p> </td> 
   <td> <p>Selecteer de velden die u wilt verwijderen.</td> 
  </tr> 
 </tbody> 
</table>

#### Documenten exporteren

Deze module exporteert documenten die u opgeeft, zoals bronnen, uitvoeringen en tekst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u een document, binder of sjabloon wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Bron</p> </td> 
   <td> <p>Schakel deze optie in om bronbestanden op te nemen in het exporteren.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Uitvoeringen</p> </td> 
   <td> <p>Schakel deze optie in om uitvoeringenbestanden op te nemen in het exporteren.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Alle versies</p> </td> 
   <td> <p>Schakel deze optie in om alle versies van de documentbestanden op te nemen in de exportbewerking.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Tekst</p> </td> 
   <td> <p>Schakel deze optie in om de tekst van het brondocument in het exporteren op te nemen.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Eén document ophalen

Deze module wint meta-gegevens voor één enkel document, binder, of malplaatje terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u gegevens voor een document, binder of malplaatje wilt terugwinnen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document-id / Binder-id / Sjabloonnaam</p> </td> 
   <td> <p>Selecteer de velden waarvoor u gegevens wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

#### Gebruikersactie starten

In deze module worden handelingen gestart voor documenten en binder, zoals het verzenden van een document ter controle of het wijzigen van de status.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u een handeling op een document of een binder wilt uitvoeren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document/Binder</p> </td> 
   <td> <p>Selecteer het document of de binder waarop u de handeling wilt uitvoeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Versie van document/Binding-versie</p> </td> 
   <td> <p>Selecteer het document of de binder waarop u de handeling wilt uitvoeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Handeling</p> </td> 
   <td> <p>Selecteer de handeling die u wilt uitvoeren in het document of de map.</td> 
  </tr> 
 </tbody> 
</table>

#### Documenten weergeven

In deze module worden alle documenten van het geselecteerde type weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u documenten, binders of sjablonen wilt weergeven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum aantal geretourneerde resultaten</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>

#### Exportresultaten van document ophalen

Deze module retourneert de resultaten van een eerder aangevraagd document exporteren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Taak-id</p> </td> 
   <td> <p>Voer de id in van de taak waarvoor u resultaten wilt retourneren of wijs deze toe. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Meerdere documenten bijwerken

Deze module werkt veelvoudige documenten of malplaatjes bij gebruikend een Csv- dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u sjablonen of documenten wilt maken</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Bestandsgegevens</p> </td> 
   <td> <p>Wijs het CSV-bestand toe dat wordt gebruikt om de documenten te maken.</td> 
  </tr> 
 </tbody> 
</table>

#### Eén document bijwerken

Deze module werkt één document, binder, of malplaatje bij.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u een document, documentversie, binder of sjabloon wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID / Naam</p> </td> 
   <td> <p>Als u een sjabloon bijwerkt, voert u een nieuwe naam voor de sjabloon in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Nieuwe sjabloonnaam</p> </td> 
   <td> <p>Voer de id of naam in van het object dat u wilt bijwerken of wijs deze toe.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Velden selecteren</p> </td> 
   <td> <p>Selecteer de velden waarvoor u gegevens wilt invoeren en voer de gegevens in die velden in.</td> 
  </tr> 
 </tbody> 
</table>

### Object



#### Objecten weergeven

Met deze module haalt u alle vault-objecten op in de geverifieerde vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Gelokaliseerde labels ophalen</p> </td> 
   <td> <p>Selecteer Ja om gelokaliseerde (vertaalde) tekenreeksen voor het label en label_meervoudig objecten velden op te halen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum aantal geretourneerde resultaten</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>

### Overige

* [Een aangepaste API-aanroep maken](#make-a-custom-api-call)
* [Een VQL-query maken](#make-a-vql-query)
* [Logboeken lezen](#read-logs)

#### Een aangepaste API-aanroep maken

Deze actiemodule maakt een aangepaste aanroep naar de Veva Vault-API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding</td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>baseurl/api/v</code> .  Bijvoorbeeld: <code>/objects/documents</code> . Neem <code>baseurl/api/v/</code> niet op, omdat het al is opgenomen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Methode</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Kopteksten</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tekenreeks query</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Lichaam</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Een VQL-query maken

Deze module maakt een query met VQL (Vault Query Language).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Selecteer of u sjablonen of documenten wilt maken</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Bestandsgegevens</p> </td> 
   <td> <p>Wijs het CSV-bestand toe dat wordt gebruikt om de documenten te maken.</td> 
  </tr> 
 </tbody> 
</table>

#### Logboeken lezen

Deze module retourneert gegevens van audittrails

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Verbinding </td> 
   <td> <p>Voor instructies over het aansluiten van uw Veva Vault rekening aan Workfront Fusion, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type controle</p> </td> 
   <td> <p>Selecteer het audittype waarvoor u gegevens wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Begindatum</p> </td> 
   <td> <p>Ga of kaart de begindatum voor de controles in die u wilt terugwinnen.</p><p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Einddatum</p> </td> 
   <td> <p>Ga of kaart de einddatum voor de controles in die u wilt terugwinnen.</p><p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Resultaat-URL </p> </td> 
   <td> <p>Selecteer CSV als u URL wilt krijgen om CSV van het resultaat te downloaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Maximum aantal geretourneerde resultaten</td> 
   <td>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</td> 
  </tr> 
 </tbody> 
</table>


