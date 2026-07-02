# Datadog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFkb2c

DataDog configuration.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Datadog`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apiKey` | `string` | Required | Datadog API key. |
| `endpoint` | `string \| undefined` | Optional | Datadog HTTP log intake endpoint. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Datadog } from 'digitalocean-apilib';

const datadog: Datadog = {
  apiKey: 'abcdefghijklmnopqrstuvwxyz0123456789',
  endpoint: 'https://mydatadogendpoint.com',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



