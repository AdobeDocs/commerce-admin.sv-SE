---
title: Skattezoner och skattesatser
description: Lär dig hur du definierar skattesatser för varje geografiskt område där du tar ut och överför skatter.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Skattezoner och skattesatser

Skattesatserna gäller i allmänhet för transaktioner som äger rum inom ett visst geografiskt område. Använd verktyget _Skattezoner och tariffnivåer_ för att ange momssatsen för varje geografiskt område som du samlar in och skickar in skatter från. Eftersom varje skattezon och skattesats har en unik identifierare kan du ha flera skattesatser för ett visst geografiskt område (t.ex. platser som inte beskattar livsmedel eller medicin, men som beskattar andra artiklar).

Moms beräknas utifrån butikens adress. Den faktiska kundskatten för en order beräknas när kunden har slutfört orderinformationen. Commerce beräknar sedan momsen enligt butikens momskonfiguration.

![Skattezoner och skattesatser](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## Definiera en ny momssats

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Tax Rate]** i det övre högra hörnet.

   ![Ny momssats](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Tax Identifier]**.

1. Om du vill tillämpa skattesatsen på ett enskilt postnummer eller postnummer anger du koden för **[!UICONTROL Zip/Post Code]**.

   Asteriskens jokertecken (`*`) kan användas för att matcha upp till tio tecken i koden. `90*` representerar till exempel alla ZIP-koder från 90000 till 9099.

1. Så här tillämpar du skattesatsen på ett intervall med postnummer:

   - Markera kryssrutan **[!UICONTROL Zip/Post is Range]** och definiera intervallet genom att ange det första och sista postnumret för **[!UICONTROL Range From]** och **[!UICONTROL Range To]**.

     ![ZIP/Post är intervall](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - Välj **[!UICONTROL State]** där momssatsen gäller.

   - Välj **[!UICONTROL Country]** där momssatsen gäller.

   - Ange **[!UICONTROL Rate Percent]** som används för momsberäkning.

1. Om du har flera butiker kan du ange **[!UICONTROL Tax Titles]** för varje butiksvy.

   >[!NOTE]
   >
   >Lämna fältet tomt om du vill använda skatteidentifieraren.

1. Klicka på **[!UICONTROL Save Rate]** när du är klar.

## Redigera en befintlig momssats

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**på sidofältet_ Admin _.

1. Hitta momssatsen i rutnätet _[!UICONTROL Tax Zones and Rates]_och öppna posten i redigeringsläge.

   Om det finns många frekvenser i listan använder du [filterkontrollerna](../getting-started/admin-grid-controls.md) för att hitta den frekvens du behöver.

1. Gör nödvändiga ändringar i **[!UICONTROL Tax Rate Information]**.

1. Uppdatera **[!UICONTROL Tax Titles]** efter behov.

1. Klicka på **[!UICONTROL Save Rate]** när du är klar.

## Ta bort momssats

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**på sidofältet_ Admin _.

1. Hitta den momssats som ska tas bort och öppna den i redigeringsläge.

1. Klicka på **[!UICONTROL Delete Rate]** på menyraden.

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.
