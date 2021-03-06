![NET_Core_Logo svg](https://user-images.githubusercontent.com/20155657/131152498-70880e11-80b3-45ab-98a3-60f266f0127f.png)
![csharp-e7b8fcd4ce](https://user-images.githubusercontent.com/20155657/131152478-de89a88c-6240-4d20-8bae-06a527573c24.png)

## Starting new service on .NET Core

Pre-requisited

> Visual Studio IDE is recommended though you can utilize other IDE's like Intelij Rider.<br/>
> We use .NET 5 framework(will be upgrading to .NET 6 when available).

Generating new project

> We use single sln approach for multi-project service<br/>
> Either use Visual Studio for creating new project or use cli: `dotnet new sln`<br/>
> To keep segregation between projects it is recommended that each project should be created in separated folder under sln directory.
>
> ## Steps to create new webapp
>
> - Through cli
>   - Create a directory for solution(sln) and run command `dotnet new sln` to create sln file.
>     - eg: `mkdir DemoApi` navigate to this directory and `dotnet new sln`
>   - Create separate directories for different projects.
>     - Here we will be creating two directories one `DempApi` which will consist of actual project and second will be `DemoApiTest` for xUnit project.
>     - Next we will navigate to `DemoApi` directory and use command `dotnet new webapi`. This will use wepapi template to create a project with some default settings configured.
> - Through IDE
>   - Using Visual Studio create new project and select Web Api template and follow the wizard.

.NET folder naming convention and patterns

> - Recommended approach is to use Pascalcase `eg: TestService, DemoService` for folder, filenames(including classes, interfaces, enums and others), names of methods.
> - CamelCase for local variable names.
>   - add \_ to class members.
>   - Dependency Indected resources must be readonly and should be defined in relevant scope.
> - For services use Interface pattern so you can have different implementations if desired.

Following TDD approach.

> .NET uses separate project for unit test. However, unit test can also be writted within same project but having separate project is recommended.
> For unit test we use xUnit testing tool which is open source and TDD adherent.
>
> ## Steps to create new xUnit project
>
> - Through cli
>   - Follow same approach as above having separate directory for project under your solution folder.
>   - Use command `dotnet new xunit` which uses xunit template to create a project with some default settings configured.
> - Through IDE
>   - Using Visual Studio create new project and select xUnit template and follow the wizard.

## How to

|        Topic        |
| :----------------- |
|    [Authorization](https://github.com/itsbibeksaini/docs/blob/main/DotNet/authorization.md) |
| [Swashbuckle Swagger](https://github.com/itsbibeksaini/docs/blob/main/DotNet/swagger.md) |
|  [Entity framework](https://github.com/itsbibeksaini/docs/blob/main/DotNet/entityframework.md) |
|     [Http Client](https://github.com/itsbibeksaini/docs/blob/main/DotNet/httpclient.md) |
| [gRPC server and client](https://github.com/itsbibeksaini/docs/blob/main/DotNet/gRPC.md) |
| [Startup tasks](https://github.com/itsbibeksaini/docs/blob/main/DotNet/startuptask.md) |
| [Custom razor engine](https://github.com/itsbibeksaini/docs/blob/main/DotNet/customRazorEngine.md) |
| [Custom authorization]() |


