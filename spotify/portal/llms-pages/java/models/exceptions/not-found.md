# Not Found

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/java/x-redirect/JTI0bSUyRk5vdEZvdW5k

*This model accepts additional fields of type Object.*


# Class Name

`NotFoundException`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`ErrorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/java/models/structures/error-object.md) | Required | - | ErrorObject getError() | setError(ErrorObject error) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
try {
    // make the API call
} catch (NotFoundException e) {
    e.printStackTrace();
} catch (ApiException e) {
    e.printStackTrace();
}
```



