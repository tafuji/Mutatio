# Mutatio
Visual Studio for Mac add-in/extension for converting old PCLs to .NET Standard 2.0 targeting projects automatically.

## Warning

```This extension is making it first steps, please make sure you have a back up of your code before using it!```

## Installation

1. Download the `.mpack` file from [here](https://github.com/yuv4ik/mutatio/tree/master/Versions)
2. Launch Visual Studio, open the Visual Studio menu and select `Extensions...`
3. In the bottom left of the Extensions Manager dialog, click `Install from file...`
4. Choose the `.mpack` file you downloaded in step 1
5. When prompted, select Install

## Usage

`Mutatio` can convert newly created or existing projects. Please keep in mind that there might be `NuGet` packages that does not support .NET Standard 2.0, in this case you may see `NuGet` related exceptions.

In order to convert a project, right click on it and select `Convert to NET Standard 2.0`.

## Details

The technical conversion from old PCL to .NET Standard 2.0 is very simple and described [here](https://gist.github.com/yuv4ik/063a35fe3986e62d69aee2f0ed0607bf).

#### The conversion process is consist of:

* Creating a backup of `*.csproj`, `packages.config` & `/Properties` in `root/mutatio_backup`
* Generating new `*.csproj`
    * All the packages from `packages.json` will be defined in new `*.csproj`
* Deleting of `*.csproj`, `packages.config` & `/Properties`
* Re-opening the solution

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details