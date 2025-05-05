---
title: "Konfigurera [!DNL Inventory Management] globala alternativ"
description: Lär dig hur du konfigurerar  [!DNL Inventory Management] standardkonfigurationsalternativen för produkter och resurser för dina webbplatser.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Konfigurera globala alternativ för [!DNL Inventory Management]

Konfigurera standardkonfigurationsalternativen för produkter och lager för dina webbplatser. Vissa av dessa inställningar kan åsidosättas per produkt genom [Konfigurera produktalternativ](product-options.md). Mer information om hur du konfigurerar inställningarna för avståndsprioritet finns i [Konfigurera algoritm för avståndsprioritet](distance-priority-algorithm.md).

## Konfigurera produkt- och Stock-alternativ globalt

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Inventory]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Stock Options]** och ange alternativen:

   ![Alternativ för Stock](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Ställ in **[!UICONTROL Decrease Stock When Order is Placed]** på `Yes` om du vill justera lagerbehållningen när en order placeras.

   - Om du vill returnera artiklar till Stock om en order avbryts, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** till `Yes`.

   - Om du vill fortsätta visa produkter i katalogen som inte längre finns i lager anger du **[!UICONTROL Display Out of Stock Products]** till `Yes`.

   - Om [prisaviseringar](alert-setup.md) är aktiverade kan kunderna registrera sig för att få meddelanden när produkten är tillbaka i lager.

   - Ange ett belopp för **[!UICONTROL Only X left Threshold]** om du vill ange startvärdet för att visa det sista återstående lagerbeloppet på produktsidan.

     Meddelandet visas när lagerkvantiteten når tröskelvärdet. Om värdet till exempel är `3` visas meddelandet `Only 3 left` när lagerkvantiteten är tre. Meddelandet justeras så att kvantiteten i lager återspeglas tills kvantiteten når noll.

   - Om du vill visa ett In Stock- eller Out of Stock-meddelande på produktsidan anger du **[!UICONTROL Display Products Availability In Stock on Storefront]** till `Yes`.

   - Om du vill kontrollera lagret när en produkt läses in i kundvagnen anger du **[!UICONTROL Enable Inventory Check On Cart Load]** till `Yes`. När det här alternativet är inaktiverat hoppas lagerkontrollen över. Om du inaktiverar det här alternativet går det snabbare att checka ut, särskilt om det finns många artiklar i kundvagnen. Men om du hoppar över förvalidering kan kunderna se fel som inte finns i lager senare i utcheckningsprocessen.

   - Ställ in **[!UICONTROL Synchronize with Catalog]** på `Yes` om du vill att lagret och katalogen ska vara konsekventa. När det här alternativet är aktiverat justeras lagerdata efter katalogändringarna (t.ex. borttagen produkt, ändrad produkt-SKU och ändrad produkttyp).

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Product Stock Options]** och ange alternativen:

   - Om du vill aktivera [lagerkontrollen](enable.md) för din katalog anger du **[!UICONTROL Manage Stock]** till `Yes`.

     ![ProduktStock-alternativ](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Backorders]** till något av följande:

     | Alternativ | Beskrivning |
     | ----- | ----- |
     | `No Backorders` | [Restorder](backorders.md) accepteras inte när produkten inte finns i lager. |
     | `Allow Qty Below 0` | Restorder accepteras när kvantiteten är under noll. |
     | `Allow Qty Below 0 and Notify Customer` | Restorder accepteras när kvantiteten underskrider noll och systemet meddelar kunden om att ordern fortfarande kan läggas. |

   - Ange **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Ange ett belopp för **[!UICONTROL Out-of-Stock Threshold]**:

     | Värde | Beskrivning |
     | ----- |-----|
     | Positivt belopp | Om du har inaktiverat Restorder anger du ett positivt belopp. |
     | Noll | Om du aktiverar Restorder kan du ange `0` för oändliga backorder. |
     | Negativt belopp | Om du aktiverar Restorder bör du ange ett negativt belopp. Beloppet läggs till i den säljbara kvantiteten. Ange till exempel `-50` om du vill tillåta order upp till detta belopp. |

   - Ange **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** för vald grupp och belopp.

   - För **[!UICONTROL Notify for Quantity Below]** anger du den lagernivå som utlöser ett meddelande om att artikeln inte finns i lager.

   - Om du vill aktivera kvantitetsökningar för produkten anger du **[!UICONTROL Enable Qty Increments]** till `Yes`. För **[!UICONTROL Qty Increments]** anger du sedan antalet artiklar som måste köpas för att uppfylla kravet.

     Till exempel kan ett objekt som säljs i steg om sex köpas i kvantiteter om `6`, `12`, `18` och så vidare.

   - För [!DNL Inventory Management] är **[!UICONTROL Automatically Return Credit Memo Item to Stock]** inställt på `No`. När du skickar en kreditnota anger och väljer du att returnera aktien till källor.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Admin bulk operations]** och ange alternativen:

   ![Admin - gruppåtgärder](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Ange att **[!UICONTROL Run asynchronously]** ska köra massåtgärder asynkront för massproduktåtgärder

     De här åtgärderna omfattar [tilldelning och frigörande av källor](bulk-assignment.md) och [överföring av lager till källan](inventory-transfer.md). Den samlar in massåtgärder upp till den asynkrona gruppstorleken och kör sedan dessa åtgärder. Det här alternativet är inaktiverat som standard. Vi rekommenderar att du granskar prestanda med gruppåtgärder innan du aktiverar.

     >[!NOTE]
     >
     >Om du vill konfigurera och ge stöd för _asynkrona köhanterare_ måste du skapa ett kommando via kommandoraden. Det här steget kan kräva utvecklarhjälp. Se [Starta meddelandekökonsumenter](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) i _Konfigurationshandboken_.

   - Om det är aktiverat anger du **[!UICONTROL Asynchronous batch size]**. Standardbatchstorleken är 100. När massprocesser når den här mängden utlöses den av systemet.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
