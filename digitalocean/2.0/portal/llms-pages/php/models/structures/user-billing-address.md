# User Billing Address

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlVzZXJCaWxsaW5nQWRkcmVzcw

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`UserBillingAddress`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `addressLine1` | `?string` | Optional | Street address line 1 | getAddressLine1(): ?string | setAddressLine1(?string addressLine1): void |
| `addressLine2` | `?string` | Optional | Street address line 2 | getAddressLine2(): ?string | setAddressLine2(?string addressLine2): void |
| `city` | `?string` | Optional | City | getCity(): ?string | setCity(?string city): void |
| `countryIso2Code` | `?string` | Optional | Country (ISO2) code | getCountryIso2Code(): ?string | setCountryIso2Code(?string countryIso2Code): void |
| `createdAt` | `?string` | Optional | Timestamp billing address was created | getCreatedAt(): ?string | setCreatedAt(?string createdAt): void |
| `postalCode` | `?string` | Optional | Postal code | getPostalCode(): ?string | setPostalCode(?string postalCode): void |
| `region` | `?string` | Optional | Region | getRegion(): ?string | setRegion(?string region): void |
| `updatedAt` | `?string` | Optional | Timestamp billing address was updated | getUpdatedAt(): ?string | setUpdatedAt(?string updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\UserBillingAddressBuilder;
use DigitalOceanApiLib\ApiHelper;

$userBillingAddress = UserBillingAddressBuilder::init()
    ->addressLine1('101 Shark Row')
    ->addressLine2('address_line24')
    ->city('Atlantis')
    ->countryIso2Code('US')
    ->createdAt('2019-09-03T16:34:46.000+00:00')
    ->postalCode('12345')
    ->region('OC')
    ->updatedAt('2019-09-03T16:34:46.000+00:00')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



