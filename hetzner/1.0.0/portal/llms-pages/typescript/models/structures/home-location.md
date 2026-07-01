# Home Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkhvbWVMb2NhdGlvbg

Location the Floating IP was created in. Routing is optimized for this Location.

*This model accepts additional fields of type unknown.*


# Interface Name

`HomeLocation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `string` | Required | City the Location is closest to |
| `country` | `string` | Required | ISO 3166-1 alpha-2 code of the country the Location resides in |
| `description` | `string` | Required | Description of the Location |
| `id` | `number` | Required | ID of the Location |
| `latitude` | `number` | Required | Latitude of the city closest to the Location |
| `longitude` | `number` | Required | Longitude of the city closest to the Location |
| `name` | `string` | Required | Unique identifier of the Location |
| `networkZone` | `string` | Required | Name of network zone this Location resides in |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { HomeLocation } from 'hetzner-cloud-apilib';

const homeLocation: HomeLocation = {
  city: 'Falkenstein',
  country: 'DE',
  description: 'Falkenstein DC Park 1',
  id: 1,
  latitude: 50.47612,
  longitude: 12.370071,
  name: 'fsn1',
  networkZone: 'eu-central',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



