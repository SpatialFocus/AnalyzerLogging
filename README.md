# AnalyzerLogging

When using .NET analyzers (see [.NET Compiler Platform](https://github.com/dotnet/roslyn)) like the [StyleCop Analyzer](https://github.com/DotNetAnalyzers/StyleCopAnalyzers) you can enable logging of the analyzer results for builds in the  [SARIF](https://github.com/sarif-standard/sarif-spec) JSON file format. This is done by adding `<ErrorLog>` to the `<PropertyGroup>` configuration section in the proj file.

To make this configuration step more convenient you can use AnalyzerLogging which adds

    <Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
        <PropertyGroup>
            <ErrorLog>$(MSBuildProjectDirectory)\report.json</ErrorLog>
        </PropertyGroup>
    </Project>

via a shared props file.

To install AnalyzerLogging, run the following command in the Package Manager Console

    Install-Package AnalyzerLogging
