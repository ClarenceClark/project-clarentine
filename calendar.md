# The Clarentine Calendar

Current version: 0.1.0

This is the formal specification for the Clarentine calendar. This document is a _work is progress_; it will change as feedback is incorporated.

All pronunciations shall follow the rules of Standard Clarentine English Pronunciation (will be published later; it's still a work in progress).

__NOTE: all numbers are written in base 10d/12e, or base-twelve.__

### Day

The fundamental unit of time in the Clarentine Calendar is the _day_. The time of day is defined and notated the same way as in UTC.

### Divisions of Time

There are two _types_ of time periods: a __division__, and a __subdivision__. Divisions are converted to each other at a 1:10 ratio.

#### Divisions

| Name  | Plural | Postfix form | Composed of |
| ----- | ------ | ------------ | ----------- |
| Day   | Days   | dies         | UTC day     |
| Month | Months | menses       | 10 days     |
| Year  | Years  | anni         | 10 months   |

#### Subdivisions

| Prefix | Number of divisions |
| ------ | ------------------- |
| tri-   | 3                   |
| quad-  | 4                   |
| hex-   | 6                   |

#### Examples

**Days**

1. 3 days = 1 tridie
2. 4 days = 1 quadie
3. 6 days = 1 hexdie
4. 10 days = 1 month

**Month**

1. 3 months = 1 trimenses
2. 4 months = 1 quadmenses
3. 6 months = 1 hexmenses
4. 10 months = 1 year

### Epoch

This calendar uses the "J2000" epoch. The date 0y-00 11:58:55.816 is defined as J2000, or 1 January 2000 11:58:55.816 UTC, or 1 January 2000 11:59:27.816 TAI (UTC and TAI times in decimal).

### Notation

Date format:

"y\*-md", where "y\*" is the year to as many digits as needed, "m" the month, and "d" the day.

All numbers are filled into the template from right-to-left, from the least significant to the most significant. All missing numbers are assumed to be the current division of time. The hyphen between the year and the month/day can be left out. 

If the year is followed by a "y", the year shall be interpreted _absolutely_ with the normal rules of interpreting a number, instead of assuming that they represent the current division of time.

For example:

1. 42 : Current year, month 4, day 2
2. 3-56 : Current 10-year, year 3, month 5, day 6
3. 1234-78 : Current 10000-year, year 1234, month 7, day 8
4. 9ab : Current 10-year (and all above), year 9, month A, day B
5. 3y-45 : Year 3, month 4, day 5


### Names

All days, months, and years shall be named numerically, with the number corresponding to their position. For example:

1. Day 1 -> first day of the month
2. Day A -> eleventh day of the month
3. Month 5 -> fifth month of the year