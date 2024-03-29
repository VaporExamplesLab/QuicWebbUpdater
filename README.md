# [QuicWebbUpdater][t]
[t]:https://github.com/VaporExamplesLab/QuicWebbUpdater

<p align="center">
    <a href="http://docs.vapor.codes/3.0/">
        <img src="http://img.shields.io/badge/read_the-docs-2196f3.svg" alt="Documentation">
    </a>
    <a href="LICENSE">
        <img src="http://img.shields.io/badge/license-MIT-brightgreen.svg" alt="MIT License">
    </a>
    <a href="https://swift.org">
        <img src="http://img.shields.io/badge/swift-4.2-brightgreen.svg" alt="Swift 4.2">
    </a>
</p>

<a id="toc"></a>
[Getting Started](#GettingStarted) •
[Original Setup](#OriginalSetup) •
[Resources](#Resources) 

## Getting Started <a id="GettingStarted"></a>[▴](#toc)

**Prerequisites**

* [Install Xcode 10 ⇗](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)
* [Install homebrew ⇗](https://brew.sh/)
* [Install vapor toolbox ⇗](https://docs.vapor.codes/3.0/install/macos/)

**Download|Clone & Run**

Steps to download repository:

``` bash
## go to your working directory
cd <your-choosen-directory-path>

## download and unzip
wget https://github.com/VaporExamplesLab/QuicWebbUpdater/archive/master.zip
unzip master.zip -d QuicWebbUpdater
rm master.zip     # remove download

cd QuicWebbUpdater-master

# update dependencies 
# with `-y` yes to generate and open Xcode project
vapor update -y
```

Or, alternate steps to clone repository instead of download:

``` bash
## go to your working directory
cd <your-choosen-directory-path>

## either clone
##    add --bare option for an unattached instance
git clone git@github.com:VaporExamplesLab/QuicWebbUpdater.git 

cd QuicWebbUpdater

# update dependencies 
# with `-y` yes to generate and open Xcode project
vapor update -y
```

Set Xcode scheme Run Arguments.

```
--original-dir='path_original_blog_content'
--processed-dir='path_process_blog_content'
--verbose
```

![Xcode Run Arguments](README_files/XcodeArguments.png)

Click the run button and check the results in a browser at `http://localhost:8080`.

![TBD:LandingPage](README_files/LandingPage.png)

## Original Setup <a id="OriginalSetup"></a>[▴](#toc)

The following steps were completed to create the `QuicWebbUpdater` example. 


``` bash
mkdir QuicWebbUpdater
cd QuicWebbUpdater
swift package init --type executable
swift package generate-xcodeproj
open QuicWebbUpdater.xcodeproj/
```

Setting "upload" creation dates 

``` bash
cd <PATH>/blog_content_original/markdown
## -t changes access and modified times.
touch -t 201811220800 2018/11/FirstPost.md 

touch 2018/11/FirstPost_files/*
touch 2018/11/FirstPost_files/figure1.png
touch 2018/11/FirstPost_files/figure2.jpg
touch 2018/11/FirstPost_files/figure2.png
touch 2018/11/FirstPost_files/figure3.pdf
touch 2018/11/FirstPost_files/figure3.png
touch 2018/11/FirstPost_files/figure4.gif
touch 2018/11/FirstPost_files/figure4.png


touch 2018/11/FirstPost_files/more/*
touch 2018/11/FirstPost_files/more/folder-2103508.svg

```


## Resources <a id="Resources"></a>[▴](#toc)

* [Bootstrap ⇗](https://getbootstrap.com)


