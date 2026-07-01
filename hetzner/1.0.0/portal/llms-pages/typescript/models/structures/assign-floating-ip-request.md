# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |

*This model accepts additional fields of type unknown.*


# Interface Name

`AssignFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | `number` | Required | ID of the Server the Floating IP shall be assigned to |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AssignFloatingIpRequest } from 'hetzner-cloud-apilib';

const assignFloatingIpRequest: AssignFloatingIpRequest = {
  server: 42,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



