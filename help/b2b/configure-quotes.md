---
title: Konfigurera offerter
description: Lär dig mer om offertkonfigurationen, som styr det minsta orderbelopp som krävs för offertförfrågningar, offertens livstid och bifogade filer.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Konfigurera offerter

Om citattecken är aktiverade i de allmänna [B2B-funktionerna](enable-basic-features.md) kan du konfigurera stöd för citattecken i Admin. Offertkonfigurationen avgör den minsta ordermängd som krävs för offertförfrågningar, offertens livstid och vilka filformat som stöds för bifogade filer.

>[!NOTE]
>
>Offertkonfigurationsalternativ och möjligheten att använda offertförhandlingsfunktioner styrs med [rollresurserna](../systems/permissions-user-roles.md#role-resources). Dessa rollresurser måste väljas för den administratörsanvändarroll som tilldelas administratörsanvändarkontot. Om du vill ge åtkomst till offertfunktioner i Admin går du till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, markerar rollen och navigerar till [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] i trädet_ Rollresurser _.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Quotes]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL General]** och gör följande:

   ![Konfiguration av försäljningsofferter - allmän](./assets/quotes-general.png){width="700" zoomable="yes"}

   Se [Citattecken](../configuration-reference/sales/quotes.md) i _konfigurationsreferensen_ för en fullständig lista över alternativ för citattecken och deras funktioner.

   - Ange **[!UICONTROL Minimum Amount]** i kundvagnen som måste uppfyllas innan en anbudsförfrågan kan skickas.

   - För **[!UICONTROL Minimum Amount Message]** anger du det meddelande som du vill ska visas när kundvagnssumman inte uppfyller minimibeloppet.

   - För **[!UICONTROL Default Expiration Period]** anger du det antal **[!UICONTROL days]**, **[!UICONTROL weeks]** eller **[!UICONTROL months]** som en offert ska förbli giltig.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Attached files]** och gör följande:

   - För **[!UICONTROL File formats for upload]** anger du suffixet för varje filtyp som du stöder för filer som är kopplade till en offert.

     Ange varje filsuffix med gemener och avgränsade med kommatecken.

     Som standard stöds följande format: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` och `jpeg`

   - För **[!UICONTROL Maximum file size]** anger du den maximala storleken för en bifogad fil i MB.

     Värdet som du anger kan åsidosättas av serverinställningen.

     ![Konfiguration av försäljningsofferter - bifogade filer](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
