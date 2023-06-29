# Enums
- an enum - enumeration type - is a value type defined by a set of named constants of the underlying integral numeric type.
- example: a list of Seasons can be held inside an enum Season
- enums are VALUE TYPES
    - they contain a direct instance of the type, while a reference type would contain a reference to the type instead.
- enums are useful because you can assign constant values for readability rather than a value. For instance, an enum WeekDays with property Monday ```Weekdays.Monday``` is easier to read than the number 0 when referring to a day in the week.
```c#
enum Season
{ 
    Spring,
    Summer,
    Autumn,
    Winter
}
```
- each value in an enum is associated with an int, starting with 0
    - you can explicitly assign these values if you wanted to - for example, assigning error codes to a list of potential errors
- enums are great for readability because they provide symbolic named constants, so you only remember names, not values :)
