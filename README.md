# Repro for dotnet pack error

Clone this repro, `cd` into `ClassLibrary/ClassLibrary`, and run `dotnet pack -c Release`:

    PS C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1> dotnet pack -c Release
    Microsoft (R) Build Engine version 15.1.1012.6693
    Copyright (C) Microsoft Corporation. All rights reserved.

    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018: The "PackTask" task failed unexpectedly.\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018: System.IO.FileNotFoundException: File not found: 'C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\bin\Release\netstandard1.4\ClassLibrary1.dll'.\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at NuGet.Packaging.PackageBuilder.AddFiles(String basePath, String source, String destination, String exclude)\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at NuGet.Packaging.PackageBuilder.PopulateFiles(String basePath, IEnumerable`1 files)\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at NuGet.Commands.MSBuildProjectFactory.CreateBuilder(String basePath, NuGetVersion version, String suffix, Boolean buildIfNeeded, PackageBuilder builder)\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at NuGet.Commands.PackCommandRunner.BuildFromProjectFile(String path)\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at NuGet.Commands.PackCommandRunner.BuildPackage(String path)\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at NuGet.Commands.PackCommandRunner.BuildPackage()\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at NuGet.Build.Tasks.Pack.PackTask.Execute()\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at Microsoft.Build.BackEnd.TaskExecutionHost.Microsoft.Build.BackEnd.ITaskExecutionHost.Execute()\r [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
    C:\Program Files\dotnet\sdk\1.0.3\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(104,5): error MSB4018:    at Microsoft.Build.BackEnd.TaskBuilder.<ExecuteInstantiatedTask>d__25.MoveNext() [C:\Work\DotnetPackErrorRepro\ClassLibrary1\ClassLibrary1\ClassLibrary1.csproj]
