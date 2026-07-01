# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | Description of the Image, will be auto-generated if not set | String getDescription() | setDescription(String description) |
| `Labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) | Labels getLabels() | setLabels(Labels labels) |
| `Type` | [`Type63Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) | Type63Enum getType() | setType(Type63Enum type) |


# Example

```java
import cloud.hetzner.api.models.CreateImageRequest;
import cloud.hetzner.api.models.Labels;
import cloud.hetzner.api.models.Type63Enum;

CreateImageRequest createImageRequest = new CreateImageRequest.Builder()
    .description("my image")
    .labels(new Labels.Builder()
        .labelkey("labelkey4")
        .build())
    .type(Type63Enum.SNAPSHOT)
    .build();
```



