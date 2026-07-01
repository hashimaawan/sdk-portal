# AbstractLogger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGQ29uZmlndXJhdGlvbiUyRkFic3RyYWN0TG9nZ2Vy

An abstract class for custom logger implementation.

# Abstract Methods

| Name | Description | Return Type | Parameters | Method Signature |
|  --- | --- | --- | --- | --- |
| log | Logs a message with a specified log level and additional parameters. | None | 1. level (int): The log level of the message.<br>2. message (str): The message template to log.<br>3. params: (Dict[str, Any]): The parameters to include in the log message. | log(self, level, message, params) |

# Usage Example

## Client Initialization with Custom Logger

In order to provide custom logger implementation, the `AbstractLogger` class must be inherited so that you can override the `log` behavior.

```python
import structlog
from hetznercloudapi.logging.sdk_logger import AbstractLogger


class CustomLogger(AbstractLogger):

    def __init__(self):
        structlog.configure(
            processors=[
                structlog.processors.TimeStamper(fmt="iso"),
                structlog.processors.JSONRenderer(),
            ]
        )
        self._logger = structlog.get_logger()

    def log(self, level, message, params):
        self._logger.log(level, message, *params.values(), **params)
```

Following is how the custom logger implementation can be injected in the SDK client.

```python
client = HetznercloudapiClient(
    logging_configuration=LoggingConfiguration(
        logger=CustomLogger()
    )
)
```



