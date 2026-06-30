# Error Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkVycm9yUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`ErrorResponseException`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Message` | `*string` | Optional | A message detailing the error |
| `Status` | `*int` | Optional | HTTP Status Code |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
if err != nil {
    switch typedErr := err.(type) {
    case *errors.ErrorResponseException:
        log.Fatalln(typedErr)
    default:
        log.Fatalln(err)
    }
}
```



