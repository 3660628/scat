# Scat: Installation Steps #

## Required Pharo download ##
  * Download a Pharo 1.3 One Click package with CogVM from: [here](https://gforge.inria.fr/frs/download.php/29274/Pharo-1.3-13315-OneClick.zip).

## Installation ##
<a href='http://www.youtube.com/watch?feature=player_embedded&v=EvnUd4TqkUc' target='_blank'><img src='http://img.youtube.com/vi/EvnUd4TqkUc/0.jpg' width='425' height=344 /></a>

<sub>* WARNING * This process will modify some base Morphic classes and methods from the system, so please use a fresh image!</sub>

If you are behind a web proxy, you need to configure the proxy in the Pharo Settings.

From time to time, SqueakSource site is down. Please check the availability of this web site before launching the install process.

In order to install the last version of Scat, you can execute the following Gofer expression:

```
Gofer new squeaksource: 'nscratch'; package: 'NScratch'; load
```

or load the NScratch package from the following Monticello repository:
```
MCHttpRepository
   location: 'http://www.squeaksource.com/nscratch'
   user: ''
   password: ''
```


  * Be patient, the process might take a while, as several external plugins, media files and other required packages are going to be downloaded and extracted automatically

  * When done, run the following code from a Workspace:
```
ScratchFrameMorph open
```
  * A block browser and canvas should open. Some things work, some don’t...