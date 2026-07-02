# Track Io Timing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRyYWNrSW9UaW1pbmc

Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms.


# Enum Type Name

`TrackIoTiming`


# Fields

| Name |
|  --- |
| `Off` |
| `On` |


# Example

```csharp
using DigitalOceanApi.Standard.Models;

TrackIoTiming trackIoTiming = TrackIoTiming.Off;
```



