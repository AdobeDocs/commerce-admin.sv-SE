---
title: Önsklistorna
description: Läs mer om önskelistor och hur de kan förbättra shoppingupplevelsen och främja mer försäljning.
exl-id: 42c73566-0e32-4639-9fa2-d504fa161ebc
feature: Customers, Storefront
source-git-commit: 9fd909c5ae6d8641bf402456d94facda4a33722d
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Önsklistorna

En önskelista är en lista över produkter som en registrerad kund kan dela med vänner eller spara för att överföra till kundvagnen senare. När önskelistor är aktiverade visas länken Lägg till i önskelista på kategori- och produktsidorna för varje produkt i butiken. Beroende på temat kan det vara en textlänk eller en grafisk bild.

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce stöder användning av flera önskelistor per kundkonto.

![Magento Open Source](../assets/open-source.svg) Magento Open Source stöder användningen av en enda önskelista per kundkonto.

Delade önskelistor skickas från en e-postadress i butik, men meddelandetexten innehåller en personlig anteckning från kunden. Du kan anpassa e-postmallen som används när önskelistor delas och välja den butikskontakt som visas som avsändare.

Önsklistorna kan uppdateras från kontrollpanelen för [kundkontot](../customers/account-dashboard.md). Artiklar kan läggas till eller överföras mellan önskelistan och vagnen av kunden eller butiksadministratören.

![Exempel på storefront - Min önskelista](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

När en produkt med flera alternativ läggs till i en önskelista inkluderas alla alternativ som kunden har valt i önskelisteobjektets beskrivning. Om kunden till exempel lägger till samma par skor i tre olika färger visas varje par som ett separat önskelisteobjekt. Men om kunden lägger till samma produkt i önskelistan flera gånger visas produkten bara en gång, men med den kvantitet som valts på produktsidan.

## Önsklistehjälp i administratören

Kunder kan [hantera sina önskelistor](wishlist-storefront.md) genom att logga in på sina konton i butiken. Som butiksadministratör kan du även hantera kundernas önskelistor från administratören.

**_Så här uppdaterar du önskelisteobjekt från administratören:_**

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Hitta kunden i listan och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. I den vänstra panelen väljer du **[!UICONTROL Wish List]** och söker efter objektet som ska redigeras i listan.

   Alla alternativ som har valts för produkten visas under produktnamnet.

   ![Commerce Admin - kundönskelista](./assets/customer-wishlist-edit-admin.png){width="600" zoomable="yes"}

1. Så här redigerar du produktalternativen:

   - Klicka på **[!UICONTROL Configure]** i kolumnen **[!UICONTROL Action]**.

   - Uppdatera alternativen och **[!UICONTROL Quantity]** efter behov på produktsidan.

   - Klicka på **[!UICONTROL OK]**.

1. Klicka på **[!UICONTROL Save Customer]** eller **[!UICONTROL Save and Continue Edit]** när du är klar.
