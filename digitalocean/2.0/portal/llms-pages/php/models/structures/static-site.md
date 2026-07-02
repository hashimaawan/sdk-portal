# Static Site

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRpY1NpdGU

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`StaticSite`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `buildCommand` | `?string` | Optional | An optional build command to run while building this component from source. | getBuildCommand(): ?string | setBuildCommand(?string buildCommand): void |
| `dockerfilePath` | `?string` | Optional | The path to the Dockerfile relative to the root of the repo. If set, it will be used to build this component. Otherwise, App Platform will attempt to build it using buildpacks. | getDockerfilePath(): ?string | setDockerfilePath(?string dockerfilePath): void |
| `environmentSlug` | `?string` | Optional | An environment slug describing the type of this app. For a full list, please refer to [the product documentation](https://www.digitalocean.com/docs/app-platform/). | getEnvironmentSlug(): ?string | setEnvironmentSlug(?string environmentSlug): void |
| `envs` | [`?(Env[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/env.md) | Optional | A list of environment variables made available to the component. | getEnvs(): ?array | setEnvs(?array envs): void |
| `git` | [`?Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/git.md) | Optional | - | getGit(): ?Git | setGit(?Git git): void |
| `github` | [`?Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/github.md) | Optional | - | getGithub(): ?Github | setGithub(?Github github): void |
| `gitlab` | [`?Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/gitlab.md) | Optional | - | getGitlab(): ?Gitlab | setGitlab(?Gitlab gitlab): void |
| `image` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getImage(): ?Image | setImage(?Image image): void |
| `logDestinations` | [`?ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/configurations-for-external-logging.md) | Optional | - | getLogDestinations(): ?ConfigurationsForExternalLogging | setLogDestinations(?ConfigurationsForExternalLogging logDestinations): void |
| `name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | getName(): string | setName(string name): void |
| `runCommand` | `?string` | Optional | An optional run command to override the component's default. | getRunCommand(): ?string | setRunCommand(?string runCommand): void |
| `sourceDir` | `?string` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. | getSourceDir(): ?string | setSourceDir(?string sourceDir): void |
| `catchallDocument` | `?string` | Optional | The name of the document to use as the fallback for any requests to documents that are not found when serving this static site. Only 1 of `catchall_document` or `error_document` can be set. | getCatchallDocument(): ?string | setCatchallDocument(?string catchallDocument): void |
| `cors` | [`?Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/cors.md) | Optional | - | getCors(): ?Cors | setCors(?Cors cors): void |
| `errorDocument` | `?string` | Optional | The name of the error document to use when serving this static site. Default: 404.html. If no such file exists within the built assets, App Platform will supply one.<br><br>**Default**: `'404.html'` | getErrorDocument(): ?string | setErrorDocument(?string errorDocument): void |
| `indexDocument` | `?string` | Optional | The name of the index document to use when serving this static site. Default: index.html<br><br>**Default**: `'index.html'` | getIndexDocument(): ?string | setIndexDocument(?string indexDocument): void |
| `outputDir` | `?string` | Optional | An optional path to where the built assets will be located, relative to the build context. If not set, App Platform will automatically scan for these directory names: `_static`, `dist`, `public`, `build`. | getOutputDir(): ?string | setOutputDir(?string outputDir): void |
| `routes` | [`?(ACriterionForRoutingHttpTrafficToAComponent[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. | getRoutes(): ?array | setRoutes(?array routes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\StaticSiteBuilder;
use DigitalOceanApiLib\Models\Builders\EnvBuilder;
use DigitalOceanApiLib\Models\Scope;
use DigitalOceanApiLib\Models\Type2;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\GitBuilder;

$staticSite = StaticSiteBuilder::init(
    'api'
)
    ->buildCommand('npm run build')
    ->dockerfilePath('path/to/Dockerfile')
    ->environmentSlug('node-js')
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
    ->runCommand('bin/api')
    ->sourceDir('path/to/dir')
    ->catchallDocument('index.html')
    ->errorDocument('error.html')
    ->indexDocument('main.html')
    ->outputDir('dist/')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



