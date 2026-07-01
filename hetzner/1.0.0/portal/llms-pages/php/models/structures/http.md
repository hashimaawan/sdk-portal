# Http

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkh0dHA

Additional configuration for protocol http


# Class Name

`Http`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `domain` | `?string` | Required | Host header to send in the HTTP request. May not contain spaces, percent or backslash symbols. Can be null, in that case no host header is sent. | getDomain(): ?string | setDomain(?string domain): void |
| `path` | `string` | Required | HTTP path to use for health checks. May not contain literal spaces, use percent-encoding instead. | getPath(): string | setPath(string path): void |
| `response` | `?string` | Optional | String that must be contained in HTTP response in order to pass the health check | getResponse(): ?string | setResponse(?string response): void |
| `statusCodes` | `?(string[])` | Optional | List of returned HTTP status codes in order to pass the health check. Supports the wildcards `?` for exactly one character and `*` for multiple ones. The default is to pass the health check for any status code between 2?? and 3??. | getStatusCodes(): ?array | setStatusCodes(?array statusCodes): void |
| `tls` | `?bool` | Optional | Use HTTPS for health check | getTls(): ?bool | setTls(?bool tls): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\HttpBuilder;

$http = HttpBuilder::init(
    '/'
)
    ->domain('example.com')
    ->response('{"status": "ok"}')
    ->statusCodes(
        [
            '2??',
            '3??'
        ]
    )
    ->tls(false)
    ->build();
```



