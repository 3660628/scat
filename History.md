# Introduction #

This page explains everything that's been done so far and what problems we have found to the current point.

# Demo #

Since a video is worth a hundred screenshots and a thousand words, we have recorded a short screencast showing some of the features that are already working:

<a href='http://www.youtube.com/watch?feature=player_embedded&v=3tcYcTBc0is' target='_blank'><img src='http://img.youtube.com/vi/3tcYcTBc0is/0.jpg' width='425' height=344 /></a>

# Scat Squeaksource repository #

Found [here](http://www.squeaksource.com/nscratch.html).

This repository is meant to hold a package that can be loaded from a 1.2.1 image to get a full-working Scat in it.

Upon loading the project, an automatic installer is fired up and all required files are downloaded and extracted (if missing), namely:
  * Original Scratch Plugins (_[download](http://code.google.com/p/scat/downloads/detail?name=scratchPlugins.zip)_)
  * Original Scratch Skins (_[download](http://download.scratch.mit.edu/source-code/ScratchSkin1.4.zip)_)
  * Original Scratch Media (_[download](http://code.google.com/p/scat/downloads/detail?name=Media.zip)_)
  * Original Scratch Locales (_[download](http://code.google.com/p/scat/downloads/detail?name=locale.zip)_)
  * Original Scratch Help (_[download](http://code.google.com/p/scat/downloads/detail?name=Help.zip)_)

Additionally, the installer adds all needed instance and class variables to system classes (VariableAdditionReference). The ExtensionsReference page details all methods that are either added to system classes or modified upon loading the project.

Please visit the [issue tracker](http://code.google.com/p/scat/issues/list) for better details on each bug.

# General concerns #

  * In many cases, the Scratch implementation took advantage of old Squeak bugs, like writing into parameters (both method and block parameters), which has been solved by creating local variables that take the value of the parameter, are used as necessary and are returned at the end of the method/block.
  * In other cases, scope bugs were abused, which also had to be fixed by using local variables.
  * Should the final product be an independent package loadable into Pharo or a full Pharo-based image?
  * Note that this project needs to add and modify quite a lot of system methods, mainly from the Morphic package, but also from some other kernel classes, like Number or String. For this reason, it is **strongly recommended** that you install the Scat package in a fresh image, as detailed in the InstallationSteps wiki page.
  * In some cases, instance and class variables had to be added into system classes, which is why we had to extend some class initialization methods as follows:
```
    ClassThatNeedsAnExtraInstVar >> initialize
       "If we don't check whether the variable already exists 
        we'll get an error when loading the package for the second time"
       (self instVarNames includes: 'someInstanceVariable') 
            ifFalse: [self addInstVarName: 'someInstanceVariable']
```

# Scat Image #

This image is now **obsolete**, as the monticello package has advanced to the point where downloading a full image is pointless. Please refer to the InstallationSteps wiki page for further instructions.

In any case, it's still downloadable [here](http://code.google.com/p/scat/downloads/detail?name=Pharo.zip&can=2&q=).