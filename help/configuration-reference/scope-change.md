---
title: Konfigurationsomfattning
description: Läs om hur du anger omfånget för konfigurationsinställningar i Commerce Admin.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Konfigurationsomfattning

Vyn Store i det övre vänstra hörnet av många konfigurationssidor filtrerar vyn av sidan för ett specifikt omfång och anger värdet för vissa enheter som används av Commerce. Den listar varje nivå i hierarkin efter namn och används för att ändra omfattningen till en annan nivå. Alla inställningar som representerar det aktuella omfånget är nedtonade, så endast de som representerar den aktuella omfångsinställningen är tillgängliga. Omfånget är från början inställt på _Standardkonfiguration_. För administratörsanvändare med begränsad åtkomst innehåller listan med tillgängliga butiksvyer bara de som användaren har [behörighet](../systems/permissions.md) att komma åt.

| Nivå | Beskrivning |
|--- |--- |
| [!UICONTROL Default Config] | Standardsystemkonfigurationen. |
| [!UICONTROL Main Website] | Namnet på webbplatsen högst upp i hierarkin. |
| [!UICONTROL Main Website Store] | Namnet på det standardarkiv som är associerat med den överordnade webbplatsen. |
| [!UICONTROL Default Store View] | Namnet på den standardbutiksvy som är associerad med det överordnade arkivet. |
| [!UICONTROL Stores Configuration] | Hoppar till rutnätet Lagrar, och är samma sak som att välja [!UICONTROL Stores] > [!UICONTROL All Stores] från sidofältet Admin. |

{style="table-layout:auto"}

![Använd kryssrutor för systemvärde markerade](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

Kryssrutan _[!UICONTROL Use System Value]_&#x200B;till höger om många konfigurationsinställningar används för att antingen tillämpa eller åsidosätta standardfältvärdet inom det aktuella konfigurationsomfånget. Standardfältvärdet kan inte ändras när kryssrutan är markerad. Om du vill ändra värdet avmarkerar du kryssrutan och anger det nya värdet. Du uppmanas att bekräfta varje gång du ändrar systemvärdet.

Kryssrutans etikett ändras enligt det aktuella omfånget och refererar alltid till den överordnade nivån som är ett steg upp i omfångshierarkin. Eftersom den överordnade nivån är en behållare för alla objekt under den nivån ärvs omfångsinställningen från den överordnade nivån, såvida den inte åsidosätts.

## Standardvärdealternativ

| Kryssruta | Beskrivning |
|--- |--- |
| [!UICONTROL Use system value] | Den här kryssrutan visas när konfigurationsomfånget är inställt på `Default Config`. |
| [!UICONTROL Use Default] | Den här kryssrutan visas när konfigurationsomfånget är inställt på Main `Website` och refererar till standardarkivet som är tilldelat webbplatsen. |
| [!UICONTROL Use Website] | Den här kryssrutan visas när konfigurationsomfånget är inställt på en viss butiksvy. När du väljer det här alternativet används inställningen från den överordnade webbplatsen som är associerad med butiksvyn. I det här fallet hoppas butiksnivån över eftersom den används i standardbutiken som är kopplad till webbplatsen. |

{style="table-layout:auto"}

## Ange omfånget

Gör följande innan du gör en konfigurationsinställning som bara gäller för en viss webbplats-, butik- eller butiksvy:

1. Gör något av följande på sidofältet _Admin_:

   - För de flesta konfigurationsinställningar går du till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - För [designrelaterade inställningar](../content-design/configuration.md) går du till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Välj sedan önskad butiksvy i rutnätet.

1. Navigera till den konfigurationsinställning som ska ändras och gör följande:

   - I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till den specifika vyn där konfigurationen gäller. När du uppmanas att bekräfta omfångsväxling klickar du på **[!UICONTROL OK]**.

     En kryssruta visas efter varje fält och ytterligare fält kan bli tillgängliga.

   - Avmarkera kryssrutan **[!UICONTROL Use system value]** efter ett fält som du vill redigera. Uppdatera sedan värdet för vyn.

   - Upprepa den här processen för alla fält som behöver uppdateras på sidan.

   ![Ange landsalternativ för den franska butiksvyn](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Snabbreferens för scope

| Omfång | Beskrivning |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Administratör | Alla webbplatser, butiker och butiksvyer i installationen hanteras av samma administratör. |
| Standardkonfiguration | De globala [standardkonfigurationsinställningarna](../getting-started/websites-stores-views.md#scope-settings) används via arkivhierarkin, såvida de inte åsidosätts på en lägre nivå. |
| Katalog | Termen _katalog_ refererar till produktdatabasen som helhet och är tillgänglig under hela installationen. |
| Produktpriser | Produktpriser kan konfigureras för applikationer på global nivå eller på webbplatsnivå. |
| Produktkonfigurationer | Attribut som används som [konfigurerbara produkt](../catalog/product-create-configurable.md)-alternativ måste ha ett globalt omfång. |
| Kunder | Kundkonton kan konfigureras för program på global nivå eller på webbplatsnivå. Varje webbplats kan ha en separat uppsättning med [kundkonton](../customers/customer-account-scope.md) eller dela kundkonton med andra webbplatser i installationen. |
| **[!UICONTROL Website]** |  |
| Domän | Ytterligare [webbplatser](../stores-purchase/introduction.md#store-structure) kan konfigureras som underdomäner till den primära domänen eller ha separata IP-adresser och dedikerade domäner. |
| Kunder | Kundkonton kan konfigureras för program på global nivå eller på webbplatsnivå. Varje webbplats kan ha en separat uppsättning med [kundkonton](../customers/customer-account-scope.md) eller dela kundkonton med andra webbplatser i installationen. |
| Valuta | Varje webbplats kan tilldelas en annan [basvaluta](../stores-purchase/currency-configuration.md). Basvalutan används för att bearbeta alla transaktioner, men en annan visningsvaluta kan visas för kunden enligt butiksvyns språkområde. |
| Produkter | Enskilda produkter tilldelas hierarkin på webbplatsnivå. I rutnätet Produkter visas alla produkter i katalogen och de webbplatser där de är tillgängliga. Inställningen [Produkt på webbplatser](../catalog/settings-basic-websites.md) identifierar varje webbplats där produkten är tillgänglig. |
| Produktpriser | [Produktpriser](../catalog/catalog-price-scope.md) kan konfigureras för program på global nivå eller på webbplatsnivå. |
| Betalningsmetoder | [Betalningsmetoder](../stores-purchase/payments.md) har konfigurerats på webbplatsnivå, men titeln och instruktionerna kan konfigureras för varje butiksvy. |
| Utcheckning | [Utcheckningsprocessen](../stores-purchase/checkout-process.md) äger rum på webbplatsnivå, men vissa visningsalternativ kan konfigureras för varje butiksvy. Alla butiker som är associerade med en webbplats har samma [utcheckningskonfiguration](../stores-purchase/checkout-process.md#checkout-options). |
| Tillåtna länder | Tillåtna länder kan konfigureras på webbplatsnivå. Inställningarna för [tillåtna länder](../getting-started/store-details.md#country-options) används i utcheckningen för att begränsa varifrån en kund kan komma. |
| **[!UICONTROL Store]** |  |
| Domän | Med flera butiker kan varje butik ha samma domän, underdomän eller distinkt domän. Mer information finns i [Lägga till butiker](../stores-purchase/stores.md#add-stores). |
| Rotkategori | Varje butik kan ha en separat uppsättning produkter och en huvudmeny som är baserad på en&quot;rotkategori&quot; och underkategorier. Varje katalog har en [rotkategori](../catalog/category-root.md) som är tilldelad på arkivnivå. |
| **[!UICONTROL Store View]** |  |
| Underkategorier | De [underkategorier](../catalog/category-create.md#category-structure) som utgör huvudmenyn (under roten) tilldelas på visningsnivån för arkivet. |
| Språk | Varje butiksvy kan tilldelas olika [nationella inställningar](../getting-started/store-details.md#locale-options). Visningsvalutan, måttenheterna och administratörsgränssnittet är specifika för språkområdet. |
| Språk | Om du vill ha stöd för flera språk måste allt innehåll, inklusive produktbeskrivningar, vara [översatt](../stores-purchase/store-localize.md#localize-products) för varje butiksvy. |
| Visa valuta | En annan [visningsvaluta](../stores-purchase/currency-configuration.md) kan användas för varje butiksvy, även om transaktionerna bearbetas på webbplatsnivå med basvalutan. |

{style="table-layout:auto"}
