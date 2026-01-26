---
title: Google AdWord
description: Lär dig hur du konfigurerar din Commerce-butik för konvertering av Google AdWords för att mäta vilka annonsklickningar som leder till en försäljning eller andra värdefulla åtgärder.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Google AdWord

[Google AdWords](https://www.google.com/adwords/) är en tjänst som du kan använda för att placera annonser i Google Search-resultat och på företagssidor i Google Display Network. På AdWords-kontrollpanelen finns verktyg för att hantera kampanjer, spåra svar och mäta resultat.

Konverteringsspårning visar antalet annonsklickningar som leder till en försäljning eller någon annan värdefull åtgärd. Sidan _Slutfört_ som visas för kunden efter att en order har skickats används för att spåra konverteringar eftersom den bara visas efter en försäljning. När du har slutfört Google AdWords-konfigurationen för din butik behöver du inte kopiera konverteringsspårningsskriptet till sidan Slutfört eftersom Commerce redan har den information som krävs. Mer information finns i [Hjälp för Google AdWords](https://support.google.com/adwords/answer/6095821).

![Adobe Ad in Google Search Results](./assets/google-adwords-adobe-ad.png){width="500"}

## Steg 1. Skapa en kampanj för Google AdWords

1. Besök [Google AdWords](https://ads.google.com/) och registrera dig för ett konto.

1. Följ instruktionerna för att skapa en kampanj.

1. Så här ställer du in konverteringsspårning för kampanjen:

   - Välj **[!UICONTROL Tools]** på fliken **[!UICONTROL Conversions]** på din AdWords-instrumentpanel och klicka på **[!UICONTROL Conversion]**.

   - Välj **[!UICONTROL Website]** när du uppmanas att ange konverteringskällan.

   - Ange ett namn för den konverteringsåtgärd som du vill spåra och klicka på **[!UICONTROL Done]**.

   - Klicka på **[!UICONTROL Value]** och tilldela konverteringen ett värde, om tillämpligt. Exempel:

      - Om du tjänar 5 USD på varje köp väljer du `Each time it happens` och tilldelar värdet `$5`.
      - Om värdet för varje försäljning varierar, lämna värdet tomt.

     Slutför genom att klicka på **[!UICONTROL Done]**.

   - Klicka på **[!UICONTROL Conversion windows]** och fyll i inställningarna för att bestämma hur länge konverteringarna ska spåras, rapporteringskategorin och attribueringsmodellen.

1. Klicka på **[!UICONTROL Save and Continue]** när du är klar.

## Steg 2. Hämta konverteringstaggen

1. Under **[!UICONTROL Install your tag]** väljer du att räkna konverteringar på **[!UICONTROL Page load]**.

1. Du kan lägga till meddelandet **[!UICONTROL Google Site Stats]** på konverteringssidan.

   Meddelandet visas i det nedre hörnet med en länk till Google säkerhetsstandarder och cookie-användning.

1. Gör något av följande om du vill välja hur du vill hantera din AdWords-tagg:

   - Om du tänker lägga till skriptet i din butik själv väljer du **[!UICONTROL Save instructions and tag]**.
   - Om du planerar att någon annan ska lägga till skriptet i din butik väljer du **[!UICONTROL Email instructions and tag]**.

1. Klicka på **[!UICONTROL Done]** när du är klar.

## Steg 3. Konfigurera din butik

{{gtag-api-note}}

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Om du konfigurerar Google AdWords för en viss butiksvy gör du följande:

   - I det övre vänstra hörnet väljer du **[!UICONTROL Store View]** som ska konfigureras.

   - När du uppmanas att bekräfta omfångsväxling klickar du på **[!UICONTROL OK]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Google AdWords]** och gör följande:

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Ange **[!UICONTROL Conversion ID]** från ditt Google AdWords-skript.

   ![Försäljningskonfiguration - Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Så här formaterar du Google Sites Stat-meddelandet:

   - Ange **[!UICONTROL Conversion Language]** till det språk som identifieras i ditt Google AdWords-skript.

   - Ange **[!UICONTROL Conversion Format]** som ska användas för Google Sites Stat-meddelandet på konverteringssidan.

      - `1` - Visar ett enradsmeddelande med en länk till mer information om Google-spårning.
      - `2` - Visar ett tvåradsmeddelande med en länk till mer information om Google-spårning.
      - `3` - Visar inget kundmeddelande.

   - Ange den [hexadecimala koden](https://www.w3schools.com/colors/colors_picker.asp){:target="_blank"} för den **[!UICONTROL Conversion Color]** som du vill använda som meddelandeetikett för Google Site Stats.

   - Ange den krypterade texten för **[!UICONTROL Conversion Label]** som visas på Google Sites Stat-meddelandet.

     Till exempel: `MlEYCOKBnGoQz6CZoAM`

     **Exempel på Google AdWords-taggkod**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. Ange **[!UICONTROL Conversion Value Type]** till något av följande:

   - `Dynamic` - Avgör att en konvertering har skett baserat på det dynamiska orderbeloppsvärdet.
   - `Constant` - Avgör att en konvertering har inträffat baserat på ett specifikt värde som angetts.

   För konverteringsvärdetypen _Konstant_ anger du en specifik **[!UICONTROL Value]** för _[!UICONTROL Order Amount]_som ska kvalificeras som en konvertering.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Steg 4. Verifiera konfigurationen

Spårningsstatusen på Google AdWords-instrumentpanelen ändras inom några timmar från `Unverified` till `No recent conversions` eller `Recording conversions`. När någon klickar på din annons och gör ett köp visas konverteringen på sidan Konverteringsåtgärder på kontrollpanelen och kampanjrapporten.
