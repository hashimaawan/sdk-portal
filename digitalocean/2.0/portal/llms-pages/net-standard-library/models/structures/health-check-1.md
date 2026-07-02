# Health Check 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkhlYWx0aENoZWNrMQ

An object specifying health check settings for the load balancer.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`HealthCheck1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CheckIntervalSeconds` | `int?` | Optional | The number of seconds between between two consecutive health checks.<br><br>**Default**: `10` |
| `HealthyThreshold` | `int?` | Optional | The number of times a health check must pass for a backend Droplet to be marked "healthy" and be re-added to the pool.<br><br>**Default**: `3` |
| `Path` | `string` | Optional | The path on the backend Droplets to which the load balancer instance will send a request.<br><br>**Default**: `"/"` |
| `Port` | `int?` | Optional | An integer representing the port on the backend Droplets on which the health check will attempt a connection.<br><br>**Default**: `80` |
| `Protocol` | [`Protocol1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/protocol-1.md) | Optional | The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.<br><br>**Default**: `Protocol1.http` |
| `ResponseTimeoutSeconds` | `int?` | Optional | The number of seconds the load balancer instance will wait for a response until marking a health check as failed.<br><br>**Default**: `5` |
| `UnhealthyThreshold` | `int?` | Optional | The number of times a health check must fail for a backend Droplet to be marked "unhealthy" and be removed from the pool.<br><br>**Default**: `5` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

HealthCheck1 healthCheck1 = new HealthCheck1
{
    CheckIntervalSeconds = 10,
    HealthyThreshold = 3,
    Path = "/",
    Port = 80,
    Protocol = Protocol1.Http,
    ResponseTimeoutSeconds = 5,
    UnhealthyThreshold = 5,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



