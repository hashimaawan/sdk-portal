# Maintenance Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlUG9saWN5

An object specifying the maintenance window policy for the Kubernetes cluster.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`MaintenancePolicy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `day` | [`Day \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/day.md) | Optional | The day of the maintenance window policy. May be one of `monday` through `sunday`, or `any` to indicate an arbitrary week day. |
| `duration` | `string \| undefined` | Optional, Read-only | The duration of the maintenance window policy in human-readable format. |
| `startTime` | `string \| undefined` | Optional | The start time in UTC of the maintenance window policy in 24-hour clock format / HH:MM notation (e.g., `15:00`). |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Day, MaintenancePolicy } from 'digitalocean-apilib';

const maintenancePolicy: MaintenancePolicy = {
  day: Day.Any,
  duration: '4h0m0s',
  startTime: '12:00',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



