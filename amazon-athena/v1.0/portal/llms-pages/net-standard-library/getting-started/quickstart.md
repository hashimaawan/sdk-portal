# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

<p>Amazon Athena is an interactive query service that lets you use standard SQL to analyze data directly in Amazon S3. You can point Athena at your data in Amazon S3 and run ad-hoc queries and get results in seconds. Athena is serverless, so there is no infrastructure to set up or manage. You pay only for the queries you run. Athena scales automatically—executing queries in parallel—so results are fast, even with large datasets and complex queries. For more information, see <a href="http://docs.aws.amazon.com/athena/latest/ug/what-is.html">What is Amazon Athena</a> in the <i>Amazon Athena User Guide</i>.</p> <p>If you connect to Athena using the JDBC driver, use version 1.1.0 of the driver or later with the Amazon Athena API. Earlier version drivers do not support the API. For more information and to download the driver, see <a href="https://docs.aws.amazon.com/athena/latest/ug/connect-with-jdbc.html">Accessing Amazon Athena with JDBC</a>.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="https://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


Amazon Web Services documentation: [https://docs.aws.amazon.com/athena/](https://docs.aws.amazon.com/athena/)


# Building

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore is enabled, these dependencies will be installed automatically. Therefore, you will need internet access for build.

* Open the solution (AmazonAthena.sln) file.

Invoke the build process using Ctrl + Shift + B shortcut key or using the Build menu as shown below.

The build process generates a portable class library, which can be used like a normal class library. More information on how to use can be found at the MSDN Portable Class Libraries documentation.

The supported version is **.NET Standard 2.0**. For checking compatibility of your .NET implementation with the generated library, [click here](https://dotnet.microsoft.com/en-us/platform/dotnet-standard#versions).


# Installation

The following section explains how to use the AmazonAthena.Standard library in a new project.

## 1. Starting a new project

For starting a new project, right click on the current solution from the solution explorer and choose `Add -> New Project`.

![Add a new project in Visual Studio](https://apidocs.io/illustration/cs?workspaceFolder=Amazon%20Athena-CSharp&workspaceName=AmazonAthena&projectName=AmazonAthena.Standard&rootNamespace=AmazonAthena.Standard&step=addProject)

Next, choose `Console Application`, provide `TestConsoleProject` as the project name and click OK.

![Create a new Console Application in Visual Studio](https://apidocs.io/illustration/cs?workspaceFolder=Amazon%20Athena-CSharp&workspaceName=AmazonAthena&projectName=AmazonAthena.Standard&rootNamespace=AmazonAthena.Standard&step=createProject)

## 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the `TestConsoleProject` as the start-up project. To do this, right-click on the `TestConsoleProject` and choose `Set as StartUp Project` form the context menu.

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Amazon%20Athena-CSharp&workspaceName=AmazonAthena&projectName=AmazonAthena.Standard&rootNamespace=AmazonAthena.Standard&step=setStartup)

## 3. Add reference of the library project

In order to use the `AmazonAthena.Standard` library in the new project, first we must add a project reference to the `TestConsoleProject`. First, right click on the `References` node in the solution explorer and click `Add Reference...`

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Amazon%20Athena-CSharp&workspaceName=AmazonAthena&projectName=AmazonAthena.Standard&rootNamespace=AmazonAthena.Standard&step=addReference)

Next, a window will be displayed where we must set the `checkbox` on `AmazonAthena.Standard` and click `OK`. By doing this, we have added a reference of the `AmazonAthena.Standard` project into the new `TestConsoleProject`.

![Creating a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Amazon%20Athena-CSharp&workspaceName=AmazonAthena&projectName=AmazonAthena.Standard&rootNamespace=AmazonAthena.Standard&step=createReference)

## 4. Write sample code

Once the `TestConsoleProject` is created, a file named `Program.cs` will be visible in the solution explorer with an empty `Main` method. This is the entry point for the execution of the entire solution. Here, you can add code to initialize the client library and acquire the instance of a Api class. Sample code to initialize the client library and using Api methods is given in the subsequent sections.

![Adding a project reference](https://apidocs.io/illustration/cs?workspaceFolder=Amazon%20Athena-CSharp&workspaceName=AmazonAthena&projectName=AmazonAthena.Standard&rootNamespace=AmazonAthena.Standard&step=addCode)


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| Production | **Default** The Amazon Athena multi-region endpoint |
| Environment2 | The Amazon Athena multi-region endpoint |
| Environment3 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |
| Environment4 | The Amazon Athena endpoint for China (Beijing) and China (Ningxia) |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Region | `Models.Region` | The AWS region<br>*Default*: `Region.useast1` |
| Environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.Production`** |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(30)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/sdk-infrastructure/configuration/httpclientconfigurationbuilder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| LogBuilder | [`LogBuilder`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/sdk-infrastructure/configuration/logbuilder.md) | Represents the logging configuration builder for API calls |
| CustomHeaderAuthenticationCredentials | [`CustomHeaderAuthenticationCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md) | The Credentials Setter for Custom Header Signature |

The API client can be initialized as follows:

## Code-Based Initialization

```csharp
using AmazonAthena.Standard;
using AmazonAthena.Standard.Authentication;
using AmazonAthena.Standard.Models;
using Microsoft.Extensions.Logging;

namespace ConsoleApp;

AmazonAthenaClient client = new AmazonAthenaClient.Builder()
    .CustomHeaderAuthenticationCredentials(
        new CustomHeaderAuthenticationModel.Builder(
            "Authorization"
        )
        .Build())
    .HttpClientConfig(httpClientConfig =>
        httpClientConfig.Timeout(TimeSpan.FromSeconds(100)))
    .Environment(AmazonAthena.Standard.Environment.Production)
    .Region(Region.Useast1)
    .LoggingConfig(config => config
        .LogLevel(LogLevel.Information)
        .RequestConfig(reqConfig => reqConfig.Body(true))
        .ResponseConfig(respConfig => respConfig.Headers(true))
    )
    .Build();
```

## Configuration-Based Initialization

```csharp
using AmazonAthena.Standard;
using Microsoft.Extensions.Configuration;

namespace ConsoleApp;

// Build the IConfiguration using .NET conventions (JSON, environment, etc.)
var configuration = new ConfigurationBuilder()
    .AddJsonFile("config.json")
    .AddEnvironmentVariables() // [optional] read environment variables
    .Build();

// Instantiate your SDK and configure it from IConfiguration
var client = AmazonAthenaClient
    .FromConfiguration(configuration.GetSection("AmazonAthena"));
```

See the [Configuration-Based Initialization](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/sdk-infrastructure/configuration/configuration-based-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`hmac (Custom Header Signature)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)

## hmac (Custom Header Signature)



Documentation for accessing and setting credentials for hmac.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| Authorization | `string` | Amazon Signature authorization v4 | `Authorization` | `Authorization` |



**Note:** Auth credentials can be set using `CustomHeaderAuthenticationCredentials` in the client builder and accessed through `CustomHeaderAuthenticationCredentials` method in the client instance.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```csharp
using AmazonAthena.Standard;
using AmazonAthena.Standard.Authentication;

namespace ConsoleApp;

AmazonAthenaClient client = new AmazonAthenaClient.Builder()
    .CustomHeaderAuthenticationCredentials(
        new CustomHeaderAuthenticationModel.Builder(
            "Authorization"
        )
        .Build())
    .Build();
```




