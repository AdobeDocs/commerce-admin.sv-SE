---
title: Administratörsverktygen och arbetsytan
description: Lär dig mer om Admin-arbetsytan, som ger tillgång till alla verktyg, data och innehåll som används för att köra din butik.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Administratörsverktygen och arbetsytan

På arbetsytan Admin får du tillgång till alla verktyg, data och innehåll som används för att köra din butik. Standardstartsidan kan ställas in i konfigurationen. Många administratörssidor har ett rutnät som visar data för avsnittet, med en uppsättning verktyg för att söka, sortera, filtrera, markera och använda åtgärder. Som standard är [Instrumentpanelen](admin-dashboard.md) startsidan för administratören. Du kan dock välja att en annan sida ska visas som startsida när du loggar in. Du kan klicka på logotypen i sidofältet Admin för att gå tillbaka till startsidan för Admin.

![Admin - arbetsyta](./assets/admin-workspace.png){zoomable="yes"}

## Workspace

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Global Search] | Sökikonen längst upp till höger kan användas för att hitta valfritt värde i databasen, inklusive produkt-, kund- och orderposter. |
| [!UICONTROL Grid Search] | Du kan använda sökrutan ovanför stödrastret för att snabbt filtrera visningen av stödrastret baserat på nyckelord som finns i posterna. |
| [!UICONTROL Sort] | Rubriken för varje kolumn kan användas för att sortera listan i stigande eller fallande ordning. |
| [!UICONTROL Filters] | Definierar en uppsättning sökparametrar som bestämmer vilka poster som visas i rutnätet. Dessutom kan filtren i huvudet i vissa kolumner användas för att begränsa listan till specifika värden. Vissa filter har ytterligare alternativ som kan väljas i en listruta. |
| [!UICONTROL Default View] | Anger stödrastrets standardkolumnlayout. |
| [!UICONTROL Columns] | Bestämmer markeringen av [kolumner](admin-grid-controls.md) och deras ordning i rutnätet. Kolumnlayouten kan ändras och sparas som en _vy_. Som standard inkluderas bara vissa av kolumnerna i rutnätet. |
| [!UICONTROL Paginate] | Sidnumreringskontrollerna används för att visa ytterligare resultatsidor. |
| [!UICONTROL Actions] | Kontrollen Åtgärder använder en åtgärd på alla markerade poster. |
| [!UICONTROL Select] | Kontrollen Välj används för att markera flera poster som ska bli åtgärdsmål. Alternativ: `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Workspace Search

Om du vill hitta en post i databasen använder du förstoringsglaset i huvudet för _Admin_. Resultatet kan vara kunder, produkter, beställningar eller andra relaterade attribut. Om du till exempel anger ett kundnamn kan resultatet innehålla kundposten och alla order som är kopplade till namnet.

![Administratörssökverktyget](./assets/admin-search.png){width="700" zoomable="yes"}

1. Klicka på ikonen _Sök_ (![förstoringsglas](../assets/icon-magnify-search.png)) i sidhuvudet för att öppna sökrutan.

1. Gör något av följande:

   - Om du vill hitta en matchning anger du de första bokstäverna i det du vill hitta.
   - Om du vill hitta en exakt matchning anger du det eller de ord du vill söka efter.

1. Klicka på ett objekt för att öppna posten i de sökresultat som visas.

## Ändra startsidan för Admin

[Kontrollpanelen](admin-workspace.md#the-dashboard) är standardstartsidan för administratören, men du kan konfigurera en annan startsida.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Välj **[!UICONTROL Admin]** i den vänstra navigeringspanelen under **[!UICONTROL Advanced]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Startup Page]**.

   ![Avancerad konfiguration - inställning för startsida för administratör](./assets/admin-startup-page.png){width="600"}

1. Ange **[!UICONTROL Startup Page]** på sidan som du vill ska visas först när du har loggat in på Admin.

   En detaljerad lista över alla administratörsalternativ finns i [Admin](../configuration-reference/advanced/admin.md) i _Konfigurationsreferens_.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
