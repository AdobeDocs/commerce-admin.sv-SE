---
title: Inställningar för fraktfirma
description: Läs mer om den support för kommersiella leveranskonton som finns för din butik.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Inställningar för fraktfirma

Om du har ett kommersiellt konto hos en operatör som stöds kan du erbjuda dina kunder en smidig möjlighet att välja den transportören vid utcheckningen. Priserna hämtas automatiskt, så du behöver inte leta upp informationen.

>[!NOTE]
>
>Se [Commerce Marketplace](../getting-started/commerce-marketplace.md) för ytterligare leveranstjänster för din Commerce-installation.

Innan du kan erbjuda kunderna ett urval av fraktfirmor måste du utföra följande steg:

- Konfigurera [leveransinställningarna](shipping-settings.md) för att upprätta butikens ursprungsplats.

- Konfigurera inställningarna för varje transportörtjänst som du vill erbjuda.

   - [**UPS**](ups.md) - United Parcel Service (UPS) erbjuder inrikes och internationell frakt per land och flyg till över 220 länder.
   - [**USPS**](usps.md) - United States Postal Service (USPS) är USA:s oberoende posttjänst. USPS erbjuder inrikes och internationell sjöfart på land och flyg.
   - [**FedEx**](fedex.md) - FedEx erbjuder inrikes och internationell frakt per land och flyg till över 220 länder.
   - [**DHL**](dhl.md) - DHL erbjuder integrerade internationella tjänster och skräddarsydda, kundfokuserade lösningar för hantering och transport av brev, varor och information.

## Dimensionell vikt

Dimensionell vikt, som ibland kallas volymetrisk vikt, är en vanlig branschpraxis som baserar transportpriset på en kombination av vikt och paketvolym. Enkelt uttryckt avgör dimensionell vikt fraktkostnaden baserat på den mängd utrymme som ett paket upptar i fraktområdet. Dimensionell vikt används vanligtvis när ett paket är relativt ljust jämfört med dess volym.

Alla större transportföretag tillämpar dimensionell vikt på vissa leveranser. Det sätt som dimensionell viktprissättning tillämpas på varierar dock från ett transportföretag till ett annat. Om ert företag har ett stort antal försändelser kan en liten skillnad i fraktpris innebära tusentals dollar under ett år.

## Konfiguration

Konfigurationsalternativen varierar för olika hållare. Alla kräver dock följande steg:

1. Öppna ett leveranskonto hos transportföretaget.

1. Ange ditt kontonummer eller användar-ID och gateway-URL:en till deras system i butikens konfiguration.

### API-borttagning för USPS Web Tools

Adobe Commerce version 2.4.6, 2.4.7 och 2.4.8 använder de äldre API:erna för webbverktyg för integrering av slutprodukten med USPS. USPS har introducerat USPS-API:er, en REST-baserad plattform som ersätter de äldre API:erna för webbverktyg.

Den 25 januari 2026 upphör USPS med de äldre API:erna för webbverktyg. Efter detta datum kommer alla begäranden till API:er för webbverktyg att misslyckas.

För att undvika avbrott i USPS-leveranserna ska du vidta följande åtgärder före den 25 januari 2026:

- Använd kvalitetskorrigeringen för [USPS REST API-migrering](https://experienceleague.adobe.com/sv/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210) för att lägga till stöd för integrering med REST API:erna för USPS.

- Uppdatera Commerce USPS-konfigurationen så att den använder REST API:er:

   - [Konfiguration av USPS-fraktfirma](usps.md)

   - [Konfiguration av leveransetikett](shipping-label-create.md)

