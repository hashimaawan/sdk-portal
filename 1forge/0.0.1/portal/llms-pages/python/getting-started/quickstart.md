# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/python/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Stock and Forex Data and Realtime Quotes


# Building

You must have Python `3.7+` installed on your system to install and run this SDK. This SDK package depends on other Python packages like pytest, etc. These dependencies are defined in the `requirements.txt` file that comes with the SDK. To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type `pip --version`. This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including `requirements.txt`) for the SDK.
* Run the command `pip install -r requirements.txt`. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&step=installDependencies)


# Installation

The following section explains how to use the m1forgefinanceapis library in a new project.

## 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&step=pyCharm)

Click on `Open` in PyCharm to browse to your generated SDK directory and then click `OK`.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&step=openProject0)

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&projectName=m1forgefinanceapis&step=openProject1)

## 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&projectName=m1forgefinanceapis&step=createDirectory)

Name the directory as "test".

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&step=nameDirectory)

Add a python file to this project.

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&projectName=m1forgefinanceapis&step=createFile)

Name it "testSDK".

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&projectName=m1forgefinanceapis&step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```python
from m1forgefinanceapis.m_1_forgefinanceapis_client import M1ForgefinanceapisClient
```

![Add a new project in PyCharm - Step 5](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&projectName=m1forgefinanceapis&libraryName=m1forgefinanceapis.m_1_forgefinanceapis_client&className=M1ForgefinanceapisClient&step=projectFiles)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

## 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on `Run`

![Run Test Project - Step 1](https://apidocs.io/illustration/python?workspaceFolder=M1Forgefinanceapis-Python&projectName=m1forgefinanceapis&libraryName=m1forgefinanceapis.m_1_forgefinanceapis_client&className=M1ForgefinanceapisClient&step=runProject)


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/python/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| http_client_instance | `Union[Session, HttpClientProvider]` | The Http Client passed from the sdk user for making requests |
| override_http_client_configuration | `bool` | The value which determines to override properties of the passed Http Client from the sdk user |
| http_call_back | `HttpCallBack` | The callback value that is invoked before and after an HTTP call is made to an endpoint |
| timeout | `float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `int` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| backoff_factor | `float` | A backoff factor to apply between attempts after the second try. <br> **Default: 2** |
| retry_statuses | `Array of int` | The http statuses on which retry is to be done. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array of string` | The http methods on which retry is to be done. <br> **Default: ["GET", "PUT", "GET", "PUT"]** |
| proxy_settings | [`ProxySettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/python/sdk-infrastructure/configuration/proxysettings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/python/sdk-infrastructure/configuration/loggingconfiguration.md) | The SDK logging configuration for API calls |

The API client can be initialized as follows:

## Code-Based Client Initialization

```python
import logging

from m1forgefinanceapis.configuration import Environment
from m1forgefinanceapis.logging.configuration.api_logging_configuration import LoggingConfiguration
from m1forgefinanceapis.logging.configuration.api_logging_configuration import RequestLoggingConfiguration
from m1forgefinanceapis.logging.configuration.api_logging_configuration import ResponseLoggingConfiguration
from m1forgefinanceapis.m_1_forgefinanceapis_client import M1ForgefinanceapisClient

client = M1ForgefinanceapisClient(
    environment=Environment.PRODUCTION,
    logging_configuration=LoggingConfiguration(
        log_level=logging.INFO,
        request_logging_config=RequestLoggingConfiguration(
            log_body=True
        ),
        response_logging_config=ResponseLoggingConfiguration(
            log_headers=True
        )
    )
)
```

## Environment-Based Client Initialization

```python
from m1forgefinanceapis.m_1_forgefinanceapis_client import M1ForgefinanceapisClient

# Specify the path to your .env file if it’s located outside the project’s root directory.
client = M1ForgefinanceapisClient.from_environment(dotenv_path='/path/to/.env')
```

See the [Environment-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/python/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.



