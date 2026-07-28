In Python, [[Python string|strings]], [[Python bytes|bytes]] and [[Python bytearray|bytearrays]] have a `%` operator for string formatting. You can use it to insert and format values at runtime, if the string contains a **conversion specifier**.

A **conversion specifier** looks like this:
1. **Start of the specifier**: `%` to signify a specifier. `%%` to skip.
2. **Mapping key**: Optional name for the mapping.
3. **Conversion flags**: Optional list of flags. 
4. **Min field width**: Optional int or `*`.
5. **Precision**: Optional. Dot, followed by precision `.2`. An `*` means read from next element.
6. **Length modifier**: Optional. `h`, `l` or `L`, but it's ignored by python.
7. **Conversion type**: How to display the variable.

```python
# Mapping key
'%s'       % 'String'
'%s %s'    % ('String1', 'String2')
'%(name)s' % {'name': 'String')

# Conversion flag
'%#4x' % 12 # '0xc'  Alternate form (0x at the start)
'%04x' % 12 # '000c' Pad with 0 when width is defined
'%-4x' % 12 # 'c   ' Left-adjusted when width is defined
'% x'  % 12 # ' c'  Add leading space for positive numbers  
'%+x'  % 12 # '+c'  Add leading sign for positive numbers

'%#0+6x' % 12 # '+0x00c' Alternate form, leading sign, pad with 0

# Minimum field width
'%4d' % 2      # '   2' Set width
'%*d' % (4, 2) # '   2' Read width from arguments

# Precision
'%.4f' % 2      # '2.0000' Set precision
'%.*f' % (4, 2) # '2.0000' Read precision from arguments

# Conversion type for strings
'%d, %i'     % 12 # '12, 12' Decimal
'%o'         % 12 # '14'     Octal       (Alternate form '0o14')
'%x, %X'     % 12 # 'c, C'   Hexadecimal (Alternate form '0xc, 0XC')

'%.2e, %.2E' % 12 # '1.20e+01, 1.20E+01' Scientific notation
'%.2f, %.2F' % 12 # '12.00, 12.00'       Fixed-point notation
'%g, %G'     % 12 # '12, 12'             General format (e or f)

'%c'         % 97 # 'a', Character

'%r, %s, %a' % 12 # '12, 12, 12' Use repr(), str(), ascii() 

# Conversion type for bytes
'%r, %s, %a' % 12 # '12, 12, 12' Use repr(), str(), ascii() 
'%b, %s'     % 12 # Uses __bytes__().
'%a, %r'     % 12 # Uses repr(obj).encode('ascii', 'backslashreplace').
```


