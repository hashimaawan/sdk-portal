# V2 Tags 400 Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjA0MDAlMjUyMEVycm9y

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2Tags400ErrorException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | `string` | Required | A message providing information about the error. |
| `Messages` | `models.Optional[[]string]` | Optional | A list of error messages. |
| `RootCauses` | `[]string` | Required | A list of underlying causes for the error, including details to help  resolve it when possible. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
if err != nil {
    switch typedErr := err.(type) {
    case *errors.V2Tags400ErrorException:
        log.Fatalln(typedErr)
    default:
        log.Fatalln(err)
    }
}
```



