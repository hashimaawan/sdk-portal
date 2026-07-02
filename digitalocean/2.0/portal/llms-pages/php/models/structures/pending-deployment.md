# Pending Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlBlbmRpbmdEZXBsb3ltZW50

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`PendingDeployment`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cause` | `?string` | Optional | - | getCause(): ?string | setCause(?string cause): void |
| `clonedFrom` | `?string` | Optional | - | getClonedFrom(): ?string | setClonedFrom(?string clonedFrom): void |
| `createdAt` | `?DateTime` | Optional | - | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `functions` | [`?(FunctionsComponentsThatArePartOfThisDeployment[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/functions-components-that-are-part-of-this-deployment.md) | Optional | - | getFunctions(): ?array | setFunctions(?array functions): void |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `jobs` | [`?(JobComponentsThatArePartOfThisDeployment[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/job-components-that-are-part-of-this-deployment.md) | Optional | - | getJobs(): ?array | setJobs(?array jobs): void |
| `phase` | [`?string(Phase)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/phase.md) | Optional | **Default**: `Phase::UNKNOWN` | getPhase(): ?string | setPhase(?string phase): void |
| `phaseLastUpdatedAt` | `?DateTime` | Optional | - | getPhaseLastUpdatedAt(): ?\DateTime | setPhaseLastUpdatedAt(?\DateTime phaseLastUpdatedAt): void |
| `progress` | [`?Progress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/progress.md) | Optional | - | getProgress(): ?Progress | setProgress(?Progress progress): void |
| `services` | [`?(ServiceComponentsThatArePartOfThisDeployment[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/service-components-that-are-part-of-this-deployment.md) | Optional | - | getServices(): ?array | setServices(?array services): void |
| `spec` | [`?AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/app-spec.md) | Optional | The desired configuration of an application. | getSpec(): ?AppSpec | setSpec(?AppSpec spec): void |
| `staticSites` | [`?(StaticSiteComponentsThatArePartOfThisDeployment[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/static-site-components-that-are-part-of-this-deployment.md) | Optional | - | getStaticSites(): ?array | setStaticSites(?array staticSites): void |
| `tierSlug` | `?string` | Optional, Read-only | - | getTierSlug(): ?string | setTierSlug(?string tierSlug): void |
| `updatedAt` | `?DateTime` | Optional | - | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `workers` | [`?(WorkerComponentsThatArePartOfThisDeployment[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/worker-components-that-are-part-of-this-deployment.md) | Optional | - | getWorkers(): ?array | setWorkers(?array workers): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\PendingDeploymentBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\FunctionsComponentsThatArePartOfThisDeploymentBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Phase;

$pendingDeployment = PendingDeploymentBuilder::init()
    ->cause('commit 9a4df0b pushed to github/digitalocean/sample-golang')
    ->clonedFrom('3aa4d20e-5527-4c00-b496-601fbd22520a')
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-07-28T18:00:00Z'))
    ->functions(
        [
            FunctionsComponentsThatArePartOfThisDeploymentBuilder::init()
                ->name('name4')
                ->namespace('namespace8')
                ->sourceCommitHash('source_commit_hash4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->id('b6bdf840-2854-4f87-a36c-5f231c617c84')
    ->phase(Phase::ACTIVE)
    ->phaseLastUpdatedAt(DateTimeHelper::fromRfc3339DateTime('0001-01-01T00:00:00Z'))
    ->tierSlug('basic')
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2020-07-28T18:00:00Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



