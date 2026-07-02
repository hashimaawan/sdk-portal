# V2 Registry Docker Credentials Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRG9ja2VyJTI1MjBDcmVkZW50aWFscyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2RegistryDockerCredentialsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auths` | [`Auths \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/auths.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2RegistryDockerCredentialsResponse } from 'digitalocean-apilib';

const v2RegistryDockerCredentialsResponse: V2RegistryDockerCredentialsResponse = {
  auths: {
    registryDigitaloceanCom: {
      auth: 'auth0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



