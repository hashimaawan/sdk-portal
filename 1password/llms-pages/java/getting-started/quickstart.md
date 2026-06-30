# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

REST API interface for 1Password Connect.


# Building

Supported Java version is **8+**.

The generated code uses a few Maven dependencies e.g., Jackson, OkHttp,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on `File -> Import`.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=import0)

* In the import dialog, select `Existing Java Project` and click `Next`.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=import1)

* Browse to locate the folder containing the source code. Select the detected location of the project and click `Finish`.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=import2)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=import3)

* After successfully building the project, the client library needs to be installed as a Maven package in your local cache. Right-click on the project, select `Show in Local Terminal -> Terminal` or use `Ctrl + Alt + T` to open Terminal.

![Importing SDK into Eclipse - Step 5](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=openTerminal)

* In the terminal dialog, run the following command to install client library.

```
mvn install -Dmaven.test.skip=true -Dmaven.javadoc.skip=true
```

![Importing SDK into Eclipse - Step 6](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=installCommand)


# Installation

The following section explains how to use the M1PasswordConnectLib library in a new project.

## 1. Starting a new project

For starting a new project, click the menu command `File > New > Project`.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=createNewProject0)

Next, choose `Maven > Maven Project` and click `Next`.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=createNewProject1)

Here, make sure to use the current workspace by choosing `Use default Workspace location`, as shown in the picture below and click `Next`.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=createNewProject2)

Following this, select the *quick start* project type to create a simple project with an existing class and a `main` method. To do this, choose `maven-archetype-quickstart` item from the list and click `Next`.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=createNewProject3)

In the last step, provide a `Group Id` and `Artifact Id` as shown in the picture below and click `Finish`.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=createNewProject4)

## 2. Add reference of the library project

The created Maven project manages its dependencies using its `pom.xml` file. In order to add a dependency on the *M1PasswordConnectLib* client library, double click on the `pom.xml` file in the `Package Explorer`. Opening the `pom.xml` file will render a graphical view on the canvas. Here, switch to the `Dependencies` tab and click the `Add` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=testProject0)

Clicking the `Add` button will open a dialog where you need to specify M1PasswordConnectLib in `Group Id`, m1-password-connect-lib in `Artifact Id` and 1.5.7 in the `Version` fields. Once added click `OK`. Save the `pom.xml` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=testProject1)

![Adding sample code](https://apidocs.io/illustration/java?workspaceFolder=1Password%20Connect-Java&workspaceName=M1PasswordConnect&projectName=M1PasswordConnectLib&rootNamespace=local.m1password&groupId=M1PasswordConnectLib&artifactId=m1-password-connect-lib&version=1.5.7&step=testProject2)

## 3. Write sample code

Once the `SimpleConsoleApp` is created, a file named `App.java` will be visible in the *Package Explorer* with a `main` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |
| ENVIRONMENT2 | - |
| ENVIRONMENT3 | - |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/sdk-infrastructure/configuration/httpclientconfiguration-builder.md) | Set up Http Client Configuration instance. |
| loggingConfig | [`Consumer<ApiLoggingConfiguration.Builder>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/sdk-infrastructure/configuration/apiloggingconfiguration-builder.md) | Set up Logging Configuration instance. |
| bearerAuthCredentials | [`BearerAuthCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/getting-started/quickstart/authorization.md) | The Credentials Setter for OAuth 2 Bearer token |

The API client can be initialized as follows:

```java
import local.m1password.Environment;
import local.m1password.M1PasswordConnectClient;
import local.m1password.authentication.BearerAuthModel;
import local.m1password.exceptions.ApiException;
import local.m1password.http.response.ApiResponse;
import org.slf4j.event.Level;

public class Program {
    public static void main(String[] args) {
        M1PasswordConnectClient client = new M1PasswordConnectClient.Builder()
            .loggingConfig(builder -> builder
                    .level(Level.DEBUG)
                    .requestConfig(logConfigBuilder -> logConfigBuilder.body(true))
                    .responseConfig(logConfigBuilder -> logConfigBuilder.headers(true)))
            .httpClientConfig(configBuilder -> configBuilder
                    .timeout(0))
            .bearerAuthCredentials(new BearerAuthModel.Builder(
                    "AccessToken"
                )
                .build())
            .environment(Environment.PRODUCTION)
            .build();

    }
}
```


# Authorization

This API uses the following authentication schemes.

* [`ConnectToken (OAuth 2 Bearer token)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/getting-started/quickstart/authorization.md)

## ConnectToken (OAuth 2 Bearer token)



Documentation for accessing and setting credentials for ConnectToken.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| AccessToken | `String` | The OAuth 2.0 Access Token to use for API requests. | `accessToken` | `getAccessToken()` |



**Note:** Auth credentials can be set using `bearerAuthCredentials` in the client builder and accessed through `getBearerAuthCredentials` method in the client instance.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```java
import local.m1password.M1PasswordConnectClient;
import local.m1password.authentication.BearerAuthModel;

public class Program {
    public static void main(String[] args) {
        M1PasswordConnectClient client = new M1PasswordConnectClient.Builder()
            .bearerAuthCredentials(new BearerAuthModel.Builder(
                    "AccessToken"
                )
                .build())
            .build();
    }
}
```




