---
title: Dataöverföring
description: Läs mer om stöd för dataöverföring, inklusive datavalidering.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: 62978d10bc1b53d3a7983b0a37ccd64e6ab0f740
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Dataöverföringar

Använd import- och exportverktygen för att hantera flera poster i en enda åtgärd. Du kan importera nya objekt samt uppdatera, ersätta och ta bort befintliga produktuppsättningar.

Du kan till exempel lägga till nya produkter i lagret, uppdatera produktdata och avancerade prisdata och ersätta en uppsättning befintliga produkter med nya produkter. Med import- och exportverktygen hanterar du stora produktkataloger effektivare eftersom du kan exportera data, redigera dem i ett kalkylblad och importera dem tillbaka till butiken i stället för att utföra flera åtgärder i administratören.

Förutom import- och exportverktygen har Adobe Commerce processer som [katalogsynkronisering](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) som exporterar produktdata från Commerce-servern till SaaS-tjänster. För funktioner som [Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html)kan synkroniseringen göra det möjligt att returnera rekommendationer med korrekta namn, priser och tillgänglighet.

## Dataverifiering

Alla data måste valideras för att säkerställa kvaliteten, tillförlitligheten och integriteten hos värdena innan de importeras till arkivet. Valideringen börjar när du klickar **[!UICONTROL Check Data]**. Under processen kontrolleras alla enheter i importfilen för följande:

- **Attribut** - Kolumnrubriknamnen verifieras för att säkerställa att de matchar motsvarande attribut i systemdatabasen. Värdet för varje attribut kontrolleras för att säkerställa att det uppfyller kraven för datatypen (decimal, integer, varchar, text och datetime).
- **Komplexa data** - Värden som härstammar från en definierad uppsättning, t.ex. en listruta eller flera valda indatatyper, verifieras för att säkerställa att värdena finns i den definierade uppsättningen.
- **Tjänstdata** - Värdena i tjänstdatakolumner verifieras för att säkerställa att egenskaperna eller de komplexa datavärdena överensstämmer med det som redan har definierats i systemdatabasen.
- **Obligatoriska värden** - För nya entiteter kontrolleras om det finns obligatoriska attributvärden i filen. För befintliga enheter behöver du inte kontrollera om det finns obligatoriska attributvärden.
- **Avgränsare** - Även om avgränsarna inte syns när de visas i ett kalkylblad, avgränsas datavärdena i en CSV-fil med kommatecken, och textvärdena omges med citattecken. Under valideringsprocessen kontrolleras formateringen för avgränsarna och varje uppsättning citattecken som omger teckensträngar.

Resultatet av valideringen visas i avsnittet Valideringsresultat och innehåller följande information:

- Antalet enheter som kontrollerats
- Antalet ogiltiga rader
- Antalet fel som hittats

Om data är giltiga kan du _Importen lyckades_ visas.

![Systemmeddelande - filen är giltig](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Om valideringen misslyckas läser du beskrivningen av varje fel och korrigerar problemet i CSV-filen. Om en rad till exempel innehåller en ogiltig SKU avbryts importen och den raden och alla efterföljande rader importeras inte. När problemet är korrekt importerar du data igen. Om många fel påträffas kan det ta flera försök att godkänna valideringen.

### Dataverifieringsmeddelanden

#### Validering

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Fel

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
