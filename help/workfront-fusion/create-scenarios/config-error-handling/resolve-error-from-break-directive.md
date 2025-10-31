---
title: Fouten oplossen die worden verwerkt door de Break-richtlijn
description: Soms, is het nuttig om een falende module opnieuw uit te voeren als er een kans is dat de reden voor de mislukking snel zou kunnen oplossen.
author: Becky
feature: Workfront Fusion
exl-id: d568942c-2cd5-430c-bdbf-e1496da25b50
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Fouten oplossen die worden verwerkt door de Break-richtlijn

Wanneer een fout door de instructie Break wordt afgehandeld, wordt een record gemaakt in de map Onvolledige uitvoeringen. Dit verslag slaat de staat van de scenariouitvoering, samen met gegevens van de vroegere modules op. De record verwijst naar de module waar de fout is opgetreden en bevat informatie over de gegevens die de module als invoer heeft ontvangen. Voor elke bundel gegevens die de fout veroorzaakt, wordt een afzonderlijke verslag gecreeerd.

Voor meer informatie, zie [&#x200B; Mening en los onvolledige uitvoeringen &#x200B;](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Fouten die voortvloeien uit de Break-richtlijn oplossen

U kunt de fout handmatig oplossen door het scenario (indien nodig) bij te werken en één keer uit te voeren.

U kunt het scenario ook vormen om een onvolledige uitvoering automatisch te verwerken door het scenario opnieuw uit te voeren. Om de module te vormen om onvolledige uitvoeringen te verwerken:

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u de tijdelijke oplossing wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik de **controle van de Stroom** pictogram ![&#x200B; controle van de Stroom &#x200B;](assets/flow-control-icon.png) en selecteer **Break**.
1. Binnen de module van het Sluiten, laat [!UICONTROL **automatisch volledige uitvoerings**] optie toe.
1. Op het **Aantal pogingen** gebied, ga of kaart het maximumaantal pogingen in dat u de module wilt de uitvoering opnieuw proberen

   Dit getal moet tussen 1 en 100 liggen.
1. In het **Interval tussen pogingen** gebied, ga of kaart het aantal notulen tussen elke poging opnieuw in.

Als deze optie is ingeschakeld en er een fout optreedt, wordt de onvolledige uitvoering opgehaald (na de in het veld [!UICONTROL Interval between attempts] opgegeven tijd) en uitgevoerd met de oorspronkelijke invoergegevens. Dit zal herhalen tot de uitvoering van de module zonder een fout voltooit of tot het Aantal gespecificeerde pogingen wordt bereikt.

>[!NOTE]
>
>Als de aanvankelijke poging opnieuw probeert ontbreekt, stijgt het interval tussen opnieuw probeert exponentieel elke andere poging.


Wanneer de optie Automatisch uitvoeren is ingeschakeld, wordt het scenario uitgevoerd als &quot;Voltooid&quot; gemarkeerd omdat de fouthandler Automatisch opnieuw proberen het probleem automatisch afhandelt. In dit geval ontvangen gebruikers geen e-mail over de mislukte uitvoering.

Als de optie Automatisch uitvoeren is uitgeschakeld, wordt de uitvoering gemarkeerd als Waarschuwing.

Er zijn sommige uitzonderingen op uitvoeringen die onder Onvolledige Uitvoeringen worden opgeslagen, en met sommige foutentypes, is auto-retry van een scenario uitvoering niet mogelijk.

## Bronnen

Voor meer informatie, zie [&#x200B; toestaan het opslaan van onvolledige uitvoeringen &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) in artikel vormt scenario montages.
