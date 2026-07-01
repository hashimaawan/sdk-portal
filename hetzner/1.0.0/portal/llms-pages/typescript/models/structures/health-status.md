# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw


# Interface Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listenPort` | `number \| undefined` | Optional | - |
| `status` | [`Status30Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/status-30.md) | Optional | - |


# Example

```ts
import { HealthStatus, Status30Enum } from 'hetzner-cloud-apilib';

const healthStatus: HealthStatus = {
  listenPort: 443,
  status: Status30Enum.Healthy,
};
```



