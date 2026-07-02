# Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkhlYWx0aENoZWNr

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`HealthCheck`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `failureThreshold` | `?int` | Optional | The number of failed health checks before considered unhealthy. | getFailureThreshold(): ?int | setFailureThreshold(?int failureThreshold): void |
| `httpPath` | `?string` | Optional | The route path used for the HTTP health check ping. If not set, the HTTP health check will be disabled and a TCP health check used instead. | getHttpPath(): ?string | setHttpPath(?string httpPath): void |
| `initialDelaySeconds` | `?int` | Optional | The number of seconds to wait before beginning health checks. | getInitialDelaySeconds(): ?int | setInitialDelaySeconds(?int initialDelaySeconds): void |
| `periodSeconds` | `?int` | Optional | The number of seconds to wait between health checks. | getPeriodSeconds(): ?int | setPeriodSeconds(?int periodSeconds): void |
| `port` | `?int` | Optional | The port on which the health check will be performed. If not set, the health check will be performed on the component's http_port.<br><br>**Constraints**: `>= 1`, `<= 65535` | getPort(): ?int | setPort(?int port): void |
| `successThreshold` | `?int` | Optional | The number of successful health checks before considered healthy. | getSuccessThreshold(): ?int | setSuccessThreshold(?int successThreshold): void |
| `timeoutSeconds` | `?int` | Optional | The number of seconds after which the check times out. | getTimeoutSeconds(): ?int | setTimeoutSeconds(?int timeoutSeconds): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\HealthCheckBuilder;
use DigitalOceanApiLib\ApiHelper;

$healthCheck = HealthCheckBuilder::init()
    ->failureThreshold(2)
    ->httpPath('/health')
    ->initialDelaySeconds(30)
    ->periodSeconds(60)
    ->port(80)
    ->successThreshold(3)
    ->timeoutSeconds(45)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



