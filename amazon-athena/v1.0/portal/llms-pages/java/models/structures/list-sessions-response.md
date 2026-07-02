# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl


# Class Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NextToken` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` | String getNextToken() | setNextToken(String nextToken) |
| `Sessions` | [`List<SessionSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` | List<SessionSummary> getSessions() | setSessions(List<SessionSummary> sessions) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.EngineVersion1;
import com.amazonaws.useast1.athena.models.ListSessionsResponse;
import com.amazonaws.useast1.athena.models.SessionState1Enum;
import com.amazonaws.useast1.athena.models.SessionSummary;
import com.amazonaws.useast1.athena.models.Status3;
import java.util.Arrays;

ListSessionsResponse listSessionsResponse = new ListSessionsResponse.Builder()
    .nextToken("NextToken6")
    .sessions(Arrays.asList(
        new SessionSummary.Builder()
            .sessionId("SessionId6")
            .description("Description4")
            .engineVersion(new EngineVersion1.Builder()
                .selectedEngineVersion("SelectedEngineVersion4")
                .effectiveEngineVersion("EffectiveEngineVersion6")
                .build())
            .notebookVersion("NotebookVersion6")
            .status(new Status3.Builder()
                .startDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .lastModifiedDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .endDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .idleSinceDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .state(SessionState1Enum.TERMINATING)
                .build())
            .build(),
        new SessionSummary.Builder()
            .sessionId("SessionId6")
            .description("Description4")
            .engineVersion(new EngineVersion1.Builder()
                .selectedEngineVersion("SelectedEngineVersion4")
                .effectiveEngineVersion("EffectiveEngineVersion6")
                .build())
            .notebookVersion("NotebookVersion6")
            .status(new Status3.Builder()
                .startDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .lastModifiedDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .endDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .idleSinceDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .state(SessionState1Enum.TERMINATING)
                .build())
            .build(),
        new SessionSummary.Builder()
            .sessionId("SessionId6")
            .description("Description4")
            .engineVersion(new EngineVersion1.Builder()
                .selectedEngineVersion("SelectedEngineVersion4")
                .effectiveEngineVersion("EffectiveEngineVersion6")
                .build())
            .notebookVersion("NotebookVersion6")
            .status(new Status3.Builder()
                .startDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .lastModifiedDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .endDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .idleSinceDateTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
                .state(SessionState1Enum.TERMINATING)
                .build())
            .build()
    ))
    .build();
```



