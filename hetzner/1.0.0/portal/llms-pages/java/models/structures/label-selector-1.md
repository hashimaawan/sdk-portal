# Label Selector 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3Ix

Configuration for type LabelSelector, required if type is `label_selector`


# Class Name

`LabelSelector1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Selector` | `String` | Required | Label selector | String getSelector() | setSelector(String selector) |


# Example

```java
import cloud.hetzner.api.models.LabelSelector1;

LabelSelector1 labelSelector1 = new LabelSelector1.Builder(
    "selector2"
)
.build();
```



