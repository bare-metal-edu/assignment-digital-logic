![Vector art of 200 in hex, subtitle of course: Bare Metal in pale green and printer's black](https://raw.githubusercontent.com/allegheny-college-cmpsc-200-fall-2024/course-materials/media/images/CMPSC%20-%200xC8%20Banner.png)

# Making Logic Gates From Transistors

| Date              |           |
|:------------------|:----------|
| 5 August 2025   | Assigned  |
| 11 September 2025  | Due       |
| Fundamental            | [![Assignment Progress](../../actions/workflows/main.yml/badge.svg?branch=main)](../../actions/workflows/main.yml) |
| Hack                   | [![Assignment Progress](../../actions/workflows/hack.yml/badge.svg?branch=hack)](../../actions/workflows/hack.yml) |

## Introduction

This week, we take a step further into digital logic by upgrading from manually-built gates to pre-assembled, multi-channel gates
that ostensibly make our job easier. But, as with everything in this course, with convenience comes greater range of expression.
(read: harder logic).

Based on our explorations last time, you have the following digital building blocks available with accompanying datasheets:

* `AND`
* `OR`
* `INVERTER` (aka `NOT`)
* `4`-switch `DIP` switch

You'll use these gates to implement a circuit known as the `Majority Circuit`, which follows this truth table:

|A|B|C|D|Out|
|-|-|-|-|---|
|0|0|0|0|0  |
|0|0|0|1|0  |
|0|0|1|0|0  |
|0|0|1|1|0  |
|0|1|0|0|0  |
|0|1|0|1|0  |
|0|1|1|0|0  |
|0|1|1|1|1  |
|1|0|0|0|0  |
|1|0|0|1|0  |
|1|0|1|0|0  |
|1|0|1|1|1  |
|1|1|0|0|0  |
|1|1|0|1|1  |
|1|1|1|0|1  |
|1|1|1|1|1  |

Hopefully, scanning this truth table, you'll see why it's called the `Majority Circuit`! One more note: you have access to as many
transistors as you want. That _may_ make some part of this a bit easier. To that end, a note of caution: wiring on this one is going
to be..._interesting_.

During this activity, we'll also use a tool called `TinkerCAD` to mock up circuits _before_ we build them in order to make sure that
we're planning out circuits to avoid overloading parts. To join the classroom for `TinkerCAD` (if you haven't already done so):

* [Join TinkerCAD class](https://www.tinkercad.com/joinclass/YCRGKSAJQ)

## Instructions

You must complete and demonstrate this circuit to  an instructor or TL using your breadboard and associated parts. This 
can be done any time during the duration of the assignment until the due date. You do not need to complete them all at once; this acitivty
can be finished _iteratively_ (that is circuit by circuit over a span of days).

In addition, you must record your findings in the `report.md` file in the `docs/` directory. This documentation will require you to fill
in some truth tables, provide some breadboard layouts, and explain how each of the circuits work, ostensibly. The report also contains
a table for the instructor or TL to fill out when circuits are demonstrated. Again, this table _must be filled out by the instructor
or a course TL_. (This means that you'll have to have `commit`s authored by one of these folks!)

## Assignment "Hack"

Just for fun (or at least what you instructor calls "fun"), your challenge is to implement a different kind of circuit: the `Equality Comparator`.
The the following truth table models this circuit:

|A|B|C|D|Out|
|-|-|-|-|---|
|0|0|0|0|1  |
|0|0|0|1|0  |
|0|0|1|0|0  |
|0|0|1|1|0  |
|0|1|0|0|0  |
|0|1|0|1|1  |
|0|1|1|0|0  |
|0|1|1|1|1  |
|1|0|0|0|0  |
|1|0|0|1|0  |
|1|0|1|0|1  |
|1|0|1|1|1  |
|1|1|0|0|0  |
|1|1|0|1|0  |
|1|1|1|0|0  |
|1|1|1|1|1  |

You'll complete this circuit using the same gates and unlimited access to transistors. However, the easiest way to do this (once you notice the
pattern of the circuit) is to use `2` `2`-switch `DIP` switches. However, this _can_ be done with a single `4`-switch `DIP` switch if you
_treat it like `2` separate switches_.

Also like the `Fundamental` assignment, you'll need to complete the `report.md` file in the `docs/` folder on the `hack` branch (it's a separate
file!). Also, similar to the `Fundamental` branch, you'll need to complete schematics of the circuits in `TinkerCAD` and provide them in the
`report.md` file.



### Truth table
