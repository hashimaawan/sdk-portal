# V2 Registry Docker Credentials Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRG9ja2VyJTI1MjBDcmVkZW50aWFscyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2RegistryDockerCredentialsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `auths` | [`?Auths`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/auths.md) | Optional | - | getAuths(): ?Auths | setAuths(?Auths auths): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2RegistryDockerCredentialsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\AuthsBuilder;
use DigitalOceanApiLib\Models\Builders\RegistryDigitaloceanComBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2RegistryDockerCredentialsResponse = V2RegistryDockerCredentialsResponseBuilder::init()
    ->auths(
        AuthsBuilder::init()
            ->registryDigitaloceanCom(
                RegistryDigitaloceanComBuilder::init()
                    ->auth('auth0')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



