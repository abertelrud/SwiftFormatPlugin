# Example - SwiftFormatPlugin

This example command plugin uses the https://github.com/apple/swift-format.git package to reformat source code. It is an example of a plugin that needs additional permissions (in this case to write to the file system). For sample purposes, the formatting instructions are taken from a `.swiftformat` file in the top-level directory of the package.

To use it, first add a dependency on https://github.com/abertelrud/SwiftFormatPlugin.git to your package. Then, assuming that you want to reformat the source code of the target named "MyLibrary" in your package, run:

```shell
swift package plugin --allow-writing-to-package-directory format-source-code --target MyLibrary
```

from the package directory (or use the `--package-path` option if invoking from a different directory).
