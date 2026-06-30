# Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkVycm9yMg

If issuance or renewal reports `failed`, this property contains information about what happened


# Class Name

`Error2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `String` | Optional | - | String getCode() | setCode(String code) |
| `Message` | `String` | Optional | - | String getMessage() | setMessage(String message) |


# Example

```java
import cloud.hetzner.api.models.Error2;

Error2 error2 = new Error2.Builder()
    .code("code2")
    .message("message4")
    .build();
```



