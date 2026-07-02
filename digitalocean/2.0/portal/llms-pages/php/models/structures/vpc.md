# Vpc

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlZwYw

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Vpc`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | A free-form text field for describing the VPC's purpose. It may be a maximum of 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` | getDescription(): ?string | setDescription(?string description): void |
| `name` | `?string` | Optional | The name of the VPC. Must be unique and may only contain alphanumeric characters, dashes, and periods.<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9\-\.]+$` | getName(): ?string | setName(?string name): void |
| `ipRange` | `?string` | Optional | The range of IP addresses in the VPC in CIDR notation. Network ranges cannot overlap with other networks in the same account and must be in range of private addresses as defined in RFC1918. It may not be smaller than `/28` nor larger than `/16`. If no IP range is specified, a `/20` network range is generated that won't conflict with other VPC networks in your account. | getIpRange(): ?string | setIpRange(?string ipRange): void |
| `region` | `?string` | Optional | The slug identifier for the region where the VPC will be created. | getRegion(): ?string | setRegion(?string region): void |
| `default` | `?bool` | Optional | A boolean value indicating whether or not the VPC is the default network for the region. All applicable resources are placed into the default VPC network unless otherwise specified during their creation. The `default` field cannot be unset from `true`. If you want to set a new default VPC network, update the `default` field of another VPC network in the same region. The previous network's `default` field will be set to `false` when a new default VPC has been defined. | getDefault(): ?bool | setDefault(?bool default): void |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference the VPC. | getId(): ?string | setId(?string id): void |
| `urn` | `?string` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` | getUrn(): ?string | setUrn(?string urn): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\VpcBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$vpc = VpcBuilder::init()
    ->description('VPC for production environment')
    ->name('env.prod-vpc')
    ->ipRange('10.10.10.0/24')
    ->region('nyc1')
    ->default(true)
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-03-13T19:20:47.442049222Z'))
    ->id('5a4981aa-9653-4bd1-bef5-d6bff52042e4')
    ->urn('do:droplet:13457723')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



