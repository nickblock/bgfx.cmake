bgfx.cmake
===================

[![Build Status](https://travis-ci.org/JoshuaBrookover/bgfx.cmake.svg?branch=master)](https://travis-ci.org/JoshuaBrookover/bgfx.cmake)

This repo is a fork of [bgfx.cmake](https://travis-ci.org/JoshuaBrookover/bgfx.cmake), to facilitate building bgfx for android.

It also merges [taka-no-me](https://github.com/taka-no-me/android-cmake) in.

Building
-------------

```

Set environment ANDROID_NDK_ROOT to the root of your ndk tools.

git clone https://github.com/JoshuaBrookover/bgfx.cmake.git
cd bgfx.cmake
git submodule init
git submodule update
mkdir build-android
cd build-android
cmake -DCMAKE_TOOLCHAIN_FILE=../cmake/android.toolchain.cmake -DANDROID_NDK=$ANDROID_NDK_ROOT -DCMAKE_BUILD_TYPE=Release -DANDROID_ABI="armeabi-v7a" -DANDROID_NATIVE_API_LEVEL=24 -DANDROID=1 ..
```

