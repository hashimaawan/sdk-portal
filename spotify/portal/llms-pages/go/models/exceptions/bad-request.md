# Bad Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkJhZFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`BadRequestException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`models.ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/error-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
if err != nil {
    switch typedErr := err.(type) {
    case *errors.BadRequestException:
        log.Fatalln(typedErr)
    default:
        log.Fatalln(err)
    }
}
```



