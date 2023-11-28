---
title: Google AdWord
description: Lär dig hur du konfigurerar din Commerce Store för Google AdWords-konverteringsspårning för att mäta annonsklickningarna som leder till en försäljning eller andra värdefulla åtgärder.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Google AdWord

[Google AdWord][1] är en tjänst som du kan använda för att placera annonser i Google Search-resultat och på företagssidor i Google Display Network. På AdWords-kontrollpanelen finns verktyg för att hantera kampanjer, spåra svar och mäta resultat.

Konverteringsspårning visar antalet annonsklickningar som leder till en försäljning eller någon annan värdefull åtgärd. The _Lyckades_ sida som visas för kunden efter att en beställning har skickats används för att spåra konverteringar eftersom den visas först efter en försäljning. När du har slutfört Google AdWords-konfigurationen för din butik behöver du inte kopiera konverteringsspårningsskriptet till sidan Slutfört eftersom Commerce redan har den information som krävs. Mer information finns på [Hjälp om Google AdWords][2].

![Adobe Ad in Google Search Results](./assets/google-adwords-adobe-ad.png){width="500"}

## Steg 1. Skapa en kampanj för Google AdWords

1. Besök [Google AdWord][3]och registrera ett konto.

1. Följ instruktionerna för att skapa en kampanj.

1. Så här ställer du in konverteringsspårning för kampanjen:

   - På **[!UICONTROL Tools]** -fliken på din AdWords-kontrollpanel, välj **[!UICONTROL Conversions]** och klicka **[!UICONTROL Conversion]**.

   - När du uppmanas att ange konverteringskällan väljer du **[!UICONTROL Website]**.

   - Ange ett namn för den konverteringsåtgärd som du vill spåra och klicka på **[!UICONTROL Done]**.

   - Klicka **[!UICONTROL Value]** och, om tillämpligt, tilldela konverteringen ett värde. Exempel:

      - Om du tjänar 5 dollar på varje köp väljer du `Each time it happens` och tilldela ett värde på `$5`.
      - Om värdet för varje försäljning varierar, lämna värdet tomt.

     Klicka på **[!UICONTROL Done]**.

   - Klicka **[!UICONTROL Conversion windows]** och fyll i inställningarna för att bestämma hur länge konverteringarna ska spåras, rapporteringskategori och attribueringsmodell.

1. När du är klar klickar du på **[!UICONTROL Save and Continue]**.

## Steg 2. Hämta konverteringstaggen

1. Under **[!UICONTROL Install your tag]** väljer du att räkna konverteringar på **[!UICONTROL Page load]**.

1. Du kan lägga till **[!UICONTROL Google Site Stats]** meddelande till konverteringssidan.

   Meddelandet visas i det nedre hörnet med en länk till Google säkerhetsstandarder och cookie-användning.

1. Gör något av följande om du vill välja hur du vill hantera din AdWords-tagg:

   - Om du tänker lägga till skriptet i din butik själv väljer du **[!UICONTROL Save instructions and tag]**.
   - Om du planerar att någon annan ska lägga till skriptet i din butik väljer du **[!UICONTROL Email instructions and tag]**.

1. När du är klar klickar du på **[!UICONTROL Done]**.

## Steg 3. Konfigurera din butik

{{gtag-api-note}}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Om du konfigurerar Google AdWords för en viss butiksvy gör du följande:

   - I det övre vänstra hörnet väljer du **[!UICONTROL Store View]** som ska konfigureras.

   - När du uppmanas att bekräfta omfångsväxling klickar du på **[!UICONTROL OK]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Google AdWords]** och gör följande:

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Ange **[!UICONTROL Conversion ID]** från ditt Google AdWords-skript.

   ![Säljkonfiguration - Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Så här formaterar du Google Sites Stat-meddelandet:

   - Ange **[!UICONTROL Conversion Language]** till det språk som identifieras i ditt Google AdWords-skript.

   - Ange **[!UICONTROL Conversion Format]** som ska användas för Google Sites Stat-meddelanden på konverteringssidan.

      - `1`  - Visar ett enradsmeddelande med en länk till mer information om Google tracking.
      - `2` - Visar ett tvåradsmeddelande med en länk till mer information om Google tracking.
      - `3` - Visar inget kundmeddelande.

   - Ange [hexadecimal kod][4]{:target=&quot;_blank&quot;} för **[!UICONTROL Conversion Color]** som du vill använda som meddelandeetikett för Google Site Stats.

   - Ange den krypterade texten för **[!UICONTROL Conversion Label]** som visas i meddelandet om Google Sites Stat.

     Exempel: `MlEYCOKBnGoQz6CZoAM`

     **Exempel på kod för Google AdWords-tagg**

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
   - `Constant` - Avgör att en konvertering har skett baserat på ett specifikt värde som angetts.

   För _Konstant_ konverteringsvärdetyp, ange en specifik **[!UICONTROL Value]** för _[!UICONTROL Order Amount]_för att kvalificera sig som konvertering.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Steg 4. Verifiera konfigurationen

Inom några timmar ändras spårningsstatusen på din Google AdWords-instrumentpanel från `Unverified` till `No recent conversions` eller `Recording conversions`. När någon klickar på din annons och gör ett köp visas konverteringen på sidan Konverteringsåtgärder på kontrollpanelen och kampanjrapporten.

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
