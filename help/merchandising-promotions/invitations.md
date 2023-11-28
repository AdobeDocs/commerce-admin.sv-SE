---
title: Händelseinbjudningar
description: Lär dig hur kunderna kan skicka och visa inbjudningar till händelser och privat försäljning från kontrollpanelen för sina kundkonton.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Händelseinbjudningar

{{ee-feature}}

När inbjudningar är aktiverade kan kunderna skicka och visa inbjudningar från kontrollpanelen för sina kundkonton. E-postinbjudan innehåller en länk till butikens inloggningssida.

## Mina inbjudningar

The _[!UICONTROL My Invitations]_i kundkontot visas alla inbjudningar som kunden har skickat. Kunder kan skicka inbjudningar till vänner och familj för butiksevenemang, presentregister, önskelistor och så vidare.

![Mina inbjudningar](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Arbetsflöde för inbjudan

1. **Kunden förbereder inbjudningar**: Från kontouppsättningen förbereder kunden listan över mottagare och slutför inbjudan. Ett anpassat meddelande kan inkluderas, beroende på konfigurationen.
1. **Kunden skickar inbjudningar**: När det är klart klickar kunden på _[!UICONTROL Send Invitations]_-knappen.
1. **Överföringen hanteras i systemet**: Systemet skickar inbjudningar i grupper enligt det nummer som angetts i konfigurationen.
1. **Kundövervakarnas svar**: Kunden övervakar statusen för varje inbjudan från kontokontrollpanelen, som `Sent`, `Accepted`, eller `Canceled`.

### Skicka en inbjudan

1. I sidofältet på deras konto i butiken väljer kunden **[!UICONTROL My Invitations]**.

1. På _Min inbjudan_ sida, klicka **[!UICONTROL Send Invitation]**.

1. Definierar det nya inbjudningsobjektet:

   - Slutför e-postinformationen.

   - (Valfritt) Skapar en inbjudan till flera adresser genom att klicka på **+** och lägga till en annan e-postadress.

     En enskild inbjudan har en begränsning på fem e-postadresser.

   - (Valfritt) Skriver in ett medföljande meddelande.

1. När det är klart klickar du **[!UICONTROL Send Invitation]**.

Ett meddelande om inbjudan skickas till den inbjudna användarens e-postadress med instruktioner om hur du ställer in kontot.

>[!NOTE]
>
>En användare kan bara skicka en inbjudan till en viss e-postadress. Om du försöker skicka om en inbjudan till samma e-postadress visas ett felmeddelande och inbjudan skickas inte.

## Aktivera inbjudningar till din butik

Inbjudningskonfigurationen aktiverar inbjudningar till butiken och avgör hur de skickas.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Invitations]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL General]** -avsnitt.

   ![Kundkonfiguration - allmänna alternativ för inbjudningar](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Invitations Functionality]** till `Yes`.

1. Ange att kunderna ska kunna hantera inbjudningar från butiken **Aktivera inbjudningar i Storefront** till `Yes`.

1. Ange **[!UICONTROL Referred Customer Group]** till något av följande:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Ange **[!UICONTROL New Accounts Registration]** till något av följande:

   - `By Invitation Only`
   - `Available to All`

1. Till **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, markera `Yes`.

1. Om du vill begränsa antalet inbjudningar som kan skickas samtidigt anger du numret i dialogrutan **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** fält.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Email]** och gör följande:

   ![Kundkonfiguration - alternativ för inbjudningar via e-post](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Välj den butiksidentitet som ska användas som **[!UICONTROL Customer Invitation Email Sender]**.

   - Välj **[!UICONTROL Customer Invitation Email Template]** används för skickade inbjudningar.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Skicka och hantera inbjudningar i administratören

I [Privata försäljningsrapporter](../getting-started/private-sales-reports.md) kan du se hur många inbjudningar som har skickats under en viss period eller till vilka kunder du har skickat inbjudningar.

### Skapa en inbjudan i administratören

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Invitations]**.

1. På nästa skärm anger du e-postadresser för att bjuda in nya kunder, lägger till ett anpassat meddelande, väljer en avsändare och väljer en inbjudningsgrupp.

   Om du har flera butiksvyer använder du **[!UICONTROL Send From]** för att ange den butiksvy som inbjudan skickas från.

   ![Information om inbjudningar](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

### Ignorera inbjudningar för en enskild enhet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Sök efter önskad inbjudan med hjälp av filter och öppna den i redigeringsläge.

1. Klicka på i det övre högra hörnet **[!UICONTROL Discard Invitation]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

### Ignorera inbjudningar för flera entiteter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Sök efter och välj de inbjudningar som ska ignoreras.

1. Överst till vänster använder du **[!UICONTROL Actions]** meny att välja **[!UICONTROL Discard Selected]** och klicka **[!UICONTROL Submit]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

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
