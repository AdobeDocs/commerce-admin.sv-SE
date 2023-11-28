---
title: "Aktivera [!DNL Inventory Management]"
description: Lär dig hur du aktiverar [!DNL Inventory Management] på global butiks- eller produktnivå.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Aktivera [!DNL Inventory Management]

Om du vill hantera ditt produktlager aktiverar du [!DNL Inventory Management] på global butiks- eller produktnivå. När _Hantera Stock_ alternativet är aktiverat, [!DNL Inventory Management] spårar automatiskt produktkvantiteter som är tillgängliga för webbplatsen via konfigurerade lager och källor. Alla funktioner och alternativ börjar spåra och rapportera när de är aktiverade, utan ytterligare konfigurering.

Er verksamhet körs och lagrar uppdateringar i takt med försäljningen. När kunderna handlar får ni exakt och uppdaterad information om tillgängliga lager per försäljningskanal och källa. Tillgängliga saldokvantiteter uppdateras per lager när kunderna lägger till produkter i varukorgen och slutför inköp samt när och när ni hanterar order, skapar leveranser och utfärdar återbetalningar. Tillgång till nya eller överförda arkivuppdateringar till era källor som är omedelbart tillgängliga för onlineförsäljning. Restorder slutförs upp till angivna tröskelvärden utan oändliga order eller ytterligare konfigurationer. Och ni anger och slutför partiella eller fullständiga leveranser från en eller flera källor med rekommendationer, vilket ger er fullständig kontroll över orderuppfyllelse och lagerbehållning.

>[!NOTE]
>
>Som standard [!DNL Inventory Management] aktiveras vid installation eller uppgradering [!DNL Commerce]. Beroende på ditt företags behov kan du aktivera eller inaktivera den spårade [!DNL Inventory Management] inom [!DNL Commerce].

Så här fungerar inställningen i enkät- och flerkällsinventeringar:

- Används [!DNL Inventory Management], aktivera _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] inställningarna på produktnivåkonfigurationen åsidosätter butikskonfigurationen.

- Om du vill använda orderhantering eller tredjepartstjänster (t.ex. ERP) inaktiverar du [!UICONTROL Manage Stock].

- Om systemstandardkonfigurationen används för produktnivåkonfigurationen åsidosätts butikskonfigurationen.

Med [!DNL Inventory Management] aktiverat, se följande för att konfigurera alla inställningar:

- [Konfigurerar globala alternativ](global-options.md) - Inställningar som påverkar hela katalogen är systemets standardinställningar.

- [Konfigurerar produktalternativ](product-options.md) - Inställningar för en specifik produkt som åsidosätter globala alternativ.

## Aktivera eller inaktivera [!DNL Inventory Management]

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Inventory]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) _ProduktStock-alternativ_ och konfigurera:

   ![ProduktStock-alternativ](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - För att hantera lager och använda alla [!DNL Commerce] funktioner, ange **[!UICONTROL Manage Stock]** till `Yes` (standard).

   - Inaktivera [!DNL Inventory Management]avmarkera **[!UICONTROL Use system value]** kryssruta och ange **[!UICONTROL Manage Stock]** till `No`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Hantera lager för en butik

Se [Konfigurera globala alternativ](global-options.md).

## Hantera lager för en produkt

Se [Konfigurerar produktalternativ](product-options.md).
