Credits:
=======
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**AOSP-11**](https://github.com/AOSP-11)
----------------------------------------------------------------------------

Getting Started:
==============

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Repo sync:
===============

To initialize your local repository, use a command like this:

```bash
    repo init -u https://github.com/KernelPanic-OpenSource/android.git -b 11
```

Then to sync up:
================

```bash
    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
Compilation of AOSP:
====================

From root directory of Project, perform following commands in terminal


```bash
. build/envsetup.sh
 brunch device-codename
```
-----------------------------------------------------------------------------
