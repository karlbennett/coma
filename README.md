coma
====

### Command Line Music Aggregator

coma is a simple command line tool that provides a way to easily play music that resides across multiple sources.
Be that local music files, songs within a streaming service, or songs located in some form of cloud storage.

#### Playing Music

To run coma simply use the `play` command to start playing music from a recognised source.
So for example to the following command would play songs from local storage.

    #> play music.local

When using a source for the first time coma will prompt for some initial sources specific setup.
For the `music.local` source this is the directory where coma should search for music files.

    #> play music.local
    Please enter a music directory: ~/Music
    Would you like to add another directory? (Y/n):

Remote sources may prompt for a user name and password so that coma can access an account.
coma will not store credentials unless absolutely necessary, it will try and only store authorisation tokens whenever possible.

To play music from more than one source just add the extra sources to the list.

    #> play music.local music.dropbox music.grooveshark

To get a list of supported sources use the `sources` command.

    #> play sources
    music.local
    music.dropbox
    music.grooveshark
    music.bitorrent
    ...
   
#### Interaction

When coma starts it will run in the background as a service so that it can be controlled from any command prompt with the use of the `play` command.
The following commands can be sent.

    #> play pause
    #> play
    #> play previous
    #> play next
    #> play stop

All the commands are pretty self explanatory, except for `play stop` which will actually stop the coma service.
