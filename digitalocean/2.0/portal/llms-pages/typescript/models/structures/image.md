# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `registry` | `string \| undefined` | Optional | The registry name. Must be left empty for the `DOCR` registry type. |
| `registryType` | [`RegistryType \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/registry-type.md) | Optional | - DOCKER_HUB: The DockerHub container registry type.<br>- DOCR: The DigitalOcean container registry type. |
| `repository` | `string \| undefined` | Optional | The repository name. |
| `tag` | `string \| undefined` | Optional | The repository tag. Defaults to `latest` if not provided.<br><br>**Default**: `'latest'` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Image, RegistryType } from 'digitalocean-apilib';

const image: Image = {
  registry: 'registry.hub.docker.com',
  registryType: RegistryType.Docr,
  repository: 'origin/master',
  tag: 'latest',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



