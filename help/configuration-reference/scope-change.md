---
title: Konfigurationsomfattning
description: Lär dig hur du anger omfånget för konfigurationsinställningar i Commerce Admin.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: eb61d90c0a3bf5cac976fc8b79b23dc717aca3e6
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Konfigurationsomfattning

Vyn Store i det övre vänstra hörnet av många konfigurationssidor filtrerar vyn av sidan för ett specifikt omfång och anger värdet för vissa enheter som används i Commerce. Den listar varje nivå i hierarkin efter namn och används för att ändra omfattningen till en annan nivå. Alla inställningar som representerar det aktuella omfånget är nedtonade, så endast de som representerar den aktuella omfångsinställningen är tillgängliga. Omfånget är från början inställt på _Standardkonfiguration_. För administratörsanvändare med begränsad åtkomst innehåller listan med tillgängliga butiksvyer endast de som användaren har tillgång till [behörighet](../systems/permissions.md) för åtkomst.

| Nivå | Beskrivning |
|--- |--- |
| [!UICONTROL Default Config] | Standardsystemkonfigurationen. |
| [!UICONTROL Main Website] | Namnet på webbplatsen högst upp i hierarkin. |
| [!UICONTROL Main Website Store] | Namnet på det standardarkiv som är associerat med den överordnade webbplatsen. |
| [!UICONTROL Default Store View] | Namnet på den standardbutiksvy som är associerad med det överordnade arkivet. |
| [!UICONTROL Stores Configuration] | Hoppar till rutnätet Lagrar, och det är samma sak som att välja [!UICONTROL Stores] > [!UICONTROL All Stores] från sidofältet Admin. |

{:style=&quot;table-layout:auto&quot;}

![Använd kryssrutorna Systemvärde](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

The _[!UICONTROL Use System Value]_kryssrutan till höger om många konfigurationsinställningar används för att antingen tillämpa eller åsidosätta standardfältvärdet inom det aktuella konfigurationsomfånget. Standardfältvärdet kan inte ändras när kryssrutan är markerad. Om du vill ändra värdet avmarkerar du kryssrutan och anger det nya värdet. Du uppmanas att bekräfta varje gång du ändrar systemvärdet.

Kryssrutans etikett ändras enligt det aktuella omfånget och refererar alltid till den överordnade nivån som är ett steg upp i omfångshierarkin. Eftersom den överordnade nivån är en behållare för alla objekt under den nivån ärvs omfångsinställningen från den överordnade nivån, såvida den inte åsidosätts.

## Standardvärdealternativ

| Kryssruta | Beskrivning |
|--- |--- |
| [!UICONTROL Use system value] | Den här kryssrutan visas när konfigurationsomfånget är inställt på `Default Config`. |
| [!UICONTROL Use Default] | Den här kryssrutan visas när konfigurationsomfånget är inställt på Main `Website`, och refererar till det standardarkiv som är tilldelat webbplatsen. |
| [!UICONTROL Use Website] | Den här kryssrutan visas när konfigurationsomfånget är inställt på en viss butiksvy. När du väljer det här alternativet används inställningen från den överordnade webbplatsen som är associerad med butiksvyn. I det här fallet hoppas butiksnivån över eftersom den används i standardbutiken som är kopplad till webbplatsen. |

{:style=&quot;table-layout:auto&quot;}

## Ange omfånget

Gör följande innan du gör en konfigurationsinställning som bara gäller för en viss webbplats-, butik- eller butiksvy:

1. På _Administratör_ sidofältet gör du något av följande:

   - För de flesta konfigurationsinställningar går du till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - För [designrelaterade inställningar](../content-design/configuration.md), gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Välj sedan önskad butiksvy i rutnätet.

1. Navigera till den konfigurationsinställning som ska ändras och gör följande:

   - I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till den specifika vy där konfigurationen gäller. När du uppmanas att bekräfta omfångsväxling klickar du på **[!UICONTROL OK]**.

     En kryssruta visas efter varje fält och ytterligare fält kan bli tillgängliga.

   - Rensa **[!UICONTROL Use system value]** efter ett fält som du vill redigera. Uppdatera sedan värdet för vyn.

   - Upprepa den här processen för alla fält som behöver uppdateras på sidan.

   ![Ange landsalternativ för den franska butiksvyn](./assets/store-view-french.png){width="700" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Snabbreferens för scope

| Omfång | Beskrivning |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Administratör | Alla webbplatser, butiker och butiksvyer i installationen hanteras av samma administratör. |
| Standardkonfiguration | Den globala [standardkonfiguration](../getting-started/websites-stores-views.md#scope-settings) -inställningarna används genom butikshierarkin, såvida de inte åsidosätts på en lägre nivå. |
| Katalog | Termen _katalog_ avser produktdatabasen som helhet och är tillgänglig under hela installationen. |
| Produktpriser | Produktpriser kan konfigureras för applikationer på global nivå eller på webbplatsnivå. |
| Produktkonfigurationer | Attribut som används som [konfigurerbar produkt](../catalog/product-create-configurable.md) måste ha ett globalt omfång. |
| Kunder | Kundkonton kan konfigureras för program på global nivå eller på webbplatsnivå. Varje webbplats kan ha en separat uppsättning [kundkonton](../customers/customer-account-scope.md) eller dela kundkonton med andra webbplatser i installationen. |
| **[!UICONTROL Website]** |  |
| Domän | Ytterligare [webbplatser](../stores-purchase/introduction.md#store-structure) kan konfigureras som underdomäner till den primära domänen eller ha separata IP-adresser och dedikerade domäner. |
| Kunder | Kundkonton kan konfigureras för program på global nivå eller på webbplatsnivå. Varje webbplats kan ha en separat uppsättning [kundkonton](../customers/customer-account-scope.md) eller dela kundkonton med andra webbplatser i installationen. |
| Valuta | Varje webbplats kan tilldelas en egen [basvaluta](../stores-purchase/currency-configuration.md). Basvalutan används för att bearbeta alla transaktioner, men en annan visningsvaluta kan visas för kunden enligt butiksvyns språkområde. |
| Produkter | Enskilda produkter tilldelas hierarkin på webbplatsnivå. I rutnätet Produkter visas alla produkter i katalogen och de webbplatser där de är tillgängliga. The [Produkt på webbplatser](../catalog/settings-basic-websites.md) används för att identifiera de webbplatser där produkten finns tillgänglig. |
| Produktpriser | [Produktpriser](../catalog/catalog-price-scope.md) kan konfigureras för program på global nivå eller på webbplatsnivå. |
| Betalningsmetoder | [Betalningsmetoder](../stores-purchase/payments.md) har konfigurerats på webbplatsnivå, men titeln och instruktionerna kan konfigureras för varje butiksvy. |
| Utcheckning | The [utcheckningsprocess](../stores-purchase/checkout-process.md) sker på webbplatsnivå, men vissa visningsalternativ kan konfigureras för varje butiksvy. Alla butiker som är kopplade till en webbplats har samma [utcheckningskonfiguration](../stores-purchase/checkout-process.md#checkout-options). |
| Tillåtna länder | Tillåtna länder kan konfigureras på webbplatsnivå. The [tillåtna länder](../getting-started/store-details.md#country-options) inställningarna används i utcheckningen för att begränsa varifrån en kund kan komma. |
| **[!UICONTROL Store]** |  |
| Domän | Med flera butiker kan varje butik ha samma domän, underdomän eller distinkt domän. Mer information finns i [Lägga till lager](../stores-purchase/stores.md#add-stores). |
| Rotkategori | Varje butik kan ha en separat uppsättning produkter och en huvudmeny som är baserad på en&quot;rotkategori&quot; och underkategorier. Varje katalog har en [rotkategori](../catalog/category-root.md) som har tilldelats på butiksnivå. |
| **[!UICONTROL Store View]** |  |
| Underkategorier | The [underkategorier](../catalog/category-create.md#category-structure) som utgör huvudmenyn (under roten) tilldelas på visningsnivå för arkivet. |
| Språk | Varje butiksvy kan tilldelas en annan [locale](../getting-started/store-details.md#locale-options). Visningsvalutan, måttenheterna och administratörsgränssnittet är specifika för språkområdet. |
| Språk | För att kunna hantera flera språk måste allt innehåll, inklusive produktbeskrivningar, vara [översatt](../stores-purchase/store-localize.md#localize-products) för varje butiksvy. |
| Visa valuta | En annan [visningsvaluta](../stores-purchase/currency-configuration.md) kan användas för varje butiksvy, även om transaktionerna bearbetas på webbplatsnivå med basvalutan. |

{:style=&quot;table-layout:auto&quot;}
