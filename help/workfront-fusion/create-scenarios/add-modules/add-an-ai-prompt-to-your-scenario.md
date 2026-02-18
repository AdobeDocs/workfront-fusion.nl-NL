---
title: Een AI-prompt toevoegen aan uw scenario
description: U kunt een AI herinnering in uw scenario omvatten dat met uw verbindt
author: Becky
feature: Workfront Fusion
source-git-commit: 09e8ca28c12990a699816671d07f85288d973bc7
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Een AI-prompt toevoegen aan uw scenario

U kunt een AI herinnering in uw scenario omvatten gebruikend ModelContext Protocol (MCP) dat met grote taalmodellen (LLMs) wordt gecombineerd. Door deze in de module van de Agent te vormen MCP, kunt u kunstmatige intelligentie aan opstellingswerkschema&#39;s gebruiken die efficiënt, veilig, en flexibel zijn.

>[!NOTE]
>
>Deze functionaliteit is los van de capaciteit om modules aan een scenario toe te voegen gebruikend AI.
>
>Voor informatie bij het toevoegen van modules met AI, zie [&#x200B; een scenario segment gebruikend AI &#x200B;](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-with-ai.md) produceren.

## Overzicht van het modelcontextprotocol

ModelContextProtocol (MCP) is een manier om AI taalmodellen met andere toepassingen veilig te verbinden. U vormt servers MCP, die het AI model toestaan om tot de toepassing toegang te hebben. Vervolgens kunt u een melding naar het AI-model sturen en gegevens van de toepassing terugsturen.

U kunt bijvoorbeeld een MCP-server configureren om een AI-model te verbinden met Gmail. Wanneer u de vraag &quot;Geef me mijn laatste 5 e-mails van Gmail,&quot;naar het grote taalmodel, het ontleedt die herinnering en verzendt het naar de server Gmail MPC, die dan tot uw Gmail kan toegang hebben en de e-mails terugkeert.

De module van de Agent MCP staat u toe om een gebruikersherinnering te verwerken gebruikend een taalmodel en servers MCP.

## Voordelen om MCP in uw scenario&#39;s van de Fusie te gebruiken

Het gebruik van MCP in uw scenario&#39;s biedt de volgende voordelen:

* Het gebruiken van MCP in uw scenario vermindert de behoefte om door alle situaties en mogelijke variaties van een actie te denken. Door een herinnering te gebruiken, elimineert u de behoefte om regex te gebruiken of gegevens te ontleden om voor deze variaties rekening te houden.
* U kunt context aan de herinnering verstrekken door elementen te gebruiken die van vorige modules, of andere functies in het toewijzingspaneel in kaart worden gebracht.
* Het gebruiken van een herinnering kan efficiënter en flexibeler zijn dan het bouwen van een scenario met specifieke modules, omdat het het redeneren op de herinnering kan gebruiken en de beste cursus van actie van de beschikbare context selecteren.
* Omdat u de servers MCP vormt die de module kan verbinden met, controleert u de veiligheid voor die server, en kan zeker zijn dat de veiligheid de behoeften van uw organisatie past.

>[!NOTE]
>
>De beschikbare functionaliteit hangt van de hulpmiddelen af beschikbaar in de server MCP, en wordt niet gecontroleerd door Fusion.

## Een AI-prompt toevoegen aan uw scenario

U kunt een AI herinnering aan uw scenario toevoegen door de module van de Agent te gebruiken MCP.

Voor instructies, zie {de module van de Agent 0} MCP [.](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md)
