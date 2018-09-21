# F# .NET Core project
How to create and develop a F# .NET Core project with Visual Studio Code
## How to install
* install latest .NET Core SDK
* install Visual Studio Code
* install the following extensions:
  * Ionide-fsharp
  * F# Language Server
## How to create a project
Create new Project:

In Terminal goto projects folder
```dotnet new sln -o ConsoleTest```

open Folder ```ConsoleTest```

To create new Library:
```
dotnet new classlib -lang F# -o src/Library
dotnet sln add src/Library/Library.fsproj
```

To create new console application:
```
dotnet new console -lang F# -o src/App
dotnet add src/App/App.fsproj reference src/Library/Library.fsproj
dotnet sln add src/App/App.fsproj
```