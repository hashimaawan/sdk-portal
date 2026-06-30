# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U


# Interface Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Action[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `firewall` | [`Firewall \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/firewall.md) | Optional | - |


# Example

```ts
import {
  CreateFirewallResponse,
  DirectionEnum,
  ProtocolEnum,
  StatusEnum,
  Type5Enum,
  Type6Enum,
} from 'hetzner-cloud-apilib';

const createFirewallResponse: CreateFirewallResponse = {
  actions: [
    {
      command: 'set_firewall_rules',
      error: {
        code: 'action_failed',
        message: 'Action failed',
      },
      finished: '2016-01-30T23:56:00+00:00',
      id: 13,
      progress: 100,
      resources: [
        {
          id: 38,
          type: 'firewall',
        }
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: StatusEnum.Success,
    },
    {
      command: 'apply_firewall',
      error: {
        code: 'action_failed',
        message: 'Action failed',
      },
      finished: '2016-01-30T23:56:00+00:00',
      id: 14,
      progress: 100,
      resources: [
        {
          id: 42,
          type: 'server',
        },
        {
          id: 38,
          type: 'firewall',
        }
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: StatusEnum.Success,
    }
  ],
  firewall: {
    appliedTo: [
      {
        type: Type6Enum.Server,
        appliedToResources: [
          {
            server: {
              id: 14,
            },
            type: Type5Enum.Server,
          }
        ],
        labelSelector: {
          selector: 'selector8',
        },
        server: {
          id: 14,
        },
      },
      {
        type: Type6Enum.Server,
        appliedToResources: [
          {
            server: {
              id: 14,
            },
            type: Type5Enum.Server,
          }
        ],
        labelSelector: {
          selector: 'selector8',
        },
        server: {
          id: 14,
        },
      }
    ],
    created: 'created6',
    id: 4,
    name: 'name6',
    rules: [
      {
        direction: DirectionEnum.In,
        protocol: ProtocolEnum.Udp,
        description: 'description2',
        destinationIps: [
          'destination_ips1',
          'destination_ips2',
          'destination_ips3'
        ],
        port: 'port8',
        sourceIps: [
          'source_ips1',
          'source_ips2',
          'source_ips3'
        ],
      }
    ],
    labels: {
      'key0': 'labels2',
      'key1': 'labels1'
    },
  },
};
```



