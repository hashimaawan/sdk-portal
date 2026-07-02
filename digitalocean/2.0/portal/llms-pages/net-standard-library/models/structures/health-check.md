# Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkhlYWx0aENoZWNr

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`HealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FailureThreshold` | `int?` | Optional | The number of failed health checks before considered unhealthy. |
| `HttpPath` | `string` | Optional | The route path used for the HTTP health check ping. If not set, the HTTP health check will be disabled and a TCP health check used instead. |
| `InitialDelaySeconds` | `int?` | Optional | The number of seconds to wait before beginning health checks. |
| `PeriodSeconds` | `int?` | Optional | The number of seconds to wait between health checks. |
| `Port` | `long?` | Optional | The port on which the health check will be performed. If not set, the health check will be performed on the component's http_port.<br><br>**Constraints**: `>= 1`, `<= 65535` |
| `SuccessThreshold` | `int?` | Optional | The number of successful health checks before considered healthy. |
| `TimeoutSeconds` | `int?` | Optional | The number of seconds after which the check times out. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

HealthCheck healthCheck = new HealthCheck
{
    FailureThreshold = 2,
    HttpPath = "/health",
    InitialDelaySeconds = 30,
    PeriodSeconds = 60,
    Port = 80L,
    SuccessThreshold = 3,
    TimeoutSeconds = 45,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



