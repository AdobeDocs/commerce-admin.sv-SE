---
title: Livstid för kundsession
description: Kundsessionens livstid avgör kundens köpsession.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---

# Livstid för kundsession

Livslängden för en kundshoppingsession bestäms av flera faktorer, bland annat serversessionens längd och användningen av en [beständig kundvagn](../stores-purchase/cart-persistent.md), och hur länge information som lagras i webbläsaren är kvar. Även om dessa är relaterade till samma kundupplevelse är de separata processer med olika förfallohändelser och livstider.

| Process | Beskrivning |
| --- | --- |
| Session | Information som lagras på servern, till exempel innehållet i kundvagnen. Om serversessionen går ut innan cookien går ut kan kunderna förlora kundvagnens innehåll och minska säkerhetsrisken. |
| Sessionscookie | Information som lagras i webbläsaren som ett antal eller en teckensträng. Om sessionscookie-filen upphör att gälla före serversessionen loggas kunden ut. Sessionskakan tas bort när kunden stänger webbläsarfönstret. Som standard är cookie-livstiden 3 600 sekunder, eller en timme. Om det inte finns någon tangentbordsaktivitet under den tiden avslutas den aktuella sessionen och kunderna måste logga in på sina konton för att kunna fortsätta handla. |

{style="table-layout:auto"}

If [Beständig kundvagn](../stores-purchase/cart-persistent.md) är aktiverat sparas kundvagnens innehåll nästa gång kunderna loggar in på sina konton. När du använder en beständig kundvagn bör du ange serversessionens livstid och sessionscookien till en lång tidsperiod.

På servern styrs sessionens längd av `php.ini` och flera variabler. För närvarande har Adobe Commerce ingen administratörskonfigurationsinställning som styr längden på serversessionen.

## Konfigurera cookie-livstid

1. På _Administratör_ sidebar, gå till [!UICONTROL **Lager**] > _[!UICONTROL Settings]_>[!UICONTROL **Konfiguration**].

1. Om du har flera butiker anger du **[!UICONTROL Store View]** Välj i det övre högra hörnet i den butik där konfigurationen gäller.

1. I den vänstra panelen under **[!UICONTROL General]**, välja **[!UICONTROL Web]**.

1. Expandera avsnittet **[!UICONTROL Default Cookie Settings]**.

   ![Inställningar för standardcookie](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Om du vill ändra standardinställningen rensar du **[!UICONTROL Use system value]** och ange det nya värdet i sekunder.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Konfigurera _Kom ihåg mig_ funktionalitet

För att underlätta inloggningen finns **[!UICONTROL Remember Me]** funktionen gör att kontoinnehavare inte kan ange sina inloggningsuppgifter varje gång de öppnar butiken. Av säkerhetsskäl är beständighetsfunktionen inaktiverad som standard.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Persistent Shopping Cart]**.

1. Expandera avsnittet **[!UICONTROL General Options]**.

1. För **[!UICONTROL Enable Persistence]**, ställs in på `Yes`. (Rensa **[!UICONTROL Use system value]** om du vill tillåta ändring av standardinställningen.)

1. För **[!UICONTROL Enable "Remember Me"]**, ställs in på `Yes` eller `No` enligt dina krav.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
