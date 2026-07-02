# Cors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNvcnM

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Cors`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `allowCredentials` | `?bool` | Optional | Whether browsers should expose the response to the client-side JavaScript code when the request’s credentials mode is include. This configures the `Access-Control-Allow-Credentials` header. | getAllowCredentials(): ?bool | setAllowCredentials(?bool allowCredentials): void |
| `allowHeaders` | `?(string[])` | Optional | The set of allowed HTTP request headers. This configures the `Access-Control-Allow-Headers` header. | getAllowHeaders(): ?array | setAllowHeaders(?array allowHeaders): void |
| `allowMethods` | `?(string[])` | Optional | The set of allowed HTTP methods. This configures the `Access-Control-Allow-Methods` header. | getAllowMethods(): ?array | setAllowMethods(?array allowMethods): void |
| `allowOrigins` | [`?(AllowOrigin[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/allow-origin.md) | Optional | The set of allowed CORS origins. | getAllowOrigins(): ?array | setAllowOrigins(?array allowOrigins): void |
| `exposeHeaders` | `?(string[])` | Optional | The set of HTTP response headers that browsers are allowed to access. This configures the `Access-Control-Expose-Headers` header. | getExposeHeaders(): ?array | setExposeHeaders(?array exposeHeaders): void |
| `maxAge` | `?string` | Optional | An optional duration specifying how long browsers can cache the results of a preflight request. This configures the `Access-Control-Max-Age` header. | getMaxAge(): ?string | setMaxAge(?string maxAge): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\CorsBuilder;
use DigitalOceanApiLib\Models\Builders\AllowOriginBuilder;
use DigitalOceanApiLib\ApiHelper;

$cors = CorsBuilder::init()
    ->allowCredentials(false)
    ->allowHeaders(
        [
            'Content-Type',
            'X-Custom-Header'
        ]
    )
    ->allowMethods(
        [
            'GET',
            'OPTIONS',
            'POST',
            'PUT',
            'PATCH',
            'DELETE'
        ]
    )
    ->allowOrigins(
        [
            AllowOriginBuilder::init()
                ->exact('https://www.example.com')
                ->prefix('prefix6')
                ->regex('regex4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            AllowOriginBuilder::init()
                ->exact('exact8')
                ->prefix('prefix6')
                ->regex('^.*example.com')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->exposeHeaders(
        [
            'Content-Encoding',
            'X-Custom-Header'
        ]
    )
    ->maxAge('5h30m')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



