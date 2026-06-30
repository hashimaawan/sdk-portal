# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/net-standard-library/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Giphy API

Official Giphy Documentation: [https://developers.giphy.com/docs/](https://developers.giphy.com/docs/)


# Building

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore is enabled, these dependencies will be installed automatically. Therefore, you will need internet access for build.

* Open the solution (GiphyAPI.sln) file.

Invoke the build process using Ctrl + Shift + B shortcut key or using the Build menu as shown below.

The build process generates a portable class library, which can be used like a normal class library. More information on how to use can be found at the MSDN Portable Class Libraries documentation.

The supported version is **.NET Standard 2.0**. For checking compatibility of your .NET implementation with the generated library, [click here](https://dotnet.microsoft.com/en-us/platform/dotnet-standard#versions).


# Installation

The following section explains how to use the GiphyAPI.Standard library in a new project.

## 1. Starting a new project

For starting a new project, right click on the current solution from the solution explorer and choose `Add -> New Project`.

![Add a new project in Visual Studio](https://apidocs.io/illustration/cs?workspaceFolder=Giphy%20API-CSharp&workspaceName=GiphyAPI&projectName=GiphyAPI.Standard&rootNamespace=GiphyAPI.Standard&step=addProject)

Next, choose `Console Application`, provide `TestConsoleProject` as the project name and click OK.

![Create a new Console Application in Visual Studio](https://apidocs.io/illustration/cs?workspaceFolder=Giphy%20API-CSharp&workspaceName=GiphyAPI&projectName=GiphyAPI.Standard&rootNamespace=GiphyAPI.Standard&step=createProject)

## 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the `TestConsoleProject` as the start-up project. To do this, right-click on the `TestConsoleProject` and choose `Set as StartUp Project` form the context menu.

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Giphy%20API-CSharp&workspaceName=GiphyAPI&projectName=GiphyAPI.Standard&rootNamespace=GiphyAPI.Standard&step=setStartup)

## 3. Add reference of the library project

In order to use the `GiphyAPI.Standard` library in the new project, first we must add a project reference to the `TestConsoleProject`. First, right click on the `References` node in the solution explorer and click `Add Reference...`

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Giphy%20API-CSharp&workspaceName=GiphyAPI&projectName=GiphyAPI.Standard&rootNamespace=GiphyAPI.Standard&step=addReference)

Next, a window will be displayed where we must set the `checkbox` on `GiphyAPI.Standard` and click `OK`. By doing this, we have added a reference of the `GiphyAPI.Standard` project into the new `TestConsoleProject`.

![Creating a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Giphy%20API-CSharp&workspaceName=GiphyAPI&projectName=GiphyAPI.Standard&rootNamespace=GiphyAPI.Standard&step=createReference)

## 4. Write sample code

Once the `TestConsoleProject` is created, a file named `Program.cs` will be visible in the solution explorer with an empty `Main` method. This is the entry point for the execution of the entire solution. Here, you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using Controller methods is given in the subsequent sections.

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Giphy%20API-CSharp&workspaceName=GiphyAPI&projectName=GiphyAPI.Standard&rootNamespace=GiphyAPI.Standard&step=addCode)



# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(100)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/sdk-infrastructure/configuration/httpclientconfigurationbuilder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| CustomQueryAuthenticationCredentials | [`CustomQueryAuthenticationCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/getting-started/authorization.md) | The Credentials Setter for Custom Query Parameter |

The API client can be initialized as follows:

## Code-Based Initialization

```csharp
using GiphyAPI.Standard;
using GiphyAPI.Standard.Authentication;

namespace ConsoleApp;

GiphyAPIClient client = new GiphyAPIClient.Builder()
    .CustomQueryAuthenticationCredentials(
        new CustomQueryAuthenticationModel.Builder(
            "api_key"
        )
        .Build())
    .HttpClientConfig(httpClientConfig =>
        httpClientConfig.Timeout(TimeSpan.FromSeconds(100)))
    .Build();
```

## Configuration-Based Initialization

```csharp
using GiphyAPI.Standard;
using Microsoft.Extensions.Configuration;

namespace ConsoleApp;

// Build the IConfiguration using .NET conventions (JSON, environment, etc.)
var configuration = new ConfigurationBuilder()
    .AddJsonFile("config.json")
    .AddEnvironmentVariables() // [optional] read environment variables
    .Build();

// Instantiate your SDK and configure it from IConfiguration
var client = GiphyAPIClient
    .FromConfiguration(configuration.GetSection("GiphyAPI"));
```

See the [Configuration-Based Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/sdk-infrastructure/configuration/configuration-based-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`api_key (Custom Query Parameter)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/getting-started/authorization.md)

## api_key (Custom Query Parameter)



Documentation for accessing and setting credentials for api_key.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| ApiKey | `string` | - | `ApiKey` | `ApiKey` |



**Note:** Auth credentials can be set using `CustomQueryAuthenticationCredentials` in the client builder and accessed through `CustomQueryAuthenticationCredentials` method in the client instance.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```csharp
using GiphyAPI.Standard;
using GiphyAPI.Standard.Authentication;

namespace ConsoleApp;

GiphyAPIClient client = new GiphyAPIClient.Builder()
    .CustomQueryAuthenticationCredentials(
        new CustomQueryAuthenticationModel.Builder(
            "api_key"
        )
        .Build())
    .Build();
```


# Test the SDK

The generated SDK also contain one or more Tests, which are contained in the Tests project. In order to invoke these test cases, you will need `NUnit 3.0 Test Adapter Extension` for Visual Studio. Once the SDK is complied, the test cases should appear in the Test Explorer window. Here, you can click `Run All` to execute these test cases.



