# Giraffe.ViewEngine.StrongName

This repo is a plain fork of [Giraffe.ViewEngine](https://github.com/giraffe-fsharp/Giraffe.ViewEngine) that adds a strong name to the assembly. If you are on any modern .NET environment (.NET core / .NET 5+), you do not need to bother with this.

You can read more on the hassle with strong names in the respective discussion issues https://github.com/giraffe-fsharp/Giraffe.ViewEngine/issues/23 https://github.com/plotly/Plotly.NET/issues/175. In short: if you can avoid strong naming your library, i'd recommend doing just that.

## release process

- update fork from upstream

- mirror changes from `src/Giraffe.ViewEngine/Giraffe.ViewEngine.fsproj` to `src/Giraffe.ViewEngine.StrongName/Giraffe.ViewEngine.StrongName.fsproj` (if there are any)

- in the project root run 
	```
	dotnet pack src/Giraffe.ViewEngine.StrongName/Giraffe.ViewEngine.StrongName.fsproj /property:<version of Giraffe.ViewEngine package> -c Release
	```

- publish package to nuget