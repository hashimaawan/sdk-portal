# Location 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvY2F0aW9uMTY

Location of the Volume. Volume can only be attached to Servers in the same Location.


# Interface Name

`Location16`


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


# Example

```ts
import { Location16 } from 'hetzner-cloud-apilib';

const location16: Location16 = {
  city: 'Falkenstein',
  country: 'DE',
  description: 'Falkenstein DC Park 1',
  id: 1,
  latitude: 50.47612,
  longitude: 12.370071,
  name: 'fsn1',
  networkZone: 'eu-central',
};
```



