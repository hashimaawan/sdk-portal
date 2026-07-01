# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q


# Interface Name

`AssignPrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assigneeId` | `number` | Required | ID of a resource of type `assignee_type` |
| `assigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `'server'` |


# Example

```ts
import { AssignPrimaryIPRequest } from 'hetzner-cloud-apilib';

const assignPrimaryIPRequest: AssignPrimaryIPRequest = {
  assigneeId: 4711,
  assigneeType: 'server',
};
```



