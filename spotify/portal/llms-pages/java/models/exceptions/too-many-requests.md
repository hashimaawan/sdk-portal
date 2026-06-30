# Too Many Requests

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/java/x-redirect/JTI0bSUyRlRvb01hbnlSZXF1ZXN0cw

*This model accepts additional fields of type Object.*


# Class Name

`TooManyRequestsException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`ErrorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/java/models/structures/error-object.md) | Required | - | ErrorObject getError() | setError(ErrorObject error) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
try {
    // make the API call
} catch (TooManyRequestsException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



