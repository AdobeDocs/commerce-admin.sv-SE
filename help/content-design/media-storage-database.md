---
title: Använda en mediedatabas
description: Lär dig hur du använder en mediedatabas för att lagra [!DNL Commerce] mediefiler.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Använda en mediedatabas

>[!IMPORTANT]
>
>Databasmedielagringsmetoden används inte i Adobe Commerce och Magento Open Source 2.4.3.

Som standard är alla bilder, kompilerade CSS-filer och kompilerade JavaScript-filer i [!DNL Commerce] -instansen lagras i filsystemet på webbservern. Du kan välja att lagra dessa filer i en databas på en databasserver. En fördel med detta är möjligheten till automatisk synkronisering och omvänd synkronisering mellan webbserverns filsystem och databasen. Du kan använda standarddatabasen för att lagra media eller skapa en. Om du vill kunna använda en nyligen skapad databas som medielagring måste du lägga till information om den och dess autentiseringsuppgifter i `env.php` -fil.

## Databasarbetsflöde

1. **Webbläsaren begär media** - En sida från butiken öppnas i kundens webbläsare och webbläsaren begär media som är angivet i HTML.

1. **Systemsökning efter media i filsystem** - Systemet söker efter mediet i filsystemet och skickar det till webbläsaren om det hittas.

1. **Systemet hittar media i databasen** - Om mediet inte hittas i filsystemet skickas en begäran om mediet till databasen som anges i konfigurationen.

1. **Systemet hittar media i databasen** - Ett PHP-skript överför filerna från databasen till filsystemet och skickar dem till kundens webbläsare. Webbläsarbegäran om media utlöser skriptet så här:

   - Om webbserver [omskrivning](../merchandising-promotions/url-rewrite.md) är aktiverade för [!DNL Commerce] och stöds av servern. PHP-skriptet körs bara när det begärda mediet inte hittas i filsystemet.
   - Om omskrivning av webbserver är inaktiverat för [!DNL Commerce], eller om det inte stöds av servern, körs PHP-skriptet ändå, även om det nödvändiga mediet är tillgängligt i filsystemet.

## Använd en databas för medielagring

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till `Default Config` för att tillämpa konfigurationen på global nivå.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Storage Configuration for Media]** och gör följande:

   ![Avancerad konfiguration - lagringskonfiguration för media](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Media Storage]** till `Database`.

   - Ange **[!UICONTROL Select Media Database]** till den databas som du vill använda.

   - Om du vill överföra befintliga medier till den nya databasen klickar du på **[!UICONTROL Synchronize]**.

   - Ange **[!UICONTROL Environment Update Time]** på några sekunder.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
