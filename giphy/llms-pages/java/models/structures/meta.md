# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/java/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Msg` | `String` | Optional | HTTP Response Message | String getMsg() | setMsg(String msg) |
| `ResponseId` | `String` | Optional | A unique ID paired with this response from the API. | String getResponseId() | setResponseId(String responseId) |
| `Status` | `Integer` | Optional | HTTP Response Code | Integer getStatus() | setStatus(Integer status) |


# Example

```java
import com.giphy.api.models.Meta;

Meta meta = new Meta.Builder()
    .msg("OK")
    .responseId("57eea03c72381f86e05c35d2")
    .status(200)
    .build();
```



