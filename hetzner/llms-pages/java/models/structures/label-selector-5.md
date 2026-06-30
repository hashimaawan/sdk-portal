# Label Selector 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I1

Configuration for type label_selector, required if type is `label_selector`


# Class Name

`LabelSelector5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selector` | `String` | Required | Label selector | String getSelector() | setSelector(String selector) |


# Example

```java
import cloud.hetzner.api.models.LabelSelector5;

LabelSelector5 labelSelector5 = new LabelSelector5.Builder(
    "env=prod"
)
.build();
```



