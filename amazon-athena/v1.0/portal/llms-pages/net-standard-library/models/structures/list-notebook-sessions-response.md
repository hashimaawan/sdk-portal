# List Notebook Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVzcG9uc2U


# Class Name

`ListNotebookSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookSessionsList` | [`List<NotebookSessionSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/notebook-session-summary.md) | Required | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

ListNotebookSessionsResponse listNotebookSessionsResponse = new ListNotebookSessionsResponse
{
    NotebookSessionsList = new List<NotebookSessionSummary>
    {
        new NotebookSessionSummary
        {
            SessionId = "SessionId4",
            CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
        },
    },
    NextToken = "NextToken0",
};
```



