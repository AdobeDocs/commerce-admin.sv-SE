---
title: Cron (schemalagda aktiviteter)
description: Lär dig hur du styr körning och schemaläggning av Commerce cron-jobb i Admin.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Cron (schemalagda aktiviteter)

Adobe Commerce och Magento Open Source utför vissa åtgärder enligt schema genom att regelbundet köra ett skript. Du kan styra körning och schemaläggning av Commerce cron-jobb från Admin. Butiksåtgärder som körs enligt ett cron-schema omfattar, men är inte begränsade till:

- [E-post](email-communications.md)
- [Katalogprisregler](../merchandising-promotions/price-rules-catalog.md)
- [Nyhetsbrev](../merchandising-promotions/newsletters.md)
- [Generering av XML-webbplatskarta](../merchandising-promotions/sitemap-xml.md)
- [Valutakursuppdateringar](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce tjänster måste installeras i crontab för att säkerställa att kärnkomponenterna och vissa tillägg från tredje part fungerar som förväntat. Mer information om hur du installerar tjänster på crontab finns i [instruktionerna i _installationshandboken_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=sv-SE).

Dessutom kan du konfigurera följande så att de körs enligt ett cron-schema:

- Uppdateringar och omindexering av ordersystemets stödraster
- Löptid för väntande betalning

Kontrollera att [bas-URL:erna](../stores-purchase/store-urls.md) för arkivet är korrekt inställda så att URL:erna som genereras under kroniåtgärder är korrekta. Information om Adobe Commerce i molninfrastruktur finns i [Konfigurera kundjobben](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html?lang=sv-SE) i _Commerce i molninfrastrukturguiden_. Information om lokala inställningar finns i [Konfigurera och kör ikon](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=sv-SE) i _konfigurationshandboken_.

## Konfigurera cron

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Cron]**.

   ![Avancerad konfiguration - viktiga uppgifter](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Slutför följande inställningar för grupperna **[!UICONTROL Index]** och **[!UICONTROL Default]**.

   Inställningarna är desamma i alla avsnitt.

   - **[!UICONTROL Generate Schedules Every]** - Definierar hur ofta schemat genereras (i minuter). Scheman lagras i databasen.
   - **[!UICONTROL Schedule Ahead for]** - Definierar hur långt i förväg gjorda kronijobb är schemalagda (i minuter). Om den här inställningen till exempel är inställd på `10` och kron körs, schemaläggs kron-jobb för de kommande 10 minuterna.
   - **[!UICONTROL Missed if not Run Within]** - Definierar tiden (i minuter) som används för att fastställa ett missat jobb. Om cron-jobbet inte körs vid den schemalagda tidpunkten och den angivna tiden går, kan det inte köras och dess status är inställd på `Missed`.
   - **[!UICONTROL History Cleanup Every]** - Definierar den tid (i minuter) som historiken för avslutade uppgifter rensas från databasen.
   - **[!UICONTROL Success History Lifetime]** - Definierar den tid (i minuter) som historiken för kronijobb med statusen `Successful` finns kvar i databasen.
   - **[!UICONTROL Failure History Lifetime]** - Definierar den tid (i minuter) som historiken för kronijobb med statusen `Error` finns kvar i databasen.
   - **[!UICONTROL Use Separate Process]** - Definierar om alla cron-jobb från gruppen körs i en separat systemprocess. Alternativ: `Yes` / `No`

   ![Avancerad konfiguration - kundgruppsindex](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
