# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool` | Required | - |
| `MaxAgeInMinutes` | `int?` | Optional | **Constraints**: `>= 0`, `<= 10080` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ResultReuseByAgeConfiguration resultReuseByAgeConfiguration = new ResultReuseByAgeConfiguration
{
    Enabled = false,
    MaxAgeInMinutes = 134,
};
```



