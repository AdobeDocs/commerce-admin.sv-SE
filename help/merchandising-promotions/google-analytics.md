---
title: '[!DNL Google Analytics]'
description: Lär dig använda [!DNL Google Analytics] för att samla in användbar statistik för era Commerce-sajter.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] ger möjlighet att definiera ytterligare anpassade mått och mätvärden för spårning, med stöd för interaktioner offline och i mobilappar samt tillgång till pågående uppdateringar. [!DNL Google Analytics] 4 är Google nästa generation av mätningslösning och ersätter [!DNL Universal Analytics]. Den 1 juli 2023 slutar standardegenskaperna för Universal Analytics att bearbeta nya träffar.

>[!NOTE]
>
>Om ditt företag omfattas av sekretessbestämmelser som [Allmän dataskyddsförordning](../getting-started/compliance-gdpr.md) och/eller [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), se [Sekretessinställningar för Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Om du aktiverar [Begränsningsläge för cookie](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] samlar inte in uppgifter om besökare såvida de inte har godkänt cookies.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Steg 1: Konfigurera [!UICONTROL Google Analytics] 4

Om du inte redan har en [!DNL Google Analytics] 4 Konfigurera din webbplats på något av följande sätt:

- [Ställ in insamling av analysdata för första gången](https://support.google.com/analytics/answer/9304153)
- [Lägg till Google Analytics 4 på en webbplats med [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Steg 2: Slutför Commerce-konfigurationen

1. Logga in på Admin för din Commerce Store.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Google GTag]** -avsnitt.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Google Analytics4]** underavsnitt och gör följande:

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Lämna **[!UICONTROL Account type]** as `Google Analytics4`.

   - Ange **[!UICONTROL Measurement ID]**. Mer information finns på [Hjälp om Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Om du vill utföra A/B-tester och andra prestandatester på ditt innehåll anger du **Content Experiments** till `Yes`.

   ![Säljkonfiguration - Google API för Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>Den 1 juli 2023 kommer standardegenskaper för Universal Analytics inte längre att bearbeta data. Om du fortfarande litar på [!DNL Universal Analytics]rekommenderar vi att du [förbered användning av Google Analytics 4](https://support.google.com/analytics/answer/10759417) gå framåt.

### Steg 1: Konfigurera Google Universal Analytics

Besök Google webbplats och registrera dig för en [Google Universal Analytics][1] konto.

### Steg 2: Slutför Commerce-konfigurationen

1. Logga in på Admin för din Commerce Store.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Google Analytics]** och gör följande:

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Ange [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Om du vill utföra A/B-tester och andra prestandatester på ditt innehåll anger du **[!UICONTROL Content Experiments]** till `Yes`.

   ![Säljkonfiguration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Förbättrad e-handel

Enhanced Ecommerce är en plugin för [!DNL Google Universal Analytics] som ger er insikt i kundernas beteende när det gäller att handla och köpa. Du kan använda Förbättrad e-handel för att skapa rapporter om viktiga kundaktiviteter, som när kunderna lägger till artiklar i kundvagnen, påbörjar utcheckningen eller slutför ett köp. Ni kan också identifiera och analysera mönster för kunder som överger sina varukorgar utan att göra något inköp.

Följande instruktioner visar hur du konfigurerar [!DNL Google Tag Manager] med [!DNL Universal Analytics] för att ta fram data och rapporter för e-handel.

### Steg 1. Registrera dig för Google-konton

1. Registrera dig för en [Google Tag Manager](google-tag-manager.md) och slutför Commerce-konfigurationen.

1. Registrera dig för en ny [Google Universal Analytics][1] konto.

### Steg 2. Konfigurera Förbättrad e-handel

1. Logga in på ditt Google Universal Analytics-konto.

1. Skapa en egenskap för Enhanced Ecommerce-analys med följande inställningar:

   - Status: PÅ
   - Samhörande produkter: PÅ
   - Aktivera Förbättrad e-handelsrapportering: PÅ
   - Checkout Labeling: (not required)

1. När du är klar klickar du på **[!UICONTROL Submit]**.

### Steg 3. Skapa taggar och utlösare

1. Logga in på [!DNL Google Tag Manager] och skapa följande utlösare:

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
   >The [!UICONTROL Checkout] -händelsen aktiveras endast för de inbyggda Commerce-betalningsmetoderna (som `Check / Money Order` och `Cash On Delivery Payment`). Den här händelsen körs inte för `PayPal checkout` och andra externa betalningsmetoder som använder omdirigering till utcheckning från externa resurser.

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

   - Ange följande **[!UICONTROL Add to Cart]** spårningsinställningar:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Lägg i kundvagnen |
     | [!UICONTROL Trigger] | addToCart |

   - Ange följande **[!UICONTROL Checkout option]** spårningsinställningar:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Utcheckningsalternativ |
     | [!UICONTROL Trigger] | checkoutOption |

   - Ange följande **[!UICONTROL PageView]** spårningsinställningar:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Fyll i följande **[!UICONTROL Product Click]** spårningskonfiguration:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Produktklick |
     | [!UICONTROL Trigger] | productClick |

   - Fyll i följande **[!UICONTROL Promotion Click]** spårningskonfiguration:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Kampanjklickning |
     | [!UICONTROL Trigger] | promotionClick |

   - Fyll i följande **[!UICONTROL Remove from Cart]** spårningskonfiguration:

     | Inställning | Värde |
     |--- |--- |
     | [!UICONTROL Track Type] | Händelse |
     | [!UICONTROL Category] | E-handel |
     | [!UICONTROL Action] | Ta bort från kundvagnen |
     | [!UICONTROL Trigger] | removeFromCart |

1. När du är klar klickar du på **[!UICONTROL Preview]** och verifiera att taggarna fungerar som de ska.

1. När du har verifierat inställningarna klickar du **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
