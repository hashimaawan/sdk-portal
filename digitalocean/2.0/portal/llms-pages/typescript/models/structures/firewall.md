# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Firewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. |
| `dropletIds` | `number[] \| null \| undefined` | Optional | An array containing the IDs of the Droplets assigned to the firewall. |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. |
| `name` | `string \| undefined` | Optional | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` |
| `pendingChanges` | [`PendingChange[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. |
| `status` | [`Status9 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". |
| `tags` | `string[] \| null \| undefined` | Optional | - |
| `inboundRules` | [`InboundRule[] \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/inbound-rule.md) | Optional | - |
| `outboundRules` | [`OutboundRule[] \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/outbound-rule.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Firewall, Status9 } from 'digitalocean-apilib';

const firewall: Firewall = {
  createdAt: '2020-05-23T21:24:00Z',
  dropletIds: [
    8043964
  ],
  id: 'bb4b2611-3d72-467b-8602-280330ecd65c',
  name: 'firewall',
  pendingChanges: [
    {
      dropletId: 8043964,
      removing: false,
      status: 'waiting',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  status: Status9.Waiting,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



