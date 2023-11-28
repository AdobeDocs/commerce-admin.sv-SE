---
title: Meddelande om misslyckade betalningar
description: Lär dig hur du konfigurerar e-postkommunikation för en betalningsmetod som inte kan slutföra en transaktion.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Meddelande om misslyckade betalningar

Ett meddelande skickas till butikskontakten eller en utsedd administratörsanvändare om betalningsmetoden som valts under utcheckningen inte kan slutföra transaktionen.

## Steg 1: Uppdatera e-postmallen

Se till att du har uppdaterat den e-postmall som behövs för att återspegla ert varumärke. En fullständig lista över mallar finns på [E-postmallslista](../systems/email-templates.md#email-template-list).

## Steg 2: Konfigurera e-postmeddelanden om misslyckade betalningar

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Payment Failed Emails]** -avsnitt.

   ![E-postmeddelanden om misslyckade betalningar](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Ange alternativ för att betala misslyckade e-postmeddelanden:

   - Ange **[!UICONTROL Payment Failed Email Sender]** till den butikskontakt som visas som avsändare av meddelandet.
   - Ange **[!UICONTROL Payment Failed Email Receiver]** till den butikskontakt som ska ta emot meddelanden om misslyckade e-postöverföringar.
   - Ange **[!UICONTROL Payment Failed Template]** till mallen som används för e-postmeddelandet som skickas när betalningsmetoden misslyckas under utcheckningen.

1. För **[!UICONTROL Send Payment Failed Email Copy To]** anger du e-postadressen till alla som ska få en kopia av den misslyckade betalningen.

   Om du skickar en kopia till flera mottagare avgränsar du varje adress med ett kommatecken.

1. Ange **[!UICONTROL Payment Failed Copy Method]** till något av följande:

   - `Bcc` - Skickar en _blankt text_ genom att inkludera mottagaren i rubriken för samma e-postmeddelande som skickas till kunden. Mottagaren av hemlig kopia är inte synlig för kunden.
   - `Separate Email` - Skickar kopian som ett separat e-postmeddelande.

1. Klicka på **[!UICONTROL Save Config]**.
