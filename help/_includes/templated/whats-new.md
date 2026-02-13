---
source-git-commit: 78d6e7fa263246e8fa52aa0386b35e4bb39553ad
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---
# Ny mall

## Nyheter

Det här avsnittet innehåller de ändringar som har gjorts under de senaste 60 dagarna. Vi utelämnar alla mindre uppdateringar, som kopieringsredigering, från den här listan.

### 10 februari 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Beskrivning</th>
      <th>Typ</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Uppdateringar av administratörsdokumentationen för februari-utgåvan av Adobe Commerce as a Cloud Service:<br />- Dokumentationen för <a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/order-management/invoices#custom-capture-amounts">anpassade fångstbelopp</a> har lagts till när fakturor skapas i REST API, som gör att handlare kan samla in anpassade belopp när de skapar fakturor för partiella hämtningar och specialiserade betalningsscenarier.<br />- Anger vilka rapporter på <a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/start/reporting/reports-menu">Rapporter-menyn</a> som nu endast är PaaS.</p>
</td>
      <td>
        Viktig uppdatering
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/0c602db5a7291b95d725bce59df53923490d6b96">bekräfta</a></td>
    </tr>
  </tbody>
</table>

### 2 februari 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Beskrivning</th>
      <th>Typ</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p><a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law">Kompatibilitet med cookies</a> har uppdaterats för att lägga till den saknade <code class="language-plaintext highlighter-rouge">mage-cache-timeout</code> localStorage-nyckeln och konvertera listan över undantagna cookies till ett tabellformat.</p>
</td>
      <td>
        Teknik, feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/ebb6348c6b5a30f5de4025f39bae0061b397a4b9">bekräfta</a></td>
    </tr>
    <tr>
      <td><p>[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Uppdaterade förutsättningarna för att konfigurera IMS-integreringen för Adobe Commerce för att ge information om hur du begär åtkomst till Adobe Admin Console.</p>
</td>
      <td>
        Teknik, feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/8ea546c5e1cc9296c8b056ea7e25984a66d43851">bekräfta</a></td>
    </tr>
  </tbody>
</table>

### 31 januari 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Beskrivning</th>
      <th>Typ</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p><a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-groups">Kundgrupperna</a> i kundhanteringshandboken har uppdaterats för att klargöra att administratörsanvändare inte kan redigera en kunds kundgrupp efter att kunden har tilldelats ett företag.</p>
</td>
      <td>
        Teknisk
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.sv-SE/pull/81">pull-förfrågan</a></td>
    </tr>
  </tbody>
</table>

### 20 januari 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Beskrivning</th>
      <th>Typ</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Ändrade produktreferenser från"Adobe Sensei" till"Adobe AI" för att återspegla Adobe varumärkesuppdateringar.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/4077b922dae0ed9a9050a5f6160143a636646daa">bekräfta</a></td>
    </tr>
  </tbody>
</table>

### 16 januari 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Beskrivning</th>
      <th>Typ</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Lagt till förtydligande när <a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/config/sales/sales-emails#order-ready-for-pickup-in-store">e-postmeddelanden om beställning klar för hämtning finns tillgängliga i Store</a>.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/65fd67dcd3c14daddfc0f36493dc6da3630898a1">bekräfta</a></td>
    </tr>
  </tbody>
</table>

### 15 januari 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Beskrivning</th>
      <th>Typ</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Följande funktioner har lagts till i Adobe Commerce as a Cloud Service:<br />- Stöd har lagts till för <a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/systems/security/captcha/security-google-recaptcha-enterprise">Google reCAPTCHA Enterprise</a> som ger avancerat robotskydd med adaptiv riskanalys och maskininlärningsfunktioner.<br />- Omvandla försändelsspårningsnummer som finns i e-postmeddelanden från oformaterad text till klickbara länkar genom att <a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/delivery/shipping-settings#shipment-tracking-urls">aktivera URL:er för anpassad spårning</a>. Den här funktionen stöds för USPS, UPS, FedEx och DHL.<br /> - Du kan nu kombinera rabatter för nivåindelad prissättning med katalogregelrabatter med hjälp av <a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/products/pricing/product-price-tier#enable-tier-pricing-for-catalog-price-rules">katalogprisregler</a>. Tack vare den här förbättringen kan ni skapa mer dynamiska och konkurrenskraftiga prissättningsstrategier.</p>
</td>
      <td>
        Viktig uppdatering, nytt ämne
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/70e73b47c4b0342ade3deab64dbe39f29b82191f">bekräfta</a></td>
    </tr>
  </tbody>
</table>

### 17 december 2025

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Beskrivning</th>
      <th>Typ</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p><a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty">Avsnittet </a> om belöningar och lojalitet har uppdaterats för att klargöra hur momsen beräknas när kunderna använder belöningspoäng eller butikskrediter under utcheckningen.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/1154cd5ced746ac6dfd609946528f281774bbaaa">bekräfta</a></td>
    </tr>
  </tbody>
</table>
