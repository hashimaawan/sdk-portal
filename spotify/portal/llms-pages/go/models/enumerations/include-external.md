# Include External

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkluY2x1ZGUlMjUyMEV4dGVybmFs

If `include_external=audio` is specified it signals that the client can play externally hosted audio content, and marks
the content as playable in the response. By default externally hosted audio content is marked as unplayable in the response.


# Class Name

`IncludeExternal`


# Fields

| Name |
|  --- |
| `Audio` |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    includeExternal := models.IncludeExternal_Audio

}
```



