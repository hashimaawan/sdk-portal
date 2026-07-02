# V2 Cdn Endpoints Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2CdnEndpointsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `endpoint` | [`?Endpoint`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/endpoint.md) | Optional | - | getEndpoint(): ?Endpoint | setEndpoint(?Endpoint endpoint): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2CdnEndpointsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\EndpointBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$v2CdnEndpointsResponse1 = V2CdnEndpointsResponse1Builder::init()
    ->endpoint(
        EndpointBuilder::init(
            'origin2'
        )
            ->certificateId('00001b94-0000-0000-0000-000000000000')
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->customDomain('custom_domain6')
            ->endpoint('endpoint6')
            ->id('00001f7a-0000-0000-0000-000000000000')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



