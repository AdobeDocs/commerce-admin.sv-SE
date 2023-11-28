---
title: Köer för nyhetsbrev
description: Lär dig hur du hanterar nyhetsbrevsköer för att skicka flera grupper med nyhetsbrev.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Köer för nyhetsbrev

För att hantera inläsningen på servern skickas nyhetsbrev med många prenumeranter i en kö med flera grupper. Du kan kontrollera nyhetsbrevskön regelbundet för att kontrollera status och se hur många som har bearbetats. Eventuella problem som uppstår under överföringen visas på _Problem med nyhetsbrev_ rapport.

## Skicka ett nyhetsbrev

1. På _Administratör_ meny, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. I rutnätet hittar du [mall för nyhetsbrev](newsletter-template.md) som ska skickas och ange **[!UICONTROL Action]** kolumn till `Queue Newsletter`.

1. För **[!UICONTROL Queue Date Start]** väljer du det datum då överföringen ska börja i kalendern (![Kalenderikon](../assets/icon-calendar.png)).

1. För **[!UICONTROL Subscribers From]** markerar du varje butiksvy som ska inkluderas i e-postsändningen.

1. Fyll i e-postrubrikinformationen:

   - Ange en kort beskrivning av nyhetsbrevet för **[!UICONTROL Subject]** e-postrubrikens rad.

   - Ange **[!UICONTROL Sender Name]**.

   - För **[!UICONTROL Sender Email]** anger du avsändarens e-postadress.

     Avsändarens standardnamn och e-postadress anges i konfigurationen.

     ![Information om kön för nyhetsbrev](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Om tillämpligt, skriv en anteckning i **[!UICONTROL Message]** ovanför instruktionerna.

   >[!NOTE]
   >
   >Ta inte bort instruktionerna, som krävs enligt lag i många jurisdiktioner.

1. Om du vill använda anpassade format i ett nyhetsbrev lägger du till dem i **[!UICONTROL Newsletter Styles]** fält.

1. När du är klar klickar du på **[!UICONTROL Save and Resume]**.

   Nyhetsbrevet visas i kön och väntar på att bearbetas.

## Kontrollera om det finns problem

På _Administratör_ meny, gå till **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Knappfält

| Knapp | Beskrivning |
|--- |--- |
| **[!UICONTROL Back]** | Återgår till sidan för nyhetsbrevmallar utan att spara ändringarna. |
| **[!UICONTROL Reset]** | Återställer alla osparade ändringar i köinformationsformuläret till deras tidigare värden. |
| **[!UICONTROL Preview Template]** | Öppnar en förhandsgranskningssida på en separat flik. |
| **[!UICONTROL Save and Resume]** | Sparar alla gjorda ändringar. Placerar nyhetsbrevet i kö. |
| **[!UICONTROL Save Newsletter]** | Sparar alla gjorda ändringar. Placerar nyhetsbrevet i kö. |

{style="table-layout:auto"}

## Kolumner

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas varje nyhetsbrevmall. |
| [!UICONTROL Queue Start] | Det datum då nyhetsbrevet skickades ut. |
| [!UICONTROL Queue End] | Det datum då nyhetsbrevet slutade skickas. |
| [!UICONTROL Subject] | Ämne för nyhetsbrevmall. |
| [!UICONTROL Status] | Anger status för nyhetsbrevets utskick. Möjliga värden: `Sent`, `Canceled`, `Not Sent`, `Sending`, eller `Paused`. |
| [!UICONTROL Processed] | Anger hur många nyhetsbrev som skickades. |
| [!UICONTROL Recipients] | Anger hur många nyhetsbrev prenumeranterna har fått. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: öppnar ett separat fönster för att förhandsgranska mallen. |

{style="table-layout:auto"}
