## Enable hotreload in Visual Studio for ASP.Net project

To enable runtime compilation for all environments:

Install the Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation NuGet package.

Run the below command in the folder contains .csprj file
```
dotnet add package Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation --version <depending on .net version in the project>

```
Call AddRazorRuntimeCompilation in Program.cs:

C#

Copy
var builder = WebApplication.CreateBuilder(args);

builder.Services.AddRazorPages()
    .AddRazorRuntimeCompilation();

https://learn.microsoft.com/en-us/aspnet/core/mvc/views/view-compilation?view=aspnetcore-6.0&tabs=visual-studio#enable-runtime-compilation-for-all-environments
