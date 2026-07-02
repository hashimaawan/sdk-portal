# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CodeBlock` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` | String getCodeBlock() | setCodeBlock(String codeBlock) |


# Example

```java
import com.amazonaws.useast1.athena.models.CalculationConfiguration;

CalculationConfiguration calculationConfiguration = new CalculationConfiguration.Builder()
    .codeBlock("CodeBlock2")
    .build();
```



