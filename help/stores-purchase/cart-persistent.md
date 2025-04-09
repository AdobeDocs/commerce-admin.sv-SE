---
title: Kartbeständighet
description: Lär dig hur en beständig kundvagn spårar oköpta varukorgsartiklar och sparar informationen för kundens nästa besök.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: a6cfcbb5774c0bafc3b7e7c96881329bde837837
workflow-type: tm+mt
source-wordcount: '1038'
ht-degree: 0%

---

# Kartbeständighet

En beständig kundvagn sparar en referens till kundens konto på den aktuella enheten och ser till att kundvagnens innehåll förblir tillgängligt när den inloggade sessionen går ut.

Om en kund är _ihågkommen_ är innehållet i kundvagnen tillgängligt på den aktuella enheten när den inloggade sessionen går ut. När sessionen är slut öppnas kundens kundvagn via den beständiga kundvagnssessionen. Om samma kund loggar in på en annan enhet eller webbläsare och lägger till något i kundvagnen, och sedan återgår till enheten med en aktiv beständig session, uppdateras kundvagnen med de tillagda artiklarna.

Om du använder en konstant kundvagn kan du minska antalet övergivna kundvagnar och öka försäljningen. Den beständiga kundvagnen **visar inte** känslig kontoinformation när som helst.

Om du vill hantera användningen av kundvagnsbeständighet för din webbplats eller inom specifika butiksvyer kan du [konfigurera beständiga inställningar för kundvagn](#configure-a-persistent-cart). Mer information om hur de här inställningarna påverkar shoppingupplevelsen i butiken finns i [Konsekvent kundvagnsarbetsflöde](#persistent-cart-workflow).

>[!NOTE]
>
>Den beständiga kundvagnsfunktionen är endast tillgänglig för kunder som är registrerade och inloggade. Gästkunder kan inte använda den beständiga kundvagnsfunktionen.

## Beständigt kundvagnsarbetsflöde

När den beständiga kundvagnen är [aktiverad](#configure-a-persistent-cart) beror arbetsflödet på:

- Värdena för inställningarna _[!UICONTROL Enable Remember Me]_och_[!UICONTROL Clear Persistence on Log Out]_
- Kundens beslut att markera eller avmarkera kryssrutan _[!UICONTROL Remember Me]_
- När den beständiga cookien rensas

När kundsessionen förfaller visas en `Not Jane Smith?`-länk i sidhuvudet under följande villkor:
- den inloggade kunden har valt alternativet _[!UICONTROL Remember Me]_och en beständig cookie används
- kunden loggar ut när systemet har konfigurerats med _[!UICONTROL Clear Persistence on Sign Out]_inställt på `No`.

Systemet sparar en post med kundvagnsinnehållet på den aktuella enheten, även om den inloggade sessionen går ut. Med länken `Not Jane Smith?` kan kunden avsluta den beständiga sessionen och börja arbeta som gäst, eller logga in som en annan eller samma kund.

Om kunden markerade kryssrutan _[!UICONTROL Remember Me]_när han loggade in skapar och underhåller din butik en separat beständig cookie. Denna cookie hjälper kunden att hålla kundens kundvagn tillgänglig även när de har stängt webbläsaren eller navigerat till en annan webbplats och den inloggade sessionen förfaller.

Om samma kund besöker din butik via flera webbläsare medan han/hon är inloggad eller medan en beständig session är aktiv, återspeglas kundens ändringar i kundvagnsinnehållet i en webbläsare i andra webbläsare när sidan uppdateras.

>[!NOTE]
>
>För att säkerställa kundvagnssynkronisering på flera enheter eller webbläsare måste kunderna logga in på varje ny enhet de använder för att handla. För inloggade kunder synkroniseras innehållet i kundvagnen mellan flera enheter och webbläsare så länge de är inloggade under samma konto, oavsett konfiguration av beständig kundvagn.

### Beteende för kryssrutan &quot;Kom ihåg mig&quot;

Kunderna kan markera kryssrutan _[!UICONTROL Remember Me]_på inloggningssidan, autentiserings-popup, utcheckning av inloggningar eller när de skapar ett nytt konto för att hålla innehållet i kundvagnen tillgängligt på den aktuella enheten när den inloggade sessionen förfaller.

| Kommer du ihåg mig? | Resultat |
| ------------ |  ------ |
| Markerad | Skapar en beständig cookie och håller innehållet i kundvagnen tillgängligt på den aktuella enheten när kundinloggningssessionen går ut. |
| Inte markerad | Skapar inte en beständig cookie och innehållet i kundvagnen är inte tillgängligt på den aktuella enheten när inloggningssessionen går ut. Observera att kundvagnens innehåll fortfarande sparas på kundens konto och läses in igen nästa gång kunden loggar in. |

{style="table-layout:auto"}

![Kom ihåg min kundinloggning](./assets/remember-me-customer-login.png){width="600" zoomable="yes"}
![Kom ihåg min autentisering-popup](./assets/remember-me-authentication-pop-up.png){width="600" zoomable="yes"}
![Kom ihåg mig när jag checkar ut inloggningar](./assets/remember-me-checkout-sign-ins.png){width="600" zoomable="yes"}

### beteendet Rensa persistens vid utloggning

När kunden loggar in eller registrerar med alternativet _Kom ihåg mig_ markerat avgör konfigurationen för alternativet _Rensa beständighet vid utloggning_ beteendet för beständig kundvagn.

|  | Rensa beständighet vid utloggning inställd på Ja | Clear Persistence on Sign Out set to No |
| ------ | ------ | ------ |
| _Kommentarer_ kund loggar ut | Tar bort både session och beständiga cookies så att kundvagnens innehåll försvinner på den aktuella enheten tills samma kund loggar in igen. | Tar bort sessionscookien, men den beständiga cookien är fortfarande aktiv. Kundvagnens innehåll är fortfarande tillgängligt på den aktuella enheten. |
| _Kund med minnen_ loggar inte ut, men sessionscookien upphör att gälla | Den beständiga cookie-filen är fortfarande aktiv och kundvagnsinnehållet är tillgängligt från den aktuella enheten. | Den beständiga cookie-filen är fortfarande aktiv och kundvagnsinnehållet är tillgängligt från den aktuella enheten. |

### Ett exempel på en öppen session på en delad dator

Jane slutför sin semesterbutik som en _påminnelse_ inloggad kund. Hon tillför en present åt John i sin kundvagn, och något till sin mor. Sedan går hon till köket för en bit mat och inloggningen går ut.

John sitter ner på datorn för att handla lite snabbt medan Jane är i köket. Utan att märka länken `Not Jane Smith?` överst på sidan hittar John en trevlig present åt Jane och lägger till den i kundvagnen. När han checkar ut ser han att leverans- och faktureringsadresserna är förifyllda och tror att han är inloggad. John har så bråttom att han inte lägger märke till ytterligare objekt under _ordergranskningen_ och skickar ordern. Jane kundvagn är nu tom, och John köpte alla presenter.

## Konfigurera en beständig kundvagn

Under konfigurationen av en beständig kundvagn kan du ange hur länge cookies ska användas och vilka alternativ du vill göra tillgängliga för olika kundaktiviteter.

Om du vill använda den beständiga kundvagnen måste kundens webbläsare vara inställd på att tillåta cookies. Det finns två typer av cookies som används för kundvagnsåtgärder:

- **Sessionscookie** - En sessionscookie finns under ett enda besök på webbplatsen. Denna cookie upphör att gälla när kunden loggar ut eller när sessionen upphör.

- **Beständig cookie** - En långvarig, beständig cookie finns fortfarande när den inloggade sessionen har avslutats. Denna cookie säkerställer att innehållet i kundens kundvagn förblir tillgängligt när kunden loggar ut eller sessionen förfaller.

Mer information om hur de här konfigurationsinställningarna påverkar kundarbetsflödet finns i [Konsekvent kundvagnsarbetsflöde](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
