# V2 Apps Alerts Destinations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsAlertsDestinationsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alert` | [`Alert1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/alert-1.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Phase1,
  Status2,
  V2AppsAlertsDestinationsResponse,
} from 'digitalocean-apilib';

const v2AppsAlertsDestinationsResponse: V2AppsAlertsDestinationsResponse = {
  alert: {
    componentName: 'component_name2',
    emails: [
      'emails9'
    ],
    id: 'id0',
    phase: Phase1.Configuring,
    progress: {
      steps: [
        {
          endedAt: '2016-03-13T12:52:32.123Z',
          name: 'name2',
          reason: {
            code: 'code2',
            message: 'message4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          startedAt: '2016-03-13T12:52:32.123Z',
          status: Status2.Success,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          endedAt: '2016-03-13T12:52:32.123Z',
          name: 'name2',
          reason: {
            code: 'code2',
            message: 'message4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          startedAt: '2016-03-13T12:52:32.123Z',
          status: Status2.Success,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          endedAt: '2016-03-13T12:52:32.123Z',
          name: 'name2',
          reason: {
            code: 'code2',
            message: 'message4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          startedAt: '2016-03-13T12:52:32.123Z',
          status: Status2.Success,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
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



