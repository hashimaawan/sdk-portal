# Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlNlc3Npb25TdW1tYXJ5

Contains summary information about a session.


# Class Name

`SessionSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-version-1.md) | Optional | - | EngineVersion1 getEngineVersion() | setEngineVersion(EngineVersion1 engineVersion) |
| `NotebookVersion` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getNotebookVersion() | setNotebookVersion(String notebookVersion) |
| `Status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/status-3.md) | Optional | - | Status3 getStatus() | setStatus(Status3 status) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.EngineVersion1;
import com.amazonaws.useast1.athena.models.SessionState1Enum;
import com.amazonaws.useast1.athena.models.SessionSummary;
import com.amazonaws.useast1.athena.models.Status3;

SessionSummary sessionSummary = new SessionSummary.Builder()
    .sessionId("SessionId0")
    .description("Description8")
    .engineVersion(new EngineVersion1.Builder()
        .selectedEngineVersion("SelectedEngineVersion4")
        .effectiveEngineVersion("EffectiveEngineVersion6")
        .build())
    .notebookVersion("NotebookVersion2")
    .status(new Status3.Builder()
        .startDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .lastModifiedDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .endDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .idleSinceDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .state(SessionState1Enum.TERMINATING)
        .build())
    .build();
```



