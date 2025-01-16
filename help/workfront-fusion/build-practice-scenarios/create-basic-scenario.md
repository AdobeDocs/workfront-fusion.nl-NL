---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Een basisscenario maken
description: Leer hoe u een eenvoudig automatiseringsscenario maakt met Adobe Workfront Fusion. Automatiseringsscenario's automatiseren Workfront-processen, waaronder gegevensmanipulatie en -transformatie. Dit voorbeeld neemt u door het proces om een scenario tot stand te brengen dat naar a  [!DNL Workfront]  taak in Workfront zoekt en het in een project omzet.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# Een basisscenario maken

De rol van [!DNL Adobe Workfront Fusion] is om uw processen te automatiseren zodat u zich op nieuwe taken kunt concentreren eerder dan het herhalen van de zelfde taken opnieuw en opnieuw. Het werkt door acties binnen en tussen apps en de diensten te verbinden om een scenario tot stand te brengen dat uw gegevens automatisch overbrengt en transformeert. Het scenario dat u voor gegevens in een app of service maakt, verwerkt die gegevens om het gewenste resultaat te verkrijgen.

Dit voorbeeld doorloopt u het proces om een scenario tot stand te brengen dat naar een verzoek in Workfront zoekt en het in een project omzet.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie</td> 
   <td> <p>Nieuw: [!UICONTROL Standard]</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidig: Geen [!DNL Workfront Fusion] vereiste licentie.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] [!DNL Workfront] -abonnement: uw organisatie moet het abonnement aanschaffen [!DNL Adobe Workfront Fusion] .</li><li>[!UICONTROL Ultimate] [!DNL Workfront] abonnement: [!DNL Workfront Fusion] is opgenomen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet [!DNL Adobe Workfront Fusion] aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++



## Een praktijkscenario maken

### Beginnen met het maken van het scenario

1. In het **gebied van Scenario&#39;s**, klik **creeer een nieuw scenario**.

   Om van het gebied van Scenario&#39;s de plaats te bepalen, zie [ Navigeren de Fusie van Workfront ](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md).

   De vertoningen van de scenario redacteur, die een lege module in het centrum bevatten.

1. Selecteer de naam van de tijdelijke aanduiding **[!UICONTROL New scenario]** in de linkerbovenhoek en voer een naam in.
1. Ga met [ verder toevoegen en vormen de eerste module ](#add-and-configure-the-first-module).

### De eerste module toevoegen en configureren

1. Klik op de lege module om de app te kiezen waaruit u een module wilt selecteren.

   Rechts van de module wordt een lijst met apps weergegeven.

1. Selecteer **[!DNL Adobe Workfront]** . Als deze niet zichtbaar is, klikt u op de zoekbalk onder aan de lijst, typt u &quot;Workfront&quot; en selecteert u deze wanneer deze wordt weergegeven in de lijst.

   In de lijst worden alle modules weergegeven die u kunt gebruiken. [!DNL Workfront]

1. Klik op de module **[!UICONTROL Search]** .

   Het venster van de moduleconfiguratie opent.

1. Selecteer in het vak [!UICONTROL Connection] de Workfront-verbinding.

   Als u geen verbinding van Workfront hebt, zie [ een verbinding ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md) creëren
1. Selecteer **[!UICONTROL Issue]** in het vak [!UICONTROL Record Type] . Dit plaatst de module aan onderzoek slechts kwesties, die verzoeken omvatten.

   U kunt **[!UICONTROL Issue]** in de lijst vinden als u begint het woord &quot;[!UICONTROL Issue]&quot; te typen.

1. Selecteer **[!UICONTROL First Matching Record]** in het vak **[!UICONTROL Result Set]** .

   Dit plaatst de module om slechts het eerste verslag terug te keren het vindt dat aan de criteria voldoet.
1. In het **[!UICONTROL Search criteria]** gebied, vorm de criteria om de specifieke taak terug te keren.

   1. Selecteer in het eerste vak onder [!UICONTROL Search Criteria] het veld dat u in de zoekopdracht wilt opnemen. Selecteer **[!UICONTROL Name]** voor dit voorbeeld.

      U kunt **[!UICONTROL Name]** in de lijst vinden als u begint het woord &quot;[!UICONTROL name]&quot; te typen.
   1. Voor de exploitant, klik de dropdown pijl naast **bestaat** en verander het in [!UICONTROL **Bevat (geval ongevoelig)**].

      Hierdoor kan de module projecten zoeken met de door u gekozen woorden in de naam, zelfs als u niet de volledige naam invoert of de naam met het onjuiste geval invoert (zoals alle hoofdletters).
   1. Voer in het laatste veld onder [!UICONTROL Search Criteria] een woord of uitdrukking in die zich in de naam bevindt van de taak die u zoekt.

1. Selecteer in de lijst **[!UICONTROL Outputs]** de velden die de module moet uitvoeren. Selecteer in dit voorbeeld de velden **[!UICONTROL ID]** en **[!UICONTROL Name]** .

   >[!TIP]
   >
   >U kunt **Cmd+F** gebruiken ([!DNL Mac] OS) of **CTRL-F** ([!DNL Windows] OS) om een gebied snel te vinden.

1. Klik **[!UICONTROL OK]** om de moduleconfiguratie te bewaren.

1. Klik met de rechtermuisknop op de module, klik op **[!UICONTROL Rename]** en typ een naam met een beschrijving van wat de module moet doen (zoals &#39;Zoeken naar aanvragen&#39;). Klik vervolgens op **[!UICONTROL OK]** .

   De naam wordt net onder de module weergegeven. Hieronder bevat [!DNL Workfront Fusion] een korte beschrijving van het type actie dat door de module wordt uitgevoerd.

   ![](assets/module-renamed-wf.png)

1. Ga met [ verder toevoegen en vormen de tweede module ](#add-and-configure-the-second-module).

## De tweede module toevoegen en configureren

1. Beweeg de cursor over de gedeeltelijke cirkel rechts van de sectie van de module en klik vervolgens op **[!UICONTROL Add another module]** .
1. Selecteer [!DNL Adobe Workfront] in de lijst met toepassingen en kies vervolgens de module **[!UICONTROL Convert object]** .
1. Selecteer in het veld [!UICONTROL Connection] dezelfde Workfront-verbinding als in de vorige module.
1. Selecteer **[!UICONTROL issue]** in het veld **[!UICONTROL Record type]** omdat de module een uitgave converteert.
1. Op het **[!UICONTROL Convert to]** gebied, uitgezochte **Project**.
1. Klik naast het veld Taak-id op de kaarthandeling om deze in te schakelen.

   De schakeloptie wordt blauw als deze is ingeschakeld. Hierdoor kunt u de taak-id uit de vorige module toewijzen.

   ![ Kaart knevel ](assets/map-toggle.png)
1. Klik op het veld **[!UICONTROL Task ID]** .

   Er wordt een deelvenster geopend waarin u kunt selecteren wat u wilt gebruiken als de id van de taak die u naar een project wilt converteren. Omdat u toewijzing hebt ingeschakeld, bevat het deelvenster uitvoer van eerdere modules. U hebt de id geselecteerd als uitvoer van de vorige module, zodat deze nu beschikbaar is in het deelvenster.

   Dit deelvenster wordt het deelvenster Toewijzing genoemd. Voor meer informatie over het mappingpaneel, zie [ Overzicht van de Toewijzing ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).
1. Selecteer **identiteitskaart** in het mappingpaneel.

   Er wordt een ID-blok weergegeven in het veld Id. Het toont het aantal van de module het van in kaart wordt gebracht, en het gebied dat in kaart wordt gebracht.

   ![ identiteitskaart van de Kaart ](assets/map-id.png)

1. Klik het **gebied van identiteitskaart van het Malplaatje**, beginnen de naam van het malplaatje van Workfront te typen u voor dit project wilt gebruiken, dan het selecteren wanneer het in de lijst verschijnt.
1. Klik **[!UICONTROL OK]** om de moduleconfiguratie te bewaren.

1. Klik met de rechtermuisknop op de module, klik op **[!UICONTROL Rename]** en typ een naam om te beschrijven wat de module moet doen (bijvoorbeeld &quot;Omzetten in project)&quot;. Klik vervolgens op **[!UICONTROL OK]** .

1. Ga aan [ Test het scenario ](#test-the-scenario) verder.

## Het scenario testen

Alvorens u uw scenario activeert, is het belangrijk om het te testen door het minstens eens in werking te stellen en de resultaten te bekijken. Dit helpt u begrijpen hoe de gegevens door het scenario stromen en om het even welke fouten vinden.

Voor dit scenario, zou een succesvolle test in het bepalen van het verzoek resulteren en het omzetten in een project.

1. Klik op **[!UICONTROL Run once]** in de linkerbenedenhoek van de scenarioeditor.
1. Nadat het scenario eindigt lopend, klik de bel boven de eerste module om informatie over de bundel van gegevens te bekijken die de module, met inbegrip van gegevens verwerkte die uit het verzoek worden gehaald dat de module terugkeerde.

1. Klik op de bel met de uitvoeringcontrole boven de tweede module om de invoer (de aanvraag) en de uitvoer (het omgezette project) weer te geven.

   Zie voor meer informatie over de gegevens in de inspectiepbellen:

   * Voor algemene informatie, zie [ de uitvoeringsstroom van het Scenario ](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Voor informatie over verwerkte bundels, zie [ uitvoering Scenario, cycli, en fasen ](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. Klik in [!DNL Workfront Fusion] in de linkerbenedenhoek op **[!UICONTROL Save]** om de voortgang van het scenario op te slaan.

   >[!IMPORTANT]
   >
   >Sla de bestanden vaak op terwijl u ze gebruikt en test een scenario.

>[!TIP]
>
>Wij adviseren de facultatieve maar nuttige praktijk om nota&#39;s over elke module toe te voegen.
>
>1. Klik met de rechtermuisknop op een module en selecteer vervolgens **[!UICONTROL Add a note]** .
>1. Typ een overzicht voor de module in de notitie die wordt weergegeven.
>
>    U kunt meerdere notities toevoegen voor een module.
>
>1. Sluit het **[!UICONTROL Notes]** -gebied.
>
>     Nadat u een notitie aan een scenario hebt toegevoegd, wordt een oranje stip weergegeven op het **[!UICONTROL Notes]** pictogram ![](assets/notes-icon-w-dot.png) onder aan de scenario-editor.
>
>1. Klik op het pictogram **[!UICONTROL Notes]** ![](assets/notes-icon-w-dot.png) om uw notities weer te geven.
>

## Het scenario activeren

De laatste stap in het creëren van een scenario is het activeren.

Omdat dit scenario naar een specifieke kwestie zoekt, is er geen behoefte om het te activeren. Wanneer u een scenario activeert, wordt het uitgevoerd volgens een schema of wanneer een specifieke actie in een toepassing plaatsvindt. Nadat u een scenario activeert, door gebrek, loopt het om de 15 minuten. U kunt dit veranderen door te bepalen wanneer en hoe vaak u het wilt lopen.

Voor meer informatie over het activeren van scenario&#39;s, zie [ een scenario ](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md) activeren of deactiveren.

Voor informatie over programma&#39;s, zie [ Plan een scenario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Volgende stappen

* [ voeg een trekkermodule ](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) toe om het scenario toe te staan om nieuwe verzoeken periodiek te zoeken en hen in projecten om te zetten.
* [ voeg een webhaak ](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) toe om het scenario toe te staan om uit te voeren telkens als een verzoek is ingegaan.
* [ voeg een filter ](/help/workfront-fusion/build-practice-scenarios/add-filter-basic-scenario.md) toe om ervoor te zorgen dat slechts bepaalde verzoeken in projecten worden omgezet.
* [ voeg een functie ](/help/workfront-fusion/build-practice-scenarios/use-function-to-build-practice-scenario.md) toe die de naam van het nieuwe project aanpast.
