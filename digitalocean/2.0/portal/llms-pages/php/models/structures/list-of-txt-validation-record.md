# List of TXT Validation Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3QlMjUyMG9mJTI1MjBUWFQlMjUyMHZhbGlkYXRpb24lMjUyMHJlY29yZA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ListOfTxtValidationRecord`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `txtName` | `?string` | Optional, Read-only | - | getTxtName(): ?string | setTxtName(?string txtName): void |
| `txtValue` | `?string` | Optional, Read-only | - | getTxtValue(): ?string | setTxtValue(?string txtValue): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ListOfTxtValidationRecordBuilder;
use DigitalOceanApiLib\ApiHelper;

$listOfTxtValidationRecord = ListOfTxtValidationRecordBuilder::init()
    ->txtName('_acme-challenge.app.example.com')
    ->txtValue('lXLOcN6cPv0nproViNcUHcahD9TrIPlNgdwesj0pYpk')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



