# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/ruby/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Furkot provides Rest API to access user trip data.
Using Furkot API an application can list user trips and display stops for a specific trip.
Furkot API uses OAuth2 protocol to authorize applications to access data on behalf of users.

Furkot API description: [https://help.furkot.com/widgets/furkot-api.html](https://help.furkot.com/widgets/furkot-api.html)


# Building

The generated code depends on a few Ruby gems. The references to these gems are added in the gemspec file. The easiest way to resolve the dependencies, build the gem and install it is through Rake:

1. Install Rake if not already installed: `gem install rake`
2. Install Bundler if not already installed: `gem install bundler`
3. From terminal/cmd navigate to the root directory of the SDK.
4. Invoke: `rake install`

Alternatively, you can build and install the gem manually:

1. From terminal/cmd navigate to the root directory of the SDK.
2. Run the build command: `gem build furkot_trips.gemspec`
3. Run the install command: `gem install furkot_trips-1.0.0.gem`

![Installing Gem](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&gemVer=1.0.0&gemName=furkot_trips&step=buildSDK)


# Installation

The following section explains how to use the furkot_trips ruby gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

## 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting `File -> Close Project`. Next, click on `Create New Project` to create a new project from scratch.

![Create a new project in RubyMine - Step 1](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&step=createNewProject0)

Next, provide `TestApp` as the project name, choose `Rails Application` as the project type, and click `OK`.

![Create a new Rails Application in RubyMine - Step 2](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&step=createNewProject1)

In the next dialog make sure that the correct Ruby SDK is being used (>= 2.6 and <= 3.2) and click `OK`.

![Create a new Rails Application in RubyMine - Step 3](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&step=createNewProject2)

## 2. Add reference of the gem

In order to use the `furkot_trips` gem in the new project we must add a gem reference. Locate the `Gemfile` in the Project Explorer window under the `TestApp` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: `gem 'furkot_trips', '1.0.0'`

![Add new reference to the Gemfile](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&gemVer=1.0.0&gemName=furkot_trips&step=addReference)

## 3. Adding a new Rails Controller

Once the `TestApp` project is created, a folder named `controllers` will be visible in the *Project Explorer* under the following path: `TestApp > app > controllers`. Right click on this folder and select `New -> Run Rails Generator...`.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&gemVer=1.0.0&gemName=furkot_trips&step=addCode0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the `controller` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&step=addCode1)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide `Hello` and include an action named `Index` and click `OK`.

![Add a new Controller](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&gemVer=1.0.0&gemName=furkot_trips&step=addCode2)

A new controller class named `HelloController` will be created in a file named `hello_controller.rb` containing a method named `Index`.

1. Add the `require 'furkot_trips'` statement to require the gem in the controller file.
2. Add the `include FurkotTrips` statement to include the sdk module in the controller file.
3. In the `Index` method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?workspaceFolder=FurkotTrips&gemName=furkot_trips&step=addCode3)


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
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/getting-started/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 60** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/configuration/proxysettings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| furkot_auth_access_code_credentials | [`FurkotAuthAccessCodeCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/getting-started/authorization.md) | The credential object for OAuth 2 Authorization Code Grant |
| furkot_auth_implicit_credentials | [`FurkotAuthImplicitCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/getting-started/authorization.md) | The credential object for OAuth 2 Implicit Grant |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ruby
require 'furkot_trips'
include FurkotTrips

client = Client.new(
  furkot_auth_access_code_credentials: FurkotAuthAccessCodeCredentials.new(
    o_auth_client_id: 'OAuthClientId',
    o_auth_client_secret: 'OAuthClientSecret',
    o_auth_redirect_uri: 'OAuthRedirectUri',
    o_auth_scopes: [
      OAuthScopeFurkotAuthAccessCodeEnum::READTRIPS
    ]
  ),
  furkot_auth_implicit_credentials: FurkotAuthImplicitCredentials.new(
    o_auth_client_id: 'OAuthClientId',
    o_auth_redirect_uri: 'OAuthRedirectUri',
    o_auth_scopes: [
      OAuthScopeFurkotAuthImplicitEnum::READTRIPS
    ]
  ),
  environment: Environment::PRODUCTION
)
```

## Environment-Based Client Initialization

```ruby
require 'furkot_trips'
include FurkotTrips

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`furkot_auth_access_code (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/getting-started/authorization.md)
* [`furkot_auth_implicit (OAuth 2 Implicit Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/getting-started/authorization.md)

## furkot_auth_access_code (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for furkot_auth_access_code.

### Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| OAuthClientId | `String` | OAuth 2 Client ID | `o_auth_client_id` |
| OAuthClientSecret | `String` | OAuth 2 Client Secret | `o_auth_client_secret` |
| OAuthRedirectUri | `String` | OAuth 2 Redirection endpoint or Callback Uri | `o_auth_redirect_uri` |
| OAuthToken | `OAuthToken` | Object for storing information about the OAuth token | `o_auth_token` |
| OAuthScopes | `Array[OAuthScopeFurkotAuthAccessCodeEnum]` | List of scopes that apply to the OAuth token | `o_auth_scopes` |



**Note:** Auth credentials can be set using `FurkotAuthAccessCodeCredentials` object, passed in as named parameter `furkot_auth_access_code_credentials` in the client initialization.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```ruby
require 'furkot_trips'
include FurkotTrips

client = Client.new(
  furkot_auth_access_code_credentials: FurkotAuthAccessCodeCredentials.new(
    o_auth_client_id: 'OAuthClientId',
    o_auth_client_secret: 'OAuthClientSecret',
    o_auth_redirect_uri: 'OAuthRedirectUri',
    o_auth_scopes: [
      OAuthScopeFurkotAuthAccessCodeEnum::READTRIPS
    ]
  )
)
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `get_authorization_url` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```ruby
auth_url = client.furkot_auth_access_code.get_authorization_url
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
  token = client.furkot_auth_access_code.fetch_token
  # update the cloned configuration with the token
  furkot_auth_access_code_credentials = client.config.furkot_auth_access_code_credentials.clone_with(o_auth_token: token)
  config = client.config.clone_with(furkot_auth_access_code_credentials: furkot_auth_access_code_credentials)
  # re-instantiate the client with updated configuration
  client = FurkotTrips::Client.new(config: config)
rescue OAuthProviderException => ex
  # handle exception
rescue APIException => ex
  # handle exception
end
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthAccessCodeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/models/enumerations/o-auth-scope-furkot-auth-access-code.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list trips and stops info |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```ruby
if client.auth.token_expired?
  begin
    token = client.auth.refresh_token
    # Update the cloned configuration with the token
    furkot_auth_access_code_credentials = client.config.furkot_auth_access_code_credentials.clone_with(o_auth_token: token)
    config = client.config.clone_with(furkot_auth_access_code_credentials: furkot_auth_access_code_credentials)
    # Re-instantiate the client with updated configuration
    client = Client.new(config: config)
  rescue OAuthProviderException => ex
    # handle exception
  rescue APIException => ex
    # handle exception
  end
end
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```ruby
# store token
save_token_to_database(client.config.furkot_auth_access_code_credentials.o_auth_token)
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```ruby
# load token later...
token = load_token_from_database

# Update the cloned configuration with the token
  furkot_auth_access_code_credentials = client.config.furkot_auth_access_code_credentials.clone_with(o_auth_token: token)
config = client.config.clone_with(furkot_auth_access_code_credentials: furkot_auth_access_code_credentials)
# Re-instantiate the client with updated configuration
client = Client.new(config: config)
```

### Complete example



```ruby
require 'furkot_trips'

include FurkotTrips

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
  furkot_auth_access_code_credentials = client.config.furkot_auth_access_code_credentials.clone_with(o_auth_token: previous_token)
  config = client.config.clone_with(furkot_auth_access_code_credentials: furkot_auth_access_code_credentials)
  # re-instantiate the client with updated configuration
  client = FurkotTrips::Client.new(config: config)
else
  # redirect user to a page that handles authorization
end
```

## furkot_auth_implicit (OAuth 2 Implicit Grant)



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Implicit Grant* to obtain a user's consent to perform an API request on user's behalf. This authorization includes the following steps

This process requires the presence of a client-side JavaScript code on the redirect URI page to receive the *access token* after the consent step is completed.

### 1\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page. The `get_authorization_url` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```ruby
auth_url = client.furkot_auth_implicit.get_authorization_url
```

### 2\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

The redirect URI will receive the *access token* as the `token` argument in the URL fragment.

```
https://example.com/oauth/callback#token=XXXXXXXXXXXXXXXXXXXXXXXXX
```

The access token must be extracted by the client-side JavaScript code. The access token can be used to authorize any further endpoint calls by the JavaScript code.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthImplicitEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/ruby/models/enumerations/o-auth-scope-furkot-auth-implicit.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list users trips info |




