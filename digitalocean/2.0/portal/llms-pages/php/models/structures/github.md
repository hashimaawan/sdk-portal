# Github

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkdpdGh1Yg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Github`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `branch` | `?string` | Optional | The name of the branch to use | getBranch(): ?string | setBranch(?string branch): void |
| `deployOnPush` | `?bool` | Optional | Whether to automatically deploy new commits made to the repo | getDeployOnPush(): ?bool | setDeployOnPush(?bool deployOnPush): void |
| `repo` | `?string` | Optional | The name of the repo in the format owner/repo. Example: `digitalocean/sample-golang` | getRepo(): ?string | setRepo(?string repo): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\GithubBuilder;
use DigitalOceanApiLib\ApiHelper;

$github = GithubBuilder::init()
    ->branch('main')
    ->deployOnPush(true)
    ->repo('digitalocean/sample-golang')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



