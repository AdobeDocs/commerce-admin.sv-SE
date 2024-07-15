---
title: Kundadressattribut
description: Lär dig mer om attributen för kundadresser och hur du konfigurerar dessa attributegenskaper.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# Kundadressattribut

{{ee-feature}}

Attributet Kundadress avgör vilka egenskaper för gatuadresser som anges i [adressboken](account-dashboard-address-book.md) från kundens konto eller under [utcheckningen](../stores-purchase/checkout-process.md).

Anpassade adressattribut kan konfigureras för att ge ytterligare information, t.ex. en valfri e-postadress, ett Skype-konto, alternativt telefonnummer, byggnad eller region. Det anpassade attributet kan sedan införlivas i [adressmallen](address-templates.md) som används för att skapa försäljningsdokument. Processen att skapa ett anpassat adressattribut är nästan densamma som att skapa ett [kundattribut](attribute-properties.md).

Kundadressattribut används i följande formulär:

- [Kundadressregistrering](account-create.md)
- [Kundkontoadress](account-dashboard-address-book.md)

![Admin - Kundadressattribut](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Steg 1: Slutför attributegenskaperna

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Attribute]** i det övre högra hörnet.

   ![Egenskaper för kundattribut](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. Gör följande i avsnittet **[!UICONTROL Attribute Properties]**:

   - Ange en **[!UICONTROL Default Label]** som identifierar attributet under datainmatningen.

   - Ange en **[!UICONTROL Attribute Code]** som identifierar attributet i systemet.

     Attributkoden måste börja med en bokstav och kan innehålla valfri kombination av gemener (a-z) och siffror (0-9). Koden får innehålla högst 30 tecken och får inte innehålla specialtecken eller blanksteg. Understrecket (_) kan användas för att ange ett mellanslag.

     >[!TIP]
     >
     >**_Kortkommando:_** Om du bara vill fylla i de obligatoriska fälten rullar du nedåt till [!UICONTROL Storefront Properties], anger [!UICONTROL Sort Order] och sparar.

1. Ange **[!UICONTROL Input Type]** till något av följande för att avgöra vilken typ av indatakontroll som används för datainmatning:

   - `Text Field` - Ett textfält med en rad.
   - `Text Area` - Ett textområde med flera rader.
   - `Multiple Line` - Skapar flera textrader för attributet, ungefär som en gatuadress med flera rader. Antalet separata datainmatningsrader kan vara mellan 2 och 20. Använd `Default Value` för att ange fältets startvärde.
   - `Date` - Visar ett datumfält med en popup-kalender. Ytterligare egenskaper: Använd `Default Value` för att ange fältets ursprungliga värde. <br/>Använd `Minimal Value` för att ange det tidigaste datum som kan anges.  Använd `Maximum Value` för att ange det senaste datumet som kan anges.
   - `Dropdown` - En nedrullningsbar lista där endast ett värde kan väljas.
   - `Multiple Select` - En nedrullningsbar lista där flera värden kan väljas.
   - `Yes/No` - Ett fält som bara erbjuder ett val av `Yes`- eller `No`-värden.
   - `File (attachment)` - Ett fält som tillåter att en fil överförs och associeras med kundattributet som en bifogad fil.
   - `Image File` - Ett fält som tillåter att en bild överförs till galleriet och associeras med kundattributet.

1. Om kunden måste ange ett värde i fältet anger du **[!UICONTROL Values Required]** till `Yes`.

1. Om du vill tilldela ett initialt värde till fältet anger du **[!UICONTROL Default Value]**.

1. Om du vill kontrollera om de data som anges i fältet är korrekta innan posten sparas, anger du **[!UICONTROL Input Validation]** till den typ av data som ska tillåtas i fältet. Vilka värden som är tillgängliga beror på _[!UICONTROL Input Type]_som har angetts.

   - `None` - Fältet har ingen indatavalidering under datainmatning.
   - `Alphanumeric` - Accepterar alla kombinationer av siffror (0-9) och alfabetiska tecken (a-z, A-Z) under datainmatning. Om du vill ta med specialtecken läser du [!UICONTROL Escape HTML Entities] i nästa steg.
   - `Alphanumeric with Space` - Accepterar alla kombinationer av siffror (0-9), alfabetiska tecken (a-z, A-Z) och mellanslag under datainmatning.
   - `Numeric Only` - Accepterar endast siffror (0-9) under datainmatning.
   - `Alpha Only` - Accepterar endast alfabetiska tecken (a-z, A-Z) under datainmatning.
   - `URL` - Accepterar endast en URL under datainmatning.
   - `Email` - Accepterar endast en e-postadress under datainmatning.
   - `Length Only` - Validerar indata baserat på längden på de data som anges i fältet.

1. Om du vill använda ett förbearbetningsfilter på värden som anges i ett textfält, textområde eller flera radindatatyper anger du **[!UICONTROL Input/Output Filter]** till något av följande:

   - `None` - Använder inte ett filter för text som anges i fältet.
   - `Strip HTML Tags` - Tar bort HTML-taggar från texten. Det här filtret kan hjälpa dig att rensa data som klistras in i ett fält från en annan källa som innehåller HTML-taggar.
   - `Escape  HTML Entities` - Konverterar specialtecken som finns i texten till en giltig escape-sekvens i HTML, till exempel `&;`. Escape-sekvenser placeras mellan ett et-tecken och ett semikolon och används ofta för typografiska citattecken, copyright och varumärkessymboler. Escape-sekvenser används också för att identifiera tecken som symbolerna mindre än (`<`) och större än (`>`) samt et-tecknet som också används i koden. Det här filtret kan hjälpa dig att rensa specialtecken som ibland klistras in i databasfält från ordbehandlare.

1. Fyll i kundrutnät och segmentegenskaper:

   - Om du vill kunna inkludera kolumnen i kundrutnätet anger du **[!UICONTROL Add to Column Options]** till `Yes`.

   - Om du vill filtrera kundstödrastret efter det här attributet anger du **[!UICONTROL Use in Filter Options]** till `Yes`.

   - Om du vill filtrera kundrutnätet efter textattribut med olika filtermatchningsvillkor anger du **[!UICONTROL Grid Filter Condition Type]** till `Partial Match`, `Prefix Match` eller `Full Match`. Det påverkar inte fältet _Sök efter nyckelord_ för stödrastret.

   - Om du vill söka i kundstödrastret efter det här attributet anger du **[!UICONTROL Use in Search Options]** till `Yes`.

   - Om du vill göra det här attributet tillgängligt för [kundsegment](customer-segments.md) anger du **[!UICONTROL Use in Customer Segment]** till `Yes`.

## Steg 2: Slutför butiksegenskaperna

1. Bläddra ned till avsnittet **[!UICONTROL Storefront Properties]**.

   ![Kundadressattribut - Storefront-egenskaper](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Om du vill göra attributet synligt för kunderna anger du **[!UICONTROL Show on Storefront]** till `Yes`.

1. Ange ett tal i fältet **[!UICONTROL Sort Order]**, som bestämmer utseendeordningen när det listas med andra attribut.

1. Ange **[!UICONTROL Forms to Use]** för varje formulär som ska innehålla attributet.

   Om du vill välja båda alternativen håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) när du klickar på varje formulär.

   - [Kundadressregistrering](account-create.md)
   - [Kundkontoadress](account-dashboard-address-book.md)

## Steg 3: Slutför etiketten och spara

1. Välj **[!UICONTROL Manage Labels/Options]** i panelen till vänster.

1. Under **[!UICONTROL Manage Titles]** anger du en etikett som identifierar attributet för varje [butiksvy](../getting-started/websites-stores-views.md).

1. Klicka på **[!UICONTROL Save Attribute]** när du är klar.

   ![Kundadressattribut - etiketter/alternativ](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Fältbeskrivningar

### [!UICONTROL Attribute Properties]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Default Label] | Standardetiketten som identifierar attributet i Admin och storefront. |
| [!UICONTROL Attribute Code] | En unik kod som identifierar attributet i systemet. Koden kan innehålla upp till 21 tecken och får inte innehålla mellanslag eller specialtecken. Understreckssymbolen kan användas i stället för ett mellanslag. |
| [!UICONTROL Input Type] | Bestämmer den [indatakontroll](../catalog/attributes-input-types.md) som används för datainmatning. Alternativ: <br/>**`Text Field`**- Ett textfält med en rad.<br/>**`Text Area`** - Ett textområde med flera rader. <br/>**`Multiple Line`**- Skapar flera textrader för attributet, ungefär som en gatuadress med flera rader. Antalet separata datainmatningsrader kan vara mellan 2 och 20.<br/>**`Date`** - Visar ett datumfält med en popup-kalender.<br/>**`Dropdown`**- En nedrullningsbar lista där endast ett värde kan väljas.<br/>**`Multiple Select`** - En nedrullningsbar lista där flera värden kan väljas. <br/>**`Yes/No`**- Ett fält som bara erbjuder ett val av `Yes`- eller `No`-värden.<br/>**`File (attachment)`** - Ett fält som tillåter att en fil överförs och associeras med kundattributet som en bifogad fil. <br/>**`Image File`**- Ett fält som tillåter att en bild överförs till galleriet och associeras med kundattributet. |
| [!UICONTROL Values Required] | Anger om ett värde måste anges i fältet. Alternativ: `Yes` / `No` |
| [!UICONTROL Default Value] | Anger det inledande värdet för attributet. |
| [!UICONTROL Input Validation] | Valet av alternativ avgörs av indatatypen. Alternativ: <br/>**`None`**- Fältet har ingen indatavalidering under datainmatning.<br/>**`Alphanumeric`** - Accepterar alla kombinationer av siffror (0-9) och alfabetiska tecken (a-z, A-Z) under datainmatning. <br/>**`Alphanumeric with Space`**- Tillåter att utrymmen i gatuadressen uppfyller transportörens längdkrav. Vid utcheckning kan kunden ange valfri kombination av siffror (0-9), alfabetiska tecken (a-z, A-Z) och blanksteg i mottagarens och avsändarens gatuadress. Eventuella extra blanksteg trimmas när adressen sparas.<br/>**`Numeric Only`** - Accepterar endast siffror (0-9) under datainmatning. <br/>**`Alpha Only`**- Accepterar endast alfabetiska tecken (a-z, A-Z) under datainmatning.<br/>** URL **- Accepterar endast en URL under datainmatning.<br/>**`Email`** - Accepterar endast en e-postadress under datainmatning. <br/>**`Length Only`**- Validerar indata baserat på längden på de data som anges i fältet. |
| [!UICONTROL Input/Output Filter] | Tillämpar ett förbearbetningsfilter på värden som anges i ett textfält, textområde eller flera rader innan posten sparas. Alternativ: <br/>**`None`**- Använder inte ett filter för text som anges i fältet.<br/>**`Strip HTML Tags`** - Tar bort HTML-taggar från texten. Det här filtret kan hjälpa dig att rensa data som klistras in i ett fält från en annan källa som innehåller HTML-taggar. <br/>**`Escape HTML Entities`**- Konverterar specialtecken som finns i texten till en giltig escape-sekvens i HTML, till exempel `amp;`. Escape-sekvenser placeras mellan ett et-tecken och ett semikolon och används ofta för typografiska citattecken, copyrightsymboler och varumärkessymboler. Escape-sekvenser används också för att identifiera tecken som symbolerna mindre än (`<`) och större än (`>`) samt et-tecknet som också används i koden. Det här filtret kan hjälpa dig att rensa specialtecken som ibland klistras in i databasfält från ordbehandlare. |
| [!UICONTROL Add to Column Options] | Anger om attributet ingår som en kolumn i rutnätet [Kunder](./customers-all.md). Alternativ: `Yes` / `No` |
| Använd i filteralternativ | Anger om attributet kan användas som ett filter för sökåtgärder från rutnätet. Alternativ: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Anger filtermatchningsvillkor för attribut i sökåtgärder från rutnätet. Det påverkar inte fältet _[!UICONTROL Search by keyword]_för stödrastret. Alternativ: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Anger om attributvärdet kan användas som nyckelord i sökåtgärder. Alternativ: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Avgör om attributet ingår i villkoren för [kundsegment](./customer-segments.md). Alternativ: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Show on Storefront] | Avgör om attributet visas som ett fält i kundinformationen i butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Sort Order] | Anger sorteringsordningen för det här attributet i relation till andra kundattribut. Sorteringsordningen bestämmer den sekvens som fält får fokus under datainmatning när tangentbordsnavigering används. |
| [!UICONTROL Forms to Use in] | Anger vilka sidor med datainmatningsformulär som attributet finns på. Alternativ: <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
