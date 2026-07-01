# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Action[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `firewall` | [`Firewall \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/firewall.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CreateFirewallResponse,
  Direction,
  Protocol,
  Status,
  Type5,
  Type6,
} from 'hetzner-cloud-apilib';

const createFirewallResponse: CreateFirewallResponse = {
  actions: [
    {
      command: 'set_firewall_rules',
      error: {
        code: 'action_failed',
        message: 'Action failed',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      finished: '2016-01-30T23:56:00+00:00',
      id: 13,
      progress: 100,
      resources: [
        {
          id: 38,
          type: 'firewall',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: Status.Success,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      command: 'apply_firewall',
      error: {
        code: 'action_failed',
        message: 'Action failed',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      finished: '2016-01-30T23:56:00+00:00',
      id: 14,
      progress: 100,
      resources: [
        {
          id: 42,
          type: 'server',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          id: 38,
          type: 'firewall',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: Status.Success,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  firewall: {
    appliedTo: [
      {
        type: Type6.Server,
        appliedToResources: [
          {
            server: {
              id: 14,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            type: Type5.Server,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        labelSelector: {
          selector: 'selector8',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        server: {
          id: 14,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        type: Type6.Server,
        appliedToResources: [
          {
            server: {
              id: 14,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            type: Type5.Server,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        labelSelector: {
          selector: 'selector8',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        server: {
          id: 14,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    created: 'created6',
    id: 4,
    name: 'name6',
    rules: [
      {
        direction: Direction.In,
        protocol: Protocol.Udp,
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
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    labels: {
      'key0': 'labels2',
      'key1': 'labels1'
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



