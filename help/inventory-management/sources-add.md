---
title: Lägg till en lagerkälla
description: Lär dig hur du skapar en källa för en plats, till exempel ett lagerställe, en fysisk butik, ett distributionscenter eller en avsändare.
exl-id: 1bff9986-8722-4fb5-ac83-41de82325f7b
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Lägg till en källa

Hantera lagerhantering och orderhantering från flera platser med anpassade källor. Skapa en källa för varje plats, t.ex. lagerlokaler, butiker, distributionscenter och lossningsplatser. Tilldela källor och uppdateringskvantiteter per produkt

Om du redigerar standardkällan kan du redigera alla konfigurationer förutom namn och kod. Vi rekommenderar att handlare med en enda källa lägger till information som matchar deras plats.

## Lägg till en lagerkälla

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Klicka på **[!UICONTROL Add New Source]**.

   ![Hantera källor](assets/inventory-sources.png)

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL General]** och gör följande:

   - Identifiera lagerkällan genom att ange en unik **[!UICONTROL Name]**.

   - Ange ett unikt **[!UICONTROL Code]**.

     Koden stöder versaler och gemener, siffror, bindestreck och understreck. Koden är ett unikt ID som används vid tilldelning till lager och export av importerade data.

   - Om den här lagerkällan är klar att användas anger du **[!UICONTROL Is Enabled]** till `Yes`.

   - Ange en kort beskrivning **[!UICONTROL Description]** för den här platsen för snabb referens eller ytterligare information.

   - För **[!UICONTROL Latitude]** och **[!UICONTROL Longitude]** Ange GPS-koordinaterna (Global Positioning System) för lokaliseringen.

     Hitta GPS-koordinaterna med [Google Maps][1]anger du adressen i sökrutan. Högerklicka på markören på kartan och välj **[!UICONTROL What's here?]**. GPS-koordinaterna visas i informationsrutan nedanför gatuadressen.

     ![Allmänna källalternativ](assets/inventory-source-general.png)

   - Om den här lagerkällan är en hämtningsplats anger du **[!UICONTROL Use as Pickup Location]** till `Yes`.

     Standardkällan kan inte användas som hämtningsplats för hämtningsorder i butiken.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Contact Info]** och gör följande:

   - För **[!UICONTROL Contact Name]** anger du det fullständiga namnet på den primära kontakten på platsen.

   - Ange en **[!UICONTROL Email]** adress för att kontakta platsen.

   - För **[!UICONTROL Phone]** anger du riktnummer och telefonnummer.

   - För **[!UICONTROL Fax]** anger du riktnummer och telefonnummer för faxet, om tillgängligt.

     ![Kontaktinformation](assets/inventory-source-contact-info.png)

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Address Data]** och gör följande:

   - Välj **[!UICONTROL Country]**.

   - För **[!UICONTROL State/Province]** anger du standardförkortningen för den aktuella regionen.

   - Ange **[!UICONTROL City]**.

   - Ange fysisk **[!UICONTROL Street]** adress.

   - För **[!UICONTROL Postcode]** Ange postnummer.

     ![Adressdata](assets/inventory-source-address.png)

1. Om du angav källan som en hämtningsplats i det tidigare steget expanderar du ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Pickup Location]** och ge beskrivande information om platsen:

   - Ange **[!UICONTROL Frontend Name]** på hämtningsplatsen.

   - Ange en **[!UICONTROL Frontend Description]** på hämtningsplatsen. Använd den här textrutan för att visa butikstimmar, platsen i förhållande till andra landmärken eller annan användbar information som hjälper kunden att välja rätt hämtningsplats.

     ![Hämtningsplats](assets/inventory-pickup-location.png)

   Mer information om hur du konfigurerar e-postmeddelanden när du använder en källa som hämtningsplats finns i [Försäljningsmejl](../configuration-reference/sales/sales-emails.md) i _Referenshandbok för konfiguration_.

1. Gör något av följande om du vill spara ditt arbete:

   - Om du vill spara ditt arbete och fortsätta redigera klickar du på **[!UICONTROL Save & Continue]**.

   - Om du vill spara ditt arbete och gå tillbaka till sidan Hantera källor klickar du på nedpilen (![Menypil](../assets/icon-menu-down-arrow-red.png)) och välja **[!UICONTROL Save & Close]**.

   - Om du vill spara ditt arbete på den aktuella källposten och ange en ny källa väljer du **[!UICONTROL Save & New]**.

## Knappfält

| Knapp | Beskrivning |
|--|--|
| [!UICONTROL Back] | Återgår till sidan Hantera källor. |
| [!UICONTROL Reset] | Återställer alla fält i formuläret till sina värden när de senast sparades. |
| [!UICONTROL Save & Continue] | Sparar alla ändringar och låter formuläret vara öppet för vidare redigering. Klicka på nedpilen om du vill se ytterligare alternativ:<br/>**[!UICONTROL Save & Close]**- Sparar ändringar i den aktuella posten, stänger formuläret och återgår till sidan Hantera källor.<br/>**[!UICONTROL Save & New]** - Sparar ändringar, stänger den aktuella posten och öppnar ett nytt tomt formulär. |

## Fältbeskrivningar

| Fält | Beskrivning |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | (Obligatoriskt) Ett unikt namn som identifierar lagerkällan för administratörsanvändare. |
| [!UICONTROL Code] | (Obligatoriskt) En unik alfanumerisk kod som används av systemet för att identifiera lagerkällan. Ange koden med versaler eller gemener, utan mellanslag. Om det behövs kan du använda ett bindestreck eller ett understreck i stället för ett mellanslag. Koden kan inte redigeras efter att källan har skapats. Det är ett unikt ID som används när du tilldelar källor till lager och exporterar och/eller importerar produktdata. |
| [!UICONTROL Is Enabled] | Fastställer om lagerkällan är tillgänglig för användning. Alternativ: Ja/Nej |
| [!UICONTROL Description] | En kort beskrivning av lagerkällans plats. Inkludera information som är användbar för dina Admin-användare. |
| [!UICONTROL Latitude] | Anger latitudkoordinaten för lagerkällan för GPS. Ange värdet som ett tal, föregånget av ett plus- eller minustecken efter behov. Gradsymbolen och bokstäverna är inte tillåtna. Exempel: Latitude 32.7555 |
| [!UICONTROL Longitude] | Anger longitudkoordinaten för lagerkällan för GPS. Ange värdet som ett tal, föregånget av ett plus- eller minustecken efter behov. Gradsymbolen och bokstäverna är inte tillåtna. Exempel: `-97.3308` |
| **[!UICONTROL Contact Info]** | |
| [!UICONTROL Contact Name] | Namnet på den primära kontakten på lagerkällans plats. |
| [!UICONTROL Email] | Den primära kontaktens e-postadress. |
| [!UICONTROL Phone] | Den primära kontaktens riktnummer och telefonnummer, i det format du föredrar. Till exempel: `(123) 456-7890` eller `123-456-7890` |
| [!UICONTROL Fax] | Den primära kontaktens riktnummer och faxnummer. |
| **[!UICONTROL Address Data]** | |
| [!UICONTROL Country] | (Obligatoriskt) Landet där lagerkällan finns. |
| [!UICONTROL State/Province] | Den delstat eller provins där lagerkällan finns. |
| [!UICONTROL City] | Ort där lagerkällan finns. |
| [!UICONTROL Street] | Lagerkällans gatuadress. |
| [!UICONTROL Postcode] | (Obligatoriskt) Lagerkällans postnummer. |
| **[!UICONTROL Pickup Location]** | |
| [!UICONTROL Frontend Name] | Namnet på hämtningsplatsen för källan som visas på butiken. |
| [!UICONTROL Frontend Description] | Beskrivningen av hämtningsplatsen för källan som visas på butiken. Den kan innehålla bifogade bilder. |

[1]: https://www.google.com/maps
