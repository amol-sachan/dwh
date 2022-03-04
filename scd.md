# Slowly Changing Dimentions

Slowly Changing Dimensions(SCD) - dimensions that change over time, rather than changing on regular schedule, time-base. SCD is a dimension that stores and manages both current and historical data over time in a data warehouse.

- **Type 0** - The passive method
- **Type 1** - Overwriting the old value
- **Type 2** - Creating a new additional record
- **Type 3** - Adding a new column
- **Type 4** - Using historical table
- **Type 6** - Combine approaches of types 1,2,3 (1+2+3=6)
