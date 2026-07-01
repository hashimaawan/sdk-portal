# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA


# Interface Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `healthStatus` | [`HealthStatus[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/health-status.md) | Optional | List of health statuses of the services on this target |
| `ip` | [`Ip \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `labelSelector` | [`LabelSelector7 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets |
| `server` | [`LoadBalancerTargetServer \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through |
| `targets` | [`Target[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/target.md) | Optional | List of selected targets |
| `type` | [`Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-29.md) | Required | Type of the resource |
| `usePrivateIp` | `boolean \| undefined` | Optional | Use the private network IP instead of the public IP. Default value is false. |


# Example

```ts
import {
  LoadBalancerTarget,
  Status30Enum,
  Type29Enum,
} from 'hetzner-cloud-apilib';

const loadBalancerTarget: LoadBalancerTarget = {
  type: Type29Enum.LabelSelector,
  healthStatus: [
    {
      listenPort: 142,
      status: Status30Enum.Unknown,
    },
    {
      listenPort: 142,
      status: Status30Enum.Unknown,
    }
  ],
  ip: {
    ip: 'ip8',
  },
  labelSelector: {
    selector: 'selector8',
  },
  server: {
    id: 14,
  },
  targets: [
    {
      healthStatus: [
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        },
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        }
      ],
      server: {
        id: 14,
      },
      type: 'type2',
      usePrivateIp: false,
    },
    {
      healthStatus: [
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        },
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        }
      ],
      server: {
        id: 14,
      },
      type: 'type2',
      usePrivateIp: false,
    },
    {
      healthStatus: [
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        },
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        }
      ],
      server: {
        id: 14,
      },
      type: 'type2',
      usePrivateIp: false,
    }
  ],
};
```



