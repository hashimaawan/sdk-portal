# Git

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkdpdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Git`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `branch` | `?string` | Optional | The name of the branch to use | getBranch(): ?string | setBranch(?string branch): void |
| `repoCloneUrl` | `?string` | Optional | The clone URL of the repo. Example: `https://github.com/digitalocean/sample-golang.git` | getRepoCloneUrl(): ?string | setRepoCloneUrl(?string repoCloneUrl): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\GitBuilder;
use DigitalOceanApiLib\ApiHelper;

$git = GitBuilder::init()
    ->branch('main')
    ->repoCloneUrl('https://github.com/digitalocean/sample-golang.git')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



