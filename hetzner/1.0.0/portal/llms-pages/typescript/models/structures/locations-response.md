# Locations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`LocationsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `locations` | [`Location[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/location.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LocationsResponse } from 'hetzner-cloud-apilib';

const locationsResponse: LocationsResponse = {
  locations: [
    {
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



