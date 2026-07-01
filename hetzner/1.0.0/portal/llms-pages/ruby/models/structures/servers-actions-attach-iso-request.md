# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | `String` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_actions_attach_iso_request = ServersActionsAttachIsoRequest.new(
  iso: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



