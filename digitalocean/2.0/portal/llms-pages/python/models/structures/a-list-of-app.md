# A List of App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkElMjUyMGxpc3QlMjUyMG9mJTI1MjBhcHA

An application's configuration and status.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`AListOfApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active_deployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/an-app-deployment.md) | Optional | - |
| `created_at` | `datetime` | Optional, Read-only | - |
| `default_ingress` | `str` | Optional, Read-only | - |
| `domains` | [`List[ContainsAllDomainsForTheApp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/contains-all-domains-for-the-app.md) | Optional, Read-only | - |
| `id` | `str` | Optional, Read-only | - |
| `in_progress_deployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/an-app-deployment.md) | Optional | - |
| `last_deployment_created_at` | `datetime` | Optional, Read-only | - |
| `live_domain` | `str` | Optional, Read-only | - |
| `live_url` | `str` | Optional, Read-only | - |
| `live_url_base` | `str` | Optional, Read-only | - |
| `owner_uuid` | `str` | Optional, Read-only | - |
| `pending_deployment` | [`PendingDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pending-deployment.md) | Optional | - |
| `pinned_deployment` | [`PinnedDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pinned-deployment.md) | Optional | - |
| `project_id` | `str` | Optional, Read-only | - |
| `region` | [`GeographicalInformationAboutAnAppOrigin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/geographical-information-about-an-app-origin.md) | Optional | - |
| `spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/app-spec.md) | Required | The desired configuration of an application. |
| `tier_slug` | `str` | Optional, Read-only | - |
| `updated_at` | `datetime` | Optional, Read-only | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.a_list_of_app import AListOfApp
from digitaloceanapi.models.alert import Alert
from digitaloceanapi.models.an_app_deployment import AnAppDeployment
from digitaloceanapi.models.app_spec import AppSpec
from digitaloceanapi.models.contains_all_domains_for_the_app import ContainsAllDomainsForTheApp
from digitaloceanapi.models.cors import Cors
from digitaloceanapi.models.database import Database
from digitaloceanapi.models.domain import Domain
from digitaloceanapi.models.engine import Engine
from digitaloceanapi.models.env import Env
from digitaloceanapi.models.function import Function
from digitaloceanapi.models.functions_components_that_are_part_of_this_deployment import FunctionsComponentsThatArePartOfThisDeployment
from digitaloceanapi.models.git import Git
from digitaloceanapi.models.github import Github
from digitaloceanapi.models.job import Job
from digitaloceanapi.models.minimum_tls_version import MinimumTlsVersion
from digitaloceanapi.models.operator import Operator
from digitaloceanapi.models.phase_1 import Phase1
from digitaloceanapi.models.progress_1 import Progress1
from digitaloceanapi.models.region_1 import Region1
from digitaloceanapi.models.rule import Rule
from digitaloceanapi.models.scope import Scope
from digitaloceanapi.models.type_1 import Type1
from digitaloceanapi.models.type_2 import Type2
from digitaloceanapi.models.window import Window

a_list_of_app = AListOfApp(
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
    active_deployment=AnAppDeployment(
        cause='cause6',
        cloned_from='cloned_from2',
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        functions=[
            FunctionsComponentsThatArePartOfThisDeployment(
                name='name4',
                namespace='namespace8',
                source_commit_hash='source_commit_hash4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            FunctionsComponentsThatArePartOfThisDeployment(
                name='name4',
                namespace='namespace8',
                source_commit_hash='source_commit_hash4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            FunctionsComponentsThatArePartOfThisDeployment(
                name='name4',
                namespace='namespace8',
                source_commit_hash='source_commit_hash4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        id='id0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    created_at=dateutil.parser.parse('2020-11-19T20:27:18Z'),
    default_ingress='digitalocean.com',
    domains=[
        ContainsAllDomainsForTheApp(
            certificate_expires_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            id='id0',
            phase=Phase1.CONFIGURING,
            progress=Progress1(
                steps=[
                    jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                    jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                    jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            rotate_validation_records=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ContainsAllDomainsForTheApp(
            certificate_expires_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            id='id0',
            phase=Phase1.CONFIGURING,
            progress=Progress1(
                steps=[
                    jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                    jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                    jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            rotate_validation_records=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    id='4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
    last_deployment_created_at=dateutil.parser.parse('2020-11-19T20:27:18Z'),
    live_domain='live_domain',
    live_url='google.com',
    live_url_base='digitalocean.com',
    owner_uuid='4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
    project_id='88b72d1a-b78a-4d9f-9090-b53c4399073f',
    tier_slug='basic',
    updated_at=dateutil.parser.parse('2020-12-01T00:42:16Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



