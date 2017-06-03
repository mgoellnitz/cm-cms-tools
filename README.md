# CoreMedia Content Management Server Tools

CoreMedia Content Management Server Tools assembled with Gradle to illustrate,
what a Gradle based CoreMedia workspace might look like.

This demo gradle script assembles plain, uncustomized CoreMedia Content 
Management  Server Tools in a stripped down variant of how the original Maven 
based workspace layout from CoreMedia does it.

It is meant as a hint that a migration from the Apache Maven build system (not 
its dependency management and repositories) would be an advantage for 
readability and maintence of CoreMedia workspaces.

This repository in itself is feedback about the topic, but feel free to send
any comment e.g. via the [issues][issues] section at GitHub.

Find mirrors of this git repository at [gitlab][gitlab] and [github][github].


## Prerequisites

- Access to the CoreMedia Maven artifact repositories

- A CoreMedia Content Management Server running somewhere accessible

- Database parameters of that server to be able to use all tools


## Usage

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

One defect for now is, that the needed libraries still show up in the wrong place.

```
unzip distributions/cm-cms-tools...zip
rmdir lib
mv cm*/lib .
```


[issues]: https://github.com/mgoellnitz/cm-cms-tools/issues
[github]: https://github.com/mgoellnitz/cm-cms-tools
[gitlab]: https://gitlab.com/mgoellnitz/cm-cms-tools
