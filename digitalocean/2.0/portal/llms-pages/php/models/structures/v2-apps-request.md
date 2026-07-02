# V2 Apps Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `projectId` | `?string` | Optional | The ID of the project the app should be assigned to. If omitted, it will be assigned to your default project. | getProjectId(): ?string | setProjectId(?string projectId): void |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/app-spec.md) | Required | The desired configuration of an application. | getSpec(): AppSpec | setSpec(AppSpec spec): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsRequestBuilder;
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

$v2AppsRequest = V2AppsRequestBuilder::init(
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
    ->projectId('project_id4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



