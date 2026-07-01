# Create Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `boolean \| undefined` | Optional | Auto-mount Volumes after attach |
| `datacenter` | `string \| undefined` | Optional | ID or name of Datacenter to create Server in (must not be used together with location) |
| `firewalls` | [`Firewall4[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/firewall-4.md) | Optional | Firewalls which should be applied on the Server's public network interface at creation time |
| `image` | `string` | Required | ID or name of the Image the Server is created from |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `location` | `string \| undefined` | Optional | ID or name of Location to create Server in (must not be used together with datacenter) |
| `name` | `string` | Required | Name of the Server to create (must be unique per Project and a valid hostname as per RFC 1123) |
| `networks` | `number[] \| undefined` | Optional | Network IDs which should be attached to the Server private network interface at the creation time |
| `placementGroup` | `number \| undefined` | Optional | ID of the Placement Group the server should be in |
| `publicNet` | [`PublicNet5 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/public-net-5.md) | Optional | Public Network options |
| `serverType` | `string` | Required | ID or name of the Server type this Server should be created with |
| `sshKeys` | `string[] \| undefined` | Optional | SSH key IDs (`integer`) or names (`string`) which should be injected into the Server at creation time |
| `startAfterCreate` | `boolean \| undefined` | Optional | Start Server right after creation. Defaults to true. |
| `userData` | `string \| undefined` | Optional | Cloud-Init user data to use during Server creation. This field is limited to 32KiB. |
| `volumes` | `number[] \| undefined` | Optional | Volume IDs which should be attached to the Server at the creation time. Volumes must be in the same Location. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateServerRequest } from 'hetzner-cloud-apilib';

const createServerRequest: CreateServerRequest = {
  image: 'ubuntu-20.04',
  name: 'my-server',
  serverType: 'cx11',
  automount: false,
  datacenter: 'nbg1-dc3',
  firewalls: [
    {
      firewall: 38,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  labels: { 'key1': 'val1', 'key2': 'val2' },
  location: 'nbg1',
  networks: [
    456
  ],
  placementGroup: 1,
  sshKeys: [
    'my-ssh-key'
  ],
  startAfterCreate: true,
  userData: '#cloud-config\nruncmd:\n- [touch, /root/cloud-init-worked]\n',
  volumes: [
    123
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



