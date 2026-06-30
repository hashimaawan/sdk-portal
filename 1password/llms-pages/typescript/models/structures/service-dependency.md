# Service Dependency

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlNlcnZpY2VEZXBlbmRlbmN5

The state of a registered server dependency.

*This model accepts additional fields of type unknown.*


# Interface Name

`ServiceDependency`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `string \| undefined` | Optional | Human-readable message for explaining the current state. |
| `service` | `string \| undefined` | Optional | - |
| `status` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServiceDependency } from 'm-1-password-connectlib';

const serviceDependency: ServiceDependency = {
  message: 'message6',
  service: 'service6',
  status: 'status8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



