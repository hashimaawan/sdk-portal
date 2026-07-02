# V2 Cdn Endpoints Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2CdnEndpointsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificateId` | `?string` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. | getCertificateId(): ?string | setCertificateId(?string certificateId): void |
| `customDomain` | `?string` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. | getCustomDomain(): ?string | setCustomDomain(?string customDomain): void |
| `ttl` | [`?int(Ttl)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl::ENUM_3600` | getTtl(): ?int | setTtl(?int ttl): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2CdnEndpointsRequestBuilder;
use DigitalOceanApiLib\Models\Ttl;
use DigitalOceanApiLib\ApiHelper;

$v2CdnEndpointsRequest = V2CdnEndpointsRequestBuilder::init()
    ->certificateId('892071a0-bb95-49bc-8021-3afd67a210bf')
    ->customDomain('static.example.com')
    ->ttl(Ttl::ENUM_3600)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



