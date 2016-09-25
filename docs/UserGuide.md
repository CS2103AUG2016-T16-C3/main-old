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

### Notation used:
`[date]`: Means date is an optional argument<br>
`<hour>`: Replace by the actual hour

### Primary Commands

<a id="help"></a>
#### Viewing help: `#help`
Format: `#help`

> Help is also shown if you enter an incorrect command, like `asdf`

#### Viewing help for a specific command: `#help`
Format: `#help <#command>`

Examples:
  * `#help #add`
  * `#help #list`

<a id="add"></a>
#### Adding a task to the list: `#add`
Format: `#add #desc <task description> [<extensions>]`

> Task description outlines the task to be added.<br> Extensions allow specifying more details about the task, such as deadlines and venues. <br>
Without any extensions, this will be added as a floating task. <br>
The details can be changed at any time using the `#edit` command.

Examples:
  * `#add Dinner with Mum`
<!-- TODO: add other examples -->

#### Listing tasks: `#list`
Format: `#list [<extensions>]`

> Without any extensions, this will simple list all tasks<br>
Extensions allow listing according to what you wish to see<br>

Examples:
  * `#list`
<!-- TODO: add other examples -->

### Extensions:

<a id="desc"></a>
#### Task Description: `#desc`
Format: `#desc <task description>`

>Task description is simply plaintext about your task

Examples:
* `#add #desc Dinner with Mum`
<!-- TODO: add other examples -->

<a id="at"></a>
#### At a certain time: `#at`
Format: `#at <time> [<date>]`

> Time indicates when the event begins. See format [here](#data-formats)<br>
Date indicates the date on which the event is. Defaults to the current day if not specified. See format [here](#data-formats)

Examples:
* `#add Dinner with Mum #at 7:15pm`
<!-- TODO: add other examples -->

<a id="before"></a>
#### Before a certain time: `#before`
Format: `#before <time> [<date>]`

> Time indicates what is the last time by which this task should be done. See format [here](#data-formats)<br>
Date indicates the last date by which this task should be done. Defaults to the current day if not specified. See format [here](#data-formats)

Examples:
  * `#add Finish 2103T Tutorial #before 11:59pm`
<!-- TODO: add other examples -->

<a id="after"></a>
#### After a certain time: `#after`
Format: `#after <time> [<date>]`
> Time indicates the time after which the task should be done. See format [here](#data-formats)<br>
Date indicates the date after which the task should be done. Defaults to the current day if not specified. See format [here](#data-formats)

Examples:
  * `#add Pay bills #after 11:50pm 30 Dec 2030`
<!-- TODO: add other examples -->

<a id="venue"></a>
#### At a Venue: `#venue`
Format: `#venue <description of venue>`
> The venue description is just stored as plain text

Examples:
  * `#add Lunch with Arthur #venue Avalon`
<!-- TODO: add other examples -->

## Data Formats

  <a id="time"></a>
  * `time`: `<hour>[:<minutes>]<am/pm>`<br>
    Examples:
    * `7pm`
    * `3:45am`
    * `1:00pm`
  <a id="day"></a>
  * `day`: `<Integer>`<br>
    Examples:
    * `1`
    * `31`
  <a id="month"></a>
  * `month`: `<3-letter abbreviation>`<br>
    Examples:
    * `Jan`
    * `Mar`
    * `Sep`
  <a id="year"></a>
  * `year`: `4-digit integer`<br>
    Examples:
    * `2016`
    * `2020`
  <a id="date"></a>
  * `date`: `<day> <month> [<year>]`<br>
    Examples:
    * `5 Oct`
    * `5 Nov`

## Command Summary

Type | Command | Format
:--------: | :--------: | ----- |
Basic | [Help](#help) | `#help`
Basic | [Add](#add) | `#add <task description> [<extensions>]`
Basic | [List](#) | `#list`
Basic | [Delete](#) | `#delete 1`
Extension | [At](#at) | `#at <time> [<date>]`
Extension | [Before](#by) | `#by <time> [<date>]`
Extension | [After](#after) | `#after <time> [<date>]`
Extension | [Venue](#venue) | `#venue <description of venue>`
Data | [Time](#time) | `<hour>[:<minutes>]<am/pm>`
Data | [Day](#day) | `<Integer>`
Data | [Month](#month) | `<3-letter abbreviation>`
Data | [Year](#year) | `<4-digit integer>`
Data | [Date](#date) | `<day> <month> [<year>]`
