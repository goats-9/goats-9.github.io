---
title: "docker on Android Part 3: Building docker"
date: 2023-12-27T12:18:10+05:30
draft: false
toc: true
---

**Note: As of the day of writing this, the latest version of the docker package
is broken on Termux.** This part of the blog series demonstrates how to build an
older working version of docker. If the latest version of docker works, please
skip this part.

In case you require to build an older version of docker, the following steps may
be helpful.

1. Follow the instructions
   [here](https://github.com/termux/termux-packages/wiki/Build-environment) to
   setup the package building environment on your Host OS preferably.

2. Checkout the relevant version of the `termux-packages` repo.

    ```bash
    git checkout 64e0fe
    ```

3. Build the docker package!

    ```bash
    ./build-package.sh -I docker
    ```

4. **Note**: since this is an outdated version, some source tarball URLs may be
   invalid. Replace them with other source URLs, or if you want to replace them
   with source tarballs for newer versions, ensure that the `sha256sum` is also
   changed.

5. After the packages are built on the Host OS, use `adb push` to push them to
   your phone, where they can then be installed from inside Termux.