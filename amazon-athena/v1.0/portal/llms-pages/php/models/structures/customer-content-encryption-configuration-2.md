# Customer Content Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkN1c3RvbWVyQ29udGVudEVuY3J5cHRpb25Db25maWd1cmF0aW9uMg

*This model accepts additional fields of type array.*


# Class Name

`CustomerContentEncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `kmsKey` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:key/?[a-zA-Z_0-9+=,.@\-_/]+$\|^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:alias/?[a-zA-Z_0-9+=,.@\-_/]+$\|^alias/[a-zA-Z0-9/_-]+$\|[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getKmsKey(): string | setKmsKey(string kmsKey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CustomerContentEncryptionConfiguration2Builder;
use AmazonAthenaLib\ApiHelper;

$customerContentEncryptionConfiguration2 = CustomerContentEncryptionConfiguration2Builder::init(
    'KmsKey4'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



