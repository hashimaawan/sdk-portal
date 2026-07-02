# Health Check 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkhlYWx0aENoZWNrMQ

An object specifying health check settings for the load balancer.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`HealthCheck1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkIntervalSeconds` | `number \| undefined` | Optional | The number of seconds between between two consecutive health checks.<br><br>**Default**: `10` |
| `healthyThreshold` | `number \| undefined` | Optional | The number of times a health check must pass for a backend Droplet to be marked "healthy" and be re-added to the pool.<br><br>**Default**: `3` |
| `path` | `string \| undefined` | Optional | The path on the backend Droplets to which the load balancer instance will send a request.<br><br>**Default**: `'/'` |
| `port` | `number \| undefined` | Optional | An integer representing the port on the backend Droplets on which the health check will attempt a connection.<br><br>**Default**: `80` |
| `protocol` | [`Protocol1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/protocol-1.md) | Optional | The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.<br><br>**Default**: `Protocol1.Http` |
| `responseTimeoutSeconds` | `number \| undefined` | Optional | The number of seconds the load balancer instance will wait for a response until marking a health check as failed.<br><br>**Default**: `5` |
| `unhealthyThreshold` | `number \| undefined` | Optional | The number of times a health check must fail for a backend Droplet to be marked "unhealthy" and be removed from the pool.<br><br>**Default**: `5` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { HealthCheck1, Protocol1 } from 'digitalocean-apilib';

const healthCheck1: HealthCheck1 = {
  checkIntervalSeconds: 10,
  healthyThreshold: 3,
  path: '/',
  port: 80,
  protocol: Protocol1.Http,
  responseTimeoutSeconds: 5,
  unhealthyThreshold: 5,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



