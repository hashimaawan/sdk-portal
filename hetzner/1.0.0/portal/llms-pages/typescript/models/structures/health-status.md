# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw

*This model accepts additional fields of type unknown.*


# Interface Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listenPort` | `number \| undefined` | Optional | - |
| `status` | [`Status30 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/status-30.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { HealthStatus, Status30 } from 'hetzner-cloud-apilib';

const healthStatus: HealthStatus = {
  listenPort: 443,
  status: Status30.Healthy,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



