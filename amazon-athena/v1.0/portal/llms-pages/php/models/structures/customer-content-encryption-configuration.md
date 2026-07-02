# Customer Content Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkN1c3RvbWVyQ29udGVudEVuY3J5cHRpb25Db25maWd1cmF0aW9u

Specifies the KMS key that is used to encrypt the user's data stores in Athena.


# Class Name

`CustomerContentEncryptionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `kmsKey` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:key/?[a-zA-Z_0-9+=,.@\-_/]+$\|^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:alias/?[a-zA-Z_0-9+=,.@\-_/]+$\|^alias/[a-zA-Z0-9/_-]+$\|[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | getKmsKey(): string | setKmsKey(string kmsKey): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CustomerContentEncryptionConfigurationBuilder;

$customerContentEncryptionConfiguration = CustomerContentEncryptionConfigurationBuilder::init(
    'KmsKey2'
)->build();
```



