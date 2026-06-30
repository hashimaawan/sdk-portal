# Unauthorized

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRlVuYXV0aG9yaXplZA

*This model accepts additional fields of type interface{}.*


# Class Name

`UnauthorizedException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`models.ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/error-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
if err != nil {
    switch typedErr := err.(type) {
    case *errors.UnauthorizedException:
        log.Fatalln(typedErr)
    default:
        log.Fatalln(err)
    }
}
```



