---
title: Lägg till anpassade variabler
description: Lär dig hur du skapar anpassade variabler och infogar dem på sidor, i block och i produktinnehåll.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%

---

# Lägg till anpassade variabler

För att uppfylla ditt företags specifika behov kan du skapa anpassade variabler och infoga dem i [sidorna](../content-design/pages.md), [block](../content-design/blocks.md) och [e-postmallar](email-templates.md). Listan med tillåtna variabler som visas när du klickar på knappen _Infoga variabel_ innehåller både [fördefinierade](variables-predefined.md) och anpassade variabler. Listan med tillgängliga variabler för en viss e-postmall bestäms av de data som är kopplade till mallen. I [Variabelreferens](variables-reference.md) finns en lista över e-postmallar som används ofta och tillhörande variabler.

![Egna variabler](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Endast tillåtna fördefinierade eller anpassade variabler kan användas i mallar för e-post och nyhetsbrev.

## Steg 1: Skapa en egen variabel

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Variable]**.

1. Ange en identifierare för **[!UICONTROL Variable Code]** och använd alla gemener utan blanksteg.

   Om det behövs kan du använda ett understreck eller ett bindestreck för att representera ett mellanslag. Till exempel: `my_custom_variable`

1. Ange en **[!UICONTROL Variable Name]** som används som intern referens. Till exempel: `My Custom Variable`

1. Om du vill ange värdet som är associerat med variabeln gör du något av följande:

   - För **[!UICONTROL Variable HTML Value]** anger du variabelvärdet som är formaterat med enkla HTML-taggar. Exempel:

     `<b>This formatted content appears in place of the variable.</b>`

   - För **[!UICONTROL Variable Plain Value]** anger du variabelvärdet som ren text utan formatering. Exempel:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Om du behöver mer utrymme drar du i textrutans nedre högra hörn.

   ![Ny anpassad variabel](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Steg 2: Infoga den anpassade variabeln i ditt innehåll

Använd [!DNL Page Builder] för att infoga en anpassad variabel.

1. Öppna sidan, blocket, kategorin eller produkten där du vill lägga till variabeln i innehållet.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Content]**.

1. Klicka på **[!UICONTROL Edit with Page Builder]**.

1. Klicka på **[!UICONTROL Elements]** i den vänstra panelen och gör något av följande:

   - Klicka i ett textområde där du vill infoga variabeln.

   - Dra ett nytt **[!UICONTROL Text]**-objekt till scenen.

1. Klicka på ( ![Infoga variabel](./assets/editor-btn-insert-variable.png) ) längst till höger i redigeringsverktygsfältet om du vill infoga en variabel.

   ![[!DNL Page Builder] scen och panel &#x200B;](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. I listan väljer du den anpassade variabel som du vill infoga och klickar på **[!UICONTROL Insert Variable]**.

   ![Ny anpassad variabel](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   Variabelidentifieraren visas som en platshållare i redigeraren.

   ![[!DNL Page Builder] stage - variabelplatshållare &#x200B;](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.
