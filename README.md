<h1 align="center">
  <br />
  <img
    src="./_docs/assets/icon.png"
    alt="Mega Man Robots API"
    width="150"
  />
  <br />
  <b>Mega Man Robots API</b>
  <br />
  <sub
    ><sup><b>(MEGA-MAN-ROBOTS)</b></sup></sub
  >
  <br />
  </h1>

This repository contains a .NET Core-based API designed to manage and provide data about *MegaMan* bosses, serving as a backend for applications requiring this information in JSON format. This project leverages [.NET](https://dot.net) open source technologies to deliver a robust solution for listing MegaMan boss data in the following JSON format:
```json
{
  "Id": 1,
  "Code": "DLN/DRN-003",
  "Name": "Cutman",
  "HP": 150,
  "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
```


This repository is not an official .NET or .NET Framework support location, however, we will respond to issues filed here as best we can. Please file .NET product issues at the main project repositories listed below.

## In this repository

- [Project Overview](#project-overview)
- [Installation Guide](Documentation/INSTALLATION.md)
- [Project Structure](#project-structure)
- [Endpoints](#endpoints)
- [Techniques Used](#techniques-used)
- [Dependencies](#dependencies)

Please contribute to this repository via [pull requests](https://github.com/seu-usuario/megaman-bosses-api/pulls).

## Project Overview

This project is an API built with [.NET Core 3.1](https://dotnet.microsoft.com/en-us/download/dotnet/3.1) to list and manage data about MegaMan bosses. Its primary goal is to serve as a backend providing JSON responses for applications needing MegaMan boss information. The API uses a service layer (`IRobotServices`) to handle data operations and is built with a modular structure for scalability.

For detailed setup instructions, see the [Installation Guide](Documentation/INSTALLATION.md).

## Project Structure

The project is organized as follows:  
- .vs/ : Visual Studio configuration files  
- .vscode/ : Visual Studio Code settings  
- bin/ : Compiled binaries  
- Controllers/ : API controllers  
- Database/ : Database configurations (DbContext, migrations)  
- middlewares/ : Custom middlewares  
- Models/ : Data models and DTOs  
- obj/ : Temporary build files  
- Properties/ : Project properties  
- Services/ : Business logic and services  
- appsettings.json : General configuration  
- appsettings.Development.json : Development environment settings  
- global.json : .NET global configuration  
- MegamanApi.csproj : Project file  
- MegamanApi.sln : Visual Studio solution  
- Program.cs : Application entry point  
- Startup.cs : API startup configuration  

## Endpoints

The API provides the following endpoints under the `api/v1/robots` route:

| Method | Endpoint            | Description                         | Success Response         | Error Response                  |
|--------|---------------------|-------------------------------------|--------------------------|---------------------------------|
| GET    | /api/v1/robots      | Retrieves a list of all bosses      | 200 OK (JSON array)      | -                               |
| GET    | /api/v1/robots/{id} | Retrieves a specific boss by ID     | 200 OK (JSON object)     | 404 Not Found (error message)   |
| POST   | /api/v1/robots      | Placeholder for creating a new boss | 200 OK                   | -                               |

## Techniques Used

The project incorporates the following development techniques:  
- **Dependency Injection**: Used to inject `IRobotServices` into the `RobotsController`, promoting loose coupling and testability.  
- **Repository/Service Pattern**: Business logic is abstracted into the `Services` layer, separating it from controllers.  
- **RESTful Design**: Endpoints follow REST conventions with appropriate HTTP methods (GET, POST) and meaningful routes.  
- **Object-Relational Mapping (ORM)**: [Microsoft.EntityFrameworkCore](https://github.com/dotnet/efcore) maps database entities to C# objects.  
- **DTOs (Data Transfer Objects)**: `RobotReadDTO` structures data returned by the API, ensuring encapsulation.  

## Dependencies

The project depends on the following NuGet packages:  

| Name                                      | Version | Description                                      |
|-------------------------------------------|---------|------------------------------------------------|
| [Microsoft.EntityFrameworkCore]           | 3.1.8   | ORM for database access                        |
| [Microsoft.EntityFrameworkCore.Design]    | 3.1.8   | Design-time tools for EF Core                  |
| [Microsoft.EntityFrameworkCore.SqlServer] | 3.1.8   | SQL Server database provider for EF Core       |
| [Newtonsoft.Json]                         | 12.0.2  | Library for JSON serialization/deserialization |

## Finding .NET Open Source Projects

Here are some excellent community-maintained lists of projects & libraries:  
- [Awesome .NET](https://github.com/quozd/awesome-dotnet)  
- [Awesome .NET MAUI](https://github.com/jsuarezruiz/awesome-dotnet-maui)  
- [Awesome Blazor](https://github.com/AdrienTorris/awesome-blazor)  

There are many projects that you can use and contribute to, some of which are listed below. Please do contribute to these projects!

### .NET

- [.NET (dotnet/core)](https://github.com/dotnet/core)  
- [ASP.NET Core (dotnet/aspnetcore)](https://github.com/dotnet/aspnetcore)  
- [Entity Framework Core (dotnet/efcore)](https://github.com/dotnet/efcore)  
- [JSON.NET (JamesNK/Newtonsoft.Json)](https://github.com/JamesNK/Newtonsoft.Json)  

### .NET Docs

- [.NET docs (dotnet/docs)](https://github.com/dotnet/docs)  
- [ASP.NET Core docs (dotnet/AspNetCore.Docs)](https://github.com/dotnet/AspNetCore.Docs)  
- [Entity Framework docs (dotnet/EntityFramework.Docs)](https://github.com/dotnet/EntityFramework.Docs)  

### Community

Here is a short list of projects to check out:  
- [MonoGame](https://github.com/MonoGame/MonoGame)  
- [MVVM Cross](https://github.com/MvvmCross/MvvmCross)  
- [ReactiveUI](https://github.com/reactiveui/ReactiveUI)  

## .NET Foundation

This project aligns with the goals of the [.NET Foundation](https://www.dotnetfoundation.org/projects), which supports many .NET open source initiatives, including ASP.NET Core and .NET Core. You may want to consider [joining the .NET Foundation](https://dotnetfoundation.org/community/).  

Check out the [.NET Foundation Forums](https://forums.dotnetfoundation.org/) to see what others are talking about, or start a new discussion to ask a question or make a point.

## License

This repository is licensed with the [MIT](LICENSE) license.

🎮 Celso Ocampo Castro -
[(https://github.com/GuJinCell)]
