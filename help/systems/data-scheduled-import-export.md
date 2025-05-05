---
title: Schemalagd import och export
description: Lär dig hur du hanterar schemalagda dataimport- och exportåtgärder.
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '2429'
ht-degree: 0%

---

# Schemalagd import och export

{{ee-feature}}

Tidsplanerade importer och exporter kan köras dagligen, varje vecka eller varje månad. De filer som ska importeras eller exporteras kan finnas på lokala Adobe Commerce-servrar eller på fjärranslutna FTP-servrar. Schemalagd import/export implementeras som standard och kräver ingen ytterligare konfiguration. Alla schemalagda importer och exporter hanteras av Cron-jobbschemaläggaren.

## Schemalagd import/export

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**&#x200B;på sidofältet_ Admin _.

   ![Schemalagd import/export av data](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. Om du vill skapa ett nytt schemalagt import- eller exportjobb klickar du på lämplig knapp och följer instruktionerna för den schemalagda jobbtypen.

   - [Lägg till schemalagd export](#schedule-an-export)
   - [Lägg till schemalagd import](#schedule-an-import)

1. När posten sparas visas jobbet i rutnätet _[!UICONTROL Scheduled Import/Export]_.

   >[!NOTE]
   >
   >När du skapar eller uppdaterar en schemalagd import/export ändras systemkonfigurationen. När du har sparat måste du åtgärda det cacheminnet som visas högst upp på Admin-sidan och tömma cacheminnet för att tillämpa det nya eller uppdaterade schemat.

1. [!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Efter varje schemalagt jobb placeras en kopia av filen i katalogen `var/log/import_export` på den lokala Adobe Commerce-servern.

   Information om varje åtgärd skrivs inte till loggen. Om ett fel inträffar skickas ett meddelande om det misslyckade import-/exportjobbet med en beskrivning av felet.

## Schemalägg en import

Den schemalagda importprocessen liknar den manuella importprocessen för de tillgängliga importfilformaten och typerna av importenheter:

- Importfilen ska vara i .CSV-format
- Du kan importera produkt- och kunddata

Fördelen med schemalagd import är att du automatiskt kan importera en datafil flera gånger efter att du har angett importparametrar och schemalägga endast en gång.

Information om varje importåtgärd skrivs inte till en logg, men om ett fel uppstår får du ett e-postmeddelande om att det gick att importera _misslyckades_ med en beskrivning av felet. Resultatet av det senaste schemalagda importjobbet visas i kolumnen Senaste resultat på sidan Schemalagd import/export.

[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Efter varje importåtgärd placeras en kopia av importfilen i katalogen `var/log/import_export` på den server där Adobe Commerce eller Magento Open Source distribueras. Tidsstämpeln, markören för den importerade enheten (produkter eller kunder) och typen av åtgärd (i det här fallet import) läggs till i importfilens namn.

Efter varje schemalagt importjobb utförs en indexeringsåtgärd automatiskt. I den vänstra delen återspeglas ändringar i beskrivningarna och annan textinformation efter att de uppdaterade uppgifterna har skickats till databasen, och prisändringarna återspeglas först efter omindexeringsåtgärden.

### Steg 1: Slutför importinställningarna

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Scheduled Import]** i det övre högra hörnet.

1. Ange alternativ för schemaläggning och import:

   - **[!UICONTROL Name]** - Ange ett namn för den schemalagda importen.

   - **[!UICONTROL Description]** - Ange en kort beskrivning som förklarar syftet med importen och hur den ska användas.

   - **[!UICONTROL Entity Type]** - Ange något av följande:

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]** - Ange något av följande:

      - `Add/Update Complex Data` - Lägger till eller uppdaterar nya komplexa data till befintliga komplexa data för befintliga poster i databasen. Det här är standardvärdet.
      - `Replace` - Skriver över befintliga komplex för befintliga entiteter i databasen.
      - `Delete Entities` - Tar bort befintliga poster i databasen.
      - `Custom Action` - Anpassar befintliga enheter i databasen.

     >[!NOTE]
     >
     >För entitetstyperna _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_, _[!UICONTROL Customers and Addresses (single file)]_&#x200B;och&#x200B;_[!UICONTROL Stock Sources]_ visas följande importbeteenden: `Add/Update`, `Replace` och `Delete`. För entitetstyperna _Kundekonomi_, _Kundens huvudfil_ och _Kunder och adresser_ visas följande importbeteenden: `Add/Update Complex Data`, `Delete Entities` och `Custom Action`.

   - **[!UICONTROL Start Time]** - Ange timma, minut och sekund när importen är schemalagd att börja.

   - **[!UICONTROL Frequency]** - Ange något av följande: `Daily`, `Weekly` eller `Monthly`

   - **[!UICONTROL On Error]** - Ange något av följande: `Stop Import` eller `Continue Processing`

   - **[!UICONTROL Status]** - Om du vill aktivera den schemalagda importen anger du `Enabled`.

   - **[!UICONTROL Field Separator]** - Ange tecknet som används för att avgränsa fält i importfilen. Standardtecknet är ett komma.

   - **[!UICONTROL Multiple Value Separator]** - Ange tecknet som används för att avgränsa flera värden inom ett fält.

   ![Dataimport - schemalagda importinställningar](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### Steg 2: Fyll i importfilsinformationen

1. Ange **[!UICONTROL Server Type]** till något av följande:

   - `Local Server` - Importerar data från den server där Adobe Commerce är installerat.
   - `Remote FTP` - Importerar data från en fjärrserver.

   ![Dataimport - information om schemalagda importfiler](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >När fjärrlagringsmodulen är aktiverad växlar `Local Server` automatiskt till `Remote Storage`.

1. Ange **[!UICONTROL File Directory]** som importfilen kommer från.

   - `Local Server` - Ange en relativ sökväg i Commerce-installationen. Exempel: `var/import`. Om fjärrlagringsmodulen är konfigurerad använder du `import_export/import`.
   - `Remote FTP server` - Ange den fullständiga URL:en och sökvägen till importmappen på fjärrservern.

1. Ange **[!UICONTROL File Name]** som ska importeras.

1. För **[!UICONTROL Images File Directory]** anger du sökvägen till den katalog där produktbilder lagras.

   På en lokal server anger du en relativ sökväg som: `var/import`. På en fjärrlagring anger du en relativ sökväg som: `import_export/import` eller `import_export/import/some/dir`.

### Steg 3: Konfigurera misslyckade e-postmeddelanden för import

![Dataimport - det gick inte att importera e-postmeddelanden](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Failed Email Receiver]** till den butikskontakt som ska ta emot meddelanden om ett fel inträffar under importen.

1. Ange **[!UICONTROL Failed Email Sender]** till butikskontakten som visas som meddelandets avsändare.

1. Ange **[!UICONTROL Failed Email Template]** till mallen som används för meddelandet.

1. För **[!UICONTROL Send Failed Email Copy To]** anger du e-postadressen till alla som ska få en kopia av meddelandet.

   Avgränsa flera e-postadresser med komma.

1. Ange **[!UICONTROL Failed Email Copy Method]** till något av följande:

   - `Bcc` - Skickar en kopia av det misslyckade importmeddelandet med blindhet. Mottagarens namn och adress inkluderas i den ursprungliga e-postdistributionen, men döljs.
   - `Separate Email` - Skickar en kopia av det misslyckade importmeddelandet som ett separat e-postmeddelande.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Det nya schemalagda importjobbet läggs till i listan på sidan _[!UICONTROL Scheduled Import/Export]_. Från den här sidan kan den köras direkt för testning och redigering. Importfilen valideras innan varje importjobb körs.

>[!NOTE]
>
>När du skapar eller uppdaterar en schemalagd import/export ändras systemkonfigurationen. När du har sparat måste du åtgärda det cacheminnet som visas högst upp på Admin-sidan och tömma cacheminnet för att tillämpa det nya eller uppdaterade schemat.

### Fältbeskrivningar

#### [!UICONTROL Import Settings]

| Fält | Beskrivning |
| ----- | ----------- | 
| [!UICONTROL Name] | Importens namn. Hjälper dig att skilja på det om många olika schemalagda importer skapas. |
| [!UICONTROL Description] | (Valfritt) Du kan ange en beskrivning. |
| [!UICONTROL Entity Type] | Definierar de data som ska importeras. |
| [!UICONTROL Import Behavior] | Definierar hur komplexa data hanteras om de enheter som importeras finns i databasen. Komplexa produktdata omfattar kategorier, webbplatser, anpassade alternativ, nivåpriser, relaterade produkter, merförsäljning, korsförsäljning och tillhörande produktdata. Komplexa data för kunderna inkluderar adresser. Alternativ:<br>**[!UICONTROL Add/Update Complex Data]**- Nya komplexa data läggs till eller uppdateras till befintliga komplexa data för befintliga poster i databasen. Det här är standardvärdet.<br>**[!UICONTROL Add/Update]** - Nya data läggs till i de befintliga posterna i databasen. Alla fält utom `sku` kan uppdateras för produkter. Flera fältvärden som inte finns med i CSV-filen, t.ex. kategorier eller webbplatser, finns kvar i databasen efter importen.<br>**[!UICONTROL Replace]**- Befintliga komplexa data för befintliga entiteter ersätts.<br>**[!UICONTROL Delete Entities]** - Om importerade entiteter finns i databasen tas de bort från databasen.<br>**[!UICONTROL Custom Action]**- Befintliga komplexa entiteter anpassas under importprocessen. |
| [!UICONTROL Start Time] | Ange starttimmen, minuter och sekunder för importen. |
| [!UICONTROL Frequency] | Definiera hur ofta importen ska köras. Alternativ: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | Definiera systembeteendet om fel påträffas under filvalideringen. Alternativ:<br>**Stoppa import** - Filen importeras inte om fel påträffas under valideringen. Det här är standardvärdet.<br>**Fortsätt bearbeta** - Om fel påträffas under valideringen, men det går att importera filen, importeras den. |
| [!UICONTROL Status] | Importen är aktiverad som standard. Du kan göra uppehåll genom att ange statusen till `Disabled`. |
| [!UICONTROL Field Separator] | Bestämmer vilket tecken som används för att avgränsa fält. Standardvärde: `,` (komma) |
| [!UICONTROL Multiple Value Separator] | Anger det tecken som används för att avgränsa flera värden inom ett fält. Standardvärde: `,` (komma) |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| Fält | Beskrivning |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Du kan importera från en fil på den server där Commerce är distribuerat (välj `Local Server`) eller från fjärr-FTP-servern (välj `Remote FTP`). Om du väljer _[!UICONTROL Remote FTP]_&#x200B;visas ytterligare alternativ för autentiseringsuppgifter och filöverföringsinställningar. Om fjärrlagringsmodulen är aktiverad växlas typen `Local Server` automatiskt till `Remote Storage`. |
| [!UICONTROL File Directory] | Ange den katalog där importfilen finns. Om servertypen är inställd på _[!UICONTROL Local Server]_&#x200B;anger du sökvägen i förhållande till Commerce installationskatalog. Till exempel: `var/import` eller `import_export/import` för fjärrlagring. |
| [!UICONTROL File Name] | Ange namnet på importfilen. |
| [!UICONTROL Images File Directory] | Ange sökvägen till den katalog där produktbilderna lagras. Ange en relativ sökväg för en lokal server. Till exempel: `var/import` eller `import_export/import` för fjärrlagring. |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| Fält | Beskrivning |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Ange den e-postadress till vilken ett e-postmeddelande (ej godkänd import) skickas om importen misslyckas. |
| [!UICONTROL Failed Email Sender] | Ange den e-postadress som används som avsändare för den misslyckade importen. |
| [!UICONTROL Failed Email Template] | Välj en mall för e-postmeddelandet som inte kunde importeras. Som standard är endast alternativet Import misslyckades (standardmall från språkområde) tillgängligt. Anpassade mallar kan skapas under _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_. |
| [!UICONTROL Send Failed Email Copy To] | Den e-postadress till vilken en kopia av det importerade e-postmeddelandet inte kunde skickas. |
| [!UICONTROL Send Failed Email Copy Method] | Välj kopieringsmetod för e-post som inte kunde importeras. |

{style="table-layout:auto"}

## Schemalägg en export

Schemalagd export liknar manuell [export](data-export.md) i det tillgängliga exportfilformatet och de typer av entiteter som kan exporteras:

- Du kan exportera till CSV-format
- Du kan exportera produkt- och kunddata

Fördelen med att använda schemalagd export är att du kan exportera data flera gånger automatiskt efter att du har angett exportparametrar och schemalägga endast en gång.

Detaljerad information om varje export skrivs inte till en logg, men om ett fel uppstår får du ett e-postmeddelande om att exporten misslyckades, som innehåller felbeskrivningen. Resultatet av det senaste exportjobbet visas i kolumnen Senaste resultat på sidan Schemalagd import/export.

[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Efter varje export placeras exportfilen på den användardefinierade platsen och en kopia i katalogen `var/log/import_export` på den server där Adobe Commerce eller Magento Open Source distribueras. Tidsstämpeln och markören för den exporterade enheten (produkter eller kunder) och typen av åtgärd (i det här fallet export) läggs till i exportfilens namn.

### Steg 1: Slutför exportinställningarna

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Scheduled Export]** i det övre högra hörnet och gör följande:

   - Ange **[!UICONTROL Name]** för den schemalagda exporten.

   - Ange en kort **[!UICONTROL Description]** som förklarar syftet med exporten och hur den ska användas.

   - Ange **[!UICONTROL Entity Type]** till något av följande:

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     Avsnittet _[!UICONTROL Entity Attributes]_&#x200B;längst ned på sidan uppdateras för att återspegla den valda entitetstypen.

   - Ange **[!UICONTROL Start Time]** till timmen, minuten och sekunden när exporten är schemalagd att börja.

   - Ange **[!UICONTROL Frequency]** till något av följande:

      - `Daily`
      - `Weekly`
      - `Monthly`

1. Om du vill aktivera den schemalagda exporten anger du **[!UICONTROL Status]** till `Enabled`.

1. Acceptera `CSV` som standard **[!UICONTROL File Format]**.

   ![Schemalagda exportinställningar](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### Steg 2: Fyll i exportfilsinformationen

1. Ange **[!UICONTROL Server Type]** till något av följande:

   - `Local Server` - Om du vill spara exportfilen på den server där Commerce är installerat.
   - `Remote FTP` - Så här sparar du exportfilen på en fjärrserver.

   ![Information om schemalagd exportfil](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >När fjärrlagringsmodulen är aktiverad växlar `Local Server` automatiskt till `Remote Storage`.

1. För **[!UICONTROL File Directory]** anger du katalogen där exportfilen ska sparas enligt följande:

   - För **[!UICONTROL Local Server]** anger du en relativ sökväg i Commerce-installationen, till exempel `var/export`. Om fjärrlagringsmodulen är konfigurerad använder du `import_export/export`.
   - För **[!UICONTROL Remote FTP server]** anger du den fullständiga URL:en och sökvägen till målmappen på målservern.

1. Om servern _[!UICONTROL Remote FTP]_&#x200B;är markerad anger du autentiseringsuppgifter för anslutningen till servern och väljer ytterligare inställningar:

   - Ange fjärr-FTP-värdadress för **[!UICONTROL FTP Host[:Port]]**.
   - För **[!UICONTROL User Name]** anger du det användarnamn som används för att komma åt fjärrservern.
   - För **[!UICONTROL Password]** anger du lösenordet för det angivna användarnamnskontot.
   - För **[!UICONTROL File Mode]** väljer du `Binary` eller `ASCII`.
   - För **[!UICONTROL Passive Mode]** väljer du `No` eller `Yes`.

### Steg 3: Konfigurera e-postmeddelanden om exportfel

1. Ange **[!UICONTROL Failed Email Receiver]** till den butikskontakt som ska få ett meddelande om ett fel inträffar under exporten.

1. Ange **[!UICONTROL Failed Email Sender]** till butikskontakten som visas som meddelandets avsändare.

1. Ange **[!UICONTROL Failed Email Template]** till mallen som används för meddelandet.

1. För **[!UICONTROL Send Failed Email Copy To]** anger du e-postadressen till alla som ska få en kopia av meddelandet.

   Om du har flera e-postadresser avgränsas de med kommatecken.

1. Ange **[!UICONTROL Failed Email Copy Method]** till något av följande:

   - `Bcc` - Skickar en kopia med blindhet. Mottagarens namn och adress inkluderas i den ursprungliga e-postdistributionen, men är dolt.
   - `Separate Email` - Skickar kopian som ett separat e-postmeddelande.

### Steg 4: Välj entitetsattribut

1. I avsnittet _[!UICONTROL Entity Attributes]_&#x200B;väljer du de attribut du vill ta med i exportdata.

   - Om du vill filtrera exportdata efter attributvärde anger du attributvärdet i kolumnen _[!UICONTROL Filter]_.
   - Om du vill exkludera produkter eller kunder med vissa attributvärden anger du värdena för de attribut som du vill exkludera och markerar kryssrutan i kolumnen Hoppa över.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Det nya schemalagda exportjobbet läggs till i listan på sidan _[!UICONTROL Scheduled Import/Export]_. Från den här sidan kan den köras direkt, för testning och redigering.

>[!NOTE]
>
>När du skapar eller uppdaterar en schemalagd import/export ändras systemkonfigurationen. När du har sparat måste du åtgärda det cacheminnet som visas högst upp på Admin-sidan och tömma cacheminnet för att tillämpa det nya eller uppdaterade schemat.

### Fältbeskrivningar

#### [!UICONTROL Export Settings]

| Fält | Beskrivning |
| ----- | ----------- | 
| [!UICONTROL Name] | Namnet på exporten. Hjälper dig att skilja på det om många olika schemalagda exporter skapas. |
| [!UICONTROL Description] | (Valfritt) En beskrivning av den planerade exporten. |
| [!UICONTROL Entity Type] | Identifierar de data som ska exporteras. När markeringen är klar visas enhetsattributen nedan. Alternativ: `Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | Ange starttimmen, minuter och sekunder för exporten. |
| [!UICONTROL Frequency] | Definiera hur ofta exportjobbet ska köras. Alternativ: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Status] | En ny schemalagd export är aktiverad som standard. Du kan göra uppehåll genom att ange Status till Inaktiverad. Alternativ: `Enabled` / `Disabled` |
| [!UICONTROL File Format] | Välj exportfilens format. För närvarande är bara alternativet `.CSV` tillgängligt. |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| Fält | Beskrivning |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Anger exportfilens plats. Alternativ:<br>**Lokal server** - Placerar exportfilen på samma server som Commerce distribueras till. Om fjärrlagringsmodulen är aktiverad växlas `Local Server` till `Remote Storage`.<br>**Fjärr-FTP** - Placerar exportfilen på en fjärrserver. Ytterligare alternativ för autentiseringsuppgifter och filöverföringsinställningar visas. |
| [!UICONTROL File Directory] | Ange den katalog där exportfilen placeras. Om _[!UICONTROL Server Type]_&#x200B;är inställt på `Local Server` anger du sökvägen i förhållande till installationssökvägen för Commerce. Till exempel `var/export` eller `import_export/export` för fjärrlagring. |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| Fält | Beskrivning |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Ange den e-postadress till vilken ett e-postmeddelande (export misslyckades e-post) skickas om exporten misslyckas. |
| [!UICONTROL Failed Email Sender] | Ange den e-postadress som används som e-postavsändare som inte kan exporteras. |
| [!UICONTROL Failed Email Template] | Välj en mall för den misslyckade e-postexporten. Som standard är bara alternativet `Export Failed (Default Template from Locale)` tillgängligt. |
| [!UICONTROL Send Failed Email Copy To] | Den e-postadress till vilken en kopia av det misslyckade e-postmeddelandet skickas. |
| [!UICONTROL Send Failed Email Copy Method] | Ange sändningsmetod för kopiering för e-post som inte kunde exporteras. |

{style="table-layout:auto"}
