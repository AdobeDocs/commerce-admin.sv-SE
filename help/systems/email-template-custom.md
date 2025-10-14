---
title: Anpassa e-postmallar
description: Lär dig hur du anpassar e-postmallar för varje webbplats-, butik- eller butiksvy.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: c0d6523f820558c8cd6cfa6b745568784b9e784c
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Anpassa e-postmallar

Commerce innehåller en standardmall för e-post för brödavsnittet i varje meddelande som skickas av systemet. Mallen för brödtextinnehållet kombineras med sidhuvud- och sidfotsmallarna för att skapa det fullständiga meddelandet. Innehållet formateras med HTML och CSS, och kan enkelt redigeras och anpassas genom att [variabler](variables-predefined.md) läggs till. E-postmallar kan anpassas för varje webbplats, butik eller butiksvy. Om du använder anpassade mallar måste du uppdatera [systemkonfigurationen](email-templates.md#configure-email-templates) för att se till att rätt mall används. Mer information om hur du kan använda villkorssatser när du anpassar e-postmallen finns i [utvecklardokumentationen](https://developer.adobe.com/commerce/frontend-core/guide/templates/email/#theme-based-customizations-1).

![Exempel - välkomstförhandsgranskning av e-post](./assets/email-template-preview.png){width="500" zoomable="yes"}

Standardmallarna innehåller din logotyp och din butiksinformation och kan användas utan ytterligare anpassningar. Som en god vana bör du dock visa varje mall och göra nödvändiga ändringar innan du skickar dem till kunderna.

- [Huvudmall](email-template-custom.md#header-template)
- [Sidfotsmall](email-template-custom.md#footer-template)
- [Meddelandemallar](email-template-custom.md#message-templates)

![E-postmallar](./assets/email-templates.png){width="700" zoomable="yes"}

## Mallinformation

| Fält | Beskrivning |
| ----- | ----------- |
| [!UICONTROL Template Name] | Namnet på den anpassade mallen. |
| [!UICONTROL Insert Variable] | Infogar en variabel i mallen vid markörens plats. |
| [!UICONTROL Template Subject] | Mallämne visas i kolumnen Ämne och kan användas för att sortera och filtrera mallarna i listan. |
| [!UICONTROL Template Content] | Innehållet i mallen i HTML. |
| [!UICONTROL Template Styles] | Alla CSS-formatdeklarationer som behövs för att formatera mallen kan anges i rutan _[!UICONTROL Template Styles]_. |

{style="table-layout:auto"}

## Huvudmall

När du har slutfört [konfigurationen](email-templates.md#configure-email-templates) innehåller e-posthuvudmallen din logotyp som är länkad till din butik. Om du har grundläggande kunskaper om HTML kan du enkelt använda [fördefinierade variabler](variables-predefined.md) för att lägga till butikskontaktinformation i sidhuvudet.

### Steg 1. Läs in standardmallen

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Template]**.

1. Klicka på **[!UICONTROL Template]**-väljaren i avsnittet **[!UICONTROL Load default template]** och välj `Magento_Email` > `Header`.

   ![E-postmallhuvud - läsa in standardmall](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Load Template]**.

   HTML-koden och -variablerna från mallen visas i formuläret.

### Steg 2. Anpassa mallen

1. Ange **[!UICONTROL Template Name]** för din anpassade rubrik.

1. Ange en **[!UICONTROL Template Subject]** som hjälp att ordna mallarna.

   I rutnätet kan listan med mallar sorteras och filtreras efter kolumnen _[!UICONTROL Subject]_.

   ![Information om e-postmallhuvud](./assets/email-template-information.png){width="600" zoomable="yes"}

1. I rutan **[!UICONTROL Template Content]** ändrar du HTML efter behov.

   >[!NOTE]
   >
   >När du arbetar i mallkoden ska du se till att inte skriva över något som omges av dubbla klammerparenteser.

1. Om du vill infoga en [variabel](variables-reference.md) placerar du markören i koden där du vill placera variabeln och klickar på **[!UICONTROL Insert Variable]**.

1. Välj den variabel som du vill infoga.

   ![Huvudmall - Infoga variabel](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   När en variabel är markerad infogas en [markup-tagg](markup-tags.md) för variabeln i koden.

   Även om variablerna för e-postadressen i Store är de som oftast finns i huvudet, kan du ange koden för valfritt system eller [anpassad variabel](variables-custom.md) direkt i mallen.

1. Om du behöver göra några CSS-deklarationer anger du formaten i rutan **[!UICONTROL Template Styles]**.

1. När du är redo att granska ditt arbete klickar du på **[!UICONTROL Preview Template]**.

   Gör de ändringar som behövs i mallen.

1. Klicka på **[!UICONTROL Save Template]** när du är klar.

   Din anpassade rubrik visas nu i listan över tillgängliga e-postmallar.

### Steg 3. Uppdatera konfigurationen

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Leta reda på den butiksvy som du vill konfigurera i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Transactional Emails]**.

1. Välj den **[!UICONTROL Header Template]** som används som standard för e-postmeddelanden.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

![Konfiguration av transaktionsbaserad e-postdesign - huvudmall](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Sidfotsmall

Sidfoten för e-postmallen innehåller e-postmeddelandets avslutande och signaturrad. Du kan ändra avslutningen så att den passar ditt format och lägga till ytterligare information, till exempel företagsnamnet och företagsadressen under ditt namn.

### Steg 1. Läs in standardmallen

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Template]**.

1. Klicka på **[!UICONTROL Template]**-väljaren i avsnittet **[!UICONTROL Load default template]** och välj `Magento_Email` > `Footer`.

1. Klicka på **[!UICONTROL Load Template]**.

   HTML-koden och -variablerna från mallen visas i formuläret.

### Steg 2. Anpassa och förhandsgranska mallen

1. Ange **[!UICONTROL Template Name]** för din anpassade sidfot.

1. Ange en **[!UICONTROL Template Subject]** som hjälp att ordna mallarna.

   I rutnätet kan mallarna sorteras och filtreras efter kolumnen _[!UICONTROL Subject]_.

   ![Sidfot för e-postmall - information](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. I rutan **[!UICONTROL Template Content]** ändrar du HTML efter behov.

   >[!NOTE]
   >
   >När du arbetar i mallkoden ska du se till att inte skriva över något som omges av dubbla klammerparenteser.

1. Om du vill infoga en [variabel](variables-reference.md) placerar du markören i koden där du vill placera variabeln och klickar på **[!UICONTROL Insert Variable]**.

1. Välj den variabel som du vill infoga.

   När en variabel är markerad infogas en [markup-tagg](markup-tags.md) för variabeln i koden.

   Även om lagringskontaktvariablerna är de som oftast finns i sidfoten kan du ange koden för alla system eller [anpassade variabler](variables-custom.md) direkt i mallen.

1. Om du behöver göra några CSS-deklarationer anger du formaten i rutan **[!UICONTROL Template Styles]**.

### Steg 3. Uppdatera konfigurationen

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Leta reda på den butiksvy som du vill konfigurera i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Transactional Emails]**.

1. Välj den **[!UICONTROL Footer Template]** som används som standardsidfot i e-postmeddelanden.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

![Konfiguration av transaktionsbaserad e-postdesign - sidfotsmall](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Meddelandemallar

Att anpassa brödtexten i varje meddelande är detsamma som att anpassa sidhuvudet eller sidfoten. Den enda skillnaden är meddelandemallen för varje aktivitet eller händelse som utlöser ett meddelande. Du kan använda mallarna som de är, eller anpassa dem så att de matchar din röst och ditt varumärke. Förutom malltexten finns det ett brett urval av tillåtna [fördefinierade &#x200B;](variables-predefined.md)- och [anpassade](variables-custom.md)-variabler som du kan skapa och lägga till i mallen.

### Steg 1. Läs in standardmallen

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Template]**.

   ![E-postmallar - läsa in standardmall](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Gör följande:

   - Under **[!UICONTROL Load default template]** väljer du den **[!UICONTROL Template]** som du vill anpassa.

   - Klicka på **[!UICONTROL Load Template]**.

### Steg 2. Anpassa mallen

1. Ange ett namn för den anpassade mallen för **[!UICONTROL Template Name]**.

1. Ändra **[!UICONTROL Template Subject]** om det behövs.

   Detta är den första raden i meddelandet, som är hälsningsfrasen som standard. Du kan lämna det som det är eller ange något mer beskrivande.

1. Observera sökvägen **[!UICONTROL Currently Used For]** till mallen, som är sökvägen som används för att uppdatera konfigurationen.

   ![E-postmallar - mallinformation](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. I rutan **[!UICONTROL Template Content]** ändrar du HTML efter behov.

   Innehållet består av en kombination av HTML-taggar, CSS-direktiv, variabler och text.

   >[!NOTE]
   >
   >När du arbetar i mallkoden ska du se till att inte oavsiktligt skriva över koden som omges av dubbla klammerparenteser.

1. Om du vill infoga en variabel placerar du markören i koden där du vill att variabeln ska visas.

   Valet av variabler varierar beroende på mall och inkluderar tillåtna [fördefinierade](variables-predefined.md) - och [anpassade](variables-custom.md) -variabler, om sådana finns.

1. Klicka på **[!UICONTROL Insert Variable]** och välj den variabel som du vill infoga.

   Ett kommando som infogar variabeln omges av klammerparenteser och läggs till i koden vid markörens plats. Exempel:

   `customVar code=my_custom_variable`

1. Om du vill göra CSS-deklarationer anger du formaten i **[!UICONTROL Template Styles]**.

   ![E-postmallar - lägg till anpassade format](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Anpassade format används bara i e-postmeddelandet om `{{template config_path="design/email/header_template"}}` finns i _[!UICONTROL Template Styles]_. Om du vill använda anpassad CSS utan någon standardhuvudmall måste du ange dem här i HTML-taggen `<style>`.

### Steg 3. Uppdatera konfigurationen

Breadcrumb-spåret _[!UICONTROL Currently Used For]_&#x200B;visar var mallen används. I det här exemplet finns mallkonfigurationen på sidan&#x200B;_[!UICONTROL Customer Configuration]_, i avsnittet _[!UICONTROL Create New Account Options]_&#x200B;och i fältet&#x200B;_[!UICONTROL Default Welcome Email]_.

- Sida - [!UICONTROL Customer Configuration]
- Avsnitt - [!UICONTROL Create New Account Options]
- Fält - [!UICONTROL Default Welcome Email]

1. Klicka på länken i det synliga spåret **[!UICONTROL Currently Used For]** för att öppna mallkonfigurationssidan.

   ![Aktuell e-postmall](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Utöka ![expanderingsväljaren](../assets/icon-display-expand.png) i avsnittet och hitta fältet för den e-postmall som du har anpassat.

1. Avmarkera kryssrutan **[!UICONTROL Use system value]** och klicka på namnet på din anpassade mall.

   ![Kundkonfiguration - standardmall för välkomstmeddelanden](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. Klicka på **[!UICONTROL Cache Management]** i meddelandet längst upp på arbetsytan och rensa bort eventuell ogiltig cache.

### Steg 4. Förhandsgranska och spara mallen

1. När du är redo att granska ditt arbete klickar du på **[!UICONTROL Preview Template]**.

1. Uppdatera mallen efter behov.

1. Klicka på **[!UICONTROL Save Template]** när du är klar.

   Din anpassade mall är nu tillgänglig i listan över e-postmallar.
