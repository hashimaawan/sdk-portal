# V2 Apps Components Logs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBDb21wb25lbnRzJTI1MjBMb2dzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsComponentsLogsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `historicUrls` | `string[] \| undefined` | Optional | - |
| `liveUrl` | `string \| undefined` | Optional | A URL of the real-time live logs. This URL may use either the `https://` or `wss://` protocols and will keep pushing live logs as they become available. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsComponentsLogsResponse } from 'digitalocean-apilib';

const v2AppsComponentsLogsResponse: V2AppsComponentsLogsResponse = {
  historicUrls: [
    'historic_urls9',
    'historic_urls0',
    'historic_urls1'
  ],
  liveUrl: 'ws://logs/build',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



