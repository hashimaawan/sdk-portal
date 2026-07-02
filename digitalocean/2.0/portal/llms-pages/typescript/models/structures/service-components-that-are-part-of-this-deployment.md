# Service Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZpY2UlMjUyMGNvbXBvbmVudHMlMjUyMHRoYXQlMjUyMGFyZSUyNTIwcGFydCUyNTIwb2YlMjUyMHRoaXMlMjUyMGRlcGxveW1lbnQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ServiceComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | - |
| `sourceCommitHash` | `string \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  ServiceComponentsThatArePartOfThisDeployment,
} from 'digitalocean-apilib';

const serviceComponentsThatArePartOfThisDeployment: ServiceComponentsThatArePartOfThisDeployment = {
  name: 'web',
  sourceCommitHash: '54d4a727f457231062439895000d45437c7bb405',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



