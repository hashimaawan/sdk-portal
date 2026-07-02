# Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlNpemU

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Size`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `TrueClass \| FalseClass` | Required | This is a boolean value that represents whether new Droplets can be created with this size.<br><br>**Default**: `true` |
| `description` | `String` | Required | A string describing the class of Droplets created from this size. For example: Basic, General Purpose, CPU-Optimized, Memory-Optimized, or Storage-Optimized. |
| `disk` | `Integer` | Required | The amount of disk space set aside for Droplets of this size. The value is represented in gigabytes. |
| `memory` | `Integer` | Required | The amount of RAM allocated to Droplets created of this size. The value is represented in megabytes.<br><br>**Constraints**: `>= 8`, *Multiple Of*: `8` |
| `price_hourly` | `Float` | Required | This describes the price of the Droplet size as measured hourly. The value is measured in US dollars. |
| `price_monthly` | `Float` | Required | This attribute describes the monthly cost of this Droplet size if the Droplet is kept for an entire month. The value is measured in US dollars. |
| `regions` | `Array[String]` | Required | An array containing the region slugs where this size is available for Droplet creates. |
| `slug` | `String` | Required | A human-readable string that is used to uniquely identify each size. |
| `transfer` | `Float` | Required | The amount of transfer bandwidth that is available for Droplets created in this size. This only counts traffic on the public interface. The value is given in terabytes. |
| `vcpus` | `Integer` | Required | The integer of number CPUs allocated to Droplets of this size. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
size = Size.new(
  available: true,
  description: 'Basic',
  disk: 25,
  memory: 1024,
  price_hourly: 0.00743999984115362,
  price_monthly: 5,
  regions: [
    'ams2',
    'ams3',
    'blr1',
    'fra1',
    'lon1',
    'nyc1',
    'nyc2',
    'nyc3',
    'sfo1',
    'sfo2',
    'sfo3',
    'sgp1',
    'tor1'
  ],
  slug: 's-1vcpu-1gb',
  transfer: 1,
  vcpus: 1,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



