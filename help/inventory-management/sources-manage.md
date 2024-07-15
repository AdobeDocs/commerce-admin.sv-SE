---
title: Hantera lagerkällor
description: Lär dig mer om källor och hur de definierar de fysiska platser där produktlager hanteras och skickas för orderleverans, eller var det finns tjänster tillgängliga.
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Hantera källor

Källor är de fysiska platser där produktlager hanteras och skickas för orderleverans, eller där tjänster finns tillgängliga. De här platserna kan vara lagerlokaler, butiker, distributionscentraler, hämtningsplatser och lossningsplatser. Du allokerar lagerkvantiteter till de här källorna och [!DNL Commerce] aggregerar automatiskt den totala säljbara produkten för dina lager. För stora företag kan du lägga till flera källor för alla dina platser: på olika geografiska platser per land och kontinent, platser i en stad, baserat på typen av lager, även baserat på tjänster.

Du bör ange specifika fysiska geografiska platser när du skapar en källa. Det gör att algoritmen _Distansprioritet_ kan jämföra platsen för leveransdestinationsadressen med de tillgängliga källplatserna för att fastställa den närmaste källan för leverans. Du kan använda Google Maps eller offlineberäkningar, som använder geokoder. Mer information om den här _algoritmen för avståndsprioritet_ finns i [Konfigurera algoritm för avståndsprioritet](distance-priority-algorithm.md).

Börja med en _standardversion av Source_ som du kan uppdatera men inte inaktivera. Den här källan används av handlare med en enda källa och för produktmigrering. Du behöver alltid en standardkälla.

- **Platsinformation** - Varje källa innehåller namn, land, fysisk adress för platsen och en kontaktpunkt.
- **Aktiverar resurser** - Du kan aktivera och inaktivera källor efter behov. Aktivera bara en källa om den godkänner och slutför order och restorder.
- **Tillgängligt lager** - Tilldela och uppdatera lagerkvantiteter för varje källa via produktsidan. Lagerkvantiteterna beräknas, tillhandahålls och reserveras genom käll- och lagermappningen.

I följande diagram illustreras källorna till en Bicycle Shop-handlare som säljer en bergscykel som är tillgänglig för lager och tillgänglig för SSA för leveranser.

![Exempel på källdiagram](assets/diagram-sources.png){width="600" zoomable="yes"}

Alla butiker börjar med en standardinställd Source som måste vara aktiverad:

- Alla nya produkter som importeras till [!DNL Commerce] kräver en källa och ett lager som automatiskt tilldelas för omedelbar åtkomst till [!DNL Inventory Management].
- Handlare med en enda källa använder standardinställningen Source som sin enda lagerplats och sina leveranser.

## Redigera källor

Du kan uppdatera namn, adress, GPS-plats och kontaktinformation. Källkoden är ett skyddat värde som fungerar som ett unikt ID som associerar källan med dina produktkvantiteter och lager.

Om du redigerar Source Standard kan du redigera alla konfigurationer förutom namn och kod. Vi rekommenderar att handlare med en enda källa lägger till information som matchar deras plats.

På sidan _[!UICONTROL Manage Sources]_visas alla tillgängliga lagerplatser och leveransanläggningar. Du kan lägga till nya lagerkällor och redigera befintliga platser.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**på sidofältet_ Admin _.

1. Mer information om hur du lägger till en lagerplats finns i [Lägga till en ny Source](sources-add.md).

1. Hitta lagerkällan och öppna den i läget _Redigera_.

1. Uppdatera informationen och spara ändringarna.

   ![Hantera källor](assets/inventory-sources.png){width="600" zoomable="yes"}

## Knappfält

| Knapp | Beskrivning |
|--|--|
| [!UICONTROL Add New Source] | Öppnar formuläret New Source som används för att ange en ny lagerkälla, leveransanläggning eller plats. |

## Hantera kolumnbeskrivningar för källor

| Kolumn | Beskrivning |
|--|--|
| [!UICONTROL Code] | En unik alfanumerisk kod som används av systemet för att identifiera lagerkällan. |
| [!UICONTROL Name] | Ett unikt namn som identifierar lagerkällan för administratörsanvändare. |
| [!UICONTROL Is Enabled] | Anger om lagerkällan är aktiv och tillgänglig att använda. |
| [!UICONTROL Pickup Location] | Anger om källan är aktiv som hämtningsplats för [butiksleverans](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | Om du klickar på **[!UICONTROL Edit]** öppnas lagerkällposten i redigeringsläge. |

## Andra kolumner

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Latitude] | Anger latitudkoordinaten för lagerkällan för GPS. Ange värdet som ett tal, föregånget av ett plus- eller minustecken efter behov. Gradsymbolen och bokstäverna är inte tillåtna. Till exempel: `32.7555` |
| [!UICONTROL State/Province] | Den delstat eller provins där källan finns. |
| [!UICONTROL Postcode] | Källans postnummer. |
| [!UICONTROL Email] | Den primära kontaktens e-postadress. |
| [!UICONTROL Longitude] | Anger longitudkoordinaten för lagerkällan för GPS. Ange värdet som ett tal, föregånget av ett plus- eller minustecken efter behov. Gradsymbolen och bokstäverna är inte tillåtna. Exempel: Longitude -97.3308 |
| [!UICONTROL City] | Ort där källan finns. |
| [!UICONTROL Phone] | Den primära kontaktens telefonnummer. |
| [!UICONTROL Country] | Det land där källan finns. |
| [!UICONTROL Street] | Källans gatuadress. |
| [!UICONTROL Fax] | Den primära kontaktens riktnummer och faxnummer. |
