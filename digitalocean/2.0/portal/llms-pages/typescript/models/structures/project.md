# Project

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb2plY3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Project`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was created. |
| `description` | `string \| undefined` | Optional | The description of the project. The maximum length is 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` |
| `environment` | [`MEnvironment \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/environment.md) | Optional | The environment of the project's resources. |
| `id` | `string \| undefined` | Optional, Read-only | The unique universal identifier of this project. |
| `name` | `string \| undefined` | Optional | The human-readable name for the project. The maximum length is 175 characters and the name must be unique.<br><br>**Constraints**: *Maximum Length*: `175` |
| `ownerId` | `number \| undefined` | Optional, Read-only | The integer id of the project owner. |
| `ownerUuid` | `string \| undefined` | Optional, Read-only | The unique universal identifier of the project owner. |
| `purpose` | `string \| undefined` | Optional | The purpose of the project. The maximum length is 255 characters. It can<br>have one of the following values:<br><br>- Just trying out DigitalOcean<br>- Class project / Educational purposes<br>- Website or blog<br>- Web Application<br>- Service or API<br>- Mobile Application<br>- Machine learning / AI / Data processing<br>- IoT<br>- Operational / Developer tooling<br><br>If another value for purpose is specified, for example, "your custom purpose",<br>your purpose will be stored as `Other: your custom purpose`.<br><br>**Constraints**: *Maximum Length*: `255` |
| `updatedAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the project was updated. |
| `isDefault` | `boolean \| undefined` | Optional | If true, all resources will be added to this project if no project is specified. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { MEnvironment, Project } from 'digitalocean-apilib';

const project: Project = {
  createdAt: '2018-09-27T20:10:35Z',
  description: 'My website API',
  environment: MEnvironment.Production,
  id: '4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679',
  name: 'my-web-api',
  ownerId: 258992,
  ownerUuid: '99525febec065ca37b2ffe4f852fd2b2581895e7',
  purpose: 'Service or API',
  updatedAt: '2018-09-27T20:10:35Z',
  isDefault: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



