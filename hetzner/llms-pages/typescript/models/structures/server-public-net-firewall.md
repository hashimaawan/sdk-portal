# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs


# Interface Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number \| undefined` | Optional | ID of the Resource |
| `status` | [`Status72Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |


# Example

```ts
import { ServerPublicNetFirewall, Status72Enum } from 'hetzner-cloud-apilib';

const serverPublicNetFirewall: ServerPublicNetFirewall = {
  id: 42,
  status: Status72Enum.Applied,
};
```



