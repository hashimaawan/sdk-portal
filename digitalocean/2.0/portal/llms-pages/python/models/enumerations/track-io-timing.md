# Track Io Timing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlRyYWNrSW9UaW1pbmc

Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms.


# Enum Type Name

`TrackIoTiming`


# Fields

| Name |
|  --- |
| `OFF` |
| `ON` |


# Example

```python
from digitaloceanapi.models.track_io_timing import TrackIoTiming

track_io_timing = TrackIoTiming.OFF
```



