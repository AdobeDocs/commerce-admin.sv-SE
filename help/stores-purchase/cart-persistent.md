---
title: Kartbeständighet
description: Lär dig hur en beständig kundvagn spårar oköpta varukorgsartiklar och sparar informationen för kundens nästa besök.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# Kartbeständighet

En beständig kundvagn håller reda på oköpta artiklar som finns kvar i kundvagnen och sparar informationen för kundens nästa besök. Kunder som _sparad_ kan få innehållet i kundvagnen återställt nästa gång de besöker din butik.

En kundvagn kan minska antalet övergivna kundvagnar och öka försäljningen. Det är viktigt att förstå att den beständiga kundvagnen inte visar känslig kontoinformation vid något tillfälle. Medan den beständiga kundvagnen används måste både registrerade kunder och gästshoppare antingen logga in på ett befintligt konto eller skapa ett konto innan de går till kassan. För gästkunder är en beständig kundvagn det enda sättet att hämta information från en tidigare session.

Om du vill hantera användningen av kundvagnsbeständighet för din webbplats eller inom specifika butiksvyer kan du [konfigurera beständig kundvagn](#configure-a-persistent-cart) inställningar. Mer information om hur de här inställningarna påverkar shoppingupplevelsen i din butik finns i [Beständigt kundvagnsarbetsflöde](#persistent-cart-workflow).

>[!NOTE]
>
>När du använder en beständig kundvagn bör du ange serversessionens livstid och sessionscookien till en lång tidsperiod. Se [Sessionslivstid](../customers/customer-online-options.md) för mer information.

Om du vill använda den beständiga kundvagnen måste kundens webbläsare vara inställd på att tillåta cookies. Det finns två typer av cookies som används för kundvagnsåtgärder:

- **Sessionscookie** - En sessionscookie finns under ett enda besök på webbplatsen och upphör när kunden lämnar webbplatsen, eller efter en viss tidsperiod.

- **Beständig cookie** - En långvarig, beständig cookie finns kvar efter sessionens slut och sparar en lista över kundens kundvagnsinnehåll för framtida referens.

## Beständigt kundvagnsarbetsflöde

När kundvagnen är permanent [aktiverad](#configure-a-persistent-cart), beror arbetsflödet på:

- Värdena för _Aktivera Kom ihåg mig_ och _Rensa genomskinlighet vid utloggning_ inställningar
- Kundens beslut att välja eller rensa _Kom ihåg mig_ kryssruta
- När den beständiga cookien rensas

När en beständig cookie används `Not Jane Smith?` visas i sidhuvudet. Detta meddelande ger kunden möjlighet att avsluta den beständiga sessionen och börja arbeta som gäst, eller logga in som en annan kund. Systemet sparar en förteckning över innehållet i kundvagnen, även om kunden senare använder olika enheter för att handla i din butik. En kund kan till exempel lägga till ett objekt i kundvagnen från en bärbar dator, lägga till fler objekt från en mobil enhet och slutföra utcheckningsprocessen från en surfplatta.

Det finns en separat, fristående, beständig cookie för varje webbläsare. Om kunden använder flera webbläsare samtidigt som han/hon besöker din butik under en och samma beständiga session, återspeglas ändringar som görs i en webbläsare i alla andra webbläsare när sidan uppdateras. Medan den beständiga kundvagnen är aktiverad skapar och underhåller din butik en separat beständig cookie för varje webbläsare som en kund använder för att logga in eller skapa ett konto.

### Exempel: En öppen session på en delad dator

Jane slutför sin semester med en ständig session. Hon tillför en present åt John i sin kundvagn, och något till sin mor. Sen går hon till köket för att ta en bit mat.

John sitter ner på datorn för att handla lite snabbt medan Jane är i köket. Utan att märka `Not Jane Smith?` överst på sidan hittar han en trevlig present åt Jane och lägger in den i kundvagnen. När han går till kassan och loggar in som sig själv läggs båda artiklarna i Jane kundvagn till i kundvagnen. John har så bråttom att han inte lägger märke till fler saker under _Beställningsgranskning_ och skickar beställningen. Jane kundvagn är nu tom, och John köpte alla presenter.

### Kom ihåg mig

Kunderna kan välja _Kom ihåg mig_ på inloggningssidan för att spara innehållet i kundvagnen.

| Kommer du ihåg mig? | Resultat |
| ------------ |  ------ |
| Markerad | Skapar en beständig cookie och sparar innehållet i kundvagnen för kundens nästa inloggade session. |
| Inte markerad | Skapar inte en beständig cookie och sparar inte kundvagnsinformationen för kundens nästa inloggade session. |

{style="table-layout:auto"}

### Fortsätt beständighet vid utloggning - nej

| Åtgärd | Resultat |
| ------ | ------ |
| Kundinloggning | Anropar den beständiga cookien utöver den sessionscookie som redan används. |
| Kundloggning | Tar bort sessionscookien, men den beständiga cookien är fortfarande aktiv. Nästa gång kunden loggar in återställs kundvagnsartiklarna eller läggs till i alla nya artiklar i vagnen. |
| Kunden loggar inte ut och sessionscookien förfaller | Den beständiga cookie-filen gäller fortfarande. |

{style="table-layout:auto"}

### Rensa beständighet vid utloggning

| Åtgärd | Resultat |
| ------ | ------ |
| Kundinloggning | Anropar den beständiga cookien utöver den sessionscookie som redan används. |
| Kundloggning | Tar bort båda cookies. |
| Kunden loggar inte ut, men sessions-cookien förfaller | Den beständiga cookie-filen gäller fortfarande. |

{style="table-layout:auto"}

## Beständiga kundvagnsinställningar och -effekter

| Inställningar | Effekt |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** är inställd på `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**har något värde.<br/><br/>The** Kom ihåg mig **kryssrutan inte är tillgänglig på inloggnings- och registreringssidan. | Den beständiga cookien används inte. |
| **[!UICONTROL Enable Remember Me]** är inställd på `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**har något värde.<br/><br/>** Kom ihåg mig **är inte markerat. | Sessionscookien används som vanligt. Den beständiga cookien används inte. |
| **[!UICONTROL Enable Remember Me]** är inställd på `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**är inställd på `Yes`.<br/><br/>** Kom ihåg mig **är inställd på `Yes`. | När en kund loggar in tillämpas båda cookies. När en kund loggar ut tas båda cookies bort. Om en kund inte loggar in men sessionscookien förfaller, används den beständiga cookien fortfarande. Förutom att logga ut tas den beständiga cookien bort när dess livstid tar slut eller när kunden klickar på `Not Jane Smith` länk. |
| **[!UICONTROL Enable Remember Me]** är inställd på `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**är inställd på `No`.<br/><br/>** Kom ihåg mig **är inställd på `Yes` | När en kund loggar in tillämpas båda cookies. När en kund loggar ut tas sessionscookien bort. Den beständiga sessionen fortsätter. Den beständiga cookien tas bort när dess livstid tar slut eller när kunden klickar på `Not Jane Smith` länk. |

{style="table-layout:auto"}

## Konfigurera en beständig kundvagn

Under konfigurationen av en beständig kundvagn kan du ange hur länge cookies ska användas och vilka alternativ du vill göra tillgängliga för olika kundaktiviteter.

Mer information om hur kundarbetsflödet bestäms av de här inställningarna finns i [Beständigt kundvagnsarbetsflöde](#persistent-cart-workflow).

>[!NOTE]
>
>Om sessionscookien upphör att gälla medan kunden är inloggad, förblir den beständiga cookien aktiv.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Persistent Shopping Cart]**.

1. Om du vill aktivera den beständiga kundvagnen och visa fler alternativ anger du **[!UICONTROL Enable Persistence]** till `Yes`.

   ![Aktivera och konfigurera kundvagnens beständighet](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Mer information om de här konfigurationsinställningarna finns i [_Konfigurationsreferens_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Rensa **[!UICONTROL Use system value]** om du vill ändra inställningarna.

1. För **[!UICONTROL Persistence Lifetime (seconds)]** anger du hur länge (i sekunder) som den beständiga cookien ska vara.

   Standardvärdet 31 536 000 sekunder är lika med ett år. Den högsta tillåtna tiden är 100 år.

1. Ange **[!UICONTROL Enable "Remember Me"]** till något av följande:

   - `Yes` - Visar _Kom ihåg mig_ kryssrutan på inloggningssidan i din butik, så att kunderna kan välja att spara sin kundvagnsinformation.

   - `No` - Upprepande kan fortfarande aktiveras, men kunderna kan inte välja om de vill spara sin information.

1. Om du vill förmarkera _Kom ihåg mig_ kryssruta för kunden, ange **[!UICONTROL Remember Me Default Value]** till `Yes`.

   Kunden kan rensa det här alternativet om han eller hon vill.

1. Ange **[!UICONTROL Clear Persistence on Log Out]** till något av följande:

   - `Yes` - Kundvagnen raderas när en registrerad kund loggar ut.

   - `No` - Kundvagnen sparas när en registrerad kund loggar ut.

   >[!NOTE]
   >
   >Om sessionscookien upphör att gälla medan kunden fortfarande är inloggad, används den beständiga cookien.

1. Ange **[!UICONTROL Persist Shopping Cart]** till något av följande:

   - `Yes` - Om sessionscookien går ut bevaras den beständiga cookien. Om en gästkund loggar in eller skapar ett konto senare återställs kundvagnen.

   - `No` - Kundvagnen bevaras inte för gäster efter att sessionscookien har upphört att gälla.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Persist Wish List]** för att avgöra om kundens önskelistor behålls när sessionen avslutas:

   - `Yes` - Innehållet i önskelistan sparas när sessionen avslutas.

   - `No` - Önsterlistan sparas inte när sessionen avslutas.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Persist Recently Ordered Items]** för att avgöra om tillståndet för nyligen beställda objekt behålls när sessionen avslutas:

   - `Yes` - Tillståndet för nyligen beställda objekt sparas när sessionen avslutas.

   - `No` - Tillståndet för nyligen beställda objekt sparas inte när sessionen avslutas.

1. Ange **[!UICONTROL Persist Currently Compared Products]** till `Yes` eller `No`.

1. Ange **[!UICONTROL Persist Comparison History]** till `Yes` eller `No`.

1. Ange **[!UICONTROL Persist Recently Viewed Products]** till `Yes` eller `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Persist Customer Group Membership and Segmentation]** för att avgöra om statusen för kundens gruppmedlemskap och segmenteringskriterier behålls när sessionen avslutas:

   - `Yes` - Status för kundens gruppmedlemskap och segmenteringsdata sparas när sessionen avslutas.

   - `No` - Tillståndet för kundens gruppmedlemskap och segmenteringsdata sparas inte när sessionen avslutas.

1. Klicka på **[!UICONTROL Save Config]**.
