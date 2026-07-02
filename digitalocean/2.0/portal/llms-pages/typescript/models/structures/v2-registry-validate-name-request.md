# V2 Registry Validate Name Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwVmFsaWRhdGUlMjUyME5hbWUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2RegistryValidateNameRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2RegistryValidateNameRequest } from 'digitalocean-apilib';

const v2RegistryValidateNameRequest: V2RegistryValidateNameRequest = {
  name: 'example',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



