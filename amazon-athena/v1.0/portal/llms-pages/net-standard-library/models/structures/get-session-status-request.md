# Get Session Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXF1ZXN0


# Class Name

`GetSessionStatusRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```csharp
using AmazonAthena.Standard.Models;

GetSessionStatusRequest getSessionStatusRequest = new GetSessionStatusRequest
{
    SessionId = "SessionId6",
};
```



