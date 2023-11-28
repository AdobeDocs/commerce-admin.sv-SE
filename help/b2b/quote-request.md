---
title: Anbudsförfrågan
description: Lär dig hur kunder som är kopplade till ett företagskonto kan skicka en anbudsförfrågan.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: 21361104fa06425df0b44d5c7ae204ef4d9e21ac
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Anbudsförfrågan

Om citattecken är aktiverade i [Konfiguration av försäljningsfunktioner](configure-quotes.md), kan en auktoriserad köpare från ett företag inleda prisförhandlingsprocessen genom att begära en offert från sin kundvagn. Om en köpare inte är redo att skicka en offert för förhandling kan han eller hon spara den som ett utkast.

>[!NOTE]
>
>En offertförfrågan får inte innehålla rabattkoder eller presentkort.

## Kundupplevelse av anbudsförfrågan

1. Kunden loggar in på sitt användarkonto som köpare med [behörighet](account-company-roles-permissions.md) för att begära en offert.

1. Lägger till de produkter de vill ska ingå i offerten i kundvagnen.

1. Markeringar **[!UICONTROL Request a Quote]**.

   ![Begär en offert från kundvagnen](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. I **[!UICONTROL Add your comment]** skriver en kort anteckning som beskriver begäran.

1. Skriver in a **[!UICONTROL Quote Name]**.

   ![Ange offertkommentarer och namn](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Bifogar vid behov ett stöddokument eller en bild till offerten:

   - Markeringar **[!UICONTROL Attach file]**.
   - Väljer filen i systemet.

   Som standard är [bifogad fil](configure-quotes.md) kan vara upp till 2 MB i något av följande filformat: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG eller JPEG, PNG.

1. Skapar och bearbetar offerten:

   - Skickar offerten till säljaren genom att välja **[!UICONTROL Request a Quote]**.
   - [!BADGE 1.5.0-betafunktion]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}**[!UICONTROL Save as Draft]**.

     Om köparen sparar offerten som ett utkast är offerten tillgänglig i [!UICONTROL My Quotes] in `Draft` tillstånd. Det är inte synligt för säljaren förrän köparen öppnar offerten och skickar in den.
