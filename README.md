![Vector art of 200 in hex, subtitle of course: Bare Metal in pale green and printer's black](https://raw.githubusercontent.com/allegheny-college-cmpsc-200-fall-2024/course-materials/media/images/CMPSC%20-%200xC8%20Banner.png)

# Making Logic Gates From Transistors

| Date              |           |
|:------------------|:----------|
| 30 August 2025   | Assigned  |
| 8 September 2025  | Due       |
| Fundamental            | [![Assignment Progress](../../actions/workflows/main.yml/badge.svg?branch=main)](../../actions/workflows/main.yml) |
| Hack                   | [![Assignment Progress](../../actions/workflows/hack.yml/badge.svg?branch=hack)](../../actions/workflows/hack.yml) |

## Introduction

This first assignment sees us applying some basic principles of electronics in order to create digital logic from the basic
building block of a digital circuit: the transistor. For this assignment, you're given:

* 1 LED diode
* 2 NPN transistors
* 3 resistors (2 @ 2.2K, 1 @ 220)
* 1 2-switch DIP switch
* An 830-point breadboard
* Power supply unit (PSU)
* 6V power supply
* Many, many wires

These materials can create a surprising number of digital logic outcomes. In specific, we're going to look at:

* `AND`
* `OR`
* `INVERTER` (aka `NOT`)

We'll learn how to combine these in future weeks to create even more discering logic, but for now we'll start with some basics.

During this activity, we'll also use a tool called `TinkerCAD` to mock up circuits _before_ we build them in order to make sure that
we're planning out circuits to avoid overloading parts. To join the classroom for `TinkerCAD` (if you haven't already done so):

* [Join TinkerCAD class](https://www.tinkercad.com/joinclass/YCRGKSAJQ)

## Instructions

You must complete and demonstrate each of these circuits to either an instructor or TL using your breadboard and associated parts. This 
can be done any time during the duration of the assignment until the due date. You do not need to complete them all at once; this acitivty
can be finished _iteratively_ (that is circuit by circuit over a span of days).

In addition, you must record your findings in the `report.md` file in the `docs/` directory. This documentation will require you to fill
in some truth tables, provide some breadboard layouts, and explain how each of the circuits work, ostensibly. The report also contains
a table for the instructor or TL to fill out when circuits are demonstrated. Again, this table _must be filled out by the instructor
or a course TL_. (This means that you'll have to have `commit`s authored by one of these folks!)

### `NOT`

<img width="1103" height="768" alt="NPN Transistor - NOT Gate-schematic" src="https://github.com/user-attachments/assets/146bb87c-ea84-4896-9021-592ca9f4d476" />

The following truth table describes the `NOT` gate, a digital logic circuit that "flips" the inputs:

| A | Out |
|:--|:----|
| 0 | 1   |
| 1 | 0   |

### `AND`

<img width="1102" height="1023" alt="NPN Transistor - AND Gate-schematic" src="https://github.com/user-attachments/assets/07bc01ee-2071-44c1-a700-1cb445847075" />

The following truth table describes the `AND` gate, a digital logic circuit that only reports when both
inputs are `TRUE` or `ON`:

| A | B | Out |
|:--|:--|:----|
| 0 | 0 | 0   |
| 0 | 1 | 0   |
| 1 | 0 | 0   |
| 1 | 1 | 1   |

### `OR`

<img width="1312" height="1044" alt="NPN Transistor - OR Gate-schematic" src="https://github.com/user-attachments/assets/5ec91361-7f51-498c-8765-844fadc4be8a" />

The following truth table describes the `OR` gate, a digital logic circuit that only reports when one or
both inputs are `TRUE` or `ON`:

| A | B | Out |
|:--|:--|:----|
| 0 | 0 | 0   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 1   |


## Assignment "Hack"

Let's take it a bit further. We've already looked at `NOT`, but did you know that there are two more circuits that deal in negatives: the
`NAND` and the `NOR`? Below, you'll find the truth tables that represent the desired outcome of each of these circuits which you'll need
to replicate in order to solve this `Hack`.

Like the `Fundamental` assignment, you'll need to complete the `report.md` file in the `docs/` folder on the `hack` branch (it's a separate
file!). Also, similar to the `Fundamental` branch, you'll need to complete schematics of the circuits in `TinkerCAD` and provide them in the
`report.md` file.

### `NAND`

Short for `NOT AND`, the `NAND` behaves a bit peculiarly:

| A | B | Out |
|:--|:--|:----|
| 0 | 0 | 1   |
| 0 | 1 | 1   |
| 1 | 0 | 1   |
| 1 | 1 | 1   |

### `NOR`

We're interested in _everything but `OR`_ in this case, which means:

| A | B | Out |
|:--|:--|:----|
| 0 | 0 | 1   |
| 0 | 1 | 0   |
| 1 | 0 | 0   |
| 1 | 1 | 0   |
