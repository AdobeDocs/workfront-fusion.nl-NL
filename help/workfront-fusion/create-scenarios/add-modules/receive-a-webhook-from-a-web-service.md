---
title: Webhaak voor een webservice zonder aansluiting configureren
description: Als een webservice momenteel geen speciale connector in Workfront Fusion heeft, maar ondersteuning biedt voor het verzenden van webhooks, kunt u de service aan een scenario toevoegen met de aangepaste webhmodule als instant trigger.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Webhaak voor een webservice zonder aansluiting configureren

Als een webservice momenteel geen speciale connector in Workfront Fusion heeft, maar ondersteuning biedt voor het verzenden van webhooks, kunt u de service aan een scenario toevoegen met de aangepaste webhmodule als instant trigger. Dit proces wordt geroepen ontvangend een webhaak, en het vereist één of andere configuratie op de kant van de toepassing u met verbindt.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket 
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
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Selecteer of Prime Workfront Plan: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront Plan: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Een webhaak ontvangen

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waarin u een webhaak wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Voeg de **Webhooks > Webhaak van de Douane** module toe om met uw scenario te beginnen.
1. Klik **toevoegen** naast het gebied van de Webhaak.
1. Ga de naam van a **Webhaak** in de doos die toont
1. (Optioneel) Configureer de webhaak.

   Voor instructies, zie [ Webhooks ](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

1. Klik **sparen**.

1. Klik **adres van het Exemplaar aan klembord**, dan klik O.K. **&#x200B;**.

1. Meld u aan bij de webservice en voer de volgende handelingen uit:

   1. Maak een webhaak in het gedeelte Instellingen voor de webservice.

      Specifieke instructies zijn afhankelijk van de toepassing. We raden u aan in de documentatie van de toepassing te zoeken naar &quot;Een webhaak maken&quot;.
   1. Plak het adres dat u in stap 3 naar het klembord hebt gekopieerd.
   1. Selecteer de gebeurtenis die de webhaak activeert.

1. Voer het scenario uit.

   Wanneer de gebeurtenis of de gebeurtenissen voorkomen, teweegbrengt de Webhamodule van de Douane en het scenario loopt.
