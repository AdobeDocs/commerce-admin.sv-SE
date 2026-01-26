---
title: '[!DNL Google Analytics]'
description: Lär dig hur du kan använda  [!DNL Google Analytics] för att samla in användbar statistik för dina Commerce-webbplatser.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] ger dig möjlighet att definiera ytterligare anpassade dimensioner och mätvärden för spårning, med stöd för interaktioner offline och i mobilappar samt tillgång till pågående uppdateringar. [!DNL Google Analytics] 4 är Google nästa generations mätningslösning och ersätter [!DNL Universal Analytics]. Den 1 juli 2023 slutar standardegenskaperna för Universal Analytics att bearbeta nya träffar.

>[!NOTE]
>
>Om ditt företag omfattas av sekretessbestämmelser som [General Data Protection Regulation](../getting-started/compliance-gdpr.md) och/eller [California Consumer Privacy Act](../getting-started/compliance-ccpa.md) kan du läsa [Google Privacy Settings](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Om du aktiverar [läget för cookie-begränsning](../getting-started/compliance-cookie-law.md) samlar [!DNL Google Analytics] inte in data om besökare om de inte har accepterat cookies.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Steg 1: Konfigurera [!UICONTROL Google Analytics] 4

Om du inte redan har en [!DNL Google Analytics] 4-konfiguration för din plats gör du något av följande:

- [Konfigurera insamling av analysdata för första gången](https://support.google.com/analytics/answer/9304153)
- [Lägg till Google Analytics 4 på en webbplats med  [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Steg 2: Slutför Commerce-konfigurationen

1. Logga in på Admin for your Commerce store.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Google GTag]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i underavsnittet **[!UICONTROL Google Analytics4]** och gör följande:

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Lämna **[!UICONTROL Account type]** som `Google Analytics4`.

   - Ange din **[!UICONTROL Measurement ID]**. Mer information finns i [Google Analytics-hjälpen](https://support.google.com/analytics/answer/9539598).

   - Om du vill utföra A/B-tester och andra prestandatester på ditt innehåll anger du **Content Experiments** till `Yes`.

   ![Försäljningskonfiguration - Google API för Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Google Universal Analytics

>[!IMPORTANT]
>
>Den 1 juli 2023 kommer standardegenskaper för Universal Analytics inte längre att bearbeta data. Om du fortfarande förlitar dig på [!DNL Universal Analytics] rekommenderar vi att du [förbereder dig för att använda Google Analytics 4](https://support.google.com/analytics/answer/10759417) framåt.

### Steg 1: Konfigurera Google Universal Analytics

Besök Google webbplats och registrera dig för ett [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en) -konto.

### Steg 2: Slutför Commerce-konfigurationen

1. Logga in på Admin for your Commerce store.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Google Analytics]** och gör följande:

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Ange din [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Om du vill utföra A/B-tester och andra prestandatester på ditt innehåll anger du **[!UICONTROL Content Experiments]** till `Yes`.

   ![Försäljningskonfiguration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Förbättrad e-handel

Förbättrad e-handel är en plugin för [!DNL Google Universal Analytics] som ger dig insikt i kundernas beteende när det gäller att handla och köpa. Du kan använda Förbättrad e-handel för att skapa rapporter om viktiga kundaktiviteter, som när kunderna lägger till artiklar i kundvagnen, påbörjar utcheckningen eller slutför ett köp. Ni kan också identifiera och analysera mönster för kunder som överger sina varukorgar utan att göra något inköp.

Följande instruktioner visar hur du konfigurerar [!DNL Google Tag Manager] med [!DNL Universal Analytics] för att skapa data och rapporter för Förbättrad e-handel.

### Steg 1. Registrera dig för Google-konton

1. Registrera dig för ett [Google Tag Manager](google-tag-manager.md)-konto och slutför Commerce-konfigurationen.

1. Registrera ett nytt [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en)-konto.

### Steg 2. Konfigurera Förbättrad e-handel

1. Logga in på ditt Google Universal Analytics-konto.

1. Skapa en egenskap för Enhanced Ecommerce-analys med följande inställningar:

   - Status: PÅ
   - Samhörande produkter: PÅ
   - Aktivera Förbättrad e-handelsrapportering: PÅ
   - Checkout Labeling: (not required)

1. Klicka på **[!UICONTROL Submit]** när du är klar.

### Steg 3. Skapa taggar och utlösare

1. Logga in på ditt [!DNL Google Tag Manager]-konto och skapa följande utlösare:

   | Namn | Händelsetyp | Filter |
   |--- |--- |--- |
   | `addToCart` | Egen händelse |  |
   | `checkout` | Egen händelse |  |
   | `checkout only` | Sidvy | Sidans URL matchar RegEx /checkout/.* |
   | `checkoutOption` | Egen händelse |  |
   | `gtm.dom` | Egen händelse |  |
   | `productClick` | Egen händelse |  |
   | `promotionClick` | Egen händelse |  |
   | `removeFromCart` | Egen händelse |  |

   >[!NOTE]
   >
   >Händelsen [!UICONTROL Checkout] aktiveras endast för de inbyggda grundläggande betalningsmetoderna i Commerce (till exempel `Check / Money Order` och `Cash On Delivery Payment`). Den här händelsen körs inte för `PayPal checkout` och andra externa betalningsmetoder som använder omdirigering till utcheckning från externa resurser.

1. Skapa följande Universal Analytics-taggar med samma grundläggande konfiguration.

   - Universella analystaggar

     | Namn | Typ | Utlösare |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | utcheckning |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - Konfiguration av grundläggande tagg

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (Spårnings-ID från ditt Universal Analytics-konto.) |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. Slutför de enskilda spårningskonfigurationerna.

   - Ange följande **[!UICONTROL Add to Cart]**-spårningsinställningar:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Lägg i kundvagnen |
     | [!UICONTROL Trigger] | addToCart |

   - Ange följande **[!UICONTROL Checkout option]**-spårningsinställningar:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Utcheckningsalternativ |
     | [!UICONTROL Trigger] | checkoutOption |

   - Ange följande **[!UICONTROL PageView]**-spårningsinställningar:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Slutför följande **[!UICONTROL Product Click]**-spårningskonfiguration:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Produktklick |
     | [!UICONTROL Trigger] | productClick |

   - Slutför följande **[!UICONTROL Promotion Click]**-spårningskonfiguration:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Kampanjklickning |
     | [!UICONTROL Trigger] | promotionClick |

   - Slutför följande **[!UICONTROL Remove from Cart]**-spårningskonfiguration:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Ta bort från kundvagnen |
     | [!UICONTROL Trigger] | removeFromCart |

1. När det är klart klickar du på **[!UICONTROL Preview]** och kontrollerar att taggarna fungerar som de ska.

1. När du har verifierat inställningarna klickar du på **[!UICONTROL Publish]**.
