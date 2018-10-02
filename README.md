# Catch2

Catch2 is a C++ test framework used by the [Collector](https://github.com/PaladinAI/ddat-collector),
[Local Agent](https://github.com/PaladinAI/ddat-localagent) and
[Platform](https://github.com/PaladinAI/ddat-platform).

## Publishing to Conan server

To update the package, run:

    conan export-pkg . Catch/2.4.1@paladin/develop --build-folder=Build
    conan upload Catch/2.4.1@paladin/develop -r paladin
