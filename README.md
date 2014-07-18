dumbo
=====

CLI Tool for merging Puppet files within enviroments

### What is this crap??

When using puppet to deploy servers and applications within different environments, normally each environment has a different SOURCE puppet file which contains the specific configuration for the services.

Some times when a new version needs to be deployed (dev-> release, release->prod...) of a source file, the puppet file of the next environment needs to be updated with NEW puppet properties which not were there before. If your puppet file is small you can do this manually, but if its big dumbo comes to the help!


### To install

```
$ npm install
$ sudo ln -s /path/to/dumboexec /usr/bin/dumbo
```

### Usage

on the unix terminal

```
$ luis@boxita$ dumbo
ERROR not enough arguments
usage: dumbo <LESSERENV> <GREATERENV>
usage: dumbo --all --dryrun <LESSERENV> <GREATERENV>
```

--all will show ALL lines of the source, not only the changes

--dryrun will not generate a new file, will only show the outout in the terminal

when not using --dryrun, dumbo will generate a new file called as GREATERENV.new

remember to check the source code and hack it to suit your needs!
