# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_firewall_response = CreateFirewallResponse.new(
  actions: [
    Action.new(
      command: 'set_firewall_rules',
      error: Error.new(
        code: 'action_failed',
        message: 'Action failed',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      finished: '2016-01-30T23:56:00+00:00',
      id: 13,
      progress: 100,
      resources: [
        Resource.new(
          id: 38,
          type: 'firewall',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: Status::SUCCESS,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Action.new(
      command: 'apply_firewall',
      error: Error.new(
        code: 'action_failed',
        message: 'Action failed',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      finished: '2016-01-30T23:56:00+00:00',
      id: 14,
      progress: 100,
      resources: [
        Resource.new(
          id: 42,
          type: 'server',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Resource.new(
          id: 38,
          type: 'firewall',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: Status::SUCCESS,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  firewall: Firewall.new(
    applied_to: [
      AppliedTo.new(
        type: Type6::SERVER,
        applied_to_resources: [
          AppliedToResource.new(
            server: Server.new(
              id: 14,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            type: Type5::SERVER,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        label_selector: LabelSelector.new(
          selector: 'selector8',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        server: Server.new(
          id: 14,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      AppliedTo.new(
        type: Type6::SERVER,
        applied_to_resources: [
          AppliedToResource.new(
            server: Server.new(
              id: 14,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            type: Type5::SERVER,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        label_selector: LabelSelector.new(
          selector: 'selector8',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        server: Server.new(
          id: 14,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    created: 'created6',
    id: 4,
    name: 'name6',
    rules: [
      Rule.new(
        direction: Direction::ENUM_IN,
        protocol: Protocol::UDP,
        description: 'description2',
        destination_ips: [
          'destination_ips1',
          'destination_ips2',
          'destination_ips3'
        ],
        port: 'port8',
        source_ips: [
          'source_ips1',
          'source_ips2',
          'source_ips3'
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    labels: {
      'key0' => 'labels2',
      'key1' => 'labels1'
    },
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



