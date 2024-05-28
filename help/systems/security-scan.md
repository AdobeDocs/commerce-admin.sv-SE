---
title: Säkerhetssökning
description: Lär dig hur du kör en förbättrad säkerhetsgenomsökning och övervakar alla dina Adobe Commerce- och Magento Open Source-sajter.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Säkerhetssökning

Med den förbättrade säkerhetssökningen kan du övervaka var och en av dina Adobe Commerce- och Magento Open Source-sajter, inklusive PWA, för att upptäcka kända säkerhetsrisker och skadlig kod, samt få korrigeringsuppdateringar och säkerhetsmeddelanden.

- Få insikt i butikens säkerhetsstatus i realtid.
- Få förslag baserat på bästa praxis för att lösa problem.
- Schemalägg en säkerhetsgenomsökning som ska köras varje vecka, varje dag eller på begäran.
- Kör över 21 000 säkerhetstester för att identifiera potentiell skadlig kod.
- Få tillgång till historiska säkerhetsrapporter som spårar och övervakar webbplatsernas förlopp.
- Få åtkomst till den inskannade rapporten som visar lyckade och misslyckade kontroller, med rekommenderade åtgärder.

Verktyget för säkerhetsgenomsökning är tillgängligt utan kostnad från instrumentpanelen i [Commerce/Magento](../getting-started/commerce-account-create.md). Teknisk information finns på [Konfigurera verktyget för säkerhetsgenomsökning](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) i _Infrastrukturhandbok för Commerce on Cloud_.

![Verktyget för säkerhetsgenomsökning](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Kör en säkerhetssökning

1. Logga in på din Commerce hemsida [Commerce/Magento](../getting-started/commerce-account-create.md).

1. Granska och godkänn villkoren för användning av verktyget för säkerhetsgenomsökning.

   - Välj **[!UICONTROL Security Scan]**.
   - Klicka på **[!UICONTROL Go to Security Scan]**.
   - Läs **[!UICONTROL Terms and Conditions]**.
   - Klicka **[!UICONTROL Agree]** för att fortsätta.

1. På _[!UICONTROL Monitored Websites]_sida, klicka **[!UICONTROL +Add Site]**.

   Om du har flera platser med olika domäner, konfigurerar du en separat sökning för varje domän.

   ![Övervakade platser](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Gör något av följande om du vill verifiera ditt ägarskap av webbplatsdomänen genom att lägga till en bekräftelsekod:

   **Commerce storefront**:

   - Ange **[!UICONTROL Site URL]** och **[!UICONTROL Site Name]**.
   - Klicka på **[!UICONTROL Generate Confirmation Code]**.
   - Klicka **Kopiera** om du vill kopiera bekräftelsekoden till Urklipp.

     ![Generera bekräftelsekod](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Logga in på administratören för din butik som användare med fullständig administratörsbehörighet och gör följande:

      - I _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Hitta platsen i listan och klicka på **[!UICONTROL Edit]**.
      - Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL HTML Head]** -avsnitt.
      - Bläddra nedåt till **[!UICONTROL Scripts and Style Sheets]** och klicka i textrutan i slutet av en befintlig kod och klistra in bekräftelsekoden i textrutan.

        ![Skript och formatmallar](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - När du är klar klickar du på **[!UICONTROL Save Configuration]**.

   **PWA storefront**:

   - Ange **[!UICONTROL Site URL]** och **[!UICONTROL Site Name]**.

   - För **[!UICONTROL Confirmation Code]** väljer du `META Tag` och klicka sedan på **[!UICONTROL Generate Code]**.

   - Klicka **[!UICONTROL Copy]** om du vill kopiera den genererade bekräftelsekod-META-taggen till Urklipp.

     ![Generera bekräftelsekod](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Gå till projektkatalogen för PWA Studio storefront och gör följande:

      - Gå till projektkatalogen PWA Studio `packages > venia-concept > template.html`.
      - Lägg till den kopierade bekräftelsekoden (den genererade META-taggen) i huvudet på HTML och spara ändringarna.

        ![Bekräftelsekod för kopia](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Gå tillbaka till CLI för PWA Studio och använd garn för att installera projektberoenden och köra projektbyggkommandot.

        ```sh
        yarn install &&
        yarn build
        ```

      - *I ditt Cloud-projekt*, skapa `pwa` och kopiera innehållet i ditt storefront-projekts `dist` mapp.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Använd Git CLI-verktyget för att mellanlagra, genomföra och överföra dessa ändringar till ditt Cloud-projekt.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        När byggprocessen är klar kommer ändringarna att distribueras till din PWA-butik.

1. Återgå till _[!UICONTROL Security Scan]_i ditt Commerce-konto och klicka **[!UICONTROL Verify Confirmation Code]**för att etablera ägarskap till domänen.

1. När bekräftelsen är klar konfigurerar du **[!UICONTROL Set Automatic Security Scan]** alternativ för någon av följande typer:

   **Skanna varje vecka (rekommenderas)**:

   - Välj **[!UICONTROL Week Day]**, **[!UICONTROL Time]** och **[!UICONTROL Time Zone]** att sökningen ska göras varje vecka.
   - Som standard är genomsökningen schemalagd att börja varje vecka vid midnatt lördag, UTC och fortsätta till början av söndagen.

     ![Skanna varje vecka](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Sök dagligen**:

   - Välj **[!UICONTROL Time]** och **[!UICONTROL Time Zone]** att sökningen ska göras varje dag.
   - Som standard är genomsökningen schemalagd att börja varje dag vid midnatt, UTC.

     ![Sök dagligen](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Ange **[!UICONTROL Email Address]** där du vill få meddelanden om slutförda sökningar och säkerhetsuppdateringar.

   ![E-postadress](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Submit]**.

   När ägarskapet för domänen har verifierats visas webbplatsen i listan Övervakade webbplatser i ditt Commerce-konto.

1. Om du har flera webbplatser med olika domäner upprepar du den här processen för att konfigurera en säkerhetsgenomsökning för varje.
