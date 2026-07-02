# A List of App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkElMjUyMGxpc3QlMjUyMG9mJTI1MjBhcHA

An application's configuration and status.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`AListOfApp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `activeDeployment` | [`?AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/an-app-deployment.md) | Optional | - | getActiveDeployment(): ?AnAppDeployment | setActiveDeployment(?AnAppDeployment activeDeployment): void |
| `createdAt` | `?DateTime` | Optional, Read-only | - | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `defaultIngress` | `?string` | Optional, Read-only | - | getDefaultIngress(): ?string | setDefaultIngress(?string defaultIngress): void |
| `domains` | [`?(ContainsAllDomainsForTheApp[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/contains-all-domains-for-the-app.md) | Optional, Read-only | - | getDomains(): ?array | setDomains(?array domains): void |
| `id` | `?string` | Optional, Read-only | - | getId(): ?string | setId(?string id): void |
| `inProgressDeployment` | [`?AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/an-app-deployment.md) | Optional | - | getInProgressDeployment(): ?AnAppDeployment | setInProgressDeployment(?AnAppDeployment inProgressDeployment): void |
| `lastDeploymentCreatedAt` | `?DateTime` | Optional, Read-only | - | getLastDeploymentCreatedAt(): ?\DateTime | setLastDeploymentCreatedAt(?\DateTime lastDeploymentCreatedAt): void |
| `liveDomain` | `?string` | Optional, Read-only | - | getLiveDomain(): ?string | setLiveDomain(?string liveDomain): void |
| `liveUrl` | `?string` | Optional, Read-only | - | getLiveUrl(): ?string | setLiveUrl(?string liveUrl): void |
| `liveUrlBase` | `?string` | Optional, Read-only | - | getLiveUrlBase(): ?string | setLiveUrlBase(?string liveUrlBase): void |
| `ownerUuid` | `?string` | Optional, Read-only | - | getOwnerUuid(): ?string | setOwnerUuid(?string ownerUuid): void |
| `pendingDeployment` | [`?PendingDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pending-deployment.md) | Optional | - | getPendingDeployment(): ?PendingDeployment | setPendingDeployment(?PendingDeployment pendingDeployment): void |
| `pinnedDeployment` | [`?PinnedDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pinned-deployment.md) | Optional | - | getPinnedDeployment(): ?PinnedDeployment | setPinnedDeployment(?PinnedDeployment pinnedDeployment): void |
| `projectId` | `?string` | Optional, Read-only | - | getProjectId(): ?string | setProjectId(?string projectId): void |
| `region` | [`?GeographicalInformationAboutAnAppOrigin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/geographical-information-about-an-app-origin.md) | Optional | - | getRegion(): ?GeographicalInformationAboutAnAppOrigin | setRegion(?GeographicalInformationAboutAnAppOrigin region): void |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/app-spec.md) | Required | The desired configuration of an application. | getSpec(): AppSpec | setSpec(AppSpec spec): void |
| `tierSlug` | `?string` | Optional, Read-only | - | getTierSlug(): ?string | setTierSlug(?string tierSlug): void |
| `updatedAt` | `?DateTime` | Optional, Read-only | - | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AListOfAppBuilder;
use DigitalOceanApiLib\Models\Builders\AppSpecBuilder;
use DigitalOceanApiLib\Models\Builders\DatabaseBuilder;
use DigitalOceanApiLib\Models\Engine;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\DomainBuilder;
use DigitalOceanApiLib\Models\MinimumTlsVersion;
use DigitalOceanApiLib\Models\Type1;
use DigitalOceanApiLib\Models\Builders\MFunctionBuilder;
use DigitalOceanApiLib\Models\Builders\AlertBuilder;
use DigitalOceanApiLib\Models\Operator;
use DigitalOceanApiLib\Models\Rule;
use DigitalOceanApiLib\Models\Window;
use DigitalOceanApiLib\Models\Builders\CorsBuilder;
use DigitalOceanApiLib\Models\Builders\EnvBuilder;
use DigitalOceanApiLib\Models\Scope;
use DigitalOceanApiLib\Models\Type2;
use DigitalOceanApiLib\Models\Builders\GitBuilder;
use DigitalOceanApiLib\Models\Builders\GithubBuilder;
use DigitalOceanApiLib\Models\Builders\JobBuilder;
use DigitalOceanApiLib\Models\Region1;
use DigitalOceanApiLib\Models\Builders\AnAppDeploymentBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\FunctionsComponentsThatArePartOfThisDeploymentBuilder;
use DigitalOceanApiLib\Models\Builders\ContainsAllDomainsForTheAppBuilder;
use DigitalOceanApiLib\Models\Phase1;
use DigitalOceanApiLib\Models\Builders\Progress1Builder;

$aListOfApp = AListOfAppBuilder::init(
    AppSpecBuilder::init(
        'web-app-01'
    )
        ->databases(
            [
                DatabaseBuilder::init(
                    'name6'
                )
                    ->clusterName('cluster_name8')
                    ->dbName('db_name0')
                    ->dbUser('db_user8')
                    ->engine(Engine::PG)
                    ->production(false)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
        ->domains(
            [
                DomainBuilder::init(
                    'domain6'
                )
                    ->minimumTlsVersion(MinimumTlsVersion::ENUM_12)
                    ->type(Type1::PRIMARY)
                    ->wildcard(false)
                    ->zone('zone2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                DomainBuilder::init(
                    'domain6'
                )
                    ->minimumTlsVersion(MinimumTlsVersion::ENUM_12)
                    ->type(Type1::PRIMARY)
                    ->wildcard(false)
                    ->zone('zone2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
        ->functions(
            [
                MFunctionBuilder::init(
                    'name4'
                )
                    ->alerts(
                        [
                            AlertBuilder::init()
                                ->disabled(false)
                                ->operator(Operator::LESS_THAN)
                                ->rule(Rule::MEM_UTILIZATION)
                                ->value(12.58)
                                ->window(Window::THIRTY_MINUTES)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->cors(
                        CorsBuilder::init()
                            ->allowCredentials(false)
                            ->allowHeaders(
                                [
                                    'allow_headers9',
                                    'allow_headers0'
                                ]
                            )
                            ->allowMethods(
                                [
                                    'allow_methods8',
                                    'allow_methods9',
                                    'allow_methods0'
                                ]
                            )
                            ->allowOrigins(
                                [
                                    null
                                ]
                            )
                            ->exposeHeaders(
                                [
                                    'expose_headers2'
                                ]
                            )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->envs(
                        [
                            EnvBuilder::init(
                                'key2'
                            )
                                ->scope(Scope::UNSET_)
                                ->type(Type2::GENERAL)
                                ->value('value4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            EnvBuilder::init(
                                'key2'
                            )
                                ->scope(Scope::UNSET_)
                                ->type(Type2::GENERAL)
                                ->value('value4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            EnvBuilder::init(
                                'key2'
                            )
                                ->scope(Scope::UNSET_)
                                ->type(Type2::GENERAL)
                                ->value('value4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->git(
                        GitBuilder::init()
                            ->branch('branch8')
                            ->repoCloneUrl('repo_clone_url8')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->github(
                        GithubBuilder::init()
                            ->branch('branch4')
                            ->deployOnPush(false)
                            ->repo('repo6')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
        ->jobs(
            [
                JobBuilder::init(
                    'name4'
                )
                    ->buildCommand('build_command8')
                    ->dockerfilePath('dockerfile_path6')
                    ->environmentSlug('environment_slug2')
                    ->envs(
                        [
                            EnvBuilder::init(
                                'key2'
                            )
                                ->scope(Scope::UNSET_)
                                ->type(Type2::GENERAL)
                                ->value('value4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            EnvBuilder::init(
                                'key2'
                            )
                                ->scope(Scope::UNSET_)
                                ->type(Type2::GENERAL)
                                ->value('value4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            EnvBuilder::init(
                                'key2'
                            )
                                ->scope(Scope::UNSET_)
                                ->type(Type2::GENERAL)
                                ->value('value4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->git(
                        GitBuilder::init()
                            ->branch('branch8')
                            ->repoCloneUrl('repo_clone_url8')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
        ->region(Region1::NYC)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->activeDeployment(
        AnAppDeploymentBuilder::init()
            ->cause('cause6')
            ->clonedFrom('cloned_from2')
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->functions(
                [
                    FunctionsComponentsThatArePartOfThisDeploymentBuilder::init()
                        ->name('name4')
                        ->namespace('namespace8')
                        ->sourceCommitHash('source_commit_hash4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    FunctionsComponentsThatArePartOfThisDeploymentBuilder::init()
                        ->name('name4')
                        ->namespace('namespace8')
                        ->sourceCommitHash('source_commit_hash4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    FunctionsComponentsThatArePartOfThisDeploymentBuilder::init()
                        ->name('name4')
                        ->namespace('namespace8')
                        ->sourceCommitHash('source_commit_hash4')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->id('id0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-11-19T20:27:18Z'))
    ->defaultIngress('digitalocean.com')
    ->domains(
        [
            ContainsAllDomainsForTheAppBuilder::init()
                ->certificateExpiresAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->id('id0')
                ->phase(Phase1::CONFIGURING)
                ->progress(
                    Progress1Builder::init()
                        ->steps(
                            [
                                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'),
                                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'),
                                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
                            ]
                        )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->rotateValidationRecords(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->id('4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf')
    ->lastDeploymentCreatedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-19T20:27:18Z'))
    ->liveDomain('live_domain')
    ->liveUrl('google.com')
    ->liveUrlBase('digitalocean.com')
    ->ownerUuid('4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf')
    ->projectId('88b72d1a-b78a-4d9f-9090-b53c4399073f')
    ->tierSlug('basic')
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2020-12-01T00:42:16Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



