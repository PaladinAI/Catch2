# Catch2

Catch2 is a C++ test framework used by the [Collector](https://github.com/PaladinAI/ddat-collector),
[Local Agent](https://github.com/PaladinAI/ddat-localagent) and
[Platform](https://github.com/PaladinAI/ddat-platform).

# Syncing with the upstream master branch

First, make sure the `upstream` remote is configured:

    git remote -v

    # If the upstream remote doesn't exist, add it:
    git remote add upstream https://github.com/catchorg/Catch2.git

Then merge the upstream changes from the `master` branch:

    git fetch upstream
    git checkout develop
    git merge upstream/master

# Publishing to the Conan server

To update the package, update the version number in `conanfile.py` then run:

    conan export-pkg . Catch/2.4.1@paladin/develop --build-folder=Build
    conan upload Catch/2.4.1@paladin/develop -r paladin
