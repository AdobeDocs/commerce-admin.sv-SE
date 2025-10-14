---
title: Arkivera order
description: Lär dig hur du konfigurerar orderarkivet för att förbättra prestanda och effektivisera Commerce för din organisation.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Arkivera order

{{ee-feature}}

Att arkivera beställningar regelbundet förbättrar prestanda och håller arbetsytan fri från onödig information så att du kan fokusera på den aktuella verksamheten. Fakturor, leveranser och kreditnotor kan arkiveras automatiskt eller manuellt och kan visas när som helst.

>[!NOTE]
>
>Alternativet _[!UICONTROL Archive]_&#x200B;visas bara på [[!UICONTROL Sales] menu](sales-menu.md) när arkivering är [aktiverad](../configuration-reference/sales/sales.md).

## Konfigurera orderarkivet

Din butik kan konfigureras för att arkivera order, fakturor, leveranser och kreditnotor efter ett visst antal dagar. Du kan flytta beställningar och tillhörande dokument till arkivet eller återställa dem till deras tidigare status. Arkiverade order tas inte bort och är fortfarande tillgängliga från administratören. Arkiverade data kan exporteras till en CSV-fil och öppnas i ett kalkylblad. När det här alternativet är aktiverat visas åtgärden _Arkiv_ längst upp på arbetsytan.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera avsnittet **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]**.

   ![Konfigurationsinställningar för arkivering av order, fakturor, leveranser, kreditnotor](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Archiving]** till `Yes`.

   >[!NOTE]
   >
   >Om du senare bestämmer dig för att stänga av arkiveringen återställs alla arkiverade order till det tidigare tillståndet.

1. Ange **[!UICONTROL Archive Orders Purchased]** till det antal dagar som du vill vänta innan slutförda order arkiveras.

   Som standard arkiveras beställningar 30 dagar efter köpet.

1. I listan **[!UICONTROL Order Statuses to be Archived]** väljer du varje orderstatus som ska användas för att identifiera order som ska arkiveras.

   Om du vill markera flera objekt håller du ned Ctrl (Windows) eller Kommando (Mac) samtidigt som du klickar på varje objekt.

1. Klicka på **[!UICONTROL Save Config]**.

1. Uppdatera eventuell ogiltig cache när du uppmanas till detta.

## Visa arkiverade dokument

1. Välj något av följande på menyn _[!UICONTROL Sales]_&#x200B;under&#x200B;_[!UICONTROL Archive]_:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Om du vill visa information klickar du på ett arkiverat dokument i listan.

## Tillämpa en åtgärd på ett arkiverat dokument

Markera varje dokument som ska vara mål för åtgärden och välj något av följande **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Arkivera dokument manuellt

1. Välj den typ av dokument som ska arkiveras från följande:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Markera kryssrutan för varje objekt som du vill arkivera.

1. I det övre högra hörnet anger du **[!UICONTROL Actions]** till `Move to Archive`.

1. Klicka på **[!UICONTROL Submit]** om du vill arkivera de markerade dokumenten.

## Återställ arkiverade dokument

1. Välj den typ av dokument som du vill återställa.

1. Välj dokument med något av följande alternativ:

   - Om du vill markera alla synliga dokument klickar du på **[!UICONTROL Select Visible]** i det övre vänstra hörnet.

   - Markera manuellt kryssrutan för varje dokument som du vill återställa.

1. I det övre högra hörnet anger du **[!UICONTROL Action]** till `Move to Orders Management`.

1. Klicka på **[!UICONTROL Submit]** om du vill återställa dokumenten.

## Exportera arkiverade dokument

1. Välj den typ av dokument som du vill exportera.

1. I den övre högra menyn anger du **[!UICONTROL Export to:]** till något av följande värden:

   - `CSV`
   - `Excel`

1. Klicka på **[!UICONTROL Export]**.

Din butik kan konfigureras för att arkivera order, fakturor, leveranser och kreditnotor efter ett visst antal dagar. Du kan flytta beställningar och tillhörande dokument till arkivet eller återställa dem till deras tidigare status. Arkiverade order tas inte bort och är fortfarande tillgängliga från administratören. Arkiverade data kan exporteras till en CSV-fil och öppnas i ett kalkylblad. När det här alternativet är aktiverat visas kommandot _[!UICONTROL Archive]_&#x200B;längst upp på arbetsytan.

## Arkivera order manuellt

1. Gå till **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**&#x200B;på sidofältet_ Admin _.

1. Markera kryssrutan i den första kolumnen om du vill välja ordningen i rutnätet.

1. Ställ in kontrollen **[!UICONTROL Actions]** på `Move to Archive` och sök efter meddelandet att ordningen har arkiverats.

   ![Flyttar valda order till arkivet &#x200B;](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>Mer information om hur du anger en lista över orderstatusar som kan arkiveras finns i [Konfigurera orderarkivet](#configure-the-order-archive).

## Visa en arkiverad order

1. Öppna arkivvyn på något av följande sätt:

   - Klicka på **[!UICONTROL Go to Archive]** i knappfältet ovanför stödrastret _[!UICONTROL Orders]_.

   - Gå till **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**&#x200B;på sidofältet_ Admin _.

   >[!NOTE]
   >
   >Precis som på sidan Beställningar är rubriken för den arkiverade beställningssidan _[!UICONTROL Orders]_. Den enda märkbara skillnaden är alternativet&#x200B;_[!UICONTROL Return to Orders Management]_ i knappfältet. Sidans URL anger också att du är i orderarkivet.

1. Klicka på **[!UICONTROL View]** i kolumnen _Åtgärd_.

   ![Visa en arkiverad order](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Återställa en arkiverad order

>[!NOTE]
>
>En ordning som återställs från en arkiverad order arkiveras igen enligt det antal dagar som har konfigurerats i inställningen [!UICONTROL Archive Orders Purchased] (se [Konfigurera orderarkivet](#configure-the-order-archive)). Antalet dagar beräknas utifrån datumet [!UICONTROL Updated At] för ordern, som ändras när ordningen flyttas från arkivet.

1. Gå till **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Go to Archive]** i knappfältet.

1. Leta reda på den post som ska återställas och markera den genom att klicka i kryssrutan.

   ![Välj den ordning som ska återställas](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Ange kontrollvärdet **[!UICONTROL Actions]** till `Move to Order Management`.

Leta efter meddelandet att den arkiverade ordern har tagits bort från arkivet.

## Exportera arkiverad order

1. Gå till **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Export]** på åtgärdsmenyn och välj önskat format.
