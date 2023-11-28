---
title: Uppdatera en kundprofil
description: Få tillgång till information om kundaktivitet, t.ex. när kunden senast loggade in eller ut från sitt konto, och uppdatera kundprofilen.
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Uppdatera en kundprofil

Den vänstra panelen i _[!UICONTROL Customer Information]_sidan innehåller information om kundaktivitet, adresser, orderstatistik, senaste beställningar, kundvagnsinnehåll, produktrecensioner och nyhetsbrev.

![Kundprofil](assets/cust-profile.png){width="700" zoomable="yes"}

## Redigera ett kundkonto

Metod 1: **_Snabbredigering_**

1. I den första kolumnen markerar du kryssrutan för det kundkonto som ska redigeras.

1. Ange **[!UICONTROL Actions]** kolumn till `Edit`.

   >[!INFO]
   >
   >Värdet för varje värde som kan uppdateras visas i en textruta. Endast vissa värden i den valda kundposten kan redigeras från rutnätet.

   ![Snabbredigering](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. Uppdatera något av följande värden efter behov:

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. Klicka på **[!UICONTROL Save]**.

Metod 2: **_Fullständig redigering_**

1. Leta reda på kundposten som ska redigeras i rutnätet.

1. I _Åtgärder_ kolumn längst till höger, klicka på **[!UICONTROL Edit]**.

1. Gör nödvändiga ändringar i företagsinformationen.

   >[!INFO]
   >
   >Mer information finns på [Uppdatera en kundprofil](../customers/update-account.md).

1. När du är klar klickar du på **[!UICONTROL Save Customer]**.

>[!INFO]
>
>Om du vill ångra alla redigeringar innan du sparar klickar du på **[!UICONTROL Reset]** i det övre knappfältet om du vill återställa alla ändringar till den senast sparade versionen.

## Kundinformation

### [!UICONTROL Customer View]

The _Kundvy_ innehåller information om kunden, inklusive **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]** och **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

The [Kontoinformation](../customers/account-dashboard-account-information.md) -fliken innehåller detaljerad information om kunden, där en Admin-användare kan redigera personlig information, e-post, fjärrshoppinghjälp, födelsedatum och bifoga kunden till webbplatsen eller företaget.

### [!UICONTROL Addresses]

The [Adresser](../customers/account-dashboard-address-book.md) -fliken innehåller kundens standardadresser för fakturering och leverans samt eventuella ytterligare adresser som de använder ofta.

### [!UICONTROL Orders]

The [Beställningar](../stores-purchase/orders.md) rutnätet innehåller en lista över alla aktuella kundorder. Administratören kan spåra deras status.

### [!UICONTROL Returns]

{{ee-feature}}

The [Returnerar](../stores-purchase/returns.md) -fliken visar de aktuella returnerade kundförfrågningarna.

### [!UICONTROL Shopping cart]

The [kundvagn](../stores-purchase/cart.md) I visas produkter som finns i varukorgen, men av någon anledning har köpet inte slutförts.

### [!UICONTROL Wish List]

A [önskelista](../stores-purchase/wishlists.md) visar en lista över produkter som en kund kan överföra till kundvagnen senare.

### [!UICONTROL Gift Registry]

{{ee-feature}}

The [Presentregister](../merchandising-promotions/gift-registry-storefront.md) i listas kundens aktuella presentregister och tillhörande händelse.


### [!UICONTROL Store Credit]

{{ee-feature}}

The [Butikskredit](../customers/store-credit.md) fliken visar ett belopp som återställs till ett kundkonto. Administratören kan hantera värdet.

### [!UICONTROL Newsletter]

The [Nyhetsbrev](../merchandising-promotions/newsletters.md) visas alla e-postmeddelanden som skickas till den aktuella kunden.

### [!UICONTROL Billing Agreements]

The [Faktureringsavtal](../stores-purchase/paypal-billing-agreements.md) På fliken visas alla PayPal-faktureringsavtal mellan butiken och kunden.

### [!UICONTROL Product Reviews]

The [Produktrecensioner](../catalog/settings-advanced-product-reviews.md) på den här fliken visas alla recensioner som har skickats in av den här kunden.

### [!UICONTROL Reward Points]

{{ee-feature}}

The [Belöningspunkter](../merchandising-promotions/rewards-loyalty.md) visas kundens aktuella saldo för belöningspoäng. En administratör kan hantera det här värdet.

## Knappfält

| Knapp | Beskrivning |
|----------|--------------|
| **[!UICONTROL Back]** | Återgår till kundsidan utan att spara ändringarna. |
| **[!UICONTROL Login as Customer]** | Gör det möjligt för handlaren att logga in som kund. |
| **[!UICONTROL Delete Customer]** | Tar bort kundkontot. |
| **[!UICONTROL Reset]** | Återställer alla osparade ändringar i kundformuläret till deras tidigare värden. |
| **[!UICONTROL Create Order]** | [Skapar en order](../stores-purchase/customer-account-create-order.md) som är associerad med kundkontot. |
| **[!UICONTROL Reset Password]** | Återställer kundens lösenord. |
| **[!UICONTROL Force Sign-In]** | Rensar de tokens som är kopplade till kundens lösenord och ger administratören åtkomst till kontot. |
| **[!UICONTROL Manage Shopping Cart]** | Ger åtkomst till kundens kundvagn. |
| **[!UICONTROL Save and Continue Edit]** | Sparar ändringar och håller kundkontot öppet. |
| **[!UICONTROL Save Customer]** | Sparar ändringar och stänger kundkontot. |

{style="table-layout:auto"}
