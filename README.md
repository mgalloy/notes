# notes command-line interface

## Basic syntax

notes provides a simple command-line interface to a directory of note text
files stored in git.

To create a new note:

``` shell
$ notes new
creating new note 2023.10.10.DAILY.md...
```

This will create a new "daily" note containing the following:

``` Markdown
# Daily notes for 2023-10-10

```

To create a new note with a name, and then open it in the default text editor:

``` shell
$ notes new --open "Team meeting"
creating new note 2023.10.10.Team-meeting.md...
opening 2023.10.10.Team-meeting.md...
```

```
# Team meeting

```

## The `.notesrc` file

The `~/.notesrc` file must contain the location of the notes repository.

``` INI
[repo]
location     : /Users/mgalloy/projects/notes

[notes]
editor       : nova
```
