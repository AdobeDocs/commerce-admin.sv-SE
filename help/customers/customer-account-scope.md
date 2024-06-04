---
title: Omfattning av kundkonto
description: Omfånget för kundkonton kan begränsas till webbplatsen där kontot skapades eller delas med alla webbplatser och butiker i butikshierarkin.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Omfattning av kundkonto

Sidhuvudet på alla sidor i din butik ger kunderna en inbjudan att _Logga in eller registrera_ för ett konto hos din butik. Kunder som öppnar ett konto har en rad fördelar, bland annat:

* **Skapa kundkonto** - Besökarna kan skapa ett kundkonto så att de kan använda butiken som registrerad kund.
* **Skapa ett företagskonto** Beroende på konfigurationen kan en besökare i din butik välja att skapa ett företagskonto. Mer information finns i [Adobe Commerce B2B](../b2b/introduction.md).
* **Snabbare utcheckning** — Registrerade kunder går igenom kassan snabbare eftersom mycket av informationen redan finns på deras konton.
* **Självbetjäning** — Registrerade kunder kan uppdatera sin information, kontrollera orderstatus och till och med beställa från sina konton.

Kunderna kan komma åt sitt konto genom att klicka på **[!UICONTROL My Account]** i butikens sidhuvud. Från sitt konto kan kunderna visa och ändra information, inklusive tidigare och aktuella adresser, inställningar för fakturering och frakt, prenumerationer på nyhetsbrev, önskelistor med mera.

![Mitt konto](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Ange omfattningen för kundkonton

Omfånget för kundkonton kan begränsas till webbplatsen där kontot skapades eller delas med alla webbplatser och butiker i butikshierarkin.

>[!NOTE]
>
>Om webbplatsen utesluts från kundgruppen får kunden inte logga in på webbplatsen när omfattningen av kundkontona är begränsad till webbplatsen eller delas med alla webbplatser. Se [Skapa en kundgrupp](customer-groups.md#create-a-customer-group) om du vill ha mer information om hur du utesluter webbplatser från grupper.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Customer Configuration]**.

1. Expandera avsnittet **[!UICONTROL Account Sharing Options]**.

   ![Alternativ för kontodelning](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Share Customer Accounts]** till något av följande:

   | Alternativ | Beskrivning |
   | --- | --- |
   | `Global` | Delar kundkontoinformation med alla webbplatser och butiker i installationen. |
   | `Per Website` | Begränsar kundkontoinformationen till webbplatsen där kontot skapades. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Rensa **[!UICONTROL User system value]** för att göra ändringen.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >När `Global` väljs kundinformationen i **Mitt konto** (adresser och kontoinformation som kontaktuppgifter) delas.
