---
title: Konfigurera smarta attribut för visuell marknadsföring
description: Lär dig hur du konfigurerar smarta attribut som används av Visual Merchandiser.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Konfigurera smarta attribut för visuell marknadsföring

{{ee-feature}}

Konfigurationen av Visual Merchandiser avgör vilka attribut som kan användas i försäljningsfönstret och miniminivån för aktieströskeln. Konfigurationen identifierar också det attribut som används för färg och ordningen för färgvärden.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Visual Merchandiser]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL General Options]**.

   ![Katalogkonfiguration - visuell handlare](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. I listan **[!UICONTROL Attributes for Category Rules]** väljer du varje attribut som du vill göra tillgängligt för visuell marknadsföring.

   Om du vill markera flera attribut håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje objekt.

1. Ange **[!UICONTROL Minimum Stock Threshold]** för att en produkt ska visas i Visual Merchandiser-fönstret.

1. Ange **[!UICONTROL Color Attribute Code]**.

   Standardvärdet är `color`. Om katalogen använder ett annat attribut anger du attributnamnet med gemener.

1. För **[!UICONTROL Color Order]** anger du varje färgvärde på en separat rad och i sekvens för att bestämma prioriteten för varje färg.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
