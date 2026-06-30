# Servers Actions Attach Iso Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEF0dGFjaCUyNTIwSXNvJTI1MjBSZXF1ZXN0


# Class Name

`ServersActionsAttachIsoRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | `String` | Required | ID or name of ISO to attach to the Server as listed in GET `/isos` |


# Example

```ruby
servers_actions_attach_iso_request = ServersActionsAttachIsoRequest.new(
  'FreeBSD-11.0-RELEASE-amd64-dvd1'
)
```



