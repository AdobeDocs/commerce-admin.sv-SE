---
title: Lagra URL:er
description: Lär dig mer om butiks-URL:er och hur du konfigurerar bas-URL:en och lagringskoderna.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# Lagra URL:er

Varje webbplats i en Adobe Commerce- eller Magento Open Source-installation har en bas-URL som är tilldelad butiken och en annan URL som är tilldelad administratören. Adobe använder variabler för att definiera interna länkar i relation till bas-URL:en, vilket gör det möjligt att flytta en hel butik från en plats till en annan utan att uppdatera länkarna. Standardbas-URL:er börjar med `http` och säkra bas-URL:er börjar med `https`.

- **Bas-URL** — `http://www.yourdomain.com/magento/`
- **URL för säker bas** — `https://www.yourdomain.com/magento/`
- **URL med IP-adressen** — `http://###.###.###.###/magento/` eller `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>Ändra inte Admin-URL:en från standardbas-URL:ens konfiguration. Information om hur du ändrar Admin-URL:en eller -sökvägen finns i [Använd en anpassad Admin-URL](#use-a-custom-admin-url).

## Använd ett säkert protokoll

Bas-URL:erna för din butik konfigurerades ursprungligen under Adobe Commerce-installationen. Om ett säkerhetscertifikat var tillgängligt vid den tidpunkten kan du ange att `HTTPS` URL:er ska användas för arkivet, administratören eller båda. Om din Adobe Commerce-installation innehåller flera butiker eller du planerar att lägga till fler butiker senare, kan du inkludera butikskoden i URL:en. Alla Adobe-resurser och -åtgärder kan användas med säkra protokoll.

Om det inte fanns något säkerhetscertifikat tillgängligt för domänen vid tidpunkten för installationen måste du uppdatera konfigurationen innan du startar arkivet. När ett säkerhetscertifikat har skapats för din domän kan du konfigurera en eller båda bas-URL:erna så att de fungerar med SSL- (Secure Sockets Layer) och TLS-protokoll ([Transport Layer Security][1]).

>[!IMPORTANT]
>
>Adobe rekommenderar starkt att alla sidor på en produktionsplats, inklusive innehåll och produktsidor, skickas med ett säkert protokoll.

Adobe Commerce och Magento Open Source kan konfigureras för att leverera alla sidor över `HTTPS` som standard. Om din butik har installerats med standardprotokoll kan du förbättra säkerheten genom att aktivera [HTTP Strict Transport Security][2] (HSTS) och uppgradera alla osäkra sidförfrågningar. HSTS är ett anmälningsprotokoll som förhindrar att webbläsare återger `HTTP` standardsidor som överförs med osäkert protokoll för den angivna domänen. Eftersom sökmotorer redan har indexerat varje sida i din butik med `HTTP` standardadresser, kan du konfigurera Commerce så att osäkra sidförfrågningar uppgraderas automatiskt till `HTTPS` så att du inte förlorar någon trafik. När Commerce har konfigurerats att använda säkra URL:er för både storefront och Admin visas ytterligare två fält där du kan aktivera `HSTS`.

## Konfigurera bas-URL:en

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** under _Allmänt_ i den vänstra panelen.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Base URL]**.

   - **[!UICONTROL Base URL]** - Ange den fullständiga, kvalificerade bas-URL:en för din butik. Avsluta URL:en med ett snedstreck så att den kan utökas med ytterligare URL-nycklar från din butik. Till exempel: `http://yourdomain.com/`

     >[!NOTE]
     >
     >Ändra inte platshållaren i fältet _[!UICONTROL Base Link URL]_. Det är en platshållare som används för att skapa relativa länkar till bas-URL:en.

   - **[!UICONTROL Base URL for Static View Files]** — (Valfritt) Ange en alternativ plats för bas-URL:en för statiska vyfiler genom att ange sökvägen som börjar med följande platshållare:

     \{unsecure_base_url}&rbrace;

   - **[!UICONTROL Base URL for User Media Files]** — (Valfritt) Ange en alternativ plats för bas-URL:en för användarmediefiler genom att ange sökvägen som börjar med följande platshållare:

     \{unsecure_base_url}&rbrace;

     För en vanlig installation finns det ingen anledning att uppdatera sökvägarna för statiska vyfiler eller mediefiler eftersom de är relativa till bas-URL:en.

   ![Allmän konfiguration - webbbas-URL:er](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Platshållare inom dubbla klammerparenteser är taggar för variabler.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Konfigurera den säkra bas-URL:en

Om din domän har ett giltigt säkerhetscertifikat kan du konfigurera URL:er för både storefront och Admin för att överföra data över en säker (https) kanal. Utan ett giltigt säkerhetscertifikat kan ditt arkiv inte fungera med SSL/TLS-protokoll.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet _[!UICONTROL Base URLs (Secure])_ och gör följande:

   ![Allmän konfiguration - säkra bas-URL:er](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** - Ange den fullständiga URL:en för säker bas, följt av ett snedstreck. Till exempel: `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** - Ändra inte platshållaren i URL-fältet för säker baslänk. Den används för att skapa relativa länkar till den säkra bas-URL:en.

   - **[!UICONTROL Secure Base URL for Static View Files]** — (Valfritt) Ange en alternativ plats för den säkra bas-URL:en för statiska vyfiler genom att ange sökvägen som börjar med följande platshållare:

     \{secure_base_url}&rbrace;

   - **[!UICONTROL Secure Base URL for User Media Files]** — (Valfritt) Ange en alternativ plats för den säkra bas-URL:en för användarmediefiler genom att ange sökvägen som börjar med följande platshållare:

     \{secure_base_url}&rbrace;

1. Om du vill förbättra säkerheten anger du `Yes` som båda av följande alternativ.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. Gör följande för _[!UICONTROL Enhanced Security Settings]_:

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** - Om du vill att din butik bara ska visa förfrågningar från säkra HTTPS-sidor anger du `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]** - Ange `Yes` om du vill uppgradera alla begäranden om oskyddade standardHTTP-sidor för att skydda HTTPS.

1. Ange **[!UICONTROL Offloader Header]** för servern.

   De flesta Commerce-installationer använder standardvärdet `X-Forward-Proto` för att identifiera protokollet som antingen `HTTP` eller `HTTPS`. Om serverkonfigurationen använder en annan offloader_header anger du den här.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Inkludera butikskoden i URL:er

>[!NOTE]
>
>När alternativet _Lägg till butikskod i URL:er_ är inställt på `Yes` måste du inkludera butikskoder i URL:erna för webbläsaren. Den här inställningen säkerställer att URL-omskrivningar mappas korrekt och att alla sidor öppnas utan _&quot;404 Page Not found&quot;_ -fel.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** under _[!UICONTROL General]_&#x200B;i den vänstra panelen.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL URL Options]**.

1. Ange **[!UICONTROL Add Store Code]** som din inställning:

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![Allmän konfiguration - alternativ för webb-URL](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. Klicka på länken **[!UICONTROL Cache Management]** i meddelandet längst upp på arbetsytan. Följ sedan instruktionerna för att uppdatera cachen.

   ![Cachehanteringsmeddelande](./assets/msg-cache-management.png)

## URL-felsökning

Om vissa sidor fortfarande hanteras med den osäkra URL:en (`http://`) efter att du har följt konfigurationsinstruktionerna gör du följande:

- Ändra bas-URL:en (osäker) till den säkra HTTPS-URL:en.
- Redigera filen `.htaccess` (eller belastningsutjämnaren) på servern så att den osäkra URL:en omdirigeras till den säkra URL:en.

## Använd en anpassad Admin URL

Adobe rekommenderar att du använder en unik administratörs-URL i stället för _admin_ som standard eller en vanlig term som _backend_ som [bästa säkerhetspraxis](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html). Även om webbplatsen inte skyddas direkt från en bestämd skadad skådespelare kan den minska exponeringen för skript som försöker få obehörig åtkomst.

>[!NOTE]
>
>Kontrollera med din värdleverantör innan du implementerar en anpassad Admin URL. Vissa värdtjänstleverantörer kräver en standard-URL för att uppfylla brandväggsskyddsreglerna.

I en vanlig installation följer Admin-URL:en och sökvägen omedelbart bas-URL:en. Admin-sökvägen är en katalog under roten.

- **Standardbas-URL**: `http://yourdomain.com/magento/`
- **Standardadministratörssökväg**: `admin`
- **Admin-URL och standardsökväg**: `http://yourdomain.com/magento/admin`

Även om det går att ändra Admin-URL:en och sökvägen till en annan plats, tar alla fel bort åtkomsten till Admin och måste korrigeras från servern.

>[!NOTE]
>
>Som en försiktighetsåtgärd bör du inte ändra Admin URL själv om du inte vet hur du redigerar konfigurationsfiler på servern. För Adobe Commerce-projekt som distribueras i molninfrastruktur ändrar du Admin-URL genom att följa [instruktionerna](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=en#admin-url) i *Adobe Commerce on Cloud Infrastructure Guide*.

### Metod 1: Ändra från administratör

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Admin Base URL]**.

1. Ange konfigurationsalternativ för den anpassade URL:en:

   ![Avancerad konfiguration - Admin base URL](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra inställningen.

   - Ange **[!UICONTROL Use Custom Admin URL]** till `Yes`.

   - Ange **[!UICONTROL Custom Admin URL]**: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >Admin-URL:en måste finnas i samma Commerce-installation och ha samma dokumentrot som butiken.

   - Ange **[!UICONTROL Custom Admin Path]** till `Yes`.

   - För **[!UICONTROL Custom Admin Path]** anger du sökvägen som ska användas som namn på den anpassade administratörsmappen.

     Exempel: `sample_custom_admin`

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. När ändringarna har sparats loggar du ut från Admin och loggar in igen med den nya Admin-URL:en och sökvägen.

### Metod 2: Ändra administratörssökvägen från serverkommandoraden

1. Öppna filen `app/etc/env.php` i en textredigerare och ändra värdet på parametern `frontName` i avsnittet `backend`. Spara sedan filen.

   Använd endast gemener.

   >[!NOTE]
   >
   >   Med den här metoden kan du ändra Admin Path, men inte Admin URL.

   >[!TIP]
   >
   >För Adobe Commerce i molninfrastruktur kan du skapa en anpassad administratörssökväg med variabeln `ADMIN_URL` i molngränssnittet. Se avsnittet [Administratörsvariabler](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) i _Commerce on Cloud Infrastructure Guide_.

   - **Standardadministratörssökväg**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **Ny administratörssökväg**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. Använd någon av följande metoder för att rensa cacheminnet:

   - Gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;på sidofältet_ Admin _. Klicka sedan på&#x200B;**[!UICONTROL Flush Magento Cache]**.
   - Kör följande på servern:

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >De ändringar som görs med metod 1 har prioritet framför de ändringar som görs i filen `app/etc/env.php`.

### Metod 3: Ändra administratörssökvägen med Commerce CLI

Du kan använda kommandot CLI `setup:config:set` för att ändra administratörssökvägen. I följande exempel används alternativet `--backend-frontname` för att ändra sökvägen från Commerce-roten till en ny administratörssökväg:

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

Det här kommandot uppdaterar konfigurationsalternativet `backend` > `frontName` i filen `app/etc/env.php`.

## Återställ standardadministratörs-URL och administratörssökväg

Om du har angett en ogiltig Admin URL eller en Admin Path och inte längre kommer åt backend-objektet finns det ett sätt att åtgärda det från kommandoraden.

1. Om du vill återgå till den förvalda admin-URL:en kör du det här kommandot:

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. Om du vill återgå till den förvalda administratörssökvägen (anges i `app/etc/env.php` enligt beskrivningen i metod 2) kör du det här kommandot:

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. Använd någon av följande metoder för att rensa cacheminnet:

   - Gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;på sidofältet_ Admin _. Klicka sedan på&#x200B;**[!UICONTROL Flush Magento Cache]**.
   - Kör följande på servern:

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
