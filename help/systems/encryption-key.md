---
title: Krypteringsnyckel
description: Lär dig hur du automatiskt genererar eller lägger till en egen krypteringsnyckel, som bör ändras regelbundet för att förbättra säkerheten.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Krypteringsnyckel

Adobe Commerce och Magento Open Source använder en krypteringsnyckel för att skydda lösenord och andra känsliga data. En [!DNL ChaCha20-Poly1305]-algoritm som är branschstandard används med en 256-bitars nyckel för att kryptera alla data som kräver kryptering. Detta inkluderar kreditkortsdata och integreringslösenord (betalnings- och leveransmodul). Dessutom används en stark Secure Hash-algoritm (SHA-256) för att hash-koda alla data som inte kräver dekryptering.

Under den första installationen uppmanas du att antingen låta Commerce generera en krypteringsnyckel eller ange en egen. Med krypteringsnyckelverktyget kan du ändra nyckeln efter behov. Krypteringsnyckeln bör ändras regelbundet för att förbättra säkerheten, och när som helst kan originalnyckeln bli komprometterad. När nyckeln ändras kodas alla äldre data om med den nya nyckeln.

Mer teknisk information finns i [Avancerad lokal installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) i _installationshandboken_.

## Steg 1: Gör filen skrivbar

Om du vill ändra krypteringsnyckeln kontrollerar du att följande fil är skrivbar: `[your store]/app/etc/env.php`

## Steg 2: Ändra krypteringsnyckeln

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**på sidofältet_ Admin _.

   ![Systemkrypteringsnyckel](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Gör något av följande:

   - Om du vill generera en ny nyckel anger du **[!UICONTROL Auto-generate Key]** till `Yes`.
   - Om du vill använda en annan nyckel anger du **[!UICONTROL Auto-generate Key]** till `No`. I fältet **[!UICONTROL New Key]** anger eller klistrar du sedan in den nyckel som du vill använda.

1. Klicka på **[!UICONTROL Change Encryption Key]**.

1. Registrera den nya nyckeln på en säker plats.

   Du måste dekryptera data om det uppstår problem med filerna.
