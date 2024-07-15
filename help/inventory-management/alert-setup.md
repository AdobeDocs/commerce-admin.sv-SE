---
title: Produktvarningar
description: Läs mer om produktvarningar och hur du använder dem för att meddela kunderna om lagerstatus och prisförändringar för produkter.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Produktvarningar

Kunder kan prenumerera på två typer av varningar via e-post - prisförändringsvarningar och lagervarningar. För varje typ av varning kan du bestämma om kunderna kan prenumerera, välja den e-postmall som används och identifiera avsändaren av e-postmeddelandet.

![Registrera dig för en produktvarning](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Aviseringar om prisändringar

När prisförändringsvarningar är aktiverade visas en _Meddela mig när priset faller_-länk på varje produktsida. Kunderna kan klicka på länken för att prenumerera på varningar om produkten. Gäster uppmanas att öppna ett konto i din butik. Varje gång priset ändras eller produkten blir speciell får alla som prenumererar på varningen ett e-postmeddelande.

## Aviseringar i lager

Lagervarningen skapar en länk med namnet _Meddela mig när den här produkten finns i lager_ för varje produkt som inte finns i lager. Kunder kan klicka på länken för att prenumerera på aviseringen. När produkten är tillbaka i lager får kunderna ett e-postmeddelande om att produkten är tillgänglig. Produkter med varningar har fliken _Produktvarningar_ på produktinformationspanelen som listar de kunder som har prenumererat på en varning.

![Lista över produkt- och prisaviseringsprenumerationer](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Ställ in produktvarningar

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Klicka för att expandera avsnittet _[!UICONTROL Product Alerts]_och gör följande:

   ![Produktaviseringar](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Allow Alert When Product Price Changes]** till `Yes` om du vill erbjuda kunderna aviseringar om prisändringar.

   - Ange **[!UICONTROL Price Alert Email Template]** till mallen som du vill använda för prisaviseringsmeddelanden.

   - Ange **[!UICONTROL Allow Alert When Product Comes Back in Stock]** till `Yes` om du vill att aviseringar ska visas när det finns produkter som inte finns i lager igen.

     >[!NOTE]
     >
     >Meddelandet _Meddela mig när den här produkten finns i lager_ visas bara när **[!UICONTROL Display Out of Stock Products]** är inställd på `Yes` (i Konfiguration på [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Ange **[!UICONTROL Stock Alert Email Template]** till den mall som du vill använda för produktStock-varningar.

   - Ange **[!UICONTROL Alert Email Sender]** till den [butikskontakt](../getting-started/store-details.md#store-email-addresses){target="_blank"} som du vill ska visas som avsändare av e-postaviseringen. Läs mer om [butikens e-postadresser](../configuration-reference/general/store-email-addresses.md){target="_blank"} i användarhandboken.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Konfigurera e-postmallar för produktvarningar

Konfigurera, lägg till eller ändra e-postmallen för prisaviseringen. Du kan redigera dina prisaviseringskonfigurationer efter att du har skapat ytterligare mallar.

Mer information om hur du använder e-postmeddelanden finns i [Meddelandemallar](../systems/email-template-custom.md#message-templates) i _handboken för administratörssystem_.

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Template]**.

1. Under _Läs in standardmall_ väljer du den **[!UICONTROL Template]** som du vill anpassa.

   Du kan välja den varningsmall som ingår i temat. Du kan också välja mallarna `Price Alert` eller `Stock Alert` under _[!UICONTROL Magento_PriceAlert]_.

1. Klicka på **[!UICONTROL Load Template]**.

1. Ange **[!UICONTROL Template Name]**.

   Du kan välja det här namnet i konfigurationen _Prisaviseringar_.

1. Läs igenom det befintliga innehållet och gör de ändringar som behövs för följande:

   | Fält | Beskrivning |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Den här texten visas på ämnesraden i ett e-postmeddelande. |
   | [!UICONTROL Template Content] | Texten visas i det fullständiga innehållet i det skickade e-postmeddelandet. |

1. Om du vill lägga till genererad information från [!DNL Commerce]-data använder du alternativet **[!UICONTROL Insert Variable]** för att använda en lista med tillgängliga variabler.

1. Klicka på **[!UICONTROL Save Template]**.

## Körningsinställningar för produktavisering

Med de här inställningarna kan du välja hur ofta [!DNL Commerce] söker efter ändringar som kräver att varningar skickas. Du kan också välja mottagare, avsändare och mall för e-postmeddelanden som skickas om det inte går att skicka meddelanden.

![Körningsinställningar för produktavisering](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Product Alerts Run Settings]**.

1. Ange **[!UICONTROL Frequency]** till något av följande för att avgöra hur ofta produktvarningar skickas:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Ange **[!UICONTROL Start Time]** till timma, minut och sekund för att bestämma vilken tid produktvarningar skickas.

   >[!NOTE]
   >
   >Produktvarningar skickas av&quot;product_alert&quot;-konsumenten.

1. För **[!UICONTROL Error Email Recipient]** anger du e-postadressen till den person som ska kontaktas om ett fel inträffar.

1. För **[!UICONTROL Error Email Sender]** väljer du den lagringsidentitet som visas som avsändare av felmeddelandet.

1. Ange **[!UICONTROL Error Email Template]** till transaktionens e-postmall som ska användas för felmeddelandet.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
