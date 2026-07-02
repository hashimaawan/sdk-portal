# Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkVuZHBvaW50

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Endpoint`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificateId` | `?string` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. | getCertificateId(): ?string | setCertificateId(?string certificateId): void |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the CDN endpoint was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `customDomain` | `?string` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. | getCustomDomain(): ?string | setCustomDomain(?string customDomain): void |
| `endpoint` | `?string` | Optional, Read-only | The fully qualified domain name (FQDN) from which the CDN-backed content is served. | getEndpoint(): ?string | setEndpoint(?string endpoint): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a CDN endpoint. | getId(): ?string | setId(?string id): void |
| `origin` | `string` | Required | The fully qualified domain name (FQDN) for the origin server which provides the content for the CDN. This is currently restricted to a Space. | getOrigin(): string | setOrigin(string origin): void |
| `ttl` | [`?int(Ttl)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl::ENUM_3600` | getTtl(): ?int | setTtl(?int ttl): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\EndpointBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Ttl;
use DigitalOceanApiLib\ApiHelper;

$endpoint = EndpointBuilder::init(
    'static-images.nyc3.digitaloceanspaces.com'
)
    ->certificateId('892071a0-bb95-49bc-8021-3afd67a210bf')
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-03-21T16:02:37Z'))
    ->customDomain('static.example.com')
    ->endpoint('static-images.nyc3.cdn.digitaloceanspaces.com')
    ->id('892071a0-bb95-49bc-8021-3afd67a210bf')
    ->ttl(Ttl::ENUM_3600)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



