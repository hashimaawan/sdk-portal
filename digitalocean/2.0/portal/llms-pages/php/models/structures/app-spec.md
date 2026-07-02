# App Spec

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFwcFNwZWM

The desired configuration of an application.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`AppSpec`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `databases` | [`?(Database[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/database.md) | Optional | Database instances which can provide persistence to workloads within the<br>application. | getDatabases(): ?array | setDatabases(?array databases): void |
| `domains` | [`?(Domain[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/domain.md) | Optional | A set of hostnames where the application will be available. | getDomains(): ?array | setDomains(?array domains): void |
| `functions` | [`?(MFunction[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/function.md) | Optional | Workloads which expose publicly-accessible HTTP services via Functions Components. | getFunctions(): ?array | setFunctions(?array functions): void |
| `jobs` | [`?(Job[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/job.md) | Optional | Pre and post deployment workloads which do not expose publicly-accessible HTTP routes. | getJobs(): ?array | setJobs(?array jobs): void |
| `name` | `string` | Required | The name of the app. Must be unique across all apps in the same account.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | getName(): string | setName(string name): void |
| `region` | [`?string(Region1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-1.md) | Optional | The slug form of the geographical origin of the app. Default: `nearest available` | getRegion(): ?string | setRegion(?string region): void |
| `services` | [`?(Service[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/service.md) | Optional | Workloads which expose publicly-accessible HTTP services. | getServices(): ?array | setServices(?array services): void |
| `staticSites` | [`?(StaticSite[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/static-site.md) | Optional | Content which can be rendered to static web assets. | getStaticSites(): ?array | setStaticSites(?array staticSites): void |
| `workers` | [`?(Worker[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/worker.md) | Optional | Workloads which do not expose publicly-accessible HTTP services. | getWorkers(): ?array | setWorkers(?array workers): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
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

$appSpec = AppSpecBuilder::init(
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
                ->build(),
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
                ->build(),
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
                ->build(),
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
    ->build();
```



