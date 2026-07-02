# Track Io Timing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlRyYWNrSW9UaW1pbmc

Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms.


# Class Name

`TrackIoTiming`


# Fields

| Name |
|  --- |
| `Off` |
| `On` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    trackIoTiming := models.TrackIoTiming_Off

}
```



