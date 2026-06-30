# Label Selector 12

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3IxMg

Configuration for label selector targets, required if type is `label_selector`


# Class Name

`LabelSelector12`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selector` | `String` | Required | Label selector | String getSelector() | setSelector(String selector) |


# Example

```java
import cloud.hetzner.api.models.LabelSelector12;

LabelSelector12 labelSelector12 = new LabelSelector12.Builder(
    "env=prod"
)
.build();
```



