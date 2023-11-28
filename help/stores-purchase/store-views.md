---
title: Butiksvyer
description: Lär dig hur du lägger till och redigerar en butiksvy.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 2%

---

# Butiksvyer

Butiksvyer används vanligtvis för att göra butiken tillgänglig på olika språk. Köpare kan använda språkväljaren i butikens sidhuvud för att ändra butiksvyn.

![Omfång - flera butiksvyer](./assets/scope-multiview.svg){width="550"}

## Lägga till en butiksvy

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Alla butiker](./assets/stores-all.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Create Store View]**.

   ![Skapa butiksvy](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Store]** till det överordnade arkivet för den här vyn.

1. Ange en **[!UICONTROL Name]** för butiksvyn.

   Namnet visas i språkväljaren i butikshuvudet. Exempel: `Spanish`.

1. För **[!UICONTROL Code]** anger du koden som identifierar vyn (med gemener).

   Exempel: `spanish`.

1. Aktivera vyn genom att ange **[!UICONTROL Status]** till `Enabled`.

1. (Valfritt) Ange en **[!UICONTROL Sort Order]** för att avgöra i vilken ordning den här vyn visas tillsammans med andra vyer.

1. Klicka på **[!UICONTROL Save Store View]**.

## Redigera en butiksvy

Eftersom visningsnamnet visas i språkväljaren kanske du vill ändra namnet på standardvyn till något mer beskrivande. The _Namn_ fältet är bara en etikett och kan enkelt ändras.

Om din Adobe Commerce- eller Magento Open Source-installation har en konfiguration för flera platser eller flera butiker ska du inte ändra fältet Butikskod utan att verifiera att värdet inte refereras i `index.php` -fil. Om du inte har åtkomst till servern för att undersöka filen ber du en utvecklare om hjälp.

| Fält | Ursprungligt värde | Uppdaterat värde |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. I _[!UICONTROL Store View]_i rutnätets kolumn klickar du på namnet på den vy som du vill redigera.

   När du redigerar standardvyn visas _[!UICONTROL Store]_och_[!UICONTROL Status]_ fält är inte tillgängliga.

   ![Butiksvy - redigera standardvy](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Uppdatera följande fält efter behov:

   - **[!UICONTROL Store]** (endast icke-standardvyer)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (endast om de inte används i `index.php`)
   - **[!UICONTROL Status]** (endast icke-standardvyer)
   - **[!UICONTROL Sort Order]**

1. Klicka på **[!UICONTROL Save Store View]**.
