---
title: Administratörsverktygen och arbetsytan
description: Lär dig mer om Admin-arbetsytan, som ger tillgång till alla verktyg, data och innehåll som används för att köra din butik.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Administratörsverktygen och arbetsytan

På arbetsytan Admin får du tillgång till alla verktyg, data och innehåll som används för att köra din butik. Standardstartsidan kan ställas in i konfigurationen. Många administratörssidor har ett rutnät som visar data för avsnittet, med en uppsättning verktyg för att söka, sortera, filtrera, markera och använda åtgärder. Som standard är [Kontrollpanel](admin-dashboard.md) är startsidan för administratören. Du kan dock välja att en annan sida ska visas som startsida när du loggar in. Du kan klicka på logotypen i sidofältet Admin för att gå tillbaka till startsidan för Admin.

![Administratör - arbetsyta](./assets/admin-workspace.png){zoomable=&quot;yes&quot;}

## Arbetsytekontroller

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Global Search] | Sökikonen längst upp till höger kan användas för att hitta valfritt värde i databasen, inklusive produkt-, kund- och orderposter. |
| [!UICONTROL Grid Search] | Du kan använda sökrutan ovanför stödrastret för att snabbt filtrera visningen av stödrastret baserat på nyckelord som finns i posterna. |
| [!UICONTROL Sort] | Rubriken för varje kolumn kan användas för att sortera listan i stigande eller fallande ordning. |
| [!UICONTROL Filters] | Definierar en uppsättning sökparametrar som bestämmer vilka poster som visas i rutnätet. Dessutom kan filtren i huvudet i vissa kolumner användas för att begränsa listan till specifika värden. Vissa filter har ytterligare alternativ som kan väljas i en listruta. |
| [!UICONTROL Default View] | Anger stödrastrets standardkolumnlayout. |
| [!UICONTROL Columns] | Bestämmer markeringen för [kolumner](admin-grid-controls.md) och deras ordning i rutnätet. Kolumnlayouten kan ändras och sparas som _visa_. Som standard inkluderas bara vissa av kolumnerna i rutnätet. |
| [!UICONTROL Paginate] | Sidnumreringskontrollerna används för att visa ytterligare resultatsidor. |
| [!UICONTROL Actions] | Kontrollen Åtgärder använder en åtgärd på alla markerade poster. |
| [!UICONTROL Select] | Kontrollen Välj används för att markera flera poster som ska bli åtgärdsmål. Alternativ: `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Arbetsytesökning

Om du vill söka efter en post i databasen använder du förstoringsglaset i huvudet på _Administratör_. Resultatet kan vara kunder, produkter, beställningar eller andra relaterade attribut. Om du till exempel anger ett kundnamn kan resultatet innehålla kundposten och alla order som är kopplade till namnet.

![Sökverktyg för administratörer](./assets/admin-search.png){width="700" zoomable="yes"}

1. Klicka på _Sök_ (![förstoringsglas](../assets/icon-magnify-search.png)) för att öppna sökrutan.

1. Gör något av följande:

   - Om du vill hitta en matchning anger du de första bokstäverna i det du vill hitta.
   - Om du vill hitta en exakt matchning anger du det eller de ord du vill söka efter.

1. Klicka på ett objekt för att öppna posten i de sökresultat som visas.

## Ändra startsidan för Admin

The [kontrollpanel](admin-workspace.md#the-dashboard) är standardstartsidan för Admin, men du kan konfigurera en annan startsida.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra navigeringspanelen under **[!UICONTROL Advanced]**, välja **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Startup Page]** -avsnitt.

   ![Avancerad konfiguration - Administratörens startsidinställning](./assets/admin-startup-page.png){width="600"}

1. Ange **[!UICONTROL Startup Page]** till den sida som du vill ska visas först när du har loggat in på Admin.

   En detaljerad lista över alla administratörsalternativ finns i [Administratör](../configuration-reference/advanced/admin.md) i _Konfigurationsreferens_.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
