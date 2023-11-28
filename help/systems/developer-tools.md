---
title: Utvecklarverktyg
description: Läs mer om de avancerade utvecklingsverktygen som är tillgängliga för utvecklare som arbetar med anpassningsprojekt.
exl-id: 34529aa9-201f-4817-b53b-a15b6a78a923
role: Admin, Developer
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# Utvecklarverktyg

Använd de avancerade utvecklingsverktygen för att fastställa kompileringsläget under frontend-utvecklingen, skapa ett tillåtelselista med IP-adresser och visa sökvägstips för mallar. Det finns även verktyg för att enkelt göra dekorändringar i texten i butikens och administratörens gränssnitt.

- [Åtgärdsloggar](action-log.md) ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)
- [Frontend Development Workflow](#frontend-development-workflow)
- [Använda statiska filsignaturer](#static-file-signatures)
- [Optimering av resursfiler](#optimizing-resource-files)
- [Begränsningar för utvecklarklienter](#client-restrictions)
- [Tips för mallsökväg](#template-path-hints)
- [Översätt textbundet](#translate-inline)

## Åtgärdslägen

Din Adobe Commerce- eller Magento Open Source-instans kan distribueras för att köras i _produktion_ eller _utvecklarläge_. De verktyg och konfigurationsinställningar som är särskilt utformade för utvecklare är bara tillgängliga när butiken körs i _utvecklarläge_.

Åtgärdsläget kan bara ändras från serverns kommandorad av en användare med lämplig behörighet. Se [Ange åtgärdsläge](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/set-mode.html) i _Konfigurationshandbok_ för mer information.

De flesta avsnitten i dokumentationen gäller en Commerce-instans som körs i produktionsläge. Följande konfigurationsinställningar och verktyg kan dock bara användas när installationen körs i utvecklarläge.

## Utvecklingsarbetsflöde

Frontend Development Workflow-typen avgör om mindre kompilering sker på klient- eller serversidan under utvecklingen. Less är ett tillägg till CSS som har ytterligare funktioner och konventioner och som skapar strömlinjeformad kod. Mindre kompilering på klientsidan rekommenderas för temautveckling. Kompilering på serversidan är standardläge. Alternativen för utvecklingsarbetsflöde är inte tillgängliga för butiker i produktionsläge.
Se [LESS-kompilering på klientsidan jämfört med serversidan](https://developer.adobe.com/commerce/frontend-core/guide/css/quickstart/compilation-mode/){:target=&quot;_blank&quot;} i dokumentationen för Commerce-utvecklare.

>[!NOTE]
>
>Konfiguration av frontend-utvecklingsarbetsflödet finns i [Utvecklarläge](../systems/developer-tools.md#operation-modes) endast.

![Avancerad konfiguration - frontend-arbetsflöde](../configuration-reference/advanced/assets/developer-frontend-development-workflow.png){width="600" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Front-end Development Workflow]** -avsnitt.

1. Ange **[!UICONTROL Workflow Type]** till något av följande:

   - `Client side less compilation` - Kompileringen görs i webbläsaren med det inbyggda `less.js` bibliotek.
   - `Server side less compilation` - Kompilering görs på servern med hjälp av Less PHP-biblioteket. Det här är standardläget för produktion.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Statiska filsignaturer

Genom att lägga till en digital signatur i URL:en för statiska filer kan webbläsarna identifiera när en nyare version av filen är tillgänglig. Statiska filer som kan spåras med digitala signaturer inkluderar JavaScript, CSS, bilder och teckensnitt. Signaturen läggs till i sökvägen direkt efter bas-URL:en. Om en fils signatur skiljer sig från vad som lagras i webbläsarens cache, används den nyare versionen av filen.

Se [Statisk innehållssignering](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/static-content-signing.html){:target=&quot;_blank&quot;} i dokumentationen för Commerce-utvecklare.

>[!NOTE]
>
>Konfigurationen för statiska filinställningar är endast tillgänglig när du arbetar i [utvecklarläge](../systems/developer-tools.md#operation-modes).

![Avancerad konfiguration - inställningar för statiska filer](../configuration-reference/advanced/assets/developer-static-files-settings.png){width="600" zoomable="yes"}

En detaljerad lista över konfigurationsinställningarna finns i [_Statiska filinställningar_](../configuration-reference/advanced/developer.md) i _Konfigurationsreferens_.

**_Så här aktiverar du signerade statiska filer:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Static Files Settings]** -avsnitt.

1. Ange **[!UICONTROL Sign Static Files]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Optimering av resursfiler

Den tid det tar att läsa in resursfiler kan minskas genom att filer sammanfogas och paketeras, och genom att minimera koden.

- När du sammanfogar filer kombineras separata filer av samma typ till en enda fil.
- Paketering är en teknik som grupperar separata filer för att minska antalet HTTP-begäranden som krävs för att läsa in en sida.
- Med miniatyr tas blanksteg, radbrytningar och kommentarer bort, men kodens funktion påverkas inte. Eftersom minimerade filer inte kan redigeras bör processen endast användas när du är redo att börja producera.

Som standard sammanfogar, paketerar eller minimerar inte Adobe Commerce och Magento Open Source filer, och projektutvecklaren bör avgöra vilka filoptimeringsmetoder som ska användas.

Se [Bästa praxis](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/overview.html) för mer information.

>[!NOTE]
>
>CSS- och JavaScript-filer kan optimeras i [Utvecklarläge](../systems/developer-tools.md#operation-modes) endast.

| Filtyp | Åtgärder som stöds |
| --------------- | -------------------- |
| CSS-filer | `MergeMinify` |
| JavaScript-filer | `MergeBundleMinify` |
| Mallfiler | `Minify` |

{style="table-layout:auto"}

**_Så här optimerar du resursfiler:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera för att optimera CSS-filer ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL CSS Settings]** och gör följande:

   - Ange **[!UICONTROL Merge CSS Files]** till `Yes`.
   - Ange **[!UICONTROL Minify CSS Files]** till `Yes`.

   ![Avancerad konfiguration - CSS-inställningar](../configuration-reference/advanced/assets/developer-css-settings.png){width="600" zoomable="yes"}

[_CSS-inställningar_](../configuration-reference/advanced/developer.md)

1. Optimera JavaScript-filer genom att expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL JavaScript Settings]** och gör följande:

   - Ange **[!UICONTROL Merge JavaScript Files]** till `Yes`.
   - Ange **[!UICONTROL Minify JavaScript Files]** till `Yes`.

   ![Avancerad konfiguration - JavaScript-inställningar](../configuration-reference/advanced/assets/developer-javascript-settings.png){width="600" zoomable="yes"}

1. Expandera om du vill minimera PHTML-mallfiler ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Template Settings]** avsnitt och ange **[!UICONTROL Minify Html]** till `Yes`.

   ![Avancerad konfiguration - mallinställningar](../configuration-reference/advanced/assets/developer-template-settings.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Klientbegränsningar

Innan du använder ett verktyg som [sökvägstips för mallar](#template-path-hints)ska du lägga till din IP-adress i Developer Client Restrictions (Begränsningar för utvecklarklient) i tillåtelselista för att undvika att kundernas shoppingupplevelse i butiken störs. Om du inte känner till din IP-adress kan du söka efter den online.

>[!NOTE]
>
>Begränsningar för utvecklarklienten kan anges i [Utvecklarläge](../systems/developer-tools.md#operation-modes) endast.

Teknisk information finns på [Anpassad VCL för att tillåta begäranden](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-allowlist.html) i _Handbok för Commerce on Cloud Infrastructure_.

**_Så här lägger du till din IP-adress i tillåtelselista:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Developer Client Restrictions]** -avsnitt.

   ![Avancerad konfiguration - begränsningar för utvecklarklient](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Allow IPs]** anger du din IP-adress.

   Om åtkomst krävs från flera IP-adresser avgränsar du dem med kommatecken.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. Uppdatera ogiltiga cacheminnen när du uppmanas till detta.

## Tips för mallsökväg

Tips för mallsökvägar är ett diagnostiskt verktyg som lägger till anteckningar med sökvägen till varje mall som används på sidan. Tips för mallsökvägar kan aktiveras för antingen butiken eller administratören.

>[!NOTE]
>
>Tips för mallsökväg kan redigeras i [utvecklarläge](../systems/developer-tools.md#operation-modes) endast.

Se [Hitta mallar, layouter och format](https://developer.adobe.com/commerce/frontend-core/guide/themes/debug/){:target=&quot;_blank&quot;} i dokumentationen för Commerce-utvecklare.

![Exempel på storefront - tips för mallsökvägar](./assets/storefront-template-path-hints.png){width="700" zoomable="yes"}

### Steg 1: Lägg till din IP-adress i tillåtelselista

Lägg till din IP-adress till [tillåtelselista](#client-restrictions) för att undvika störningar hos kunder som handlar i butiken. När du är klar bör du rensa Commerce-cachen för att ta bort alla tips från butiken.

![Avancerad konfiguration - begränsningar för utvecklarklient](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

### Steg 2: Aktivera tips för mallsökväg

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Debug]** och gör följande:

   ![Avancerad konfiguration - felsökning](../configuration-reference/advanced/assets/developer-debug.png){width="600" zoomable="yes"}

   - Om du vill aktivera sökvägstips för arkivet anger du **[!UICONTROL Enabled Template Path Hints for Storefront]** till `Yes`.

   - Om du bara vill aktivera sökvägstips för butiken när URL:en innehåller `templatehints` parameter, ange **Aktivera tips för Storefront med URL-parameter** till `Yes`. Ange sedan ett värde för parametern om det behövs. Standardvärdet är `magento`, men du kan använda ett anpassat värde. Om du till exempel ändrar värdet till `lorem`använder du `mymagento.com?templatehints=lorem` för att visa malltips.

   - Om du vill aktivera tips för mallsökväg för administratören anger du **[!UICONTROL Enabled Template Path Hints for Admin]** till `Yes`.

   - Om du vill inkludera namnen på blocken anger du **[!UICONTROL Add Block Class Type to Hints]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Steg 3: Rensa cachen

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Flush Magento Cache]**.

## Översätt textbundet

Du kan använda verktyget Översätt textbundet i [utvecklarläge](../systems/developer-tools.md#operation-modes) för att redigera text i gränssnittet så att den återspeglar din röst och ditt varumärke. När läget Översätt infogad är aktiverat visas all text på sidan som kan redigeras med röda konturer. Det är enkelt att redigera fältetiketter, meddelanden och annan text som visas i butiken och i Admin. Många teman använder till exempel terminologi som _Mitt konto_, _Min önskelista_ och _Min instrumentpanel_ för att hjälpa kunderna att hitta rätt. Du kanske vill använda orden _Konto_, _Önsklista_ och _Kontrollpanel_.

>[!NOTE]
>
>Verktyget Översätt textbunden är endast tillgängligt när du arbetar i [utvecklarläge](../systems/developer-tools.md#operation-modes).

Se [Översättningar - översikt](https://developer.adobe.com/commerce/frontend-core/guide/translations/) i dokumentationen för Commerce-utvecklare.

![Exempel på storefront - översättningsbar text](./assets/storefront-translate-inline.png){width="700" zoomable="yes"}

Om din butik finns på flera språk kan du göra finjusteringar i den översatta texten för den språkinställningen. På servern finns gränssnittstext i en separat CSV-fil för varje utdatablock och ordnas efter språkområde. Som ett alternativt tillvägagångssätt, i stället för att använda _Översätt textbundet_ kan du även redigera CSV-filerna direkt på servern. Översättningsfiler lagras i `app/code/Magento/<module_name>/i18n/<language_locale>.csv`.

>[!NOTE]
>
>Om du vill använda verktyget Översätt textbundet måste webbläsaren tillåta popup-fönster.

### Steg 1: Inaktivera utdatacache

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Markera följande kryssrutor:

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Ange **[!UICONTROL Actions]** styra till `Disable` och klicka **[!UICONTROL Submit]**.

### Steg 2: Aktivera verktyget Översätt textbundet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Om du vill arbeta med en viss butiksvy anger du **[!UICONTROL Store View]** som ska uppdateras.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Translate Inline]** -avsnitt.

   Rensa **[!UICONTROL Use Website]** vid behov för att ändra dessa inställningar.

   The _[!UICONTROL Enabled for Admin]_är inte tillgängligt när du redigerar en viss butiksvy.

   ![Avancerad konfiguration - översätt intern](../configuration-reference/advanced/assets/developer-translate-inline.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enabled for Storefront]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. Uppdatera ogiltiga cacheminnen när du uppmanas att göra det, men låt de inaktiverade cacherna vara som de är för tillfället.

### Steg 3: Uppdatera texten

1. Öppna butiken i en webbläsare och gå till sidan som du vill redigera.

   Använd vid behov språkväljaren för att ändra butiksvyn. Varje textsträng som kan översättas visas med röda konturer. När du hovrar över en textruta visas en bokikon ( ![Bokikon](../assets/icon-book.png) ) visas.

1. Klicka på bokikonen för att öppna _Översätt_ och gör följande:

   - Om ändringen avser den specifika butiksvyn väljer du **[!UICONTROL Store View Specific]** kryssrutan.

   - Ange det nya **[!UICONTROL Custom]** text.

1. När du är klar klickar du på **[!UICONTROL Submit]**.

   ![Ange egen text](./assets/storefront-translate-inline-detail.png){width="700" zoomable="yes"}

1. Uppdatera webbläsaren om du vill se ändringarna i butiken.

1. Upprepa den här processen för alla element i butiken som ska ändras.

### Steg 4: Återställ de ursprungliga inställningarna

1. Återvänd till administratören för din butik.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Ange **[!UICONTROL Store View]** till den specifika vy som redigerades.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Translate Inline]** -avsnitt.

1. Ange **[!UICONTROL Enabled for Frontend]** till `No`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Markera kryssrutan för följande utdatacache som tidigare var inaktiverade:

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Ange **[!UICONTROL Actions]** styra till `Enable` och klicka **[!UICONTROL Submit]**.

1. Uppdatera ogiltiga cacheminnen när du uppmanas till detta.

### Steg 5: Verifiera ändringarna i din butik

Gå till butiken och granska varje sida som har uppdaterats för att se till att ändringarna är korrekta. I detta exempel `Customer Login` ändrades till `Customer Sign In`. Om du har ändrat en viss vy använder du Språkväljaren för att växla till rätt vy.

![Exempel på butik - översatt kundinloggning](./assets/storefront-translate-inline-customer-sign-in.png){width="700" zoomable="yes"}
