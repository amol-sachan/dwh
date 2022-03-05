## Slowly Changing Dimensions

Slowly Changing Dimensions(SCD) - dimensions that change over time, rather than changing on regular schedule, time-base. SCD is a dimension that stores and manages both current and historical data over time in a data warehouse.

- **Type 0** - The passive method
- **Type 1** - Overwriting the old value
- **Type 2** - Creating a new additional record
- **Type 3** - Adding a new column
- **Type 4** - Using historical table
- **TYpe 5**
- **Type 6** - Combine approaches of types 1,2,3 (1+2+3=6)
- **Type 7** - Hybrid

### Concept to know before proceeding furthur
- [Surrogate Key](https://www.geeksforgeeks.org/surrogate-key-in-dbms/)
- [Natural Key](https://en.wikipedia.org/wiki/Natural_key)


### Type 0 (_retain original_)

Type 0 dimension attributes never change, and if there are any changes those are ignored. For example in a employee table joining date of employees is type 0 attribute.

### Type 1 (_overwrite_)

It updated old value with new value, and does not track historical data.

### Type 2 (_add new row_)

Tracks historical data by creating new record for given natural key with separate surrogate key and/or version number.

### Type 3 (_add new attribute_)

This method tracks changes using separate columns and preserves limited history(limited to columns designated for historical data).

### Type 4 (_add history table_)

In this method, one table keeps the current data and additional table i.e. history table is maintained to keep track of changes.

### Type 6 (_combined approach_)

It combines the approaches of type 1, 2 and 3.

### Type 7 (_Hybrid-both surrogate and natural key_)

Place both surrogate and natural key into the fact table.

---------------------------

### For more details and examples

- https://en.wikipedia.org/wiki/Slowly_changing_dimension
- https://www.sqlshack.com/implementing-slowly-changing-dimensions-scds-in-data-warehouses/



