---
title: Presentregister
description: Läs om hur presentregistren kan marknadsföra försäljningen när kunderna kan bjuda in släkt och vänner att köpa de produkter de valt som gåvor.
exl-id: 2e5e3d52-e93e-444c-88a1-1eaa7f178b99
feature: Marketing Tools, Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Presentregister

{{ee-feature}}

Adobe Commerce ger dina kunder möjlighet att skapa presentregister för särskilda tillfällen och bjuda in vänner och familj att köpa gåvor från presentregistret. Adobe Commerce håller reda på vilka artiklar som köpts och vilka kvantiteter som återstår.

![Exempel på storefront - presentregister för spädbarn](./assets/storefront-gift-registry-create-baby-info.png){width="700" zoomable="yes"}

Presentregisterägaren kan lägga till produkter i registret från sin [kundöversikt](gift-registry-storefront.md#gift-registry-information). Dessutom kan produkterna överföras från önskelistan eller kundvagnen. Som butiksadministratör kan du visa och dela kundpresentregister. Du kan också utföra underhåll, till exempel lägga till artiklar från kundvagnen, uppdatera kvantiteter eller ta bort ett presentregister.

Om du vill få åtkomst till ett presentregister kan mottagarna klicka på länken i det e-postmeddelande de får eller söka efter mottagarens namn, e-postadress eller presentregisterns-ID. I de flesta butiker har sidfoten på varje sida en länk till presentregistret, men platsen kan variera beroende på tema. Dessutom är [Widget](../content-design/widgets.md) kan användas för att montera [Presentregistersökning](gift-registry-search.md) var som helst i din butik.

Registreringsbesökare som vill göra ett köp kan lägga till artikeln i sina kundvagnar direkt från presentregistret. När ordern läggs uppdateras presentregistret så att köpet återspeglas.

## Arbetsflöde för presentregister

1. **Konfigurera presentregistret för butiken**. Butiksadministratören [aktiverar presentregistret](gift-registry-configure.md)och [anger registertyp och attribut](gift-registry-create.md).

1. **Kunden skapar ett eget register**. A [kund skapar ett presentregister](gift-registry-storefront.md#create-a-new-gift-registry) från sitt butikskonto för ett kommande tillfälle och fyller i de obligatoriska fälten i varje avsnitt i presentregistret. När du har lagt till objekt i registret kan det delas med vänner och familj.

1. **Kunden delar sitt register**. En länk till presentregistret finns i varje [inbjudan](gift-registry-storefront.md#share-a-gift-registry). If [Presentregistersökning](gift-registry-search.md) är tillgängligt i butiken, kan kunderna söka efter specifika presentregister efter namn, e-postadress eller presentregister-ID.

1. **Mottagarna av inbjudan lägger order**. Den som får en inbjudan eller information om registret kan lägga en order på valfritt objekt direkt från presentregistret. När artiklar säljs uppdaterar Adobe Commerce antalet i presentregistret och meddelar presentregisterägaren.
