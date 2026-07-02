# Static Site

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXRpY1NpdGU

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`StaticSite`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `build_command` | `str` | Optional | An optional build command to run while building this component from source. |
| `dockerfile_path` | `str` | Optional | The path to the Dockerfile relative to the root of the repo. If set, it will be used to build this component. Otherwise, App Platform will attempt to build it using buildpacks. |
| `environment_slug` | `str` | Optional | An environment slug describing the type of this app. For a full list, please refer to [the product documentation](https://www.digitalocean.com/docs/app-platform/). |
| `envs` | [`List[Env]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `git` | [`Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/git.md) | Optional | - |
| `github` | [`Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/github.md) | Optional | - |
| `gitlab` | [`Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/gitlab.md) | Optional | - |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `log_destinations` | [`ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/configurations-for-external-logging.md) | Optional | - |
| `name` | `str` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `run_command` | `str` | Optional | An optional run command to override the component's default. |
| `source_dir` | `str` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `catchall_document` | `str` | Optional | The name of the document to use as the fallback for any requests to documents that are not found when serving this static site. Only 1 of `catchall_document` or `error_document` can be set. |
| `cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/cors.md) | Optional | - |
| `error_document` | `str` | Optional | The name of the error document to use when serving this static site. Default: 404.html. If no such file exists within the built assets, App Platform will supply one.<br><br>**Default**: `"404.html"` |
| `index_document` | `str` | Optional | The name of the index document to use when serving this static site. Default: index.html<br><br>**Default**: `"index.html"` |
| `output_dir` | `str` | Optional | An optional path to where the built assets will be located, relative to the build context. If not set, App Platform will automatically scan for these directory names: `_static`, `dist`, `public`, `build`. |
| `routes` | [`List[ACriterionForRoutingHttpTrafficToAComponent]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.env import Env
from digitaloceanapi.models.git import Git
from digitaloceanapi.models.scope import Scope
from digitaloceanapi.models.static_site import StaticSite
from digitaloceanapi.models.type_2 import Type2

static_site = StaticSite(
    name='api',
    build_command='npm run build',
    dockerfile_path='path/to/Dockerfile',
    environment_slug='node-js',
    envs=[
        Env(
            key='key2',
            scope=Scope.UNSET,
            mtype=Type2.GENERAL,
            value='value4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Env(
            key='key2',
            scope=Scope.UNSET,
            mtype=Type2.GENERAL,
            value='value4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Env(
            key='key2',
            scope=Scope.UNSET,
            mtype=Type2.GENERAL,
            value='value4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    git=Git(
        branch='branch8',
        repo_clone_url='repo_clone_url8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    run_command='bin/api',
    source_dir='path/to/dir',
    catchall_document='index.html',
    error_document='error.html',
    index_document='main.html',
    output_dir='dist/',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



