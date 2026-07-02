# Registry Digitalocean Com

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlZ2lzdHJ5RGlnaXRhbG9jZWFuQ29t

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`RegistryDigitaloceanCom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auth` | `string \| undefined` | Optional | A base64 encoded string containing credentials for the container registry. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { RegistryDigitaloceanCom } from 'digitalocean-apilib';

const registryDigitaloceanCom: RegistryDigitaloceanCom = {
  auth: 'YjdkMDNhNjk0N2IyMTdlZmI2ZjNlYzNiZDM1MDQ1ODI6YjdkMDNhNjk0N2IyMTdlZmI2ZjNlYzNiZDM1MDQ1ODIK',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



