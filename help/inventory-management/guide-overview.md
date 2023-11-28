---
title: '''Inventory management Guide [!DNL Inventory Management] Guide'
description: Omfattande information om [!DNL Inventory Management] för Adobe Commerce- och Magento Open Source-administratörer, inklusive migrering och konfiguration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# [!DNL Inventory Management] Guide overview

Den här handboken är avsedd för administratörer av Adobe Commerce och Magento Open Source. Där finns detaljerad information om hur du aktiverar den här modulen, inklusive konfiguration och hantering av dess funktioner. Det förutsätter en grundläggande förståelse av kärnan [!DNL Commerce] konfiguration och funktionalitet.

[!DNL Inventory Management] har två områden för administratörer:

- Admin: Använd det här området för att komma åt konfigurationsgränssnittet och rapporter.
- Kommandoradsgränssnittet: Använd det här verktyget för att utföra installations- och serverdelskonfigurationsuppgifter.

Den här guiden täcker:

| Ämne | Beskrivning |
| ------- | ----------- |
| [Introduktion](introduction.md) | Översikt över [!DNL Inventory Management] funktioner som du kan använda för att hantera lager på flera platser så att din Commerce Store korrekt återspeglar det fysiska lagret. |
| [Versionsinformation](release-notes.md) | Läs versionsinformationen om du vill ha information om alla [!DNL Inventory Management] releaser. |
| Grundläggande om lager | Lär dig grunderna om lagerhantering: [Lager och källor](sources-stocks.md), [källval och reservationer](selection-reservations.md), [beställnings- och reservationsstatus](order-status.md)och [produkttyper](product-types.md) |
| Kom igång | Läs mer om [!DNL Inventory Management] och hur den passar in i Commerce-instansen och butiksåtgärder: [Handelsuppgraderingar](migrate.md), [modulinstallation och uppdatering](install-update.md), [leverantörstyper](merchant-sourcing.md)och [förändringar i källstrukturen](expand-restructure.md) |
| [Konfiguration](configuration.md) | Läs mer om konfigurationen av [!DNL Inventory Management] alternativ som bestämmer källans tillgänglighet, butiksprodukter och orderleverans. |
| [Hantera källor](sources-manage.md) | Lär dig mer om källor och hur de definierar de fysiska platser där produktlager hanteras och skickas för orderleverans, eller var det finns tjänster tillgängliga. |
| [Hantera lager](stocks-manage.md) | Lär dig hur Stock används för att representera ett virtuellt, aggregerat produktlager för källor i era försäljningskanaler. |
| [Hantera kvantiteter](quantities-manage.md) | Lär dig hur du tilldelar källor och kvantiteter för nya produkter eller ändrar befintliga produkter. |
| [Hantera beställningar och leveranser](shipments.md) | Läs mer om de andra [!DNL Inventory Management] funktioner och alternativ för att hantera lagerkvantiteter genom leveransprocessen. |
| [CLI-referens](cli.md) | Läs mer om kommandona i [!DNL Inventory Management] för att hantera lagerdata och konfigurationsinställningar. |

{style="table-layout:auto"}

## Utvecklarinformation

Se [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) i utvecklardokumentationen för mer information om modularkitektur, API:er och algoritmanpassning.

## Handelsdokumentation

{{docs-links}}

## Felsökning och support

Om du behöver information eller har frågor som inte ingår i den här handboken använder du följande resurser:

- [Inkonsekvenser i stor nummerreservation](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Lagerinkonsekvenser](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [Färgrutor som inte genomstrykningspapper når &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Lagerstatus är felaktig efter lagerinstallation](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Supportärenden](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)—Skicka in en biljett för att få ytterligare hjälp.
