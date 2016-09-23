# User Guide

* [Quick Start](#quick-start)
* [Features](#features)
* [Data Formats](#data-formats)
* [Command Summary](#command-summary)

## Quick Start

1. _Download/Installation instructions_
2. Double-click the file to start the app. The GUI should open in a few seconds.
3. To communicate with your task manager, type a command in the command box and press <kbd>Enter</kbd>.
4. Some commands to get you started:
  * **`#help`** : Brings up the help page.
  * **`#add`**` Dinner with Mum` : Adds a task `Dinner with Mum` to your list.
  * **`#list`** : Lists all tasks.
  * **`#delete`**` 3` : Deletes the 3rd contact as visible in the current list.

  Don't forget the `#` before the commands!

## Features

#### Notation used:
`[date]`: Means date is an optional argument<br>
`<hour>`: Replace by the actual hour

#### Viewing help: `#help`
Format: `#help`

> Help is also shown if you enter an incorrect command, like `asdf`

#### Viewing help for a specific command: `#help`
Format: `#help <#command>`

Examples:
  * `#help #add`
  * `#help #list`

#### Adding a task to the list: `#add`
Format: `#add <task description> [<extensions>]`

> Task Description outlines the task to be added.<br> Extensions allow specifying more details about the task, such as deadlines and venues. <br>
Without any extensions, this will be added as a floating task. <br>
The details can be changed at any time using the `#edit` command.

Examples:
  * `#add Dinner with Mum`

###### Extensions to the `#add` command:
  * `#at`<br>
    Adds events at a specific time <br>
    Format: `#at <time> [<date>]`
    > Time indicates when the event begins. [See format here](#data-formats)<br>
    Date indicates the date on which the event is. Defaults to the current day if not specified. [See format here](#data-formats)

    Examples:
    * `#add Dinner with Mum #at 7:15pm`
    * `#add Dinner with Mum #at 7pm 5 Oct`
    * `#add Dinner with Mum #at 7:15pm 15 Jan 2017`
  <br><br>

  * `#by`<br>
    Sets deadlines for tasks <br>
    Format: `#by <time> [<date>]`
    > Time indicates by when the task needs to be finished. [See format here](#data-formats)<br>
    Date indicates the date by which the task needs to be finished. Defaults to the current day if not specified. [See format here](#data-formats)

    Examples:
      * `#add Finish 2103T Tutorial #by 11:59pm`
      * `#add Finish 2103T Tutorial #by 11:59pm 5th Oct`
      * `#add Finish 2103T Tutorial #by 11:59pm 5th Oct 2016`
  <br><br>

  * `#after`<br>
    Indicates that the task should be done _after_ a certain time<br>
    Format: `#after <time> [<date>]`
    > Time indicates the time after which the task should be done. [See format here](#data-formats)<br>
    Date indicates the date after which the task should be done. Defaults to the current day if not specified. [See format here](#data-formats)

    Examples:
      * `#add Pay bills #after 11:50pm`
      * `#add Pay bills #after 11:50pm 30 Dec`
      * `#add Pay bills #after 11:50pm 30 Dec 2030`
  <br><br>

  * `#venue`<br>
    Indicates the place where the task/event will happen<br>
    Format: `#venue <description of venue>`
    > The venue description is just stored as plain text

    Examples:
      * `#add Prof's birthday party #venue i3-Aud`
      * `#add Date with destiny #venue Beneath the majestic skies`
      * `#add Lunch with Arthur #venue Avalon`

## Data Formats

  * `time`: `<hour>[:<minutes>]<am/pm>`
  * `date`: `<day> <month> [<year>]`

## Command Summary

Type | Command | Format
:--------: | :--------: | ----- |
Basic | Help | `#help`
Basic | Add | `#add <task description> [<extensions>]`
Basic | List | `#list`
Basic | Delete | `#delete 1`
Extension | At | `#at <time> [<date>]`
Extension | Venue | `#venue Pizza Hut`
Extension | By | `#by 11:59pm 20 Nov`
Extension | After | `#after 20 Nov`
Data | Time | `<hour>[:<minutes>]<am/pm>`
Data | Data | `<day> <month> [<year>]`
