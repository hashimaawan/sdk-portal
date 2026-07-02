# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

<p>Amazon Athena is an interactive query service that lets you use standard SQL to analyze data directly in Amazon S3. You can point Athena at your data in Amazon S3 and run ad-hoc queries and get results in seconds. Athena is serverless, so there is no infrastructure to set up or manage. You pay only for the queries you run. Athena scales automatically—executing queries in parallel—so results are fast, even with large datasets and complex queries. For more information, see <a href="http://docs.aws.amazon.com/athena/latest/ug/what-is.html">What is Amazon Athena</a> in the <i>Amazon Athena User Guide</i>.</p> <p>If you connect to Athena using the JDBC driver, use version 1.1.0 of the driver or later with the Amazon Athena API. Earlier version drivers do not support the API. For more information and to download the driver, see <a href="https://docs.aws.amazon.com/athena/latest/ug/connect-with-jdbc.html">Accessing Amazon Athena with JDBC</a>.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="https://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


Amazon Web Services documentation: [https://docs.aws.amazon.com/athena/](https://docs.aws.amazon.com/athena/)


# Building

You must have Python `3.7+` installed on your system to install and run this SDK. This SDK package depends on other Python packages like pytest, etc. These dependencies are defined in the `requirements.txt` file that comes with the SDK. To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type `pip --version`. This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including `requirements.txt`) for the SDK.
* Run the command `pip install -r requirements.txt`. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&step=installDependencies)


# Installation

The following section explains how to use the amazonathena library in a new project.

## 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&step=pyCharm)

Click on `Open` in PyCharm to browse to your generated SDK directory and then click `OK`.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&step=openProject0)

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&projectName=amazonathena&step=openProject1)

## 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&projectName=amazonathena&step=createDirectory)

Name the directory as "test".

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&step=nameDirectory)

Add a python file to this project.

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&projectName=amazonathena&step=createFile)

Name it "testSDK".

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&projectName=amazonathena&step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```python
from amazonathena.amazonathena_client import AmazonathenaClient
```

![Add a new project in PyCharm - Step 5](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&projectName=amazonathena&libraryName=amazonathena.amazonathena_client&className=AmazonathenaClient&step=projectFiles)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

## 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on `Run`

![Run Test Project - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Amazonathena-Python&projectName=amazonathena&libraryName=amazonathena.amazonathena_client&className=AmazonathenaClient&step=runProject)


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** The Amazon Athena multi-region endpoint |
| ENVIRONMENT2 | The Amazon Athena multi-region endpoint |
| ENVIRONMENT3 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |
| ENVIRONMENT4 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| region | `Region` | The AWS region<br>*Default*: `"us-east-1"` |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| http_client_instance | `Union[Session, HttpClientProvider]` | The Http Client passed from the sdk user for making requests |
| override_http_client_configuration | `bool` | The value which determines to override properties of the passed Http Client from the sdk user |
| http_call_back | `HttpCallBack` | The callback value that is invoked before and after an HTTP call is made to an endpoint |
| timeout | `float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `int` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| backoff_factor | `float` | A backoff factor to apply between attempts after the second try. <br> **Default: 2** |
| retry_statuses | `Array of int` | The http statuses on which retry is to be done. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array of string` | The http methods on which retry is to be done. <br> **Default: ["GET", "PUT", "GET", "PUT"]** |
| proxy_settings | [`ProxySettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/configuration/proxysettings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/configuration/loggingconfiguration.md) | The SDK logging configuration for API calls |
| custom_header_authentication_credentials | [`CustomHeaderAuthenticationCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md) | The credential object for Custom Header Signature |

The API client can be initialized as follows:

## Code-Based Client Initialization

```python
import logging

from amazonathena.amazonathena_client import AmazonathenaClient
from amazonathena.configuration import Environment
from amazonathena.http.auth.custom_header_authentication import CustomHeaderAuthenticationCredentials
from amazonathena.logging.configuration.api_logging_configuration import LoggingConfiguration
from amazonathena.logging.configuration.api_logging_configuration import RequestLoggingConfiguration
from amazonathena.logging.configuration.api_logging_configuration import ResponseLoggingConfiguration
from amazonathena.models.region import Region

client = AmazonathenaClient(
    custom_header_authentication_credentials=CustomHeaderAuthenticationCredentials(
        authorization='Authorization'
    ),
    environment=Environment.PRODUCTION,
    region=Region.USEAST1,
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
from amazonathena.amazonathena_client import AmazonathenaClient

# Specify the path to your .env file if it’s located outside the project’s root directory.
client = AmazonathenaClient.from_environment(dotenv_path='/path/to/.env')
```

See the [Environment-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`hmac (Custom Header Signature)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)

## hmac (Custom Header Signature)



Documentation for accessing and setting credentials for hmac.

### Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| Authorization | `str` | Amazon Signature authorization v4 | `authorization` |



**Note:** Auth credentials can be set using `CustomHeaderAuthenticationCredentials` object, passed in as named parameter `custom_header_authentication_credentials` in the client initialization.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```python
from amazonathena.amazonathena_client import AmazonathenaClient
from amazonathena.http.auth.custom_header_authentication import CustomHeaderAuthenticationCredentials

client = AmazonathenaClient(
    custom_header_authentication_credentials=CustomHeaderAuthenticationCredentials(
        authorization='Authorization'
    )
)
```




