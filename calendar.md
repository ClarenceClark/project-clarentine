# The Clarentine Calendar

Current version: 0.2.0

This is the formal specification for the Clarentine calendar. This document is a _work is progress_; it will change as feedback is incorporated.

All pronunciations shall follow the rules of Clarentine English Pronunciation (the specification of which will be published later; it's still a work in progress).

### Section 1: Names and Definitions

1. The fundamental unit of time in the Clarentine Calendar is the _day_. The time of day is defined and notated the same way as in UTC.
2. This calendar uses the "J2000" epoch. The date 0.0.0 11:58:55.816 (see section 2 for interpretation of this date) is defined as J2000, or 1 January 2000 11:58:55.816 UTC, or 1 January 2000 11:59:27.816 TAI.
3. There are two _types_ of time periods: a __division__, and a __subdivision__. Divisions are converted to each other at a 1:12 ratio.
    1. Divisions
      | Name  | Plural | Postfix form | Composed of |
      | ----- | ------ | ------------ | ----------- |
      | Day   | Days   | dies         | UTC day     |
      | Month | Months | menses       | 12 days     |
      | Year  | Years  | anni         | 12 months   |
    2. Sub-divisions
      | Prefix | Number of divisions |
      | ------ | ------------------- |
      | tri-   | 3                   |
      | quad-  | 4                   |
      | hex-   | 6                   |
    3. Examples
        - 3 days = 1 tridie
        - 4 days = 1 quadie
        - 12 days = 1 month
        - 3 months = 1 trimenses
        - 4 years = 1 quadanni
4. All days, months, and years shall be named numerically, with the number corresponding to their position. For example:
    - Day 1 -> first day of the month
    - Day 11 -> eleventh day of the month
    - Month 5 -> fifth month of the year

### Section 2: Notation

1. Dates consist of three groups numbers separated by a separator, which can be any of the following: 
    - Full stop: `.`
    - Hyphen: `-`
2. The numbers follow the standard rules of numerical notation.
3. From left-to-right, the first group of numbers represent the current year, the second the current month, and the third the current day. 
4. If less than three groups of numbers are present in the date, the present groups of numbers represent the least significant divisions, and omitted numbers are understood to represent the current time for the group's associated division.
5. Examples:
    - `4.2` : Current year, month 4, day 2
    - `3.5.6` : Year 3, month 5, day 6
    - `1234.07.08` : Year 1234, month 7, day 8
    - `9.10.11` : Year 9, month 10, day 11
    - `5` : Current year, current month, day 5