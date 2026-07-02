# Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlNpemU

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Size`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `available` | `bool` | Required | This is a boolean value that represents whether new Droplets can be created with this size.<br><br>**Default**: `true` | getAvailable(): bool | setAvailable(bool available): void |
| `description` | `string` | Required | A string describing the class of Droplets created from this size. For example: Basic, General Purpose, CPU-Optimized, Memory-Optimized, or Storage-Optimized. | getDescription(): string | setDescription(string description): void |
| `disk` | `int` | Required | The amount of disk space set aside for Droplets of this size. The value is represented in gigabytes. | getDisk(): int | setDisk(int disk): void |
| `memory` | `int` | Required | The amount of RAM allocated to Droplets created of this size. The value is represented in megabytes.<br><br>**Constraints**: `>= 8`, *Multiple Of*: `8` | getMemory(): int | setMemory(int memory): void |
| `priceHourly` | `float` | Required | This describes the price of the Droplet size as measured hourly. The value is measured in US dollars. | getPriceHourly(): float | setPriceHourly(float priceHourly): void |
| `priceMonthly` | `float` | Required | This attribute describes the monthly cost of this Droplet size if the Droplet is kept for an entire month. The value is measured in US dollars. | getPriceMonthly(): float | setPriceMonthly(float priceMonthly): void |
| `regions` | `string[]` | Required | An array containing the region slugs where this size is available for Droplet creates. | getRegions(): array | setRegions(array regions): void |
| `slug` | `string` | Required | A human-readable string that is used to uniquely identify each size. | getSlug(): string | setSlug(string slug): void |
| `transfer` | `float` | Required | The amount of transfer bandwidth that is available for Droplets created in this size. This only counts traffic on the public interface. The value is given in terabytes. | getTransfer(): float | setTransfer(float transfer): void |
| `vcpus` | `int` | Required | The integer of number CPUs allocated to Droplets of this size. | getVcpus(): int | setVcpus(int vcpus): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\SizeBuilder;
use DigitalOceanApiLib\ApiHelper;

$size = SizeBuilder::init(
    true,
    'Basic',
    25,
    1024,
    0.00743999984115362,
    5,
    [
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
    's-1vcpu-1gb',
    1,
    1
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



