# Build, test, and deploy with TeamCity .NET runner
The TeamCity .NET runner is a powerful tool for automating .NET development tasks. It supports all the .NET frameworks and allows you to easily manage automated builds, tests, and deployments.

The new runner supports NuGet installers, NUnit tests, F# projects, and [.NET CLI commands](https://docs.microsoft.com/en-us/dotnet/core/tools/). It also offers integration with version control systems, issue trackers, and continuous integration systems.

Before using TeamCity's .NET runner, ensure that you have .NET Framework 4.0 or higher, MSBuild 12.0 or higher, and an installed NuGet package.

For now, the .NET runner can execute the following commands:

| Basic .NET CLI commands      | Advanced commands | Visual Studio command-line mode |
| ----------- | ----------- | ----------- 
| [build](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-build)      | [msbuild](https://www.jetbrains.com/help/teamcity/net.html#msbuild)       | [devenv](https://www.jetbrains.com/help/teamcity/net.html#Visual+Studio+Command-Line+Mode) |
| [clean](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-clean)   | [vstest](https://www.jetbrains.com/help/teamcity/net.html#vstest)        | |
| [restore](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-restore) (requires .NET CLI 2.1.400+ for authentication in private feeds)      | [nuget delete](https://www.jetbrains.com/help/teamcity/net.html#nuget+delete) (requires .NET CLI 2.1.500+ for authentication in private feeds)       | |
| [pack](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-pack)   | [nuget push](https://www.jetbrains.com/help/teamcity/net.html#nuget+push) (requires .NET CLI 2.1.500+ for authentication in private feeds)        | |
| [publish](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-publish)      | | |
| [run](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-run)   | | |
| [test](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-test)      | | |

At this stage of our development, we aim to follow the example of companies like Microsoft that works to consolidate all .NET functionality into one SDK. TeamCity likewise simplifies creating .NET projects. .NET runner interchanged all previous .NET-related operations thus unifying multiple build runners in one.

However, we offer our users adequate time to move and continue to support outdated runners but do not add any new features to them. If you want to migrate, see the [.NET runner documentation](https://www.jetbrains.com/help/teamcity/net.html#.NET+Version+Detection+Algorithm) for details.

To know more about TeamCity integration with .NET, look through the [source repo](https://github.com/JetBrains/teamcity-dotnet-samples) or read the previous posts for a demo:

- [Part 1](https://blog.jetbrains.com/teamcity/2020/12/teamcity-integration-with-net-part-1-new-approach-and-demo/): New approach and demo
- [Part 2](https://blog.jetbrains.com/teamcity/2020/12/teamcity-integration-with-net-part-2-testing-and-building-projects/): Testing and building projects
- [Part 3](https://blog.jetbrains.com/teamcity/2020/12/teamcity-integration-with-net-part-3-deploying-projects/): Deploying projects

To use the .NET runner for your project, follow a few simple steps below.

1. Log into your TeamCity account and select the project you wish to work on or create a new one. As an example, we used an open-source Dache caching system developed for and in the .NET framework.
