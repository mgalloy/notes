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

The note look like:

``` Markdown
# Team meeting

```

Or, to add to an existing note:

``` shell
$ notes append --title time --stamp --last "SEP project 4 hrs"
appending to note 2023.10.02.time.md...
```

The note looks like:

``` Markdown

# Time

Fri 12:37 SEP project 4 hrs
```

## The `.notesrc` file

The `~/.notesrc` file specifies the preferences for the `notes` app. It must
contain the location of the notes repository.

``` INI
[repo]
location               : /Users/mgalloy/projects/notes
protocol               : git

[notes]
editor                 : nova
datetime_stamp_format  : %a %H:%M
```
