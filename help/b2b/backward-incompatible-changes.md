---
title: Adobe Commerce B2B-ändringar som inte är kompatibla bakåt
description: Läs om ändringar i Adobe Commerce B2B-utgåvor som kan kräva att du uppdaterar din anpassade kod.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Adobe Commerce B2B-ändringar som inte är kompatibla bakåt

Granska den övergripande referensinformationen för alla bakåtkompatibla ändringar i B2B-utgåvor av Adobe Commerce. I avsnittet med högdagrar finns information om inkompatibla ändringar som har stor effekt och som kräver detaljerade förklaringar och specialinstruktioner.

## Högdagrar

### 1.4.2 till 1.5.0

Med den här typen av företagstilldelning kan företagsanvändarkonton nu ha flera `company_id`-värden. `Magento\Company\Api\Data\CompanyCustomerInterface` uppdaterades för att ange standardvärdet `company_id` för en användare. Standardvärdet är det första företaget som tilldelats företagsanvändarkontot.

Om du uppgraderar från en tidigare version rekommenderar Adobe att du implementerar följande metoder i klasser som använder `Magento\Company\Api\Data\CompanyCustomerInterface`.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Referens

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
