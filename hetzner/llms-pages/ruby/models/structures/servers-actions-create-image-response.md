# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/image.md) | Optional | - |


# Example

```ruby
servers_actions_create_image_response = ServersActionsCreateImageResponse.new(
  Action.new(
    'command6',
    Error.new(
      'code2',
      'message4'
    ),
    'finished0',
    238,
    143.26,
    [
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      )
    ],
    'started8',
    StatusEnum::RUNNING
  ),
  Image.new(
    186,
    'created6',
    CreatedFrom.new(
      60,
      'name6'
    ),
    'deleted4',
    'deprecated8',
    'description6',
    244.18,
    128,
    141.34,
    {
      'key0': 'labels4'
    },
    'name6',
    OsFlavorEnum::DEBIAN,
    'os_version4',
    Protection.new(
      false
    ),
    Status24Enum::UNAVAILABLE,
    Type22Enum::APP,
    false
  )
)
```



