---
title: 'Inventory management Guide [!DNL Inventory Management] Guide'
description: Omfattande information om  [!DNL Inventory Management]  för Adobe Commerce- och Magento Open Source-administratörer, inklusive migrering och konfiguration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Översikt över guiden [!DNL Inventory Management]

Den här handboken är avsedd för administratörer av Adobe Commerce och Magento Open Source. Där finns detaljerad information om hur du aktiverar den här modulen, inklusive konfiguration och hantering av dess funktioner. Det förutsätter en grundläggande förståelse av kärnkonfigurationen och funktionen för [!DNL Commerce].

[!DNL Inventory Management] har två områden för administratörer:

- Admin: Använd det här området för att komma åt konfigurationsgränssnittet och rapporter.
- Kommandoradsgränssnittet: Använd det här verktyget för att utföra installations- och serverdelskonfigurationsuppgifter.

Den här guiden täcker:

| Ämne | Beskrivning |
| ------- | ----------- |
| [Introduktion](introduction.md) | Översikt över de [!DNL Inventory Management]-funktioner som du kan använda för att hantera lager på flera platser så att din Commerce-butik korrekt återspeglar den fysiska inventeringen. |
| [Versionsinformation](release-notes.md) | Granska versionsinformationen för information om alla [!DNL Inventory Management]-versioner. |
| Grundläggande om lager | Lär dig grunderna om lagerhantering: [Stock och källor](sources-stocks.md), [källval och reservationer](selection-reservations.md), [status för beställning och reservation](order-status.md) samt [produkttyper](product-types.md) |
| Kom igång | Lär dig mer om modulen [!DNL Inventory Management] och hur den passar in i dina instans- och butiksåtgärder i Commerce: [Commerce-uppgraderingar](migrate.md), [modulinstallation och uppdatering](install-update.md), [leverantörstyper](merchant-sourcing.md) och [källstrukturförändringar](expand-restructure.md) |
| [Konfiguration](configuration.md) | Lär dig mer om konfigurationen av [!DNL Inventory Management] alternativ som bestämmer källtillgänglighet, butiksprodukter och orderleverans. |
| [Hantera källor](sources-manage.md) | Lär dig mer om källor och hur de definierar de fysiska platser där produktlager hanteras och skickas för orderleverans, eller var det finns tjänster tillgängliga. |
| [Hantera lager](stocks-manage.md) | Lär dig hur Stock används för att representera ett virtuellt, aggregerat produktlager för källor i era försäljningskanaler. |
| [Hantera kvantiteter](quantities-manage.md) | Lär dig hur du tilldelar källor och kvantiteter för nya produkter eller ändrar befintliga produkter. |
| [Hantera beställningar och leveranser](shipments.md) | Lär dig mer om de ytterligare [!DNL Inventory Management] funktionerna och alternativen för att hantera lagerkvantiteter genom leveransprocessen. |
| [CLI-referens](cli.md) | Lär dig mer om kommandona från modulen [!DNL Inventory Management] för att hantera lagerdata och konfigurationsinställningar. |

{style="table-layout:auto"}

## Utvecklarinformation

Mer information om modularkitektur, API:er och algoritmanpassning finns i [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) i utvecklardokumentationen.

## Commerce-dokumentation

{{docs-links}}

## Felsökning och support

Om du behöver information eller har frågor som inte ingår i den här handboken använder du följande resurser:

- [Inkonsekvenser för stor nummerreservation](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Lagerinkonsekvenser ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [Färgrutor som inte genomstrykningspenseln når &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Stock-status är felaktig efter lagerinstallation](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Supportärenden](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) - Skicka in en biljett för att få ytterligare hjälp.
