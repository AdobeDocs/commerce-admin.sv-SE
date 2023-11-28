---
title: '''[!DNL Business Intelligence] verktyg'
description: Läs om hur Adobe Commerce och Magento Open Source kan använda intelligenta verktyg för att få den kunskap som behövs för att fatta sunda affärsbeslut.
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# [!DNL Business Intelligence] verktyg

Använd intelligenta verktyg för att få den kunskap som behövs för att fatta sunda affärsbeslut.

## [!DNL Business Intelligence] konto

När du aktiverar [!DNL Business Intelligence] via Adobe får du tillgång till fem instrumentpaneler med ungefär 70 rapporter. Dessa rapporter är utformade för att ge insikter om era data och svara på frågor som&quot;Hur växer mina order månadsvis?&quot;,&quot;Vilka är mina mest lojala kunder?&quot; och&quot;Fungerar min kupongstrategi?&quot; Mer information om den här verktygsuppsättningen finns i [Användarhandbok för MBI][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] ingår i Adobe Commerce och Magento Open Source. Den här funktionen ger er tillgång till en uppsättning dynamiska rapporter som baseras på era produkt-, order- och kunddata, med en anpassad kontrollpanel som är anpassad efter era affärsbehov. while [!DNL Advanced Reporting] använder [!DNL Business Intelligence] för analyser behöver du inte ha något Business Intelligence-konto att använda [!DNL Advanced Reporting].

Teknisk information finns i [[!DNL Advanced Reporting]][2]{:target=&quot;_blank&quot;} i utvecklardokumentationen.

>[!NOTE]
>
>[!DNL Business Intelligence] konton använder inbyggd rapportering, i stället för [!DNL Advanced Reporting] -funktion.

![Kontrollpanel för avancerad rapportering](./assets/reporting-advanced.png){width="700"}

### Krav

* Webbplatsen måste köras på en offentlig webbserver.

* Domänen måste ha ett giltigt SSL-certifikat.

* [!DNL Commerce] måste ha installerats eller uppgraderats utan fel.

* I [!DNL Commerce] konfiguration för [lagra URL:er](../stores-purchase/store-urls.md), **[!UICONTROL Base URL (Secure)]** inställningen för butiksvyn måste peka på den säkra URL:en. Exempel: `https://yourdomain.com`.

* I [!DNL Commerce] konfiguration för butiks-URL, **[!UICONTROL Use Secure URLs on Storefront]** och **[!UICONTROL Use Secure URLs in Admin]** måste anges till `Yes`.

* [[!DNL Commerce] crontab][3] skapas och cron-jobb körs på den installerade servern.

>[!NOTE]
>
>[!DNL Advanced Reporting] kan endast användas med [!DNL Commerce] installationer som kontinuerligt har använt en enda [basvaluta](../stores-purchase/currency-configuration.md).


### Steg 1: Aktivera [!DNL Advanced Reporting]

I [!DNL Commerce] konfiguration, [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) är aktiverat som standard och startar automatiskt om cron är aktiverad [konfigurerad](../configuration-reference/advanced/system.md) och springa. Ett försök att upprätta prenumerationen påbörjas i början av varje timme under de kommande 24 timmarna tills det är klart. Prenumerationsstatusen är &quot;väntande&quot; tills prenumerationen har upprättats.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra navigeringspanelen där **[!UICONTROL General]** är expanderad, välj **[!UICONTROL Advanced Reporting]** och gör följande:

   * Verifiera att **[!UICONTROL Advanced Reporting Service]** är inställd på `Enable` (standardinställningen).

   * Ange **[!UICONTROL Time of day to send data]** till timmen, minuten och sekunden, enligt en 24-timmarsklocka, som du vill att tjänsten ska ta emot uppdaterade data från din butik. Som standard skickas data kl. 2:00.

   * Under **[!UICONTROL Industry Data]** väljer du **[!UICONTROL Industry]** som bäst beskriver er verksamhet.

   ![Konfiguration av avancerad rapportering](./assets/advanced-reporting-config.png){width="400"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. Klicka på **[[!UICONTROL Cache Management]](../systems/cache-management.md)** i meddelandet längst upp på sidan och uppdatera ogiltiga cacheminnen.

1. Vänta över en natt, eller tills efter tidpunkten för nästa schemalagda uppdatering. Kontrollera sedan prenumerationens status. Om statusen fortfarande är _väntande_ kontrollerar du att din installation uppfyller alla krav.

### Steg 2: Åtkomst [!DNL Advanced Reporting]

1. Gör något av följande:

   * På _Administratör_ sidlist, välj **[!UICONTROL Dashboard]**. Klicka sedan på **[!UICONTROL Go to Advanced Reporting]**.
   * På _Administratör_ sidebar, gå till **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   The [!DNL Advanced Reporting] På kontrollpanelen finns en snabb sammanfattning av dina beställningar, kunder och produkter. Se till att bläddra nedåt för att se hela instrumentpanelen.

1. Om du vill få en bättre bild av data anger du **[!UICONTROL Filters]** i det övre högra hörnet av tidsperioden och butiksvyn som du vill ta med i rapporten. Gör sedan följande:

   * Håll pekaren över en datapunkt för mer information.
   * Klicka på varje flik för att visa alla kontrollpanelsrapporter.

   ![Datapunkt](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## Åtkomst [!DNL Advanced Reporting] dataresurser

Klicka på i det övre högra hörnet av instrumentpanelen för avancerad rapportering. **[!UICONTROL Additional Resources]**.

![Avancerade rapporteringsdataresurser](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## Felsökning

Om du får ett 404-meddelande om att sidan inte hittades kontrollerar du att din butik uppfyller kraven för [!DNL Advanced Reporting]. Följ sedan instruktionerna för att kontrollera att integreringen är installerad.

### Kontrollera att integreringen är aktiv

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. Verifiera att **[!UICONTROL Magento Analytics user]** visas i listan och **[!UICONTROL Status]** är `Active`.

1. Om du vill återskapa användaren klickar du på **[!UICONTROL Reauthorize]** och gör följande:

   ![Återauktorisera](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * Klicka på **[!UICONTROL Reauthorize]** för att godkänna åtkomst till API-resurserna.

     ![Återauktorisera åtkomst till API-resurser](./assets/advanced-reporting-integration-api.png){width="600"}

   * Kontrollera att listan med integreringstoken för tillägg är slutförd. Klicka sedan på **Klar**.

     ![Integreringstoken](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. Leta efter meddelandet som anger integreringen `Magento Analytics user` har fått ny behörighet.

1. Vänta över en natt eller tills efter tidpunkten för nästa schemalagda uppdatering.

### Verifiera gemensam basvaluta

[!DNL Advanced Reporting] kan endast användas med [!DNL Commerce] installationer som bara har använt en enda [basvaluta](../stores-purchase/currency-configuration.md) sedan installationen. Resultatet är att i historiken används samma basvaluta för alla order. [!DNL Advanced Reporting] fungerar inte om du någon gång har ändrat din basvaluta och har order i din historik som har bearbetats med olika basvalutor.

Om du vill avgöra om din butik har flera basvalutor kan du fråga din [!DNL Commerce] databas från kommandoraden med hjälp av följande MySQL-exempel. Du kan behöva ändra tabellnamnen så att de matchar datastrukturen:

```sql
select distinct base_currency_code from sales_order;
```

### Datamatchningsavvikelse

Om du märker att `Data last updated...` bildtexten visar gårdagens datum och inte dagens. Det kan finnas en fördröjning på upp till en dag i uppdateringarna för avancerad rapportering. Fördröjningen beror på att kön är större än förväntat.

## Kontrollpanelrapporter

**[!UICONTROL Orders]**

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Revenue] | Visar alla intäkter som har tagits emot av butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Orders] | Visar alla order som placerats genom butiksvyn under den definierade tidsperioden. |
| [!UICONTROL AOV] | Visar det genomsnittliga ordervärdet som placerats genom butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Refunds] | Visar alla återbetalningar som bearbetats genom butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Tax Collected] | Visar all moms som samlats in via butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Shipping Collected] | Visar alla fraktavgifter som samlats in via butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Orders by Status] | Visar antalet order efter status för butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Orders by Status] | Visar en sammanfattning av antalet order efter status. |
| [!UICONTROL Coupon Usage] | Visar alla kupongkoder och antalet användare för varje, inlösta via butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Orders and Revenue by Billing Region] | Visar antalet order och intäkter per region för butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Tax Collected by Billing Region] | Visar mängden moms som samlats in per region för butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | Visar leveransavgifter som samlats in per region för butiksvyn under den definierade tidsperioden. |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Unique Customers] | Visar antalet unika kundkonton som är associerade med butiksvyn under den definierade tidsperioden. |
| [!UICONTROL New Registered Accounts] | Visar antalet nya kundkonton som registrerats i butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Top Coupon Users] | Visar de övre kuponganvändarna per Kund-ID och antalet order som placerats med kuponger för butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Customer KPI Table] | Visar antalet order, intäkter och genomsnittligt ordervärde per kund-ID för butiksvyn under den definierade tidsperioden. |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | Visar antalet produkter som sålts via butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Products Added to Wishlists] | Listar alla produkter som lagts till i önskelistor via butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Best Selling Products by Quantity] | Visar de bästsäljande produkterna och den kvantitet som sålts genom butiksvyn under den definierade tidsperioden. |
| [!UICONTROL Best Selling Products by Revenue] | Visar de mest säljande produkterna och intäkterna som genereras av försäljningen av produkten via butiksvyn under den definierade tidsperioden. |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
