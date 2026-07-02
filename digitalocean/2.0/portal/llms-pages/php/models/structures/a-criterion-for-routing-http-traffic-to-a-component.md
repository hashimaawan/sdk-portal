# A Criterion for Routing HTTP Traffic to a Component

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkElMjUyMGNyaXRlcmlvbiUyNTIwZm9yJTI1MjByb3V0aW5nJTI1MjBIVFRQJTI1MjB0cmFmZmljJTI1MjB0byUyNTIwYSUyNTIwY29tcG9uZW50Lg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ACriterionForRoutingHttpTrafficToAComponent`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `path` | `?string` | Optional | An HTTP path prefix. Paths must start with / and must be unique across all components within an app. | getPath(): ?string | setPath(?string path): void |
| `preservePathPrefix` | `?bool` | Optional | An optional flag to preserve the path that is forwarded to the backend service. By default, the HTTP request path will be trimmed from the left when forwarded to the component. For example, a component with `path=/api` will have requests to `/api/list` trimmed to `/list`. If this value is `true`, the path will remain `/api/list`. | getPreservePathPrefix(): ?bool | setPreservePathPrefix(?bool preservePathPrefix): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ACriterionForRoutingHttpTrafficToAComponentBuilder;
use DigitalOceanApiLib\ApiHelper;

$aCriterionForRoutingHttpTrafficToAComponent = ACriterionForRoutingHttpTrafficToAComponentBuilder::init()
    ->path('/api')
    ->preservePathPrefix(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



