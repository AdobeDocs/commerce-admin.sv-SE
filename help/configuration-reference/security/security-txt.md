---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Granska konfigurationsinställningarna på [!UICONTROL Security] &gt; [!UICONTROL Security.txt] sidan för Commerce Admin.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Mer information om hur du ändrar dessa konfigurationsinställningar finns i [Rapportering av säkerhetsproblem](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![Allmänt](./assets/txt-general.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable] | Webbplats | När det här alternativet är aktiverat `security.txt` filen sparas och innehåller information som krävs av säkerhetsforskare för att rapportera potentiella säkerhetsluckor till dig. Alternativ:<br />**`Yes`**- Skapar `security.txt` fil baserad på information som anges i _Kontaktinformation_ och _Annan information_ -avsnitt.<br />**`No`** - (standard) Skapar inte `security.txt` -fil. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Contact information]

![Kontaktinformation](./assets/txt-contact-info.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email] | Webbplats | E-postadressen dit säkerhetsrapporter kan skickas. |
| [!UICONTROL Phone] | Webbplats | Ett telefonnummer som kan användas för att rapportera säkerhetsproblem. |
| [!UICONTROL Contact Page] | Webbplats | URL-adressen till en sida på din webbplats som innehåller en lista över säkerhetskontakter eller _Kontakta oss_ sida. Exempel: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Other information]

![Annan information](./assets/txt-other-info.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Encryption] | Webbplats | En URL som pekar på platsen för en krypteringsnyckel som säkerhetsforskare kan använda för att skicka krypterad kommunikation. _**Ange inte krypteringsnyckeln i det här fältet.**_ <br/><br/>Det är forskarens ansvar att verifiera att nyckeln kommer från en tillförlitlig källa. Forskaren får inte anta att nyckeln är densamma som den som användes för att generera den digitala signaturen. Exempel:<br />OpenPGP-nyckel från webbserver - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Webbplats | En URL som pekar på en sida i din butik där säkerhetsforskare erkänns, t.ex.`https://mystore.com/hall-of-fame.html`. För att förhindra framtida attacker bör du bara ta med en allmän beskrivning utan att visa specifik information om sårbarhetsproblem. Exempel:<br />Vi vill tacka följande forskare:<br />(åååå/mm/dd) Justin Thyme - SQL-injektion |
| [!UICONTROL Preferred Languages] | Webbplats | Anger minst ett rekommenderat säkerhetsrapporteringsspråk. Separera flera två tecken [språkkoder](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) med komma. Alla angivna språk har samma prioritet. Om du till exempel vill ange engelska, spanska och franska anger du `en, es, fr`. |
| [!UICONTROL Hiring] | Webbplats | URL-adressen till en sida på webbplatsen som listar säkerhetsrelaterade jobbpositioner. Exempel: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Webbplats | URL:en till sidan som beskriver din säkerhetspolicy och rutiner för rapportering av säkerhetsluckor. Exempel: `https://mystore.com/security-reporting.html` Standard: `https://mystore.com/security` |
| [!UICONTROL Signature] | Webbplats | En länk till din digitala signaturfil. Den digitala signaturen måste genereras från kommandoraden och sparas i `.well-known` på servern. Mer information finns i [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) på GitHub. Exempel: `https://mystore.com/.well-known/security.txt.sig` |

{:style=&quot;table-layout:auto&quot;}
