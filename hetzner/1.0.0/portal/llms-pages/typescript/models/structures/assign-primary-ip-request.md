# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`AssignPrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assigneeId` | `number` | Required | ID of a resource of type `assignee_type` |
| `assigneeType` | `string` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `'server'` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AssignPrimaryIpRequest } from 'hetzner-cloud-apilib';

const assignPrimaryIpRequest: AssignPrimaryIpRequest = {
  assigneeId: 4711,
  assigneeType: 'server',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



