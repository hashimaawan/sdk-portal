# Function

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkZ1bmN0aW9u

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Function`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alerts` | [`List[Alert]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/alert.md) | Optional | - |
| `cors` | [`Cors`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/cors.md) | Optional | - |
| `envs` | [`List[Env]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/env.md) | Optional | A list of environment variables made available to the component. |
| `git` | [`Git`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/git.md) | Optional | - |
| `github` | [`Github`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/github.md) | Optional | - |
| `gitlab` | [`Gitlab`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/gitlab.md) | Optional | - |
| `log_destinations` | [`ConfigurationsForExternalLogging`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/configurations-for-external-logging.md) | Optional | - |
| `name` | `str` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `routes` | [`List[ACriterionForRoutingHttpTrafficToAComponent]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/a-criterion-for-routing-http-traffic-to-a-component.md) | Optional | A list of HTTP routes that should be routed to this component. |
| `source_dir` | `str` | Optional | An optional path to the working directory to use for the build. For Dockerfile builds, this will be used as the build context. Must be relative to the root of the repo. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alert import Alert
from digitaloceanapi.models.cors import Cors
from digitaloceanapi.models.env import Env
from digitaloceanapi.models.function import Function
from digitaloceanapi.models.git import Git
from digitaloceanapi.models.github import Github
from digitaloceanapi.models.operator import Operator
from digitaloceanapi.models.rule import Rule
from digitaloceanapi.models.scope import Scope
from digitaloceanapi.models.type_2 import Type2
from digitaloceanapi.models.window import Window

function = Function(
    name='api',
    alerts=[
        Alert(
            disabled=False,
            operator=Operator.LESS_THAN,
            rule=Rule.MEM_UTILIZATION,
            value=12.58,
            window=Window.THIRTY_MINUTES,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Alert(
            disabled=False,
            operator=Operator.LESS_THAN,
            rule=Rule.MEM_UTILIZATION,
            value=12.58,
            window=Window.THIRTY_MINUTES,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    cors=Cors(
        allow_credentials=False,
        allow_headers=[
            'allow_headers9',
            'allow_headers0'
        ],
        allow_methods=[
            'allow_methods8',
            'allow_methods9',
            'allow_methods0'
        ],
        allow_origins=[
            None
        ],
        expose_headers=[
            'expose_headers2'
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    envs=[
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
    github=Github(
        branch='branch4',
        deploy_on_push=False,
        repo='repo6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    source_dir='path/to/dir',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



