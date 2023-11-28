---
title: Åtgärdsloggsrapport
description: Lär dig hur du visar, filtrerar och exporterar rapporten Åtgärdslogg, som innehåller en detaljerad beskrivning av alla loggaktiverade administratörsåtgärder.
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Åtgärdsloggsrapport

{{ee-feature}}

The _Åtgärdsloggar_ rapporten innehåller en detaljerad post över alla Admin-åtgärder som har aktiverats för loggning. Varje post är tidstämplad och registrerar användarens IP-adress och namn. Logginformationen innehåller administratörsanvändardata och relaterade ändringar som gjordes under åtgärden.

Åtgärder som du vill visa i rapporten måste vara aktiverade i [Loggning av administratörsåtgärder](action-log.md) i butiksinställningarna. Om åtgärdstypen är markerad (aktiverad) visas dessa typer av administratörsåtgärder i rapporten Åtgärdsloggar.

Rapporten kan filtreras med hjälp av alternativen i varje kolumn. Du kan ange ett enda filteralternativ eller ange filteralternativ för flera kolumner för att begränsa rapporten till att visa specifika åtgärder. Du kan också exportera rapportdata i CSV- eller Excel XML-format.

Rapporten Åtgärdsloggar innehåller följande information:

- **[!UICONTROL Time]** - datum och tid då åtgärden utfördes
- **[!UICONTROL Action Group]** - Visar åtgärdstypen, korrelerar till de åtgärder som är aktiverade på _Loggning av administratörsåtgärder_ skärm i dina butiksinställningar
- **[!UICONTROL Action]** - Visar den loggade åtgärden
- **[!UICONTROL IP Address]** - Visar IP-adressen för datorn som åtgärden utfördes på
- **[!UICONTROL Username]** - Visar inloggnings-ID för den användare som utförde åtgärden
- **[!UICONTROL Result]** - Visar om användarens åtgärd lyckades eller inte
- **[!UICONTROL Full Action Name]** - Visar backend-åtgärdens namn
- **[!UICONTROL Details]** - Visar kategorin för serverdelsåtgärd
- **[!UICONTROL Full Details]** - Visar all loggad information om administratörsåtgärden

## Visa rapporten Åtgärdsloggar

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![Åtgärdsloggar](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Om du vill visa all information om en administratörsåtgärd i listan klickar du på **[!UICONTROL View]**.

   ![Information om loggpost för åtgärd](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Filtrera rapporten Åtgärdsloggar

Du kan definiera fälten för filteralternativ och sedan klicka på **[!UICONTROL Search]** för att begränsa vilka åtgärder som visas.

Om du vill rensa filteralternativen och återgå till den fullständiga rapporten klickar du på **[!UICONTROL Reset Filter]**.

![Rapportfilter för åtgärdslogg](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Fält | description |
|--- |--- |
| [!UICONTROL Time] | I **[!UICONTROL From]** klickar du för att välja ett datum i den dynamiska kalendern för att definiera startdatumet för filtret. I **[!UICONTROL To]** klickar du för att välja ett datum för att definiera filtrets slutdatum. |
| [!UICONTROL Action Group] | Välj en åtgärdsgrupp. |
| [!UICONTROL Action] | Välj en åtgärd. |
| [!UICONTROL IP Address] | Ange IP-adressen till datorn som används för en åtgärd. |
| [!UICONTROL Username] | Välj ett användarnamn. Standard är `All Users`. |
| [!UICONTROL Result] | Välj Slutfört eller Fel. |
| [!UICONTROL Full Action Name] | Ange den text som sökningen ska matcha i fältet. |
| [!UICONTROL Details] | Ange den text som sökningen ska matcha i fältet. |

{style="table-layout:auto"}

## Exportera rapporten Åtgärdsloggar

1. För **[!UICONTROL Export to]** väljer du ett exportformat:

   - `CSV` - en kommaavgränsad värdefil som innehåller oformaterade textdata
   - `Excel XML` - Ett XML-baserat kalkylbladsdataformat

1. Klicka på **[!UICONTROL Export]**.

   Den genererade filen sparas automatiskt i den mapp du har valt för nedladdning.

   ![Export av åtgärdsloggar](./assets/action-log-report-export.png){width="200"}
