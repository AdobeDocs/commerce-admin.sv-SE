---
title: Konfigurera högsta antal rekvisitionslistor
description: Lär dig mer om konfigurationen av rekvisitionslistan, som styr det högsta antal som kan upprätthållas för varje kundkonto.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Konfigurera högsta antal rekvisitionslistor

När funktionen för rekvisitionslista är aktiverad kan kunderna skapa flera listor med artiklar som köpts ofta och använda dessa listor för orderplacering. Den är tillgänglig för både inloggade användare och gäster. Du kan aktivera rekvisitionslistor när du [konfigurera B2B-funktionerna](enable-basic-features.md).

En kund kan ha flera listor som fokuserar på produkter från olika leverantörer, köpare, team, kampanjer eller annat som effektiviserar vanliga arbetsflöden. [Funktioner för rekvisitionslista](requisition-lists.md) liknar önskelistor, med följande skillnader:

- En rekvisitionslista rensas inte efter att artiklar har skickats till kundvagnen. Det kan användas flera gånger.
- I användargränssnittet för rekvisitionslistor används en kompakt vy för att visa många objekt.

Som standard kan kunderna behålla upp till 999 rekvisitionslistor för sitt konto. Men du kan ändra konfigurationen och ange ett lägre nummer för att minska belastningen på din butik.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Requisition Lists]**.

   ![Rekvisitionslistor - allmän inställning](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Number of Requisition Lists]** anger du det maximala antalet rekvisitionslistor som kan underhållas för varje kundkonto.

   Minsta antal är `2`, och det högsta värdet är `999`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
