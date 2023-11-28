---
title: "Konfigurera [!DNL Inventory Management] globala alternativ"
description: Lär dig hur du konfigurerar standardinställningarna [!DNL Inventory Management] konfigurationsalternativ för produkt och lager för dina webbplatser.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Konfigurera [!DNL Inventory Management] globala alternativ

Konfigurera standardkonfigurationsalternativen för produkter och lager för dina webbplatser. Vissa av dessa inställningar kan åsidosättas per produkt via [Konfigurerar produktalternativ](product-options.md). Information om hur du konfigurerar inställningarna för avståndsprioritet finns i [Konfigurerar algoritmen för avståndsprioritet](distance-priority-algorithm.md).

## Konfigurera produkt- och Stock-alternativ globalt

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Inventory]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Stock Options]** och ange alternativ:

   ![Alternativ för Stock](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Om du vill justera lagerbehållningen när en order placeras anger du **[!UICONTROL Decrease Stock When Order is Placed]** till `Yes`.

   - Om du vill returnera artiklar till lager om en order annulleras, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** till `Yes`.

   - Om du vill fortsätta visa produkter i katalogen som inte längre finns i lager anger du **[!UICONTROL Display Out of Stock Products]** till `Yes`.

   - If [prisaviseringar](alert-setup.md) aktiveras kan kunderna registrera sig för att få meddelanden när produkten är tillbaka i lager.

   - Ange ett belopp för att ange hur den sista återstående lagermängden ska visas på produktsidan **[!UICONTROL Only X left Threshold]**.

     Meddelandet visas när lagerkvantiteten når tröskelvärdet. Om den till exempel är inställd på `3`, meddelandet `Only 3 left` visas när lagerkvantiteten når tre. Meddelandet justeras så att kvantiteten i lager återspeglas tills kvantiteten når noll.

   - Om du vill visa ett In Stock- eller Out of Stock-meddelande på produktsidan anger du **[!UICONTROL Display Products Availability In Stock on Storefront]** till `Yes`.

   - Om du vill kontrollera lagret när en produkt läses in i kundvagnen anger du **[!UICONTROL Enable Inventory Check On Cart Load]** till `Yes`. När det här alternativet är inaktiverat hoppas lagerkontrollen över. Om du inaktiverar det här alternativet går det snabbare att checka ut, särskilt om det finns många artiklar i kundvagnen. Men om du hoppar över förvalidering kan kunderna se fel som inte finns i lager senare i utcheckningsprocessen.

   - För att säkerställa konsekvens mellan lager och katalog anger du **[!UICONTROL Synchronize with Catalog]** till `Yes`. När det här alternativet är aktiverat justeras lagerdata efter katalogändringarna (t.ex. borttagen produkt, ändrad produkt-SKU och ändrad produkttyp).

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Product Stock Options]** och ange alternativ:

   - Aktivera [lagerstyrning](enable.md) för katalogen, ange **[!UICONTROL Manage Stock]** till `Yes`.

     ![ProduktStock-alternativ](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Backorders]** till något av följande:

     | Alternativ | Beskrivning |
     | ----- | ----- |
     | `No Backorders` | [Restorder](backorders.md) godkänns inte när produkten inte finns i lager. |
     | `Allow Qty Below 0` | Restorder accepteras när kvantiteten är under noll. |
     | `Allow Qty Below 0 and Notify Customer` | Restorder accepteras när kvantiteten underskrider noll och systemet meddelar kunden om att ordern fortfarande kan läggas. |

   - Ange **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Ange ett belopp för **[!UICONTROL Out-of-Stock Threshold]**:

     | Värde | Beskrivning |
     | ----- |-----|
     | Positivt belopp | Om du har inaktiverat Restorder anger du ett positivt belopp. |
     | Noll | Med Restorder aktiverat, går `0` ger oändliga efterbeställningar. |
     | Negativt belopp | Om du aktiverar Restorder bör du ange ett negativt belopp. Beloppet läggs till i den säljbara kvantiteten. Skriv till exempel `-50` för att tillåta order upp till detta belopp. |

   - Ange **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** för valda grupper och belopp.

   - För **[!UICONTROL Notify for Quantity Below]** anger du den lagernivå som utlöser ett meddelande om att artikeln inte finns i lager.

   - Om du vill aktivera kvantitetsökningar för produkten anger du **[!UICONTROL Enable Qty Increments]** till `Yes`. Sedan för **[!UICONTROL Qty Increments]**, ange antalet artiklar som måste köpas för att uppfylla kravet.

     En artikel som säljs i steg om sex kan till exempel köpas i kvantiteter om `6`, `12`, `18`och så vidare.

   - För [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** är inställd på `No`. När du skickar en kreditnota anger och väljer du att returnera aktien till källor.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Admin bulk operations]** och ange alternativ:

   ![Admin - gruppåtgärder](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Run asynchronously]** köra massåtgärder asynkront för massproduktåtgärder

     De här åtgärderna omfattar [tilldela och ta bort tilldelning av källor](bulk-assignment.md)och [överföra lager till källa](inventory-transfer.md). Den samlar in massåtgärder upp till den asynkrona gruppstorleken och kör sedan dessa åtgärder. Det här alternativet är inaktiverat som standard. Vi rekommenderar att du granskar prestanda med gruppåtgärder innan du aktiverar.

     >[!NOTE]
     >
     >Konfigurera och ge support _asynkrona köhanterare_ måste du ange ett kommando via kommandoraden. Det här steget kan kräva utvecklarhjälp. Se [Starta användare i meddelandekön](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) i _Konfigurationshandbok_.

   - Om den är aktiverad anger du **[!UICONTROL Asynchronous batch size]**. Standardbatchstorleken är 100. När massprocesser når den här mängden utlöses den av systemet.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
