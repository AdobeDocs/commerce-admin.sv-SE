---
title: Händelseinbjudningar
description: Lär dig hur kunderna kan skicka och visa inbjudningar till händelser och privat försäljning från kontrollpanelen för sina kundkonton.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Händelseinbjudningar

{{ee-feature}}

När inbjudningar är aktiverade kan kunderna skicka och visa inbjudningar från kontrollpanelen för sina kundkonton. E-postinbjudan innehåller en länk till butikens inloggningssida.

## Mina inbjudningar

Avsnittet _[!UICONTROL My Invitations]_&#x200B;i kundkontot innehåller alla inbjudningar som har skickats av kunden. Kunder kan skicka inbjudningar till vänner och familj för butiksevenemang, presentregister, önskelistor och så vidare.

![Mina inbjudningar](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Arbetsflöde för inbjudan

1. **Kunden förbereder inbjudningar**: Från kontokontrollpanelen förbereder kunden listan över mottagare och slutför inbjudan. Ett anpassat meddelande kan inkluderas, beroende på konfigurationen.
1. **Kunden skickar inbjudningar**: När det är klart klickar kunden på knappen _[!UICONTROL Send Invitations]_.
1. **System hanterar överföring**: Systemet skickar inbjudningar i grupper enligt det nummer som angetts i konfigurationen.
1. **Kunden övervakar svaret**: Kunden övervakar statusen för varje inbjudan från kontomanelen, till exempel `Sent`, `Accepted` eller `Canceled`.

### Skicka en inbjudan

1. I sidofältet för deras konto på butiken väljer kunden **[!UICONTROL My Invitations]**.

1. Klicka på **[!UICONTROL Send Invitation]** på sidan _Min inbjudan_.

1. Definierar det nya inbjudningsobjektet:

   - Slutför e-postinformationen.

   - (Valfritt) Skapar en inbjudan med flera adresser genom att klicka på **+** och lägga till en annan e-postadress.

     En enskild inbjudan har en begränsning på fem e-postadresser.

   - (Valfritt) Skriver in ett medföljande meddelande.

1. Klicka på **[!UICONTROL Send Invitation]** när du är klar.

Ett meddelande om inbjudan skickas till den inbjudna användarens e-postadress med instruktioner om hur du ställer in kontot.

>[!NOTE]
>
>En användare kan bara skicka en inbjudan till en viss e-postadress. Om du försöker skicka om en inbjudan till samma e-postadress visas ett felmeddelande och inbjudan skickas inte.

## Aktivera inbjudningar till din butik

Inbjudningskonfigurationen aktiverar inbjudningar till butiken och avgör hur de skickas.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Invitations]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL General]**.

   ![Kundkonfiguration - bjuder in allmänna alternativ](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Invitations Functionality]** till `Yes`.

1. Om du vill att kunderna ska kunna hantera inbjudningar från butiken anger du **Aktivera inbjudningar på Storefront** till `Yes`.

1. Ange **[!UICONTROL Referred Customer Group]** till något av följande:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Ange **[!UICONTROL New Accounts Registration]** till något av följande:

   - `By Invitation Only`
   - `Available to All`

1. Om du vill **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]** väljer du `Yes`.

1. Om du vill begränsa antalet inbjudningar som kan skickas samtidigt anger du numret i fältet **[!UICONTROL Max Invitations Allowed to be Sent at One Time]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Email]** och gör följande:

   ![Kundkonfiguration - inbjudningar till e-postalternativ](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Välj den butiksidentitet som ska användas som **[!UICONTROL Customer Invitation Email Sender]**.

   - Välj **[!UICONTROL Customer Invitation Email Template]** som används för skickade inbjudningar.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Skicka och hantera inbjudningar i administratören

I avsnittet [Privata försäljningsrapporter](../getting-started/private-sales-reports.md) kan du se hur många inbjudningar som har skickats under en angiven period, eller till kunder som du har skickat inbjudningar till.

### Skapa en inbjudan i administratören

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Invitations]** i det övre högra hörnet.

1. På nästa skärm anger du e-postadresser för att bjuda in nya kunder, lägger till ett anpassat meddelande, väljer en avsändare och väljer en inbjudningsgrupp.

   Om du har flera butiksvyer använder du alternativet **[!UICONTROL Send From]** för att ange från vilken butiksvy en inbjudan skickas.

   ![Information om inbjudningar](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

### Ignorera inbjudningar för en enskild enhet

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**&#x200B;på sidofältet_ Admin _.

1. Sök efter önskad inbjudan med hjälp av filter och öppna den i redigeringsläge.

1. Klicka på **[!UICONTROL Discard Invitation]** i det övre högra hörnet.

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.

### Ignorera inbjudningar för flera entiteter

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**&#x200B;på sidofältet_ Admin _.

1. Sök efter och välj de inbjudningar som ska ignoreras.

1. Använd menyn **[!UICONTROL Actions]** längst upp till vänster för att välja **[!UICONTROL Discard Selected]** och klicka på **[!UICONTROL Submit]**.

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.

### Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Select] | Markera kryssrutan för att markera de inbjudningar som ska bli föremål för en åtgärd, eller använd markeringskontrollen i kolumnrubriken. Alternativ: `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | Inbjudans interna ID-nummer |
| [!UICONTROL Email] | Motsvarande e-postadress till kund |
| [!UICONTROL Invitee] | Inbjuden e-postadress |
| [!UICONTROL Sent] | Tid och datum då en inbjudan skickades |
| [!UICONTROL Registered] | Tid och data när en kund registrerades |
| [!UICONTROL Status] | Status för inbjudan. Alternativ: `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | Motsvarande webbplats |
| [!UICONTROL Invitee Group] | En kundgrupp för en inbjudan |

{style="table-layout:auto"}
