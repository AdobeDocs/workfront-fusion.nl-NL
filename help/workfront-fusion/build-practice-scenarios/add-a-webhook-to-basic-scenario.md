---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Webhaak toevoegen aan een basisscenario
description: Webhooks, ook wel 'instant triggers' genoemd, zijn een specifiek type triggermodule dat een scenario kan starten wanneer een wijziging wordt aangebracht in plaats van volgens een bepaald schema.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Webhaak toevoegen aan een basisscenario

Webhooks, ook wel &#39;instant triggers&#39; genoemd, zijn een specifiek type triggermodule dat een scenario kan starten wanneer een wijziging wordt aangebracht in plaats van volgens een bepaald schema.

In dit voorbeeld, zult u een website toevoegen om een scenario te beginnen zodra om het even welke verzoeken aan een specifieke verzoekrij zijn voorgelegd. Het scenario zet dan die verzoeken in een project om.

Dit voorbeeld wijzigt het scenario dat in [&#x200B; wordt gecreeerd leidt tot een basisscenario &#x200B;](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk pakket met Workfront Automation and Integration</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie</td> 
   <td>
   <p>Geen Workfront Fusion-licentievereiste.</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>U moet een account hebben voor elke toepassing of service waarmee u verbinding maakt met Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

U moet het scenario tot stand brengen dat in [&#x200B; wordt beschreven leidt tot een basisscenario &#x200B;](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) alvorens deze procedure te volgen.

## Webhaak toevoegen en configureren


### De module Webhaak toevoegen

1. Open het scenario in de scenarioredacteur.
1. Klik op de eerste module met de rechtermuisknop aan en selecteer **module van de Schrapping**.

   De module wordt verwijderd en er blijft een lege tijdelijke aanduiding achter.

1. Klik de lege module, en selecteer **Adobe Workfront** van de lijst van apps.
1. Selecteer **Gebeurtenissen van het Controle**.
1. Klik **toevoegen** naast het gebied van de Webhaak.
1. op het gebied van het Type van Verslag, uitgezochte **Uitgave**, zodat zal de module voor veranderingen in kwesties teweegbrengen.
1. Op het gebied van de Staat, uitgezochte **Nieuwe staat**. Dit is een verplicht veld dat wordt gebruikt voor het filter, dat in dit voorbeeld niet wordt weergegeven.
1. Op het gebied van de Oorsprong van het Verslag, selecteer **Nieuw slechts Verslag**. Dit staat het scenario toe om te teweegbrengen wanneer een kwestie wordt toegevoegd, niet wanneer men wordt bijgewerkt of geschrapt.
1. Klik **sparen** om de moduleconfiguratie te bewaren.

## De tweede module bijwerken

1. Open het scenario.
1. Klik de **objecten van de Bekeerling** module om het te openen.
1. Verwijder het zwarte-id-blok in het veld Uitgave-id. Het blok is zwart omdat de module waarvan het is toegewezen niet meer beschikbaar is.
1. Selecteer het blok van identiteitskaart onder de eerste module (de Gebeurtenissen van het Controle) om het aan de tweede module in kaart te brengen.
1. Klik **OK**.



### Testen en activeren

1. Klik op **[!UICONTROL Run once]** in de linkerbenedenhoek van de scenarioeditor.

   Het scenario moet lopen om op het nieuwe verzoek te letten.
1. Ga naar de Workfront-omgeving waarmee Fusion verbinding maakt en voeg een probleem toe.

   Het scenario moet worden uitgevoerd.
1. Onderzoek de output om ervoor te zorgen dat het scenario zoals verwacht liep.
1. Wanneer u wordt tevreden dat het scenario zoals verwacht werkt, klik **plannend** knevel in laag-linkervan het scherm aan **&#x200B;**.

   Dit activeert het scenario.
1. Klik in Workfront Fusion op **[!UICONTROL Save]** in de linkerbenedenhoek om de voortgang van het scenario op te slaan.
