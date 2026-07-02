# Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRyb3BsZXQx

An object containing information about a resource scheduled for deletion.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Droplet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destroyedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format indicating when the resource was destroyed if the request was successful. |
| `errorMessage` | `string \| undefined` | Optional | A string indicating that the resource was not successfully destroyed and providing additional information. |
| `id` | `string \| undefined` | Optional | The unique identifier for the resource scheduled for deletion. |
| `name` | `string \| undefined` | Optional | The name of the resource scheduled for deletion. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Droplet1 } from 'digitalocean-apilib';

const droplet1: Droplet1 = {
  destroyedAt: '2020-04-01T18:11:49Z',
  errorMessage: 'error_message0',
  id: '61486916',
  name: 'ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



