# Functions Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkZ1bmN0aW9ucyUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`FunctionsComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `namespace` | `?string` | Optional | The namespace where the functions are deployed. | getNamespace(): ?string | setNamespace(?string namespace): void |
| `sourceCommitHash` | `?string` | Optional | The commit hash of the repository that was used to build this functions component. | getSourceCommitHash(): ?string | setSourceCommitHash(?string sourceCommitHash): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\FunctionsComponentsThatArePartOfThisDeploymentBuilder;
use DigitalOceanApiLib\ApiHelper;

$functionsComponentsThatArePartOfThisDeployment = FunctionsComponentsThatArePartOfThisDeploymentBuilder::init()
    ->name('my-functions-component')
    ->namespace('ap-b2a93513-8d9b-4223-9d61-5e7272c81c32')
    ->sourceCommitHash('54d4a727f457231062439895000d45437c7bb405')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



