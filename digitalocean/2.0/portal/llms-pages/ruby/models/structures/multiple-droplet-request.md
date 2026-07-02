# Multiple Droplet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk11bHRpcGxlJTI1MjBEcm9wbGV0JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`MultipleDropletRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `names` | `Array[String]` | Required | An array of human human-readable strings you wish to use when displaying the Droplet name. Each name, if set to a domain name managed in the DigitalOcean DNS management system, will configure a PTR record for the Droplet. Each name set during creation will also determine the hostname for the Droplet in its internal configuration. |
| `backups` | `TrueClass \| FalseClass` | Optional | A boolean indicating whether automated backups should be enabled for the Droplet.<br><br>**Default**: `false` |
| `image` | String \| Integer | Required | This is a container for one-of cases. |
| `ipv_6` | `TrueClass \| FalseClass` | Optional | A boolean indicating whether to enable IPv6 on the Droplet.<br><br>**Default**: `false` |
| `monitoring` | `TrueClass \| FalseClass` | Optional | A boolean indicating whether to install the DigitalOcean agent for monitoring.<br><br>**Default**: `false` |
| `private_networking` | `TrueClass \| FalseClass` | Optional | This parameter has been deprecated. Use `vpc_uuid` instead to specify a VPC network for the Droplet. If no `vpc_uuid` is provided, the Droplet will be placed in your account's default VPC for the region.<br><br>**Default**: `false` |
| `region` | `String` | Optional | The slug identifier for the region that you wish to deploy the Droplet in. If the specific datacenter is not not important, a slug prefix (e.g. `nyc`) can be used to deploy the Droplet in any of the that region's locations (`nyc1`, `nyc2`, or `nyc3`). If the region is omitted from the create request completely, the Droplet may deploy in any region. |
| `size` | `String` | Required | The slug identifier for the size that you wish to select for this Droplet. |
| `ssh_keys` | Array[String \| Integer] \| nil | Optional | This is Array of a container for any-of cases. |
| `tags` | `Array[String]` | Optional | A flat array of tag names as strings to apply to the Droplet after it is created. Tag names can either be existing or new tags. |
| `user_data` | `String` | Optional | A string containing 'user data' which may be used to configure the Droplet on first boot, often a 'cloud-config' file or Bash script. It must be plain text and may not exceed 64 KiB in size. |
| `volumes` | `Array[String]` | Optional | An array of IDs for block storage volumes that will be attached to the Droplet once created. The volumes must not already be attached to an existing Droplet. |
| `vpc_uuid` | `String` | Optional | A string specifying the UUID of the VPC to which the Droplet will be assigned. If excluded, the Droplet will be assigned to your account's default VPC for the region. |
| `with_droplet_agent` | `TrueClass \| FalseClass` | Optional | A boolean indicating whether to install the DigitalOcean agent used for providing access to the Droplet web console in the control panel. By default, the agent is installed on new Droplets but installation errors (i.e. OS not supported) are ignored. To prevent it from being installed, set to `false`. To make installation errors fatal, explicitly set it to `true`. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
multiple_droplet_request = MultipleDropletRequest.new(
  names: [
    'sub-01.example.com',
    'sub-02.example.com'
  ],
  image: 'ubuntu-20-04-x64',
  size: 's-1vcpu-1gb',
  backups: true,
  ipv6: true,
  monitoring: true,
  private_networking: true,
  region: 'nyc3',
  ssh_keys: [
    nil,
    nil
  ],
  tags: [
    'env:prod',
    'web'
  ],
  user_data: '#cloud-config\nruncmd:\n  - touch /test.txt\n',
  volumes: [
    '12e97116-7280-11ed-b3d0-0a58ac146812'
  ],
  vpc_uuid: '760e09ef-dc84-11e8-981e-3cfdfeaae000',
  with_droplet_agent: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



