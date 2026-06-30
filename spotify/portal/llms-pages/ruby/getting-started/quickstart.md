# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

You can use Spotify's Web API to discover music and podcasts, manage your Spotify library, control audio playback, and much more. Browse our available Web API endpoints using the sidebar at left, or via the navigation bar on top of this page on smaller screens.

In order to make successful Web API requests your app will need a valid access token. One can be obtained through <a href="https://developer.spotify.com/documentation/general/guides/authorization-guide/">OAuth 2.0</a>.

The base URI for all Web API requests is `https://api.spotify.com/v1`.

Need help? See our <a href="https://developer.spotify.com/documentation/web-api/guides/">Web API guides</a> for more information, or visit the <a href="https://community.spotify.com/t5/Spotify-for-Developers/bd-p/Spotify_Developer">Spotify for Developers community forum</a> to ask questions and connect with other developers.


# Building

The generated code depends on a few Ruby gems. The references to these gems are added in the gemspec file. The easiest way to resolve the dependencies, build the gem and install it is through Rake:

1. Install Rake if not already installed: `gem install rake`
2. Install Bundler if not already installed: `gem install bundler`
3. From terminal/cmd navigate to the root directory of the SDK.
4. Invoke: `rake install`

Alternatively, you can build and install the gem manually:

1. From terminal/cmd navigate to the root directory of the SDK.
2. Run the build command: `gem build spotify_web_api_with_fixes_and_improvements_from_sonallux.gemspec`
3. Run the install command: `gem install spotify_web_api_with_fixes_and_improvements_from_sonallux-2024.3.3.gem`

![Installing Gem](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&gemVer=2024.3.3&gemName=spotify_web_api_with_fixes_and_improvements_from_sonallux&step=buildSDK)


# Installation

The following section explains how to use the spotify_web_api_with_fixes_and_improvements_from_sonallux ruby gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

## 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting `File -> Close Project`. Next, click on `Create New Project` to create a new project from scratch.

![Create a new project in RubyMine - Step 1](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&step=createNewProject0)

Next, provide `TestApp` as the project name, choose `Rails Application` as the project type, and click `OK`.

![Create a new Rails Application in RubyMine - Step 2](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&step=createNewProject1)

In the next dialog make sure that the correct Ruby SDK is being used (>= 2.6 and <= 3.2) and click `OK`.

![Create a new Rails Application in RubyMine - Step 3](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&step=createNewProject2)

## 2. Add reference of the gem

In order to use the `spotify_web_api_with_fixes_and_improvements_from_sonallux` gem in the new project we must add a gem reference. Locate the `Gemfile` in the Project Explorer window under the `TestApp` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: `gem 'spotify_web_api_with_fixes_and_improvements_from_sonallux', '2024.3.3'`

![Add new reference to the Gemfile](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&gemVer=2024.3.3&gemName=spotify_web_api_with_fixes_and_improvements_from_sonallux&step=addReference)

## 3. Adding a new Rails Controller

Once the `TestApp` project is created, a folder named `controllers` will be visible in the *Project Explorer* under the following path: `TestApp > app > controllers`. Right click on this folder and select `New -> Run Rails Generator...`.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&gemVer=2024.3.3&gemName=spotify_web_api_with_fixes_and_improvements_from_sonallux&step=addCode0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the `controller` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&step=addCode1)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide `Hello` and include an action named `Index` and click `OK`.

![Add a new Controller](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&gemVer=2024.3.3&gemName=spotify_web_api_with_fixes_and_improvements_from_sonallux&step=addCode2)

A new controller class named `HelloController` will be created in a file named `hello_controller.rb` containing a method named `Index`.

1. Add the `require 'spotify_web_api_with_fixes_and_improvements_from_sonallux'` statement to require the gem in the controller file.
2. Add the `include SpotifyWebApiWithFixesAndImprovementsFromSonallux` statement to include the sdk module in the controller file.
3. In the `Index` method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?workspaceFolder=SpotifyWebApiWithFixesAndImprovementsFromSonallux&gemName=spotify_web_api_with_fixes_and_improvements_from_sonallux&step=addCode3)


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
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/sdk-infrastructure/configuration/proxysettings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/sdk-infrastructure/configuration/loggingconfiguration.md) | The SDK logging configuration for API calls |
| authorization_code_auth_credentials | [`AuthorizationCodeAuthCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/getting-started/quickstart/authorization.md) | The credential object for OAuth 2 Authorization Code Grant |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ruby
require 'spotify_web_api_with_fixes_and_improvements_from_sonallux'
include SpotifyWebApiWithFixesAndImprovementsFromSonallux

client = Client.new(
  authorization_code_auth_credentials: AuthorizationCodeAuthCredentials.new(
    oauth_client_id: 'OAuthClientId',
    oauth_client_secret: 'OAuthClientSecret',
    oauth_redirect_uri: 'OAuthRedirectUri',
    oauth_scopes: [
      OauthScope::APP_REMOTE_CONTROL,
      OauthScope::PLAYLIST_READ_PRIVATE
    ]
  ),
  environment: Environment::PRODUCTION,
  logging_configuration: LoggingConfiguration.new(
    log_level: Logger::INFO,
    request_logging_config: RequestLoggingConfiguration.new(
      log_body: true
    ),
    response_logging_config: ResponseLoggingConfiguration.new(
      log_headers: true
    )
  )
)
```

## Environment-Based Client Initialization

```ruby
require 'spotify_web_api_with_fixes_and_improvements_from_sonallux'
include SpotifyWebApiWithFixesAndImprovementsFromSonallux

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`oauth_2_0 (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)

## oauth_2_0 (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for oauth_2_0.

### Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| OAuthClientId | `String` | OAuth 2 Client ID | `oauth_client_id` |
| OAuthClientSecret | `String` | OAuth 2 Client Secret | `oauth_client_secret` |
| OAuthRedirectUri | `String` | OAuth 2 Redirection endpoint or Callback Uri | `oauth_redirect_uri` |
| OAuthToken | `OauthToken` | Object for storing information about the OAuth token | `oauth_token` |
| OAuthScopes | `Array[OauthScope]` | List of scopes that apply to the OAuth token | `oauth_scopes` |



**Note:** Auth credentials can be set using named parameter for any of the above credentials (e.g. `oauth_client_id`) in the client initialization.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```ruby
require 'spotify_web_api_with_fixes_and_improvements_from_sonallux'
include SpotifyWebApiWithFixesAndImprovementsFromSonallux

client = Client.new(
  authorization_code_auth_credentials: AuthorizationCodeAuthCredentials.new(
    oauth_client_id: 'OAuthClientId',
    oauth_client_secret: 'OAuthClientSecret',
    oauth_redirect_uri: 'OAuthRedirectUri',
    oauth_scopes: [
      OauthScope::APP_REMOTE_CONTROL,
      OauthScope::PLAYLIST_READ_PRIVATE
    ]
  )
)
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `get_authorization_url` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```ruby
auth_url = client.oauth_2_0.get_authorization_url
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

```ruby
begin
  token = client.oauth_2_0.fetch_token
  # update the cloned configuration with the token
  authorization_code_auth_credentials = client.config.authorization_code_auth_credentials.clone_with(oauth_token: token)
  config = client.config.clone_with(authorization_code_auth_credentials: authorization_code_auth_credentials)
  # re-instantiate the client with updated configuration
  client = SpotifyWebApiWithFixesAndImprovementsFromSonallux::Client.new(config: config)
rescue OauthProviderException => ex
  # handle exception
rescue ApiException => ex
  # handle exception
end
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScope`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/enumerations/oauth-scope.md) enumeration.

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

```ruby
if client.auth.token_expired?
  begin
    token = client.auth.refresh_token
    # Update the cloned configuration with the token
    authorization_code_auth_credentials = client.config.authorization_code_auth_credentials.clone_with(oauth_token: token)
    config = client.config.clone_with(authorization_code_auth_credentials: authorization_code_auth_credentials)
    # Re-instantiate the client with updated configuration
    client = Client.new(config: config)
  rescue OauthProviderException => ex
    # handle exception
  rescue ApiException => ex
    # handle exception
  end
end
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```ruby
# store token
save_token_to_database(client.config.authorization_code_auth_credentials.oauth_token)
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```ruby
# load token later...
token = load_token_from_database

# Update the cloned configuration with the token
  authorization_code_auth_credentials = client.config.authorization_code_auth_credentials.clone_with(oauth_token: token)
config = client.config.clone_with(authorization_code_auth_credentials: authorization_code_auth_credentials)
# Re-instantiate the client with updated configuration
client = Client.new(config: config)
```

### Complete example



```ruby
require 'spotify_web_api_with_fixes_and_improvements_from_sonallux'

include SpotifyWebApiWithFixesAndImprovementsFromSonallux

# function for storing token to database
def save_token_to_database(token)
  # code to save the token to database
end

# function for loading token from database
def load_token_from_database
  # load token from database and return it (return nil if no token exists)
end

# create a new client
client = Client.new

# obtain access token, needed for client to be authorized
previous_token = load_token_from_database
if previous_token
  # restore previous access token and update the cloned configuration with the token
  authorization_code_auth_credentials = client.config.authorization_code_auth_credentials.clone_with(oauth_token: previous_token)
  config = client.config.clone_with(authorization_code_auth_credentials: authorization_code_auth_credentials)
  # re-instantiate the client with updated configuration
  client = SpotifyWebApiWithFixesAndImprovementsFromSonallux::Client.new(config: config)
else
  # redirect user to a page that handles authorization
end
```




