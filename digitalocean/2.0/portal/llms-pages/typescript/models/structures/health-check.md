# Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkhlYWx0aENoZWNr

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`HealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `failureThreshold` | `number \| undefined` | Optional | The number of failed health checks before considered unhealthy. |
| `httpPath` | `string \| undefined` | Optional | The route path used for the HTTP health check ping. If not set, the HTTP health check will be disabled and a TCP health check used instead. |
| `initialDelaySeconds` | `number \| undefined` | Optional | The number of seconds to wait before beginning health checks. |
| `periodSeconds` | `number \| undefined` | Optional | The number of seconds to wait between health checks. |
| `port` | `bigint \| undefined` | Optional | The port on which the health check will be performed. If not set, the health check will be performed on the component's http_port.<br><br>**Constraints**: `>= 1`, `<= 65535` |
| `successThreshold` | `number \| undefined` | Optional | The number of successful health checks before considered healthy. |
| `timeoutSeconds` | `number \| undefined` | Optional | The number of seconds after which the check times out. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { HealthCheck } from 'digitalocean-apilib';

const healthCheck: HealthCheck = {
  failureThreshold: 2,
  httpPath: '/health',
  initialDelaySeconds: 30,
  periodSeconds: 60,
  port: BigInt(80),
  successThreshold: 3,
  timeoutSeconds: 45,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



