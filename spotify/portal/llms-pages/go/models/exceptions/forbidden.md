# Forbidden

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkZvcmJpZGRlbg

*This model accepts additional fields of type interface{}.*


# Class Name

`ForbiddenException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`models.ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/error-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
if err != nil {
    switch typedErr := err.(type) {
    case *errors.ForbiddenException:
        log.Fatalln(typedErr)
    default:
        log.Fatalln(err)
    }
}
```



