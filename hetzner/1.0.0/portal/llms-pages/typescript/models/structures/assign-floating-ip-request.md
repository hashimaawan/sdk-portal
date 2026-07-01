# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |


# Interface Name

`AssignFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | `number` | Required | ID of the Server the Floating IP shall be assigned to |


# Example

```ts
import { AssignFloatingIPRequest } from 'hetzner-cloud-apilib';

const assignFloatingIPRequest: AssignFloatingIPRequest = {
  server: 42,
};
```



