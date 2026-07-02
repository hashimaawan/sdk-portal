# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ReusedPreviousResult` | `bool` | Required | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

ResultReuseInformation resultReuseInformation = new ResultReuseInformation
{
    ReusedPreviousResult = false,
};
```



