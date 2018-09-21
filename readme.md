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
```dotnet new sln -o FsNetCoreTutorial```

open Folder ```FsNetCoreTutorial```

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
## Add to Git:
Ctrl+Shift+P: Git: Initialize Repository

## Publish to Github:
Create Repository ```FsNetCoreTutorial```, but no Commits!

In Terminal in Visual Studio Code type
```git remote add origin https://github.com/<path to repository>```

Sync project to Githup, then add Readme and License

## How to build:
```Ctrl+Shift+B```
Then choose ```DotNet```
## How to debug:
Press F5, then choose ```DotNet```. ```Edit Launch.json```, Path to Assembly
