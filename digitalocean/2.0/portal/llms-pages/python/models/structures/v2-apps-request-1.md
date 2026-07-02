# V2 Apps Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alert import Alert
from digitaloceanapi.models.app_spec import AppSpec
from digitaloceanapi.models.cors import Cors
from digitaloceanapi.models.database import Database
from digitaloceanapi.models.domain import Domain
from digitaloceanapi.models.engine import Engine
from digitaloceanapi.models.env import Env
from digitaloceanapi.models.function import Function
from digitaloceanapi.models.git import Git
from digitaloceanapi.models.github import Github
from digitaloceanapi.models.job import Job
from digitaloceanapi.models.minimum_tls_version import MinimumTlsVersion
from digitaloceanapi.models.operator import Operator
from digitaloceanapi.models.region_1 import Region1
from digitaloceanapi.models.rule import Rule
from digitaloceanapi.models.scope import Scope
from digitaloceanapi.models.type_1 import Type1
from digitaloceanapi.models.type_2 import Type2
from digitaloceanapi.models.v_2_apps_request_1 import V2AppsRequest1
from digitaloceanapi.models.window import Window

v_2_apps_request_1 = V2AppsRequest1(
    spec=AppSpec(
        name='web-app-01',
        databases=[
            Database(
                name='name6',
                cluster_name='cluster_name8',
                db_name='db_name0',
                db_user='db_user8',
                engine=Engine.PG,
                production=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        domains=[
            Domain(
                domain='domain6',
                minimum_tls_version=MinimumTlsVersion.ENUM_12,
                mtype=Type1.PRIMARY,
                wildcard=False,
                zone='zone2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Domain(
                domain='domain6',
                minimum_tls_version=MinimumTlsVersion.ENUM_12,
                mtype=Type1.PRIMARY,
                wildcard=False,
                zone='zone2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        functions=[
            Function(
                name='name4',
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
                github=Github(
                    branch='branch4',
                    deploy_on_push=False,
                    repo='repo6',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        jobs=[
            Job(
                name='name4',
                build_command='build_command8',
                dockerfile_path='dockerfile_path6',
                environment_slug='environment_slug2',
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
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        region=Region1.NYC,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



