---
title: Nyhetsbrev och prenumerationer
description: Lär dig mer om nyhetsbrev och hur du aktiverar den här funktionen som ett prisvärt kampanjverktyg.
exl-id: ad4488c2-1b8b-4326-8486-743c75c5b9a6
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Nyhetsbrev och prenumerationer

Att publicera ett regelbundet nyhetsbrev anses vara ett av de mest kraftfulla och prisvärda marknadsföringsverktygen som finns. Commerce ger er möjlighet att publicera och distribuera nyhetsbrev till kunder som har prenumererat, plus verktyg för att ta fram nyhetsbrevet, skapa och hantera listor över prenumeranter, utveckla innehåll och skicka trafik till er butik. Du kan också använda [sidhierarkin](../content-design/page-hierarchy.md) för att skapa ett arkiv med tidigare utgåvor.

>[!NOTE]
>
>Du kan lägga till funktioner genom att integrera din Commerce-instans med en tredjepartsleverantör av nyhetsbrev och genom att lägga till tillägg. Mer information finns i [Commerce Marketplace](../getting-started/commerce-marketplace.md).

Det första steget när du skapar nyhetsbrev är att konfigurera inställningarna för nyhetsbrevet för webbplatsen. Du kan kräva att kunderna klickar på en bekräftelselänk som skickas med e-post för att bekräfta prenumerationen. Den här metoden med dubbel anmälan kräver att kunderna bekräftar två gånger att de vill få nyhetsbrevet och minskar risken för att det kan betraktas som skräppost.

## Aktivera nyhetsbrev

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Newsletter]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL General Options]**.

1. Om du vill aktivera nyhetsbrev för butiksvyns omfång anger du **[!UICONTROL Enabled]** till `Yes`.

När du har aktiverat nyhetsbrevsfunktionen visas avsnittet _[!UICONTROL Subscription Options]_.

## Konfigurera prenumerationsalternativen

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Newsletter]**.

1. Om det behövs kan du [ändra konfigurationsomfånget](../getting-started/websites-stores-views.md#scope-settings) för att tillämpa konfigurationsändringarna för nyhetsbrevet på en viss plats/butiksvy.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Subscription Options]** och gör följande:

   ![Kundkonfiguration - prenumerationer på nyhetsbrev](../configuration-reference/customers/assets/newsletter-subscription-options.png){width="600" zoomable="yes"}

   - Bekräfta e-postmallen och avsändaren av följande e-postmeddelanden som skickas till prenumeranter:

      - [!UICONTROL Success email]
      - [!UICONTROL Confirmation email]
      - [!UICONTROL Unsubscribe email]

   - Om du vill använda processen för dubbel anmälan för att bekräfta prenumerationer anger du **[!UICONTROL Need to Confirm]** till `Yes`.

   - Om du vill tillåta personer som inte har något konto hos din butik att prenumerera på nyhetsbrevet anger du **[!UICONTROL Allow Guest Subscription]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
