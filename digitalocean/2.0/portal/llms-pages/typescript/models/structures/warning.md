# Warning

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRldhcm5pbmc

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Warning`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | [`Code \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/code.md) | Optional | A code identifier that represents the failing condition.<br><br>Failing conditions:<br><br>- `incompatible_phase` - indicates that the deployment's phase is not suitable for rollback.<br>- `incompatible_result` - indicates that the deployment's result is not suitable for rollback.<br>- `exceeded_revision_limit` - indicates that the app has exceeded the rollback revision limits for its tier.<br>- `app_pinned` - indicates that there is already a rollback in progress and the app is pinned.<br>- `database_config_conflict` - indicates that the deployment's database config is different than the current config.<br>- `region_conflict` - indicates that the deployment's region differs from the current app region.<br><br>Warning conditions:<br><br>- `static_site_requires_rebuild` - indicates that the deployment contains at least one static site that will require a rebuild.<br>- `image_source_missing_digest` - indicates that the deployment contains at least one component with an image source that is missing a digest. |
| `components` | `string[] \| undefined` | Optional | - |
| `message` | `string \| undefined` | Optional | A human-readable message describing the failing condition. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Code, Warning } from 'digitalocean-apilib';

const warning: Warning = {
  code: Code.ExceededRevisionLimit,
  components: [
    'www'
  ],
  message: 'the deployment is past the maximum historical revision limit of 0 for the "starter" app tier',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



