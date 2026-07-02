# V2 Apps Rollback Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsRollbackRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `deploymentId` | `?string` | Optional | The ID of the deployment to rollback to. | getDeploymentId(): ?string | setDeploymentId(?string deploymentId): void |
| `skipPin` | `?bool` | Optional | Whether to skip pinning the rollback deployment. If false, the rollback deployment will be pinned and any new deployments including Auto Deploy on Push hooks will be disabled until the rollback is either manually committed or reverted via the CommitAppRollback or RevertAppRollback endpoints respectively. If true, the rollback will be immediately committed and the app will remain unpinned. | getSkipPin(): ?bool | setSkipPin(?bool skipPin): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsRollbackRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsRollbackRequest = V2AppsRollbackRequestBuilder::init()
    ->deploymentId('3aa4d20e-5527-4c00-b496-601fbd22520a')
    ->skipPin(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



