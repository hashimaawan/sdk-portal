# Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNpemU

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Size`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `boolean` | Required | This is a boolean value that represents whether new Droplets can be created with this size.<br><br>**Default**: `true` |
| `description` | `string` | Required | A string describing the class of Droplets created from this size. For example: Basic, General Purpose, CPU-Optimized, Memory-Optimized, or Storage-Optimized. |
| `disk` | `number` | Required | The amount of disk space set aside for Droplets of this size. The value is represented in gigabytes. |
| `memory` | `number` | Required | The amount of RAM allocated to Droplets created of this size. The value is represented in megabytes.<br><br>**Constraints**: `>= 8`, *Multiple Of*: `8` |
| `priceHourly` | `number` | Required | This describes the price of the Droplet size as measured hourly. The value is measured in US dollars. |
| `priceMonthly` | `number` | Required | This attribute describes the monthly cost of this Droplet size if the Droplet is kept for an entire month. The value is measured in US dollars. |
| `regions` | `string[]` | Required | An array containing the region slugs where this size is available for Droplet creates. |
| `slug` | `string` | Required | A human-readable string that is used to uniquely identify each size. |
| `transfer` | `number` | Required | The amount of transfer bandwidth that is available for Droplets created in this size. This only counts traffic on the public interface. The value is given in terabytes. |
| `vcpus` | `number` | Required | The integer of number CPUs allocated to Droplets of this size. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Size } from 'digitalocean-apilib';

const size: Size = {
  available: true,
  description: 'Basic',
  disk: 25,
  memory: 1024,
  priceHourly: 0.00743999984115362,
  priceMonthly: 5,
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



