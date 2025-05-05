---
title: Inaktivera lagerkällor
description: Lär dig hur du inaktiverar källor och ändrar information, inklusive plats och kontaktpunkt.
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Inaktivera källor

Källor kan inte tas bort för att säkerställa att alla orderdata finns kvar i [!DNL Commerce]. Källor, order och leveranser är direkt kopplade till varandra. Du kan inaktivera källor och ändra information, inklusive plats och kontaktpunkt.

Beroende på statusen för dina platser kan du inaktivera en källa. En inaktiverad källa behåller alla tilldelningar per lager och produkter, men är inte tillgänglig för lager och order.

När en källa är inaktiverad:

- [!DNL Inventory Management] ignorerar och visar inte källan för leverans- eller orderbearbetning.
- Lager har inte åtkomst till lagerkvantiteter från källan för aggregerade lagersummor.
- Orderförsändelser kan inte tilldelas inaktiverade platser.

Du kan inte inaktivera Source som standard. [!DNL Commerce] använder den här källan för alla nya, importerade produkter, för paketprodukter och för support från tredje part. Du kan när som helst aktivera eller inaktivera anpassade källor.

Att ange en källa till `disabled` är användbart i följande situationer:

- Lägga till en butik eller ett lagerställe - När du öppnar nya butiker eller lägger till nya lagerställen och leveransställen online lägger du till en källpost för att ställa in produktlager med hjälp av import och anslutning till potentiella lager.
- Säsongstransporter - Semesterdagar kan vara en hektisk tid på året. Du kanske bara vill begränsa leveransen från vissa leveransställen, som lagerställen, för att hålla butiker lagrade och fokuserade på lokala kunder. Du kan också lägga till nya leveransplatser under en begränsad tid för att hantera högre försäljningspriser och inkommande order.
- Stänger en plats - När du stänger en plats för förflyttning till nya anläggningar eller permanent, inaktiverar du för att stoppa nya leveranser från platsen.

## Inaktivera en eller flera anpassade källor

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**&#x200B;på sidofältet_ Admin _.

1. Markera kryssrutan för varje aktiverad anpassad källa som du vill inaktivera.

1. Klicka på menyn _Åtgärder_ i det övre vänstra hörnet och välj **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] källor - Åtgärder-menyn](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL OK]** i bekräftelsedialogrutan.

## Aktivera eller inaktivera en enda anpassad källa

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**&#x200B;på sidofältet_ Admin _.

1. Leta reda på en anpassad källa och klicka på **[!UICONTROL Edit]**.

1. Utöka ![expanderingsväljaren](../assets/icon-display-expand.png) i avsnittet _Allmänt_ och ändra **[!UICONTROL Is Enabled]**:

   | Alternativ | Beskrivning |
   | ----- | ----- |
   | `Yes` | Source är aktiverat. Kvantiteten läggs till i försäljningsbar kvantitet. Källan visar den aktuella kvantiteten vid leveransorder. Algoritmen för Source Selection används för att kontrollera om den kan levereras. |
   | `No` | Source är inaktiverat. Kvantiteter läggs inte till i säljbara kvantiteter. Källan listar inte när leveransorder skickas. Leveransalternativen hoppar över den här källan. |

1. Klicka på **[!UICONTROL Save and Close]**.
