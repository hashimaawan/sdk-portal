# Notebook Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRk5vdGVib29rU2Vzc2lvblN1bW1hcnk

Contains the notebook session ID and notebook session creation time.


# Class Name

`NotebookSessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `CreationTime` | `*time.Time` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "amazonathena/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    notebookSessionSummary := models.NotebookSessionSummary{
        SessionId:            models.ToPointer("SessionId0"),
        CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
    }

}
```



