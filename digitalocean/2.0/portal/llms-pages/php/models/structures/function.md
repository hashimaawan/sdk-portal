# Function

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkZ1bmN0aW9u

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`MFunction`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `alerts` | [`?(Alert[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/alert.md) | Optional | - | getAlerts(): ?array | setAlerts(?array alerts): void |
| `cors` | [`?Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/cors.md) | Optional | - | getCors(): ?Cors | setCors(?Cors cors): void |
| `envs` | [`?(Env[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/env.md) | Optional | A list of environment variables made available to the component. | getEnvs(): ?array | setEnvs(?array envs): void |
| `git` | [`?Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/git.md) | Optional | - | getGit(): ?Git | setGit(?Git git): void |
| `github` | [`?Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/github.md) | Optional | - | getGithub(): ?Github | setGithub(?Github github): void |
| `gitlab` | [`?Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/gitlab.md) | Optional | - | getGitlab(): ?Gitlab | setGitlab(?Gitlab gitlab): void |
| `logDestinations` | [`?ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/configurations-for-external-logging.md) | Optional | - | getLogDestinations(): ?ConfigurationsForExternalLogging | setLogDestinations(?ConfigurationsForExternalLogging logDestinations): void |
| `name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | getName(): string | setName(string name): void |
| `routes` | [`?(ACriterionForRoutingHttpTrafficToAComponent[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. | getRoutes(): ?array | setRoutes(?array routes): void |
| `sourceDir` | `?string` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. | getSourceDir(): ?string | setSourceDir(?string sourceDir): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\MFunctionBuilder;
use DigitalOceanApiLib\Models\Builders\AlertBuilder;
use DigitalOceanApiLib\Models\Operator;
use DigitalOceanApiLib\Models\Rule;
use DigitalOceanApiLib\Models\Window;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\CorsBuilder;
use DigitalOceanApiLib\Models\Builders\EnvBuilder;
use DigitalOceanApiLib\Models\Scope;
use DigitalOceanApiLib\Models\Type2;
use DigitalOceanApiLib\Models\Builders\GitBuilder;
use DigitalOceanApiLib\Models\Builders\GithubBuilder;

$function = MFunctionBuilder::init(
    'api'
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
    ->sourceDir('path/to/dir')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



