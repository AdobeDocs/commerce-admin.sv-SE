---
title: Cron (schemalagda aktiviteter)
description: Lär dig hur du kan styra körning och schemaläggning av Commerce cron-jobb från administratören.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Cron (schemalagda aktiviteter)

Adobe Commerce och Magento Open Source utför vissa åtgärder enligt schema genom att regelbundet köra ett skript. Du kan styra körning och schemaläggning av Commerce cron-jobb från administratören. Butiksåtgärder som körs enligt ett cron-schema omfattar, men är inte begränsade till:

- [E-post](email-communications.md)
- [Katalogprisregler](../merchandising-promotions/price-rules-catalog.md)
- [Nyhetsbrev](../merchandising-promotions/newsletters.md)
- [Generering av XML-webbplatskarta](../merchandising-promotions/sitemap-xml.md)
- [Valutakursuppdateringar](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce Services måste installeras på crontab för att säkerställa att kärnkomponenter och vissa tillägg från tredje part fungerar som förväntat. Se [instruktionerna i _Installationshandbok_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) för detaljerad information om hur du installerar tjänster på crontab.

Dessutom kan du konfigurera följande så att de körs enligt ett cron-schema:

- Uppdateringar och omindexering av ordersystemets stödraster
- Löptid för väntande betalning

Se till att [bas-URL](../stores-purchase/store-urls.md) för butiken är korrekt inställda så att URL:erna som genereras under kroniåtgärder är korrekta. Information om Adobe Commerce molninfrastruktur finns på [Ställ in cron-jobb](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) i _Handbok för Commerce on Cloud Infrastructure_. Om du vill ha information på plats går du till [Konfigurera och kör ikon](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) i _Konfigurationshandbok_.

## Konfigurera cron

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Cron]** -avsnitt.

   ![Avancerad konfiguration - viktiga uppgifter](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Slutför följande inställningar för **[!UICONTROL Index]** och **[!UICONTROL Default]** grupper.

   Inställningarna är desamma i alla avsnitt.

   - **[!UICONTROL Generate Schedules Every]** - Definierar hur ofta schemat genereras (i minuter). Scheman lagras i databasen.
   - **[!UICONTROL Schedule Ahead for]** - Definierar hur långt i förväg gjorda kronijobb är schemalagda (i minuter). Om den här inställningen till exempel är inställd på `10` och cron-körningarna är schemalagda till tio minuter.
   - **[!UICONTROL Missed if not Run Within]** - Definierar tiden (i minuter) som används för att fastställa ett missat jobb. Om cron-jobbet inte körs vid den schemalagda tidpunkten och den angivna tiden går, kan det inte köras och dess status är inställd på `Missed`.
   - **[!UICONTROL History Cleanup Every]** - Definierar den tid (i minuter) som historiken för avslutade uppgifter rensas från databasen.
   - **[!UICONTROL Success History Lifetime]** - Definierar den tid (i minuter) som historiken för kronijobb med en `Successful` status finns kvar i databasen.
   - **[!UICONTROL Failure History Lifetime]** - Definierar den tid (i minuter) som historiken för kronijobb med en `Error` status finns kvar i databasen.
   - **[!UICONTROL Use Separate Process]** - Definierar om alla cron-jobb från gruppen körs i en separat systemprocess. Alternativ: `Yes` / `No`

   ![Avancerad konfiguration - kundgruppsindex](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
