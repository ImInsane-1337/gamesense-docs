# string.format

Returns a formatted version of its variable number of arguments following the description given in its first argument (which must be a string).
=== Format string options

Available numeric format specifiers:

- **%d** - Decimal integer, rounded down.
- **%o** - Octal integer, rounded down.
- **%x** - Hexadecimal integer, rounded down. Use `%X` for uppercase.
- **%f** - Floating-point number, rounded based on the specified precision.
- **%e** - Scientific notation (mantissa/exponent). Use `%E` for uppercase.
- **%g** - Shortest float representation, either `%f` or `%e`. Use `%G` for uppercase.
- **%a** - Hexadecimal float. Use `%A` for uppercase.

Numeric specifiers can be combined with one or more of the following sub-specifiers:

- Padding: Use `%5d` to pad a number to at least 5 characters. By default, it will be padded with spaces, use `%05d` to use zeroes instead. Use `%-5d` to left-justify instead of right-justify the output.
- Sign: Use `%+d` to preceed positive numbers with a plus sign or `% d` to preceed them with a space.
- `#`: When used with `%o`, `%x` or `%X` it prefixes the output with 0, 0x or 0X respectively for values different than zero. Used with e, E, f, F, g or G it forces the written output to contain a decimal point even if no more digits follow.
- Precision: Number of digits to be printed after the decimal point, for example `%011.5f` to print 5 digits after the decimal point and pad the output to at least 11 characters (including the decimal point)

Other format specifiers:

- **%c** - Single character as ascii code.
- **%s** - String
- **%q** - String between double quotes, with all special characters escaped
- **%%** - A single `%` character.

String specifiers can also be combined with the width and right-justify sub-specifiers. Use `%16s` to make sure the output string is at least 16 characters long.

===

```typescript
string.format(format: string, ...)
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| format | Format string. | string |
| undefined | Arguments to insert into the format string. | unknown |
