---
title: Webhaak voor een webservice zonder aansluiting configureren
description: Als een webservice momenteel geen speciale connector in Workfront Fusion heeft, maar ondersteuning biedt voor het verzenden van webhooks, kunt u de service aan een scenario toevoegen met de aangepaste webhmodule als instant trigger.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Webhaak voor een webservice zonder aansluiting configureren

Als een webservice momenteel geen speciale connector in Workfront Fusion heeft, maar ondersteuning biedt voor het verzenden van webhooks, kunt u de service aan een scenario toevoegen met de aangepaste webhmodule als instant trigger. Dit proces wordt geroepen ontvangend een webhaak, en het vereist één of andere configuratie op de kant van de toepassing u met verbindt.

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
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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

1. Klik **adres van het Exemplaar aan klembord**, dan klik O.K. ****.

1. Meld u aan bij de webservice en voer de volgende handelingen uit:

   1. Maak een webhaak in het gedeelte Instellingen voor de webservice.

      Specifieke instructies zijn afhankelijk van de toepassing. We raden u aan in de documentatie van de toepassing te zoeken naar &quot;Een webhaak maken&quot;.
   1. Plak het adres dat u in stap 3 naar het klembord hebt gekopieerd.
   1. Selecteer de gebeurtenis die de webhaak activeert.

1. Voer het scenario uit.

   Wanneer de gebeurtenis of de gebeurtenissen voorkomen, teweegbrengt de Webhamodule van de Douane en het scenario loopt.
