# Single and Multi-Configuration Generators  

Software builds often have several variants which we might be interested in. These variants have names like `Debug`, `Release`, `RelWithDebInfo`, and `MinSizeRel`, with properties corresponding to the name of the given variant.

A single-configuration build system always builds the software the same way, if it is generated to produce Debug builds it will always produce a Debug build. A multi-configuration build system can produce different outputs depending on the configuration specified at build time.

>**Note:** `The terms build configuration and build type are synonymous.` When dealing with single-configuration generators, which only support a single variant, the `generated variant is usually called the "build type"`. When dealing with multi-configuration generators, the available `variants are usually called the "build configurations"`. Selecting a variant at build time is usually called "selecting a configuration" ?and referred to by flags and variables as the "config".

However, this convention is not universal. Both technical and colloquial documentation often mix the two terms. Configuration and config are considered the more correct in contexts which generically address both single and multi-configuration generators.
  

The commonly used generators are as follows:

|Single-Configuration|Multi-Configuration|
|:-------------------|:------------------|
|Ninja               |Ninja Multi-Config
|Unix Makefiles      |Visual Studio (all versions)
|FASTBuild           |Xcode  

When using a single-configuration generator, the build type is selected based on the `CMAKE_BUILD_TYPE` environment variable, or can be specified directly when invoking CMake via cmake `-DCMAKE_BUILD_TYPE=<config>`.

