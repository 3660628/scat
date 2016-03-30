


---


# NOTICE #

**This project is not active anymore, all development and issues have now been moved to the** [Phratch project](https://code.google.com/p/phratch/),**which is being actively developed.**


---


**Please take a look at the PublicRelease announcement**

## STATEMENT ##

We believe there is a conspiracy going on all over the universe, evil forces are constantly fighting to take down great Smalltalk projects and port them to other languages.

In a quest against such demonic plots, a couple of us started a confidential mission to rescue the last of these endangered projects, namely [Scratch](http://scratch.mit.edu).

## MOTIVATIONS ##

It has been announced that [Scratch](http://scratch.mit.edu) is to be ported to Flash, which we consider to not be a very good decision for several reasons, including:
  * There is no open source fully working implementation of the language, so it will be impossible to freely develop [Scratch](http://scratch.mit.edu) modifications
  * The previous would endanger the continuity of projects to which we are firmly tied, such as [S4A](http://seaside.citilab.eu/scratch/arduino) or [BYOB](http://byob.berkeley.edu)
  * Flash is not working (and never will) in many embedded devices
  * If the aim of porting the project was to get it to work on the web, we consider flash to be one the worst possible choices, over javascript or even HTML5
  * [Scratch](http://scratch.mit.edu) is a pretty massive project featuring zillions of lines of code. Rewriting it from scratch (pun intended) is gonna feel wrong to many people who spent sleepless hours contributing to it

It is indeed true that [Scratch](http://scratch.mit.edu) is implemented in a very old version of Squeak, which makes modifying it a very difficult, tedious and annoying job, but we consider that dumping Smalltalk for good is not the solution to this problem.

## CONSIDERATIONS ##

Since there are modern implementations of Smalltalk that pretty much overcome all these issues, we took the decision of trying to port the whole project into one of them. We considered [Squeak](http://squeak.org/) and [Pharo](http://pharo-project.org/) to be the two only valid candidates, for obvious compatibility and licensing reasons.

Being [Pharo](http://pharo-project.org/) our main working environment, and because of its development tools being the ones in which we are by far the most productive, this is the dialect that was chosen.

## CURRENT SITUATION ##

Scat is the name of the [Scratch](http://scratch.mit.edu) port for [Pharo](http://pharo-project.org/). Pretty much everything is working, check out the [History](http://code.google.com/p/scat/wiki/History) of the project to know what has been done so far.

If you think a video is worth a thousand words, you may want to check out our ShowCase.

## FUTURE STEPS ##

We are not doing this just to have [Scratch](http://scratch.mit.edu) working in [Pharo](http://pharo-project.org/). At some point, we intend to re-engineer some of the awfully architectured parts of the project and make it modular enough to be able to extract certain parts of it for other pieces of software.

Imagine having a [Scratch](http://scratch.mit.edu) block palette and execution engine to have children (and not only children) make awesome music with, or visualizations, or scientific simulations, or even websites!

In short, imagine being able to bring the easiness of programming with [Scratch](http://scratch.mit.edu) to any possible field of computing!

THAT is our goal.

## WHAT YOU CAN DO ##

Oh sure, please come and help us! There are three levels of implication in which you can be of great use:

  * Install Scat and try it out, it is really easy, independently of your operating system, you just need to follow a couple of simple InstallationSteps
  * Find a bug and report it to the authorities at our [issue tracker](http://code.google.com/p/scat/issues/list)
  * Join the project and become the authority that processes these bugs that level-2 people reported: scat-project@googlegroups.com

May the source be with you, and may that source be written in Smalltalk!

![http://i.imgur.com/uMrin.png](http://i.imgur.com/uMrin.png)

Yours sincerely,

The Scat cat

<sub> Logo drawn by Hector Gomez </sub>
[(\*)](http://www.openclipart.org/user-detail/hector%20gomez)