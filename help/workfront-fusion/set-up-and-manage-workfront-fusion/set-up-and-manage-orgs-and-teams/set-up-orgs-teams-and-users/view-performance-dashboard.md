---
title: Het prestatiedashboard voor een organisatie weergeven
description: Fusiebeheerders kunnen een dashboard weergeven met uitvoeringsmeetgegevens voor een organisatie.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
source-git-commit: 1d8504b10d9ca74a5df5532232cda235c67b0185
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Het prestatiedashboard voor een organisatie weergeven

Het dashboard van de Prestaties van de Fusie staat u toe om snel te zien welke scenario&#39;s in werking stellen het meest, waar de vertragingen voorkomen, en hoe effectief uw arbeidersgroepen in werking stellen. Dit verstrekt zicht in real time in uitvoeringsvolumes, rijdiepte, poolgebruik, en scenario-vlakke prestaties.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Adobe Workfront Workflow Ultimate en Adobe Workfront Automation and Integration Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau</td> 
   <td> 
     <p>U moet een Workfront Fusion-beheerder zijn voor uw organisatie.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Prestatie-dashboardcomponenten

>[!NOTE]
>
>Metrische gegevens worden weergegeven per pool van workers. Als u een andere arbeidersgroep wilt weergeven, klikt u op het veld Pool in de linkerbovenhoek van het dashboard en selecteert u de groep waarvoor u metriek wilt weergeven.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

In het dashboard voor Fusieprestaties ziet u de volgende cijfers.

* **Uitvoeringen die wachten om worden verwerkt**
Dit diagram toont het aantal uitvoeringen die wachten om (ook genoemd als uitvoeringsachterstand) op een bepaald punt in tijd te worden verwerkt.

  Een groot aantal executies die wachten om te worden verwerkt, kan de prestaties in uw Fusion-instantie beïnvloeden. U zult een bericht ontvangen als uw uitvoeringsachterstand 5000 uitvoeringen bereikt. Wij adviseren het identificeren van verantwoordelijke scenario&#39;s en het wijzigen van of het onbruikbaar maken van hen. Als de hoge uitvoeringsachterstand voortduurt, zal het team van de Fusie de prestaties van uw instantie van de Fusie beschermen door de verantwoordelijke scenario&#39;s onbruikbaar te maken.
* **het Gebruik van de pool**
Deze grafiek toont het gebruik van de arbeiderspool in tijd. Als deze grafiek routinematig het gebruik van de arbeiderspool toont, kunt u sommige scenario&#39;s aan een andere pool willen toewijzen.

  Als een pool bijna 100% gebruik heeft, kunnen andere middelen die dezelfde pool gebruiken worden vertraagd of verstoord. Als dit voorkomt, adviseren wij opnieuw toewijzen een hoog-gebruiksscenario aan een andere arbeiderspool, of het wijzigen van bestaande scenario&#39;s om minder middelintensief te zijn.
* **Uitvoeringen per scenario**
Deze grafiek toont uitvoeringen per scenario. Verschillende kleuren vertegenwoordigen verschillende scenario&#39;s. Wanneer u de cursor boven het diagram houdt, wordt een venster weergegeven waarin wordt aangegeven welke kleur voor welk scenario wordt gebruikt.

  U kunt deze grafiek gebruiken om te identificeren welke scenario&#39;s een uitvoeringsachterstand of hoog gebruik van de arbeiderspool kunnen veroorzaken.
* **Duur van uitvoeringen**
Deze grafiek toont uitvoeringen per scenario. Verschillende kleuren vertegenwoordigen verschillende scenario&#39;s. Wanneer u de cursor boven het diagram houdt, wordt een venster weergegeven waarin wordt aangegeven welke kleur voor welk scenario wordt gebruikt.

  U kunt dit diagram gebruiken om scenario&#39;s te identificeren die langer duren dan normaal, met inbegrip van die die door kwesties met verbonden app of de dienst worden beïnvloed.

## Het dashboard voor Fusion Performance weergeven

1. Klik in Fusion op Prestaties in de linkernavigatie.

   Het dashboard wordt geopend.

1. Als u gegevens voor een bepaald tijdpunt wilt weergeven, beweegt u de muisaanwijzer over een dashboard en past u de cursor aan zodat deze zich over het gewenste tijdpunt beweegt.

   Op alle grafieken wordt een lijn op dat punt in de tijd weergegeven en op elke grafiek wordt een venster weergegeven waarin de gegevens voor dat moment worden weergegeven.
1. Om gegevens voor een specifiek scenario in de Uitvoeringen per scenario grafiek of de Duur van uitvoeringen grafiek te bekijken, klik op een bar van de kleur voor het scenario u gegevens voor wilt bekijken. Klik nogmaals op de grafiek om terug te keren naar de weergave waarin alle scenario&#39;s worden weergegeven.
1. Om naar een specifiek scenario te gaan dat in de Uitvoeringen per scenario grafiek of de Duur van uitvoeringen grafiek wordt getoond, klik op een bar van de kleur voor het scenario met de rechtermuisknop aan, en selecteer **Open scenario in nieuw lusje**.
1. Om een grafiek uit te breiden, klik **breid** pictogram ![&#x200B; pictogram &#x200B;](assets/expand-icon.png) bij de hoger-juiste hoek van die grafiek uit.
1. Als u het tijdbereik van het dashboard wilt wijzigen, selecteert u het veld Tijdbereik in de rechterbovenhoek van het dashboard en vervolgens een nieuw tijdframe. De langste beschikbare tijd is 24 uur en de kortste is 15 minuten.
1. Als u de diagrammen wilt vernieuwen, klikt u op het pictogram Vernieuwen in de rechterbovenhoek van het dashboard.
1. Als u een andere arbeidersgroep wilt weergeven, klikt u op het veld Pool in de linkerbovenhoek van het dashboard en selecteert u vervolgens de groep die u wilt weergeven.
