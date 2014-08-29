CoreMedia Content Management Server Tools
=========================================

Demo gradle script to assemble plain, uncustomized CoreMedia Content Management 
Server Tools in a stripped down variant of how the original Maven based workspace 
layout from CoreMedia does it.

Prerequisites
-------------

- Access to the CoreMedia Maven artifact repositories

- A CoreMedia Content Management Server running somewhere accessible

- Database parameters of that server to be able to use all tools

Usage
-----

Customizing

Change the values in the few config files presented in this workspace as needed. 
E.g. the database access definetely needs some tuning. 

Building

```
gradle build
```

Running

The resulting zip file needs to be extracted and results in the usual CoreMedia
service tools layout. Read the fine manuals at http://documentation.coremedia.com/
for details.

One defect for now is, that the neede libraries still show up in the wrong place.

```
unzip distributions/cm-cms-tools...zip
rmdir lib
mv cm*/lib .
```
