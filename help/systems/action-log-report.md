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

Rapporten _Åtgärdsloggar_ visar en detaljerad post över alla administratörsåtgärder som har aktiverats för loggning. Varje post är tidstämplad och registrerar användarens IP-adress och namn. Logginformationen innehåller administratörsanvändardata och relaterade ändringar som gjordes under åtgärden.

Åtgärder som du vill visa i rapporten måste vara aktiverade på skärmen [Administratörsåtgärder, loggning](action-log.md) i lagringsinställningarna. Om åtgärdstypen är markerad (aktiverad) visas dessa typer av administratörsåtgärder i rapporten Åtgärdsloggar.

Rapporten kan filtreras med hjälp av alternativen i varje kolumn. Du kan ange ett enda filteralternativ eller ange filteralternativ för flera kolumner för att begränsa rapporten till att visa specifika åtgärder. Du kan också exportera rapportdata i CSV- eller Excel XML-format.

Rapporten Åtgärdsloggar innehåller följande information:

- **[!UICONTROL Time]** - Datum och tid då åtgärden utfördes
- **[!UICONTROL Action Group]** - Visar åtgärdstypen, korrelerar till de åtgärder som har aktiverats på skärmen _Loggning av administrationsåtgärder_ i dina butiksinställningar
- **[!UICONTROL Action]** - Visar den loggade åtgärden
- **[!UICONTROL IP Address]** - Visar IP-adressen för datorn som åtgärden utfördes på
- **[!UICONTROL Username]** - Visar inloggnings-ID för den användare som utförde åtgärden
- **[!UICONTROL Result]** - Visar om användarens åtgärd lyckades eller misslyckades
- **[!UICONTROL Full Action Name]** - Visar backend-åtgärdens namn
- **[!UICONTROL Details]** - Visar kategori för backend-åtgärd
- **[!UICONTROL Full Details]** - Visar all loggad information för administratörsåtgärden

## Visa rapporten Åtgärdsloggar

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**på sidofältet_ Admin _.

   ![Åtgärdsloggar](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL View]** om du vill visa all information om en administratörsåtgärd som visas.

   ![Information om åtgärdsloggpost](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Filtrera rapporten Åtgärdsloggar

Du kan definiera fälten för filteralternativ och sedan klicka på **[!UICONTROL Search]** för att begränsa vilka åtgärder som visas.

Om du vill rensa filteralternativen och återgå till den fullständiga rapporten klickar du på **[!UICONTROL Reset Filter]**.

![Rapportfilter för åtgärdslogg](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Fält | description |
|--- |--- |
| [!UICONTROL Time] | I **[!UICONTROL From]** klickar du för att välja ett datum från den dynamiska kalendern för att definiera startdatumet för filtret. I **[!UICONTROL To]** klickar du för att välja ett datum för att definiera filtrets slutdatum. |
| [!UICONTROL Action Group] | Välj en åtgärdsgrupp. |
| [!UICONTROL Action] | Välj en åtgärd. |
| [!UICONTROL IP Address] | Ange IP-adressen till datorn som används för en åtgärd. |
| [!UICONTROL Username] | Välj ett användarnamn. Standardvärdet är `All Users`. |
| [!UICONTROL Result] | Välj Slutfört eller Fel. |
| [!UICONTROL Full Action Name] | Ange den text som sökningen ska matcha i fältet. |
| [!UICONTROL Details] | Ange den text som sökningen ska matcha i fältet. |

{style="table-layout:auto"}

## Exportera rapporten Åtgärdsloggar

1. Välj ett exportformat för **[!UICONTROL Export to]**:

   - `CSV` - en kommaavgränsad värdefil som innehåller oformaterade textdata
   - `Excel XML` - Ett XML-baserat kalkylbladsdataformat

1. Klicka på **[!UICONTROL Export]**.

   Den genererade filen sparas automatiskt i den mapp du har valt för nedladdning.

   ![Åtgärdsloggar - rapportexport](./assets/action-log-report-export.png){width="200"}
