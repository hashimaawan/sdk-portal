# V2 Apps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apps` | [`Array[AListOfApp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/a-list-of-app.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_response = V2AppsResponse.new(
  meta: Meta.new(
    total: 1,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  apps: [
    AListOfApp.new(
      spec: AppSpec.new(
        name: 'name2',
        databases: [
          Database.new(
            name: 'name6',
            cluster_name: 'cluster_name8',
            db_name: 'db_name0',
            db_user: 'db_user8',
            engine: Engine::PG,
            production: false,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        domains: [
          Domain.new(
            domain: 'domain6',
            minimum_tls_version: MinimumTlsVersion::ENUM_12,
            type: Type1::PRIMARY,
            wildcard: false,
            zone: 'zone2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          Domain.new(
            domain: 'domain6',
            minimum_tls_version: MinimumTlsVersion::ENUM_12,
            type: Type1::PRIMARY,
            wildcard: false,
            zone: 'zone2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        functions: [
          Function.new(
            name: 'name4',
            alerts: [
              Alert.new(
                disabled: false,
                operator: Operator::LESS_THAN,
                rule: Rule::MEM_UTILIZATION,
                value: 12.58,
                window: Window::THIRTY_MINUTES,
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              )
            ],
            cors: Cors.new(
              allow_credentials: false,
              allow_headers: [
                'allow_headers9',
                'allow_headers0'
              ],
              allow_methods: [
                'allow_methods8',
                'allow_methods9',
                'allow_methods0'
              ],
              allow_origins: [
                nil
              ],
              expose_headers: [
                'expose_headers2'
              ],
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            envs: [
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              )
            ],
            git: Git.new(
              branch: 'branch8',
              repo_clone_url: 'repo_clone_url8',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            github: Github.new(
              branch: 'branch4',
              deploy_on_push: false,
              repo: 'repo6',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        jobs: [
          Job.new(
            name: 'name4',
            build_command: 'build_command8',
            dockerfile_path: 'dockerfile_path6',
            environment_slug: 'environment_slug2',
            envs: [
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              )
            ],
            git: Git.new(
              branch: 'branch8',
              repo_clone_url: 'repo_clone_url8',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        region: Region1::BLR,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      active_deployment: AnAppDeployment.new(
        cause: 'cause6',
        cloned_from: 'cloned_from2',
        created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        functions: [
          FunctionsComponentsThatArePartOfThisDeployment.new(
            name: 'name4',
            namespace: 'namespace8',
            source_commit_hash: 'source_commit_hash4',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          FunctionsComponentsThatArePartOfThisDeployment.new(
            name: 'name4',
            namespace: 'namespace8',
            source_commit_hash: 'source_commit_hash4',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          FunctionsComponentsThatArePartOfThisDeployment.new(
            name: 'name4',
            namespace: 'namespace8',
            source_commit_hash: 'source_commit_hash4',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        id: 'id0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      default_ingress: 'default_ingress2',
      domains: [
        ContainsAllDomainsForTheApp.new(
          certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
          id: 'id0',
          phase: Phase1::CONFIGURING,
          progress: Progress1.new(
            steps: [
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' }
            ],
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          rotate_validation_records: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        ContainsAllDomainsForTheApp.new(
          certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
          id: 'id0',
          phase: Phase1::CONFIGURING,
          progress: Progress1.new(
            steps: [
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' }
            ],
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          rotate_validation_records: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        ContainsAllDomainsForTheApp.new(
          certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
          id: 'id0',
          phase: Phase1::CONFIGURING,
          progress: Progress1.new(
            steps: [
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' }
            ],
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          rotate_validation_records: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      id: 'id6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AListOfApp.new(
      spec: AppSpec.new(
        name: 'name2',
        databases: [
          Database.new(
            name: 'name6',
            cluster_name: 'cluster_name8',
            db_name: 'db_name0',
            db_user: 'db_user8',
            engine: Engine::PG,
            production: false,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        domains: [
          Domain.new(
            domain: 'domain6',
            minimum_tls_version: MinimumTlsVersion::ENUM_12,
            type: Type1::PRIMARY,
            wildcard: false,
            zone: 'zone2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          Domain.new(
            domain: 'domain6',
            minimum_tls_version: MinimumTlsVersion::ENUM_12,
            type: Type1::PRIMARY,
            wildcard: false,
            zone: 'zone2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        functions: [
          Function.new(
            name: 'name4',
            alerts: [
              Alert.new(
                disabled: false,
                operator: Operator::LESS_THAN,
                rule: Rule::MEM_UTILIZATION,
                value: 12.58,
                window: Window::THIRTY_MINUTES,
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              )
            ],
            cors: Cors.new(
              allow_credentials: false,
              allow_headers: [
                'allow_headers9',
                'allow_headers0'
              ],
              allow_methods: [
                'allow_methods8',
                'allow_methods9',
                'allow_methods0'
              ],
              allow_origins: [
                nil
              ],
              expose_headers: [
                'expose_headers2'
              ],
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            envs: [
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              )
            ],
            git: Git.new(
              branch: 'branch8',
              repo_clone_url: 'repo_clone_url8',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            github: Github.new(
              branch: 'branch4',
              deploy_on_push: false,
              repo: 'repo6',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        jobs: [
          Job.new(
            name: 'name4',
            build_command: 'build_command8',
            dockerfile_path: 'dockerfile_path6',
            environment_slug: 'environment_slug2',
            envs: [
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              ),
              Env.new(
                key: 'key2',
                scope: Scope::UNSET,
                type: Type2::GENERAL,
                value: 'value4',
                additional_properties: {
                  'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
                }
              )
            ],
            git: Git.new(
              branch: 'branch8',
              repo_clone_url: 'repo_clone_url8',
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        region: Region1::BLR,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      active_deployment: AnAppDeployment.new(
        cause: 'cause6',
        cloned_from: 'cloned_from2',
        created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        functions: [
          FunctionsComponentsThatArePartOfThisDeployment.new(
            name: 'name4',
            namespace: 'namespace8',
            source_commit_hash: 'source_commit_hash4',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          FunctionsComponentsThatArePartOfThisDeployment.new(
            name: 'name4',
            namespace: 'namespace8',
            source_commit_hash: 'source_commit_hash4',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          FunctionsComponentsThatArePartOfThisDeployment.new(
            name: 'name4',
            namespace: 'namespace8',
            source_commit_hash: 'source_commit_hash4',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        id: 'id0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      default_ingress: 'default_ingress2',
      domains: [
        ContainsAllDomainsForTheApp.new(
          certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
          id: 'id0',
          phase: Phase1::CONFIGURING,
          progress: Progress1.new(
            steps: [
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' }
            ],
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          rotate_validation_records: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        ContainsAllDomainsForTheApp.new(
          certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
          id: 'id0',
          phase: Phase1::CONFIGURING,
          progress: Progress1.new(
            steps: [
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' }
            ],
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          rotate_validation_records: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        ContainsAllDomainsForTheApp.new(
          certificate_expires_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
          id: 'id0',
          phase: Phase1::CONFIGURING,
          progress: Progress1.new(
            steps: [
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' },
              { 'key1' => 'val1', 'key2' => 'val2' }
            ],
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          rotate_validation_records: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      id: 'id6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  links: Links.new(
    pages: Pages.new(
      last: 'last6',
      mnext: 'next2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



