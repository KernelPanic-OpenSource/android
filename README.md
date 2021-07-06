## Credits:
 * [**AOSP**](https://android.googlesource.com)
 * [**Pixel Experience**](https://github.com/PixelExperience)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**AOSP-11**](https://github.com/AOSP-11)
 * [**Octavi**](https://github.com/Octavi-OS)
 * [**CherishOS**](https://github.com/CherishOS)
----------------------------------------------------------------------------

## Getting Started:

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).
----------------------------------------------------------------------------

## Install Build Packages:
Java Open JDK 8
```bash
sudo apt install openjdk-8-jdk
```

Install Packages:
If you use Ubuntu 16.04 -> 21.04 ( Not Have 20.04 ):

```bash
sudo apt install bc bison build-essential ccache curl flex g++-multilib gcc-multilib git gnupg gperf imagemagick lib32ncurses5-dev lib32readline-dev lib32z1-dev liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev libwxgtk3.0-gtk3-dev libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc zip zlib1g-dev libncurses5 python
```

If you use Ubuntu 20.04 :

```bash
sudo apt install bc bison build-essential ccache curl flex g++-multilib gcc-multilib git gnupg gperf imagemagick lib32ncurses5-dev lib32readline-dev lib32z1-dev liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev libwxgtk3.0-gtk3-dev libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc zip zlib1g-dev libncurses5 python
```

Install repo:
```bash
mkdir ~/bin
```
```bash
PATH=~/bin:$PATH #You can add this to .bashrc or .zshrc
```
```bash
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
```
```bash
chmod a+x ~/bin/repo
```
----------------------------------------------------------------------------

## Repo sync:
To initialize your local repository, use a command like this:

```bash
repo init -u https://github.com/KernelPanic-OpenSource/android.git -b 11
```

## Then to sync up:

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
----------------------------------------------------------------------------

## Compilation of AOSP:

From root directory of Project, perform following commands in terminal


```bash
. build/envsetup.sh
 brunch device-codename
```
-----------------------------------------------------------------------------
