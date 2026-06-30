# Create Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlcXVlc3Q


# Class Name

`CreateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `TrueClass \| FalseClass` | Optional | Auto-mount Volumes after attach |
| `datacenter` | `String` | Optional | ID or name of Datacenter to create Server in (must not be used together with location) |
| `firewalls` | [`Array[Firewall4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/firewall-4.md) | Optional | Firewalls which should be applied on the Server's public network interface at creation time |
| `image` | `String` | Required | ID or name of the Image the Server is created from |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `location` | `String` | Optional | ID or name of Location to create Server in (must not be used together with datacenter) |
| `name` | `String` | Required | Name of the Server to create (must be unique per Project and a valid hostname as per RFC 1123) |
| `networks` | `Array[Integer]` | Optional | Network IDs which should be attached to the Server private network interface at the creation time |
| `placement_group` | `Integer` | Optional | ID of the Placement Group the server should be in |
| `public_net` | [`PublicNet5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/public-net-5.md) | Optional | Public Network options |
| `server_type` | `String` | Required | ID or name of the Server type this Server should be created with |
| `ssh_keys` | `Array[String]` | Optional | SSH key IDs (`integer`) or names (`string`) which should be injected into the Server at creation time |
| `start_after_create` | `TrueClass \| FalseClass` | Optional | Start Server right after creation. Defaults to true. |
| `user_data` | `String` | Optional | Cloud-Init user data to use during Server creation. This field is limited to 32KiB. |
| `volumes` | `Array[Integer]` | Optional | Volume IDs which should be attached to the Server at the creation time. Volumes must be in the same Location. |


# Example

```ruby
create_server_request = CreateServerRequest.new(
  'ubuntu-20.04',
  'my-server',
  'cx11',
  false,
  'nbg1-dc3',
  [
    Firewall4.new(
      38
    )
  ],
  { 'key1' => 'val1', 'key2' => 'val2' },
  'nbg1',
  [
    456
  ],
  1,
  PublicNet5.new,
  [
    'my-ssh-key'
  ],
  true,
  '#cloud-config\nruncmd:\n- [touch, /root/cloud-init-worked]\n',
  [
    123
  ]
)
```



