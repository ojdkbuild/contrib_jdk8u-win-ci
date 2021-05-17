OpenJDK 8 Windows CI setup
==========================

[![appveyor](https://ci.appveyor.com/api/projects/status/github/ojdkbuild/contrib_jdk8u-win-ci?svg=true)](https://ci.appveyor.com/project/ojdkbuild/contrib-jdk8u-win-ci)

OpenJDK [8u-dev](https://hg.openjdk.java.net/jdk8u/jdk8u-dev/) Windows build setup on AppVeyor CI using VS2010/SDK7.1 toolchain. By default `x86` and `x86_64` builds are done in `fastdebug` mode, resulting artifacts are ignored.

Intended usage for testing patches on top of 8u-dev tip:

1. create a new repo in your GitHub account

2. copy there [appveyor.yml](https://github.com/ojdkbuild/contrib_jdk8u-win-ci/blob/master/appveyor.yml) file from this repo

3. add jdk patches to your repo and apply them to jdk8u-dev sources with `hg import` in [install](https://github.com/ojdkbuild/contrib_jdk8u-win-ci/blob/master/appveyor.yml#L36) section of the build script

4. register your GitHub account with [AppVeyor](https://ci.appveyor.com/login) using "Login with GitHub"

5. enable builds your project using "Projects" - "New Project"

6. adjust build settings (debug level, bootcyle etc) as needed

