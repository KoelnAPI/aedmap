aedmap
======

Mobile web application for the display of automated external defibrillator (AED)
locations in Cologne, Germany.

**Note:** This code is in a very early stage. Lots of feedback has to be gathered
and improvements have to be made until this should be released to a broader audience.

Current version in development can be testet here: http://www.sendung.de/aedcgn/

# Screenshots

![Screenshot 1](https://github.com/KoelnAPI/aedmap/raw/master/screenshots/2014-04-15_01_alert.png)
![Screenshot 2](https://github.com/KoelnAPI/aedmap/raw/master/screenshots/2014-04-15_02_routing.png)

# Design principles

* Optimized for use with a smartphone
* Fast loading, even with sub-optimal network bandwidth
* Simplicity, optimized for the emergency case (see below)

# Intended use cases

This application is built to enable the following szenarios:

## Detection of nearest AED

*As a user, I want to quickly find the location of the nearest AED.*

In an emergency situation, "nearest" means: Taking the shortest time to fetch.

This should make use of the current position of the user which might be detected by
the device using GPS or other means. The application should find out whether there
is only one "best guess" or whether there are several close candidates.

If there is
only one good AED in reach, the application should quickly help the user to identify
the AED location and help him/her to find their way there. 

If several AEDs are within reach, the application might use additional resources to
find out which candidate would be fastest. For example, the application could prompt
several locations via GraphHopper (pedestrian routing) and find out which can be reached
fastest.

## Browsing the environment

*As a user, I want to inform myself of AED locations nearby.*

In contrast to the emergency use case, this szenario should encourage the exploration of
the environment. A user could browse her day to day environment like a place of work in order
find out where to get an AED in an emergency situation.

## Location checking

*As a data maintainer, I want to make sure that AED locations are correct.*

The application should enable maintainers of the lcoation data to check the position
of an AED when "on the road". With GPS positioning enabled, the user could quickly identify
how good a marker matches an AED position.

## Feedback

Please leave feedback via the issues. Please be granular, i.e. open several issues if you
have feedback on several unrelated aspects of the app.

## License

MIT licensed. See file LICENSE.

## Data

The AED location data is maintained in a different repository. See https://github.com/KoelnAPI/data/tree/master/data/health/aed .

## CHANGELOG

* April 14, 2014: Added *routing*. See [issue #7](https://github.com/KoelnAPI/aedmap/issues/7) for details.
* April 4, 2014: Changed map background to custom, pre-rendered tiles. See [issue #3](https://github.com/KoelnAPI/aedmap/issues/3) for details.

