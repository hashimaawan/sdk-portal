# Health Check 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkhlYWx0aENoZWNrMQ

An object specifying health check settings for the load balancer.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`HealthCheck1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `checkIntervalSeconds` | `?int` | Optional | The number of seconds between between two consecutive health checks.<br><br>**Default**: `10` | getCheckIntervalSeconds(): ?int | setCheckIntervalSeconds(?int checkIntervalSeconds): void |
| `healthyThreshold` | `?int` | Optional | The number of times a health check must pass for a backend Droplet to be marked "healthy" and be re-added to the pool.<br><br>**Default**: `3` | getHealthyThreshold(): ?int | setHealthyThreshold(?int healthyThreshold): void |
| `path` | `?string` | Optional | The path on the backend Droplets to which the load balancer instance will send a request.<br><br>**Default**: `'/'` | getPath(): ?string | setPath(?string path): void |
| `port` | `?int` | Optional | An integer representing the port on the backend Droplets on which the health check will attempt a connection.<br><br>**Default**: `80` | getPort(): ?int | setPort(?int port): void |
| `protocol` | [`?string(Protocol1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/protocol-1.md) | Optional | The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.<br><br>**Default**: `Protocol1::HTTP` | getProtocol(): ?string | setProtocol(?string protocol): void |
| `responseTimeoutSeconds` | `?int` | Optional | The number of seconds the load balancer instance will wait for a response until marking a health check as failed.<br><br>**Default**: `5` | getResponseTimeoutSeconds(): ?int | setResponseTimeoutSeconds(?int responseTimeoutSeconds): void |
| `unhealthyThreshold` | `?int` | Optional | The number of times a health check must fail for a backend Droplet to be marked "unhealthy" and be removed from the pool.<br><br>**Default**: `5` | getUnhealthyThreshold(): ?int | setUnhealthyThreshold(?int unhealthyThreshold): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\HealthCheck1Builder;
use DigitalOceanApiLib\Models\Protocol1;
use DigitalOceanApiLib\ApiHelper;

$healthCheck1 = HealthCheck1Builder::init()
    ->checkIntervalSeconds(10)
    ->healthyThreshold(3)
    ->path('/')
    ->port(80)
    ->protocol(Protocol1::HTTP)
    ->responseTimeoutSeconds(5)
    ->unhealthyThreshold(5)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



