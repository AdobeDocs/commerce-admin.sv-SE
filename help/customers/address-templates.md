---
title: Kundadressmallar
description: Lär dig hur du kan anpassa kundadressmallar.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Kundadressmallar

{{ee-feature}}

Du kan ändra mallen som styr formatet på kundfakturerings- och leveransadresserna som visas på utskrivna fakturor, leveranser och återbetalningar, samt i adressboken för kundkontot. Om du vill ta med ytterligare information kan du skapa [anpassade attribut](attribute-properties.md) som är kopplade till kundkontot och [adressen](address-attributes.md) och införliva dem i mallen.

## Exempel 1: kort format

För adressmallen [!UICONTROL Text One Line]:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Exempel 2: långt format

För adressmallarna [!UICONTROL Text], [!UICONTROL HTML] och [!UICONTROL PDF]:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Kundadressmallar](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Ändra ordningen på adressfält

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Customer Configuration]**.

1. Klicka för att expandera avsnittet **[!UICONTROL Address Templates]**.

   Avsnittet innehåller en separat uppsättning formateringsinstruktioner för följande:

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Redigera varje mall efter behov med exemplen som referens.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
