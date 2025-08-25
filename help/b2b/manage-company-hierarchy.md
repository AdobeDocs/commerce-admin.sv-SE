---
title: Hantera företagshierarkier
description: Bygg och hantera företagshierarkier för att stödja B2B-organisationer med komplexa operativa modeller.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Hantera företagshierarkier

Med funktionen [!UICONTROL Company Hierarchy] kan du ordna flera relaterade företag under en enda överordnad företagsstruktur. Detta är idealiskt för företag med dotterföretag, franchiseavtal, flera platser eller komplexa organisationsstrukturer som behöver centraliserad hantering samtidigt som individuella företagsidentiteter bibehålls.

## Användningsexempel

* **Centralisera hantering** - Använd inställningar och konfigurationer i flera företag från ett och samma överordnade företag
* **Bibehåll struktur** - Organisera företag i en logisk hierarki som speglar din affärsorganisation
* **Effektivisera åtgärder**- Hantera offerter, inköpsorder, betalningsmetoder och leveransinställningar för hela organisationen
* **Bevara självbestämmande** - Enskilda företag behåller sin identitet men drar nytta av delade konfigurationer

## Förutsättningar

Innan du skapar en företagshierarki måste du se till att:

* B2B-funktioner aktiveras i din Commerce-installation
* Du har administratörsåtkomst för att hantera företag
* Överordnade och underordnade företag har redan skapats som enskilda företag
* Du är medveten om att om du tillämpar överordnade inställningar åsidosätts befintliga underordnade företagskonfigurationer

## Så här fungerar det

Administratörer kan skapa en företagshierarki genom att tilldela relaterade företag till ett angivet överordnat företag, som är företaget överst i organisationshierarkin.

Skapa ett överordnat företag från Admin genom att redigera ett enskilt företag (`[!UICONTROL Company Type] = Company`) och tilldela relaterade företag i konfigurationen [!UICONTROL Company Hierarchy].

![Stödraster för företagshierarki](./assets/company-hierarchy-grid.png){width="700"}

>[!NOTE]
>
>Mer information om stödrastret [!UICONTROL Company Hierarchy] finns i [Fältbeskrivningar för företagshierarki](account-company-create.md#company-hierarchy).

Hantera företagstilldelningar genom att redigera ett överordnat företag och använda stödrastret *[!UICONTROL Company Hierarchy]* för att lägga till eller ta bort företag. Använd kontrollen *[!UICONTROL Actions]* för att hantera konfigurationen för [avancerade inställningar](#change-company-settings) för företag i organisationen.

## Tilldela företag till ett moderföretag

1. Navigera till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL Companies]**.

   ![Företagsstödraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öppna företagsinformationssidan från stödrastret [!UICONTROL Companies] för att skapa tilldelningarna.

   * Om du vill tilldela ytterligare företag till ett befintligt överordnat företag väljer du åtgärden **[!UICONTROL Edit]** för det överordnade företaget.
   * Om du vill skapa ett överordnat företag väljer du åtgärden **[!UICONTROL Edit]** för det företag som har angetts som överordnat.

     Du kan inte skapa ett nytt överordnat företag från ett befintligt överordnat eller underordnat företag.

1. Expandera **[!UICONTROL Company Hierarchy]** på sidan Företagsinformation och välj sedan **[!UICONTROL Assign Companies]**.

   ![Skapa överordnat företag](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. I listan över tillgängliga företag väljer du de företag som ska tilldelas och sedan **[!UICONTROL Assign Selected Companies]**.

   ![Välj företag att tilldela](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Slutför företagstilldelningen genom att välja **[!UICONTROL Assign]** när du uppmanas till detta.

## Ta bort tilldelning från ett moderföretag

1. På sidan Företag öppnar du företagsinformationssidan för det överordnade företaget genom att välja åtgärden **[!UICONTROL Edit]**.

   ![Detaljsida för överordnat företag](./assets/company-update.png){width="700" zoomable="yes"}

1. Visa listan över tilldelade företag genom att expandera **[!UICONTROL Company Hierarchy]**.

1. Ta bort företaget från organisationen.

   * I kolumnen [!UICONTROL Action] för företaget som ska tas bort, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Ta bort ett företag från en organisation](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   * När du uppmanas till det tar du bort det tilldelade företaget från hierarkin genom att välja **[!UICONTROL Unassign]**.

## Hantera företagsinställningar för en organisation

Uppdatera konfigurationen [Avancerade inställningar](account-company-create.md#advanced-settings) för en organisation. Du kan:

* Använd de överordnade konfigurationsinställningarna för alla underordnade företag
* Använd samma inställningar för utvalda företag i organisationen

Du kan använda någon av följande inställningar:

* **Offerthantering** - Aktivera eller inaktivera möjligheten för företag att begära och hantera offerter
* **Inköpsorder** - Kontrollera om företag kan skapa och hantera inköpsorder
* **Konfiguration av betalningsmetod** - Definiera vilka betalningsmetoder som är tillgängliga för företag
* **Inställningar för betalningsmetod** - Konfigurera specifika parametrar och begränsningar för betalningsmetod
* **Tillgänglighet för leveransmetod** - Ange vilka leveransmetoder företag kan använda
* **Konfiguration av leveransmetod** - Definiera inställningar och begränsningar för leveransmetod

Under uppdateringsprocessen används de ursprungliga konfigurationsvärdena som standard till de aktuella värden som konfigurerats för det överordnade företaget. Du måste markera kryssrutan Ändra för minst en inställning för att kunna använda inställningarna för de valda företagen. Du kan också uppdatera standardvärdet för varje inställning innan du tillämpar ändringarna.

>[!WARNING]
>
>När du använder inställningarna för det överordnade företaget ersätts befintliga underordnade företagskonfigurationer, inklusive kreditbegränsningar, betalningsmetoder, leveransinställningar och anpassade begränsningar. När du har tillämpat inställningarna kan du fortfarande hantera och anpassa de avancerade inställningarna för enskilda överordnade och underordnade företag genom att redigera företagets radobjekt.

### God praxis

När du tillämpar inställningar för överordnade företag på underordnade företag bör du tänka på följande metodtips:

* Granska befintliga inställningar för underordnat företag innan du tillämpar överordnade konfigurationer
* Testinställningarna ändras för ett underordnat företag först
* informera företagsadministratörer som kan påverkas

### Använd inställningar för överordnad konfiguration för underordnade företag

1. Navigera till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL Companies]**.

1. I stödrastret [!UICONTROL Companies] redigerar du det överordnade företaget genom att välja **[!UICONTROL Edit]** i kolumnen **[!UICONTROL Action]**.

1. På detaljsidan för det överordnade företaget expanderar du avsnittet **[!UICONTROL Company Hierarchy]** för att visa företag som ingår i organisationen.

1. Välj de företag som ska konfigureras.

   ![Välj företag från företagshierarkin](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Välj **[!UICONTROL Actions]** i kontrollen **[!UICONTROL Change company settings]** ovanför stödrastret.

   ![Ändra företagsinställningar för företagshierarkin](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Ändra inställningskonfigurationen.

   * På sidan [!UICONTROL Change company settings] hittar du konfigurationsinställningen som du vill ändra.

   * Markera kryssrutan **[!UICONTROL Change]** om du vill aktivera inställningen.

   * Uppdatera värdet vid behov.

     ![Ändra företagsinställningar för flera företag](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. När du har uppdaterat konfigurationen väljer du **[!UICONTROL Apply Changes]**.

1. Välj **[!UICONTROL Change settings]** när du uppmanas att uppdatera konfigurationen för de valda företagen.

>[!MORELIKETHIS]
>
>* [Skapa ett företagskonto](account-company-create.md) - Lär dig skapa enskilda företag innan du skapar hierarkier
>* [Företagsroller och behörigheter](account-company-roles-permissions.md) - Förstå användaråtkomst inom företagsstrukturer
>* [Företagets kredithantering](credit-company.md) - Konfigurera kreditgränser och betalningsvillkor för företag
>* [Hantera företag](manage-companies.md) - Översikt över funktioner för företagshantering
>* [Aktivera B2B-funktioner](enable-basic-features.md) - Aktivera och konfigurera B2B-funktioner
