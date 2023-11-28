---
title: Exportera data
description: Lär dig mer om dataexportfilter och -attribut och hur du exporterar data från din butik.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Exportera data

Det bästa sättet att bli bekant med databasens struktur är att exportera data och öppna dem i ett kalkylblad. När du lärt dig processen kan du använda den som ett effektivt sätt att hantera stora mängder information.

Specialtecken - som likhetstecken, större och mindre än symboler, enkla och dubbla citattecken, omvänt snedstreck, vertikalstreck och et-tecken - kan orsaka problem vid dataöverföring. För att säkerställa att sådana specialtecken tolkas korrekt kan de markeras som _escape-sekvens_. Om data till exempel innehåller en textsträng, som `code="str"`, `code="str2"`, som omger texten med dubbla citattecken, säkerställer att de ursprungliga dubbla citattecknen tolkas som en del av informationen: `"code="str""`. När systemet stöter på en dubbel uppsättning med dubbla citattecken är det förstått att den yttre uppsättningen med dubbla citattecken omsluter de faktiska data.

Dataexport är en asynkron åtgärd som körs i bakgrunden så att du kan fortsätta arbeta i administratören utan att vänta på att åtgärden ska slutföras. Ett meddelande visas när uppgiften är slutförd.

## Exportvillkor

Exportfilter används för att ange de data som du vill använda i exportfilen, baserat på attributvärde. Dessutom kan du ange vilka attributdata som du vill inkludera eller exkludera från exporten.

![Kriterier för dataexport](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Exportfilter

Du kan använda filter för att avgöra vilka SKU:er som ska inkluderas i exportfilen. Om du t.ex. anger ett värde i filtret Tillverkningsland inkluderar den exporterade CSV-filen endast produkter som tillverkats i det landet.

Filtertypen motsvarar datatypen. För datumfält kan du välja datumet i kalendern ![Kalenderikon](../assets/icon-calendar.png). Se [Attributindatatyper](../catalog/attributes-input-types.md) för mer information.

Formatet på datumet bestäms av [locale](../getting-started/store-details.md#locale-options).

Om du bara vill inkludera poster med ett visst värde, t.ex. en SKU, anger du värdet i fältet Filter. Vissa fält, till exempel Price, Weight och Set Product as New, har ett intervall av värden från/till.

### Uteslut attribut

Kryssrutan i den första kolumnen används för att exkludera attribut från exportfilen. Om ett attribut utelämnas inkluderas den associerade kolumnen i exportdata, men den är tom.

| Exkludera | Filter | Resultat |
|--- |--- |--- |
| ![Rensad kryssruta](../assets/checkbox-clear.png) | Nej | Den exporterade filen innehåller alla attribut för alla befintliga poster. |
| ![Rensad kryssruta](../assets/checkbox-clear.png) | Ja | Exportfilen innehåller varje attribut med endast de poster som tillåts av filtret. |
| ![Markerad kryssruta](../assets/checkbox-selected.png) | Nej | Exportfilen innehåller inte kolumnen för attributet exclude, men innehåller alla befintliga poster. |
| ![Markerad kryssruta](../assets/checkbox-selected.png) | Ja | Exportfilen innehåller inte kolumnen för det exkluderade attributet och innehåller bara de poster som tillåts av filtret. |

{style="table-layout:auto"}

## Exportera data

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. I _Exportinställningar_ avsnitt, ange **[!UICONTROL Entity Type]** till något av följande:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![Dataexportinställningar](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Acceptera standardinställningen **[!UICONTROL Export File Format]** i CSV.

1. Om du vill omsluta specialtecken som finns i data som _escape-sekvens_ väljer du **[!UICONTROL Fields Enclosure]** kryssrutan.

1. Ändra visningen av entitetsattributen om det behövs.

   Som standard listas alla tillgängliga attribut i alfabetisk ordning i avsnittet Entitetsattribut. Du kan använda standarden [listkontroller](../getting-started/admin-grid-controls.md) om du vill söka efter särskilda attribut och sortera listan. Filtret Sök och återställ styr visningen av listan, men påverkar inte urvalet av attribut som ska inkluderas i exportfilen.

   ![Filtrerade entitetsattribut för dataexport](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Så här filtrerar du exporterade data baserat på attributvärde:

   - Om du bara vill exportera poster med specifika attributvärden anger du det obligatoriska värdet i **[!UICONTROL Filter]** kolumn. I följande exempel exporteras endast en specifik SKU.

   - Om du vill utesluta ett attribut från exporten markerar du **[!UICONTROL Exclude]** i början av raden. Om du till exempel bara vill exportera `sku` och `image` markerar du kryssrutan för alla andra attribut. Kolumnen visas i exportfilen, men utan värden.

1. Rulla ned och klicka **[!UICONTROL Continue]** i sidans nedre högra hörn.

   När uppgiften är slutförd bearbetas filen via en meddelandekö (kontrollera att ditt cron-jobb körs). Den exporterade filen sparas i `var/export/ folder`. Mer information om meddelandekön finns i [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) i _Konfigurationshandbok_.

   Du kan spara eller öppna den exporterade CSV-filen som ett kalkylblad, redigera data och sedan importera dem tillbaka till din butik.

   >[!NOTE]
   >
   >Som standard finns alla exporterade filer i `<Magento-root-directory>/var/export` mapp. Om fjärrlagringsmodulen är aktiverad finns alla exporterade filer i `<remote-storage-root-directory>/import_export/export` mapp.

## Felsökningsresurser

Hjälp med felsökning av dataexportproblem finns i följande artiklar i kunskapsbasen med Commerce Support:

- [CSV-filen för exporterade produkter visas inte](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [Produktexportfilen visas inte i Admin](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [Problem vid export av order i CSV-format](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)
