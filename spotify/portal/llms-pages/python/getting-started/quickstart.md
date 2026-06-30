# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

You can use Spotify's Web API to discover music and podcasts, manage your Spotify library, control audio playback, and much more. Browse our available Web API endpoints using the sidebar at left, or via the navigation bar on top of this page on smaller screens.

In order to make successful Web API requests your app will need a valid access token. One can be obtained through <a href="https://developer.spotify.com/documentation/general/guides/authorization-guide/">OAuth 2.0</a>.

The base URI for all Web API requests is `https://api.spotify.com/v1`.

Need help? See our <a href="https://developer.spotify.com/documentation/web-api/guides/">Web API guides</a> for more information, or visit the <a href="https://community.spotify.com/t5/Spotify-for-Developers/bd-p/Spotify_Developer">Spotify for Developers community forum</a> to ask questions and connect with other developers.


# Building

You must have Python `3.7+` installed on your system to install and run this SDK. This SDK package depends on other Python packages like pytest, etc. These dependencies are defined in the `requirements.txt` file that comes with the SDK. To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type `pip --version`. This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including `requirements.txt`) for the SDK.
* Run the command `pip install -r requirements.txt`. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&step=installDependencies)


# Installation

The following section explains how to use the spotifywebapiwithfixesandimprovementsfromsonallux library in a new project.

## 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&step=pyCharm)

Click on `Open` in PyCharm to browse to your generated SDK directory and then click `OK`.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&step=openProject0)

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&projectName=spotifywebapiwithfixesandimprovementsfromsonallux&step=openProject1)

## 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&projectName=spotifywebapiwithfixesandimprovementsfromsonallux&step=createDirectory)

Name the directory as "test".

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&step=nameDirectory)

Add a python file to this project.

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&projectName=spotifywebapiwithfixesandimprovementsfromsonallux&step=createFile)

Name it "testSDK".

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&projectName=spotifywebapiwithfixesandimprovementsfromsonallux&step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```python
from spotifywebapiwithfixesandimprovementsfromsonallux.spotifywebapiwithfixesandimprovementsfromsonallux_client import SpotifywebapiwithfixesandimprovementsfromsonalluxClient
```

![Add a new project in PyCharm - Step 5](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&projectName=spotifywebapiwithfixesandimprovementsfromsonallux&libraryName=spotifywebapiwithfixesandimprovementsfromsonallux.spotifywebapiwithfixesandimprovementsfromsonallux_client&className=SpotifywebapiwithfixesandimprovementsfromsonalluxClient&step=projectFiles)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

## 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on `Run`

![Run Test Project - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Spotifywebapiwithfixesandimprovementsfromsonallux-Python&projectName=spotifywebapiwithfixesandimprovementsfromsonallux&libraryName=spotifywebapiwithfixesandimprovementsfromsonallux.spotifywebapiwithfixesandimprovementsfromsonallux_client&className=SpotifywebapiwithfixesandimprovementsfromsonalluxClient&step=runProject)


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
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| http_client_instance | `Union[Session, HttpClientProvider]` | The Http Client passed from the sdk user for making requests |
| override_http_client_configuration | `bool` | The value which determines to override properties of the passed Http Client from the sdk user |
| http_call_back | `HttpCallBack` | The callback value that is invoked before and after an HTTP call is made to an endpoint |
| timeout | `float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `int` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| backoff_factor | `float` | A backoff factor to apply between attempts after the second try. <br> **Default: 2** |
| retry_statuses | `Array of int` | The http statuses on which retry is to be done. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array of string` | The http methods on which retry is to be done. <br> **Default: ["GET", "PUT", "GET", "PUT"]** |
| proxy_settings | [`ProxySettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/sdk-infrastructure/configuration/proxysettings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/sdk-infrastructure/configuration/loggingconfiguration.md) | The SDK logging configuration for API calls |
| authorization_code_auth_credentials | [`AuthorizationCodeAuthCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/getting-started/quickstart/authorization.md) | The credential object for OAuth 2 Authorization Code Grant |

The API client can be initialized as follows:

## Code-Based Client Initialization

```python
import logging

from spotifywebapiwithfixesandimprovementsfromsonallux.configuration import Environment
from spotifywebapiwithfixesandimprovementsfromsonallux.http.auth.oauth_2 import AuthorizationCodeAuthCredentials
from spotifywebapiwithfixesandimprovementsfromsonallux.logging.configuration.api_logging_configuration import LoggingConfiguration
from spotifywebapiwithfixesandimprovementsfromsonallux.logging.configuration.api_logging_configuration import RequestLoggingConfiguration
from spotifywebapiwithfixesandimprovementsfromsonallux.logging.configuration.api_logging_configuration import ResponseLoggingConfiguration
from spotifywebapiwithfixesandimprovementsfromsonallux.models.oauth_scope import OauthScope
from spotifywebapiwithfixesandimprovementsfromsonallux.spotifywebapiwithfixesandimprovementsfromsonallux_client import SpotifywebapiwithfixesandimprovementsfromsonalluxClient

client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient(
    authorization_code_auth_credentials=AuthorizationCodeAuthCredentials(
        oauth_client_id='OAuthClientId',
        oauth_client_secret='OAuthClientSecret',
        oauth_redirect_uri='OAuthRedirectUri',
        oauth_scopes=[
            OauthScope.APP_REMOTE_CONTROL,
            OauthScope.PLAYLIST_READ_PRIVATE
        ]
    ),
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
from spotifywebapiwithfixesandimprovementsfromsonallux.spotifywebapiwithfixesandimprovementsfromsonallux_client import SpotifywebapiwithfixesandimprovementsfromsonalluxClient

# Specify the path to your .env file if it’s located outside the project’s root directory.
client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient.from_environment(dotenv_path='/path/to/.env')
```

See the [Environment-Based Client Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`oauth_2_0 (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/getting-started/quickstart/authorization.md)

## oauth_2_0 (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for oauth_2_0.

### Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| OAuthClientId | `str` | OAuth 2 Client ID | `oauth_client_id` |
| OAuthClientSecret | `str` | OAuth 2 Client Secret | `oauth_client_secret` |
| OAuthRedirectUri | `str` | OAuth 2 Redirection endpoint or Callback Uri | `oauth_redirect_uri` |
| OAuthToken | `OauthToken` | Object for storing information about the OAuth token | `oauth_token` |
| OAuthScopes | `List[OauthScope]` | List of scopes that apply to the OAuth token | `oauth_scopes` |



**Note:** Auth credentials can be set using `AuthorizationCodeAuthCredentials` object, passed in as named parameter `authorization_code_auth_credentials` in the client initialization.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```python
from spotifywebapiwithfixesandimprovementsfromsonallux.http.auth.oauth_2 import AuthorizationCodeAuthCredentials
from spotifywebapiwithfixesandimprovementsfromsonallux.models.oauth_scope import OauthScope
from spotifywebapiwithfixesandimprovementsfromsonallux.spotifywebapiwithfixesandimprovementsfromsonallux_client import SpotifywebapiwithfixesandimprovementsfromsonalluxClient

client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient(
    authorization_code_auth_credentials=AuthorizationCodeAuthCredentials(
        oauth_client_id='OAuthClientId',
        oauth_client_secret='OAuthClientSecret',
        oauth_redirect_uri='OAuthRedirectUri',
        oauth_scopes=[
            OauthScope.APP_REMOTE_CONTROL,
            OauthScope.PLAYLIST_READ_PRIVATE
        ]
    )
)
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `get_authorization_url()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```python
auth_url = client.oauth_2_0.get_authorization_url()
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
    token = client.oauth_2_0.fetch_token('code')
    authorization_code_auth_credentials = client.config.authorization_code_auth_credentials.clone_with(oauth_token=token)
    config = client.config.clone_with(authorization_code_auth_credentials=authorization_code_auth_credentials)
    client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient(config=config)
except OauthProviderException as ex:
    # handle exception
    pass
except ApiException as ex:
    # handle exception
    pass
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScope`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/enumerations/oauth-scope.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `APP_REMOTE_CONTROL` | Communicate with the Spotify app on your device. |
| `PLAYLIST_READ_PRIVATE` | Access your private playlists. |
| `PLAYLIST_READ_COLLABORATIVE` | Access your collaborative playlists. |
| `PLAYLIST_MODIFY_PUBLIC` | Manage your public playlists. |
| `PLAYLIST_MODIFY_PRIVATE` | Manage your private playlists. |
| `USER_LIBRARY_READ` | Access your saved content. |
| `USER_LIBRARY_MODIFY` | Manage your saved content. |
| `USER_READ_PRIVATE` | Access your subscription details. |
| `USER_READ_EMAIL` | Get your real email address. |
| `USER_FOLLOW_READ` | Access your followers and who you are following. |
| `USER_FOLLOW_MODIFY` | Manage your saved content. |
| `USER_TOP_READ` | Read your top artists and content. |
| `USER_READ_PLAYBACK_POSITION` | Read your position in content you have played. |
| `USER_READ_PLAYBACK_STATE` | Read your currently playing content and Spotify Connect devices information. |
| `USER_READ_RECENTLY_PLAYED` | Access your recently played items. |
| `USER_READ_CURRENTLY_PLAYING` | Read your currently playing content. |
| `USER_MODIFY_PLAYBACK_STATE` | Control playback on your Spotify clients and Spotify Connect devices. |
| `UGC_IMAGE_UPLOAD` | Upload images to Spotify on your behalf. |
| `STREAMING` | Play content and control playback on your other devices. |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```python
if client.oauth_2_0.is_token_expired():
    try:
        token = client.oauth_2_0.refresh_token()
        authorization_code_auth_credentials = client.config.authorization_code_auth_credentials.clone_with(oauth_token=token)
        config = client.config.clone_with(authorization_code_auth_credentials=authorization_code_auth_credentials)
        client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient(config=config)
    except OauthProviderException as ex:
       # handle exception
       pass
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```python
# store token
save_token_to_database(client.config.authorization_code_auth_credentials.oauth_token)
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```python
client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient(
    authorization_code_auth_credentials=AuthorizationCodeAuthCredentials(
        oauth_token=load_token_from_database()
    )
)
```

### Complete example



```python
from spotifywebapiwithfixesandimprovementsfromsonallux.spotifywebapiwithfixesandimprovementsfromsonallux_client import SpotifywebapiwithfixesandimprovementsfromsonalluxClient
from spotifywebapiwithfixesandimprovementsfromsonallux.http.auth.oauth_2 import AuthorizationCodeAuthCredentials
from spotifywebapiwithfixesandimprovementsfromsonallux.models.oauth_scope import OauthScope
from spotifywebapiwithfixesandimprovementsfromsonallux.exceptions.oauth_provider_exception import OauthProviderException

client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient(
    authorization_code_auth_credentials=AuthorizationCodeAuthCredentials(
        oauth_client_id='OAuthClientId',
        oauth_client_secret='OAuthClientSecret',
        oauth_redirect_uri='OAuthRedirectUri',
        oauth_scopes=[
            OauthScope.APP_REMOTE_CONTROL,
            OauthScope.PLAYLIST_READ_PRIVATE
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
    authorization_code_auth_credentials = client.config.authorization_code_auth_credentials.clone_with(oauth_token=previous_token)
    config = client.config.clone_with(authorization_code_auth_credentials=authorization_code_auth_credentials)
    client = SpotifywebapiwithfixesandimprovementsfromsonalluxClient(config=config)
else:
    # redirect user to a page that handles authorization
    pass

# the client is now authorized and you can use controllers to make endpoint calls
```




