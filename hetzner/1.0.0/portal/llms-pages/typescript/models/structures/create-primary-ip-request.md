# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`CreatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assigneeId` | `number \| undefined` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. |
| `assigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` |
| `autoDelete` | `boolean \| undefined` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. |
| `datacenter` | `string \| undefined` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | - |
| `type` | [`Type51`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-51.md) | Required | Primary IP type |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreatePrimaryIpRequest, Type51 } from 'hetzner-cloud-apilib';

const createPrimaryIpRequest: CreatePrimaryIpRequest = {
  assigneeType: 'server',
  name: 'my-ip',
  type: Type51.Ipv4,
  assigneeId: 17,
  autoDelete: false,
  datacenter: 'fsn1-dc8',
  labels: { 'labelkey': 'value' },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



