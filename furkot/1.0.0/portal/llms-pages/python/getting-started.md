# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/python/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Furkot provides Rest API to access user trip data.
Using Furkot API an application can list user trips and display stops for a specific trip.
Furkot API uses OAuth2 protocol to authorize applications to access data on behalf of users.

Furkot API description: [https://help.furkot.com/widgets/furkot-api.html](https://help.furkot.com/widgets/furkot-api.html)


# Building

You must have Python `3.7+` installed on your system to install and run this SDK. This SDK package depends on other Python packages like pytest, etc. These dependencies are defined in the `requirements.txt` file that comes with the SDK. To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type `pip --version`. This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including `requirements.txt`) for the SDK.
* Run the command `pip install -r requirements.txt`. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&step=installDependencies)


# Installation

The following section explains how to use the furkottrips library in a new project.

## 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&step=pyCharm)

Click on `Open` in PyCharm to browse to your generated SDK directory and then click `OK`.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&step=openProject0)

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&projectName=furkottrips&step=openProject1)

## 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&projectName=furkottrips&step=createDirectory)

Name the directory as "test".

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&step=nameDirectory)

Add a python file to this project.

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&projectName=furkottrips&step=createFile)

Name it "testSDK".

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&projectName=furkottrips&step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```python
from furkottrips.furkottrips_client import FurkottripsClient
```

![Add a new project in PyCharm - Step 5](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&projectName=furkottrips&libraryName=furkottrips.furkottrips_client&className=FurkottripsClient&step=projectFiles)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

## 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on `Run`

![Run Test Project - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Furkottrips-Python&projectName=furkottrips&libraryName=furkottrips.furkottrips_client&className=FurkottripsClient&step=runProject)


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
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/getting-started/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| http_client_instance | `Union[Session, HttpClientProvider]` | The Http Client passed from the sdk user for making requests |
| override_http_client_configuration | `bool` | The value which determines to override properties of the passed Http Client from the sdk user |
| http_call_back | `HttpCallBack` | The callback value that is invoked before and after an HTTP call is made to an endpoint |
| timeout | `float` | The value to use for connection timeout. <br> **Default: 60** |
| max_retries | `int` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| backoff_factor | `float` | A backoff factor to apply between attempts after the second try. <br> **Default: 2** |
| retry_statuses | `Array of int` | The http statuses on which retry is to be done. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array of string` | The http methods on which retry is to be done. <br> **Default: ["GET", "PUT", "GET", "PUT"]** |
| proxy_settings | [`ProxySettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/sdk-infrastructure/configuration/proxysettings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| furkot_auth_access_code_credentials | [`FurkotAuthAccessCodeCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/getting-started/authorization.md) | The credential object for OAuth 2 Authorization Code Grant |
| furkot_auth_implicit_credentials | [`FurkotAuthImplicitCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/getting-started/authorization.md) | The credential object for OAuth 2 Implicit Grant |

The API client can be initialized as follows:

## Code-Based Client Initialization

```python
from furkottrips.configuration import Environment
from furkottrips.furkottrips_client import FurkottripsClient
from furkottrips.http.auth.furkot_auth_access_code import FurkotAuthAccessCodeCredentials
from furkottrips.http.auth.furkot_auth_implicit import FurkotAuthImplicitCredentials
from furkottrips.models.o_auth_scope_furkot_auth_access_code_enum import OAuthScopeFurkotAuthAccessCodeEnum
from furkottrips.models.o_auth_scope_furkot_auth_implicit_enum import OAuthScopeFurkotAuthImplicitEnum

client = FurkottripsClient(
    furkot_auth_access_code_credentials=FurkotAuthAccessCodeCredentials(
        o_auth_client_id='OAuthClientId',
        o_auth_client_secret='OAuthClientSecret',
        o_auth_redirect_uri='OAuthRedirectUri',
        o_auth_scopes=[
            OAuthScopeFurkotAuthAccessCodeEnum.READTRIPS
        ]
    ),
    furkot_auth_implicit_credentials=FurkotAuthImplicitCredentials(
        o_auth_client_id='OAuthClientId',
        o_auth_redirect_uri='OAuthRedirectUri',
        o_auth_scopes=[
            OAuthScopeFurkotAuthImplicitEnum.READTRIPS
        ]
    ),
    environment=Environment.PRODUCTION
)
```

## Environment-Based Client Initialization

```python
from furkottrips.furkottrips_client import FurkottripsClient

# Specify the path to your .env file if it’s located outside the project’s root directory.
client = FurkottripsClient.from_environment(dotenv_path='/path/to/.env')
```

See the [Environment-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`furkot_auth_access_code (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/getting-started/authorization.md)
* [`furkot_auth_implicit (OAuth 2 Implicit Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/getting-started/authorization.md)

## furkot_auth_access_code (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for furkot_auth_access_code.

### Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| OAuthClientId | `str` | OAuth 2 Client ID | `o_auth_client_id` |
| OAuthClientSecret | `str` | OAuth 2 Client Secret | `o_auth_client_secret` |
| OAuthRedirectUri | `str` | OAuth 2 Redirection endpoint or Callback Uri | `o_auth_redirect_uri` |
| OAuthToken | `OAuthToken` | Object for storing information about the OAuth token | `o_auth_token` |
| OAuthScopes | `List[OAuthScopeFurkotAuthAccessCodeEnum]` | List of scopes that apply to the OAuth token | `o_auth_scopes` |



**Note:** Auth credentials can be set using `FurkotAuthAccessCodeCredentials` object, passed in as named parameter `furkot_auth_access_code_credentials` in the client initialization.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```python
from furkottrips.furkottrips_client import FurkottripsClient
from furkottrips.http.auth.furkot_auth_access_code import FurkotAuthAccessCodeCredentials
from furkottrips.models.o_auth_scope_furkot_auth_access_code_enum import OAuthScopeFurkotAuthAccessCodeEnum

client = FurkottripsClient(
    furkot_auth_access_code_credentials=FurkotAuthAccessCodeCredentials(
        o_auth_client_id='OAuthClientId',
        o_auth_client_secret='OAuthClientSecret',
        o_auth_redirect_uri='OAuthRedirectUri',
        o_auth_scopes=[
            OAuthScopeFurkotAuthAccessCodeEnum.READTRIPS
        ]
    )
)
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `get_authorization_url()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```python
auth_url = client.furkot_auth_access_code.get_authorization_url()
```

### 3\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

If the user approves the request, the authorization code will be sent as the `code` query string:

```
https://example.com/oauth/callback?code=XXXXXXXXXXXXXXXXXXXXXXXXX
```

If the user does not approve the request, the response contains an `error` query string:

```
https://example.com/oauth/callback?error=access_denied
```

### 4\. Authorize the client using the code

After the server receives the code, it can exchange this for an *access token*. The access token is an object containing information for authorizing client requests and refreshing the token itself.

```python
try:
    token = client.furkot_auth_access_code.fetch_token('code')
    furkot_auth_access_code_credentials = client.config.furkot_auth_access_code_credentials.clone_with(o_auth_token=token)
    config = client.config.clone_with(furkot_auth_access_code_credentials=furkot_auth_access_code_credentials)
    client = FurkottripsClient(config=config)
except OAuthProviderException as ex:
    # handle exception
    pass
except APIException as ex:
    # handle exception
    pass
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthAccessCodeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/models/enumerations/o-auth-scope-furkot-auth-access-code.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list trips and stops info |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```python
if client.furkot_auth_access_code.is_token_expired():
    try:
        token = client.furkot_auth_access_code.refresh_token()
        furkot_auth_access_code_credentials = client.config.furkot_auth_access_code_credentials.clone_with(o_auth_token=token)
        config = client.config.clone_with(furkot_auth_access_code_credentials=furkot_auth_access_code_credentials)
        client = FurkottripsClient(config=config)
    except OAuthProviderException as ex:
       # handle exception
       pass
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```python
# store token
save_token_to_database(client.config.furkot_auth_access_code_credentials.o_auth_token)
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```python
client = FurkottripsClient(
    furkot_auth_access_code_credentials=FurkotAuthAccessCodeCredentials(
        o_auth_token=load_token_from_database()
    )
)
```

### Complete example



```python
from furkottrips.furkottrips_client import FurkottripsClient
from furkottrips.http.auth.furkot_auth_access_code import FurkotAuthAccessCodeCredentials
from furkottrips.models.o_auth_scope_furkot_auth_access_code_enum import OAuthScopeFurkotAuthAccessCodeEnum
from furkottrips.exceptions.o_auth_provider_exception import OAuthProviderException

client = FurkottripsClient(
    furkot_auth_access_code_credentials=FurkotAuthAccessCodeCredentials(
        o_auth_client_id='OAuthClientId',
        o_auth_client_secret='OAuthClientSecret',
        o_auth_redirect_uri='OAuthRedirectUri',
        o_auth_scopes=[
            OAuthScopeFurkotAuthAccessCodeEnum.READTRIPS
        ]
    )
)
# function for storing token to database
def save_token_to_database(token):
    # code to save the token to database
    pass

# function for loading token from database
def load_token_from_database():
    # load token from database and return it (return None if no token exists)
    pass

# obtain access token, needed for client to be authorized
previous_token = load_token_from_database()
if previous_token:
    # restore previous access token
    furkot_auth_access_code_credentials = client.config.furkot_auth_access_code_credentials.clone_with(o_auth_token=previous_token)
    config = client.config.clone_with(furkot_auth_access_code_credentials=furkot_auth_access_code_credentials)
    client = FurkottripsClient(config=config)
else:
    # redirect user to a page that handles authorization
    pass

# the client is now authorized and you can use controllers to make endpoint calls
```

## furkot_auth_implicit (OAuth 2 Implicit Grant)



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Implicit Grant* to obtain a user's consent to perform an API request on user's behalf. This authorization includes the following steps

This process requires the presence of a client-side JavaScript code on the redirect URI page to receive the *access token* after the consent step is completed.

### 1\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page. The `get_authorization_url()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```python
auth_url = client.furkot_auth_implicit.get_authorization_url()
```

### 2\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

The redirect URI will receive the *access token* as the `token` argument in the URL fragment.

```
https://example.com/oauth/callback#token=XXXXXXXXXXXXXXXXXXXXXXXXX
```

The access token must be extracted by the client-side JavaScript code. The access token can be used to authorize any further endpoint calls by the JavaScript code.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthImplicitEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/models/enumerations/o-auth-scope-furkot-auth-implicit.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list users trips info |




