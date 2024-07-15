---
title: "Aktivera [!DNL Inventory Management]"
description: Lär dig hur du aktiverar  [!DNL Inventory Management]  på global butik eller produktnivå.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Aktivera [!DNL Inventory Management]

Aktivera [!DNL Inventory Management] på global butik eller produktnivå om du vill hantera produktlagret. När alternativet _Hantera Stock_ är aktiverat spårar [!DNL Inventory Management] automatiskt produktkvantiteter som är tillgängliga för platsen via konfigurerade lager och källor. Alla funktioner och alternativ börjar spåra och rapportera när de är aktiverade, utan ytterligare konfigurering.

Er verksamhet körs och lagrar uppdateringar i takt med försäljningen. När kunderna handlar får ni exakt och uppdaterad information om tillgängliga lager per försäljningskanal och källa. Tillgängliga saldokvantiteter uppdateras per lager när kunderna lägger till produkter i varukorgen och slutför inköp samt när och när ni hanterar order, skapar leveranser och utfärdar återbetalningar. Tillgång till nya eller överförda arkivuppdateringar till era källor som är omedelbart tillgängliga för onlineförsäljning. Restorder slutförs upp till angivna tröskelvärden utan oändliga order eller ytterligare konfigurationer. Och ni anger och slutför partiella eller fullständiga leveranser från en eller flera källor med rekommendationer, vilket ger er fullständig kontroll över orderuppfyllelse och lagerbehållning.

>[!NOTE]
>
>Som standard är [!DNL Inventory Management] aktiverat när du installerar eller uppgraderar [!DNL Commerce]. Beroende på ditt företags behov kan du aktivera eller inaktivera den spårade [!DNL Inventory Management] i [!DNL Commerce].

Så här fungerar inställningen i enkät- och flerkällsinventeringar:

- Aktivera _[!UICONTROL Manage Stock]_om du vill använda [!DNL Inventory Management].

- [!UICONTROL Manage Stock]-inställningarna på produktnivåkonfigurationen åsidosätter butikskonfigurationen.

- Inaktivera [!UICONTROL Manage Stock] om du vill använda Order Management eller tredjepartstjänster (till exempel ERP).

- Om systemstandardkonfigurationen används för produktnivåkonfigurationen åsidosätts butikskonfigurationen.

När [!DNL Inventory Management] är aktiverat kan du se följande för att konfigurera alla inställningar:

- [Konfigurerar globala alternativ](global-options.md) - Inställningar som påverkar hela katalogen är systemets standardinställningar.

- [Konfigurerar produktalternativ](product-options.md) - Inställningar för en specifik produkt som åsidosätter globala alternativ.

## Aktivera eller inaktivera [!DNL Inventory Management]

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Inventory]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) _Alternativ för produktlager_ och konfigurera:

   ![ProduktStock-alternativ](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Om du vill hantera lager och använda alla [!DNL Commerce]-funktioner anger du **[!UICONTROL Manage Stock]** till `Yes` (standard).

   - Om du vill inaktivera [!DNL Inventory Management] avmarkerar du kryssrutan **[!UICONTROL Use system value]** och anger **[!UICONTROL Manage Stock]** till `No`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Hantera lager för en butik

Se [Konfigurera globala alternativ](global-options.md).

## Hantera lager för en produkt

Se [Konfigurera produktalternativ](product-options.md).
