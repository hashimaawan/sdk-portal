# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Furkot provides Rest API to access user trip data.
Using Furkot API an application can list user trips and display stops for a specific trip.
Furkot API uses OAuth2 protocol to authorize applications to access data on behalf of users.

Furkot API description: [https://help.furkot.com/widgets/furkot-api.html](https://help.furkot.com/widgets/furkot-api.html)


# Building

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore is enabled, these dependencies will be installed automatically. Therefore, you will need internet access for build.

* Open the solution (FurkotTrips.sln) file.

Invoke the build process using Ctrl + Shift + B shortcut key or using the Build menu as shown below.

The build process generates a portable class library, which can be used like a normal class library. More information on how to use can be found at the MSDN Portable Class Libraries documentation.

The supported version is **.NET Standard 2.0**. For checking compatibility of your .NET implementation with the generated library, [click here](https://dotnet.microsoft.com/en-us/platform/dotnet-standard#versions).


# Installation

The following section explains how to use the FurkotTrips.Standard library in a new project.

## 1. Starting a new project

For starting a new project, right click on the current solution from the solution explorer and choose `Add -> New Project`.

![Add a new project in Visual Studio](https://apidocs.io/illustration/cs?workspaceFolder=Furkot%20Trips-CSharp&workspaceName=FurkotTrips&projectName=FurkotTrips.Standard&rootNamespace=FurkotTrips.Standard&step=addProject)

Next, choose `Console Application`, provide `TestConsoleProject` as the project name and click OK.

![Create a new Console Application in Visual Studio](https://apidocs.io/illustration/cs?workspaceFolder=Furkot%20Trips-CSharp&workspaceName=FurkotTrips&projectName=FurkotTrips.Standard&rootNamespace=FurkotTrips.Standard&step=createProject)

## 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the `TestConsoleProject` as the start-up project. To do this, right-click on the `TestConsoleProject` and choose `Set as StartUp Project` form the context menu.

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Furkot%20Trips-CSharp&workspaceName=FurkotTrips&projectName=FurkotTrips.Standard&rootNamespace=FurkotTrips.Standard&step=setStartup)

## 3. Add reference of the library project

In order to use the `FurkotTrips.Standard` library in the new project, first we must add a project reference to the `TestConsoleProject`. First, right click on the `References` node in the solution explorer and click `Add Reference...`

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Furkot%20Trips-CSharp&workspaceName=FurkotTrips&projectName=FurkotTrips.Standard&rootNamespace=FurkotTrips.Standard&step=addReference)

Next, a window will be displayed where we must set the `checkbox` on `FurkotTrips.Standard` and click `OK`. By doing this, we have added a reference of the `FurkotTrips.Standard` project into the new `TestConsoleProject`.

![Creating a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Furkot%20Trips-CSharp&workspaceName=FurkotTrips&projectName=FurkotTrips.Standard&rootNamespace=FurkotTrips.Standard&step=createReference)

## 4. Write sample code

Once the `TestConsoleProject` is created, a file named `Program.cs` will be visible in the solution explorer with an empty `Main` method. This is the entry point for the execution of the entire solution. Here, you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using Controller methods is given in the subsequent sections.

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Furkot%20Trips-CSharp&workspaceName=FurkotTrips&projectName=FurkotTrips.Standard&rootNamespace=FurkotTrips.Standard&step=addCode)


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/environments.md) | The API environment. <br> **Default: `Environment.Production`** |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(100)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/configuration/httpclientconfigurationbuilder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| FurkotAuthAccessCodeCredentials | [`FurkotAuthAccessCodeCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/authorization.md) | The Credentials Setter for OAuth 2 Authorization Code Grant |
| FurkotAuthImplicitCredentials | [`FurkotAuthImplicitCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/authorization.md) | The Credentials Setter for OAuth 2 Implicit Grant |

The API client can be initialized as follows:

## Code-Based Initialization

```csharp
using FurkotTrips.Standard;
using FurkotTrips.Standard.Authentication;
using FurkotTrips.Standard.Models;
using System.Collections.Generic;

namespace ConsoleApp;

FurkotTripsClient client = new FurkotTripsClient.Builder()
    .FurkotAuthAccessCodeCredentials(
        new FurkotAuthAccessCodeModel.Builder(
            "OAuthClientId",
            "OAuthClientSecret",
            "OAuthRedirectUri"
        )
        .OAuthScopes(
            new List<OAuthScopeFurkotAuthAccessCodeEnum>
            {
                OAuthScopeFurkotAuthAccessCodeEnum.Readtrips,
            })
        .Build())
    .FurkotAuthImplicitCredentials(
        new FurkotAuthImplicitModel.Builder(
            "OAuthClientId",
            "OAuthRedirectUri"
        )
        .OAuthScopes(
            new List<OAuthScopeFurkotAuthImplicitEnum>
            {
                OAuthScopeFurkotAuthImplicitEnum.Readtrips,
            })
        .Build())
    .HttpClientConfig(httpClientConfig =>
        httpClientConfig.Timeout(TimeSpan.FromSeconds(100)))
    .Environment(FurkotTrips.Standard.Environment.Production)
    .Build();
```

## Configuration-Based Initialization

```csharp
using FurkotTrips.Standard;
using Microsoft.Extensions.Configuration;

namespace ConsoleApp;

// Build the IConfiguration using .NET conventions (JSON, environment, etc.)
var configuration = new ConfigurationBuilder()
    .AddJsonFile("config.json")
    .AddEnvironmentVariables() // [optional] read environment variables
    .Build();

// Instantiate your SDK and configure it from IConfiguration
var client = FurkotTripsClient
    .FromConfiguration(configuration.GetSection("FurkotTrips"));
```

See the [Configuration-Based Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/configuration/configuration-based-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`furkot_auth_access_code (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/authorization.md)
* [`furkot_auth_implicit (OAuth 2 Implicit Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/getting-started/authorization.md)

## furkot_auth_access_code (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for furkot_auth_access_code.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| OAuthClientId | `string` | OAuth 2 Client ID | `OAuthClientId` | `OAuthClientId` |
| OAuthClientSecret | `string` | OAuth 2 Client Secret | `OAuthClientSecret` | `OAuthClientSecret` |
| OAuthRedirectUri | `string` | OAuth 2 Redirection endpoint or Callback Uri | `OAuthRedirectUri` | `OAuthRedirectUri` |
| OAuthToken | `Models.OAuthToken` | Object for storing information about the OAuth token | `OAuthToken` | `OAuthToken` |
| OAuthScopes | `List<Models.OAuthScopeFurkotAuthAccessCodeEnum>` | List of scopes that apply to the OAuth token | `OAuthScopes` | `OAuthScopes` |



**Note:** Auth credentials can be set using `FurkotAuthAccessCodeCredentials` in the client builder and accessed through `FurkotAuthAccessCodeCredentials` method in the client instance.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```csharp
using FurkotTrips.Standard;
using FurkotTrips.Standard.Authentication;

namespace ConsoleApp;

FurkotTripsClient client = new FurkotTripsClient.Builder()
    .FurkotAuthAccessCodeCredentials(
        new FurkotAuthAccessCodeModel.Builder(
            "OAuthClientId",
            "OAuthClientSecret",
            "OAuthRedirectUri"
        )
        .OAuthScopes(
            new List<OAuthScopeFurkotAuthAccessCodeEnum>
            {
                OAuthScopeFurkotAuthAccessCodeEnum.Readtrips,
            })
        .Build())
    .Build();
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `BuildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```csharp
string authUrl = await client.FurkotAuthAccessCodeCredentials.BuildAuthorizationUrl();
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

```csharp
var authManager = client.FurkotAuthAccessCode;

try
{
    OAuthToken token = authManager.FetchToken(authorizationCode);
    // re-instantiate the client with OAuth token
    client = client.ToBuilder()
        .FurkotAuthAccessCodeCredentials(
            client.FurkotAuthAccessCodeModel.ToBuilder()
                .OAuthToken(token)
                .Build())
        .Build();
}
catch (ApiException e)
{
    // TODO Handle exception
}
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthAccessCodeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/o-auth-scope-furkot-auth-access-code.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list trips and stops info |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```csharp
if (authManager.IsTokenExpired())
{
    try
    {
        OAuthToken token = authManager.RefreshToken();
        // re-instantiate the client with OAuth token
        client = client.ToBuilder()
            .FurkotAuthAccessCodeCredentials(
                client.FurkotAuthAccessCodeModel.ToBuilder()
                    .OAuthToken(token)
                    .Build())
            .Build();
    }
    catch (ApiException e)
    {
        // TODO Handle exception
    }
}
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```csharp
// store token
SaveTokenToDatabase(client.FurkotAuthAccessCodeCredentials.OAuthToken);
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```csharp
// load token later
OAuthToken token = LoadTokenFromDatabase();

// re-instantiate the client with OAuth token
FurkotTripsClient client = client.ToBuilder()
    .FurkotAuthAccessCodeCredentials(
        client.FurkotAuthAccessCodeModel.ToBuilder()
            .OAuthToken(token)
            .Build())
    .Build();
```

### Complete example



```csharp
using FurkotTrips.Standard;
using FurkotTrips.Standard.Models;
using FurkotTrips.Standard.Exceptions;
using FurkotTrips.Standard.Authentication;
using System.Collections.Generic;
namespace OAuthTestApplication
{
    class Program
    {
        static void Main(string[] args)
        {
            FurkotTripsClient client = new FurkotTripsClient.Builder()
                .FurkotAuthAccessCodeCredentials(
                    new FurkotAuthAccessCodeModel.Builder(
                        "OAuthClientId",
                        "OAuthClientSecret",
                        "OAuthRedirectUri"
                    )
                    .OAuthScopes(
                        new List<OAuthScopeFurkotAuthAccessCodeEnum>
                        {
                            OAuthScopeFurkotAuthAccessCodeEnum.Readtrips,
                        })
                    .Build())
                .Build();
            try
            {
                OAuthToken token = LoadTokenFromDatabase();

                // Set the token if it is not set before
                if (token == null)
                {
                    var authManager = client.FurkotAuthAccessCodeCredentials;
                    string authUrl = await authManager.BuildAuthorizationUrl();
                    string authorizationCode = GetAuthorizationCode(authUrl);
                    token = authManager.FetchToken(authorizationCode);
                }

                SaveTokenToDatabase(token);
                // re-instantiate the client with OAuth token
                client = client.ToBuilder()
                    .FurkotAuthAccessCodeCredentials(
                        client.FurkotAuthAccessCodeModel.ToBuilder()
                            .OAuthToken(token)
                            .Build())
                    .Build();
            }
            catch (OAuthProviderException e)
            {
                // TODO Handle exception
            }
        }

        private static string GetAuthorizationCode(string authUrl)
        {
            // TODO Open the given auth URL, give access and return authorization code from redirect URL
            return string.Empty;
        }

        private static void SaveTokenToDatabase(OAuthToken token)
        {
            //Save token here
        }

        private static OAuthToken LoadTokenFromDatabase()
        {
            OAuthToken token = null;
            //token = Get token here
            return token;
        }
    }
}

// the client is now authorized and you can use controllers to make endpoint calls
```

## furkot_auth_implicit (OAuth 2 Implicit Grant)



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Implicit Grant* to obtain a user's consent to perform an API request on user's behalf. This authorization includes the following steps

This process requires the presence of a client-side JavaScript code on the redirect URI page to receive the *access token* after the consent step is completed.

### 1\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page. The `BuildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```csharp
string authUrl = await client.FurkotAuthImplicitCredentials.BuildAuthorizationUrl();
```

### 2\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

The redirect URI will receive the *access token* as the `token` argument in the URL fragment.

```
https://example.com/oauth/callback#token=XXXXXXXXXXXXXXXXXXXXXXXXX
```

The access token must be extracted by the client-side JavaScript code. The access token can be used to authorize any further endpoint calls by the JavaScript code.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthImplicitEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/o-auth-scope-furkot-auth-implicit.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list users trips info |




