# V2 Firewalls Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FirewallsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. |
| `dropletIds` | `number[] \| null \| undefined` | Optional | An array containing the IDs of the Droplets assigned to the firewall. |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. |
| `name` | `string` | Required | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` |
| `pendingChanges` | [`PendingChange[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. |
| `status` | [`Status9 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". |
| `tags` | `string[] \| null \| undefined` | Optional | - |
| `inboundRules` | [`InboundRule[] \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/inbound-rule.md) | Required | - |
| `outboundRules` | [`OutboundRule[] \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/outbound-rule.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Protocol, Status9, V2FirewallsRequest } from 'digitalocean-apilib';

const v2FirewallsRequest: V2FirewallsRequest = {
  name: 'firewall',
  inboundRules: [
    {
      ports: '8000',
      protocol: Protocol.Tcp,
      sources: {
        addresses: [
          '1.2.3.4',
          '18.0.0.0/8'
        ],
        dropletIds: [
          8043964
        ],
        kubernetesIds: [
          '41b74c5d-9bd0-5555-5555-a57c495b81a3'
        ],
        loadBalancerUids: [
          '4de7ac8b-495b-4884-9a69-1050c6793cd6'
        ],
        tags: [
          'tags1',
          'tags2',
          'tags3'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  outboundRules: [
    {
      ports: '8000',
      protocol: Protocol.Tcp,
      destinations: {
        addresses: [
          '1.2.3.4',
          '18.0.0.0/8'
        ],
        dropletIds: [
          8043964
        ],
        kubernetesIds: [
          '41b74c5d-9bd0-5555-5555-a57c495b81a3'
        ],
        loadBalancerUids: [
          '4de7ac8b-495b-4884-9a69-1050c6793cd6'
        ],
        tags: [
          'tags7',
          'tags8',
          'tags9'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  createdAt: '2020-05-23T21:24:00Z',
  dropletIds: [
    8043964
  ],
  id: 'bb4b2611-3d72-467b-8602-280330ecd65c',
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



