# Single Droplet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlNpbmdsZSUyNTIwRHJvcGxldCUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`SingleDropletRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | The human-readable string you wish to use when displaying the Droplet name. The name, if set to a domain name managed in the DigitalOcean DNS management system, will configure a PTR record for the Droplet. The name set during creation will also determine the hostname for the Droplet in its internal configuration. | getName(): string | setName(string name): void |
| `backups` | `?bool` | Optional | A boolean indicating whether automated backups should be enabled for the Droplet.<br><br>**Default**: `false` | getBackups(): ?bool | setBackups(?bool backups): void |
| `image` | string\|int | Required | This is a container for one-of cases. | getImage(): | setImage( image): void |
| `ipv6` | `?bool` | Optional | A boolean indicating whether to enable IPv6 on the Droplet.<br><br>**Default**: `false` | getIpv6(): ?bool | setIpv6(?bool ipv6): void |
| `monitoring` | `?bool` | Optional | A boolean indicating whether to install the DigitalOcean agent for monitoring.<br><br>**Default**: `false` | getMonitoring(): ?bool | setMonitoring(?bool monitoring): void |
| `privateNetworking` | `?bool` | Optional | This parameter has been deprecated. Use `vpc_uuid` instead to specify a VPC network for the Droplet. If no `vpc_uuid` is provided, the Droplet will be placed in your account's default VPC for the region.<br><br>**Default**: `false` | getPrivateNetworking(): ?bool | setPrivateNetworking(?bool privateNetworking): void |
| `region` | `?string` | Optional | The slug identifier for the region that you wish to deploy the Droplet in. If the specific datacenter is not not important, a slug prefix (e.g. `nyc`) can be used to deploy the Droplet in any of the that region's locations (`nyc1`, `nyc2`, or `nyc3`). If the region is omitted from the create request completely, the Droplet may deploy in any region. | getRegion(): ?string | setRegion(?string region): void |
| `size` | `string` | Required | The slug identifier for the size that you wish to select for this Droplet. | getSize(): string | setSize(string size): void |
| `sshKeys` | array<string\|int>\|null | Optional | This is Array of a container for any-of cases. | getSshKeys(): ?array | setSshKeys(?array sshKeys): void |
| `tags` | `?(string[])` | Optional | A flat array of tag names as strings to apply to the Droplet after it is created. Tag names can either be existing or new tags. | getTags(): ?array | setTags(?array tags): void |
| `userData` | `?string` | Optional | A string containing 'user data' which may be used to configure the Droplet on first boot, often a 'cloud-config' file or Bash script. It must be plain text and may not exceed 64 KiB in size. | getUserData(): ?string | setUserData(?string userData): void |
| `volumes` | `?(string[])` | Optional | An array of IDs for block storage volumes that will be attached to the Droplet once created. The volumes must not already be attached to an existing Droplet. | getVolumes(): ?array | setVolumes(?array volumes): void |
| `vpcUuid` | `?string` | Optional | A string specifying the UUID of the VPC to which the Droplet will be assigned. If excluded, the Droplet will be assigned to your account's default VPC for the region. | getVpcUuid(): ?string | setVpcUuid(?string vpcUuid): void |
| `withDropletAgent` | `?bool` | Optional | A boolean indicating whether to install the DigitalOcean agent used for providing access to the Droplet web console in the control panel. By default, the agent is installed on new Droplets but installation errors (i.e. OS not supported) are ignored. To prevent it from being installed, set to `false`. To make installation errors fatal, explicitly set it to `true`. | getWithDropletAgent(): ?bool | setWithDropletAgent(?bool withDropletAgent): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\SingleDropletRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$singleDropletRequest = SingleDropletRequestBuilder::init(
    'example.com',
    'ubuntu-20-04-x64',
    's-1vcpu-1gb'
)
    ->backups(true)
    ->ipv6(true)
    ->monitoring(true)
    ->privateNetworking(true)
    ->region('nyc3')
    ->sshKeys(
        [
            ,
            
        ]
    )
    ->tags(
        [
            'env:prod',
            'web'
        ]
    )
    ->userData('#cloud-config
runcmd:
  - touch /test.txt
')
    ->volumes(
        [
            '12e97116-7280-11ed-b3d0-0a58ac146812'
        ]
    )
    ->vpcUuid('760e09ef-dc84-11e8-981e-3cfdfeaae000')
    ->withDropletAgent(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



