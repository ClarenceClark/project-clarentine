# The Clarentine Calendar

Current revision: 0.4.0

This is the formal specification for the Clarentine calendar. This document is a _work is progress_; it will change as feedback is incorporated.

All pronunciations shall follow the rules of Clarentine English Pronunciation (the specification of which will be published later; it's still a work in progress).

## Section 1: Names and Definitions

1. The fundamental unit of time in the Clarentine Calendar is the _day_. The time of day is defined and notated the same way as in UTC.
2. This calendar uses the "J2000" epoch. The date 0.1.1 11:58:55.816 (see section 3 for interpretation of this date) is defined as J2000, or 1 January 2000 11:58:55.816 UTC, or 1 January 2000 11:59:27.816 TAI.
3. All days, cycles, and seasons shall be named numerically, with the number corresponding to their position. For example:
	- Day 1 -\> 1st day of the cycle
	- Day 11 -\> 11th day of the cycle
	- cycle 5 -\> 5th cycle of the season

## Section 2: Time Divisions

1. Time periods are divided into __divisions__. 
2. Divisions are as follows:
		| Name | Plural | Composed of |
		|:--|:--|:--|
		| Day | Days | 1 UTC day |
		| Cycle | Cycles | 12 days |
		| Season | Seasons | 12 cycles |
3. Examples:
	- 42 days = 3 cycles, 6 days
	- 1000 days = 6 seasons, 11 cycles, 4 days

## Section 3: Absolute Dates

1. Dates consist of three groups of numbers ("number groups") separated by a separator, which can be any of the following (only one option for now; more _may_ be added): 
	- Full stop: `.`
2. The numbers follow the standard rules of numerical notation.
3. From left-to-right, the first group of numbers represent the season, the second the cycle, and the third the day. 
4. A number group cannot be omitted unless a more significant number group has also been omitted.
5. A separator can be omitted if the number group to the left has been omitted as well.
6. If less than three number groups are present in the date, the present groups of numbers are assumed to represent the least significant divisions, and omitted numbers are understood to represent the current time for the group's associated division.
7. Examples:
	- `4.2` : Current season, cycle 4, day 2
	- `3.5.6` : Season 3, cycle 5, day 6
	- `1234.07.08` : Season 1234, cycle 7, day 8
	- `9.10.11` : Season 9, cycle 10, day 11
	- `5` : Current season, current cycle, day 5
	- `0.12.12`: Season 0, cycle 12, day 12
	- `0.0.0`: Invalid date; cycle and day cannot be below 0

## Section 4: Relative Dates

1. The rules for notation for relative dates are the same as absolute dates, as laid out in section 3, unless otherwise noted here.
2. In order to notate a date as relative, the postfix `-r` or `-R`must be added to the date.
3. The groups of numbers still correspond to the same divisions, but are denoting the _relative_ time from that of writing.
4. Positive dates denote the future relative to the current time; negative dates denote the past
5. If a sign is omitted, it is assumed to be in the future
6. Omitted numbers are assumed to be 0, or the current division of time as represented by that number group.
9. Examples:
	- `-1.1.1-r`: 1 season, 1 cycles, and 1 day in the past
	- `+4.6.12-r`: 4 seasons, 6 cycles, and 12 days in the future
	- `+3.2-r`: 0 seasons, 3 cycles, and 2 days in the future
	- `4.1-r`: 0 seasons, 4 cycles, and 1 day in the future