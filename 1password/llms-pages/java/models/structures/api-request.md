# API Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkFQSVJlcXVlc3Q

Represents a request that was made to the API. Including what Token was used and what resource was accessed.

*This model accepts additional fields of type Object.*


# Class Name

`ApiRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `Actor` | [`Actor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/actor.md) | Optional | - | Actor getActor() | setActor(Actor actor) |
| `RequestId` | `UUID` | Optional | The unique id used to identify a single request. | UUID getRequestId() | setRequestId(UUID requestId) |
| `Resource` | [`Resource`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/resource.md) | Optional | - | Resource getResource() | setResource(Resource resource) |
| `Result` | [`Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/result.md) | Optional | - | Result getResult() | setResult(Result result) |
| `Timestamp` | `LocalDateTime` | Optional, Read-only | The time at which the request was processed by the server. | LocalDateTime getTimestamp() | setTimestamp(LocalDateTime timestamp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import java.util.UUID;
import local.m1password.ApiHelper;
import local.m1password.models.Action;
import local.m1password.models.Actor;
import local.m1password.models.ApiRequest;
import local.m1password.models.Item2;
import local.m1password.models.Resource;
import local.m1password.models.Result;
import local.m1password.models.Type;
import local.m1password.models.Vault3;

ApiRequest apiRequest = new ApiRequest.Builder()
    .action(Action.READ)
    .actor(new Actor.Builder()
        .account("account0")
        .id(UUID.fromString("0000193c-0000-0000-0000-000000000000"))
        .jti("jti2")
        .requestIp("requestIp4")
        .userAgent("userAgent6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .requestId(UUID.fromString("000002a8-0000-0000-0000-000000000000"))
    .resource(new Resource.Builder()
        .item(new Item2.Builder()
            .id("id2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .itemVersion(108)
        .type(Type.ITEM)
        .vault(new Vault3.Builder()
            .id("id6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .result(Result.SUCCESS)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



