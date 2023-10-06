---
tags: fc, plang
course: 26111 Programming Languages
---
defines a collection of data values and a set of predefined operations on those values ;; data type

is the collection of the attributes of a variable ;; descriptor

data types that are not defined in terms of other types ;; primitive data types

data types that could no longer be decomposed ;; primitive data types

basically how they taught you how to add in binary ;; twos complement

ways of expressing the negative integers in binary
,,
- signed magnitude
- ones complement
- twos complement

data types model real numbers ;; floating-point

the accuracy of the fractional part of a value, measured as the number of bits ;; precision

a combination of the range of fractions, and more important, the range of exponents ;; range

values that are represented as ordered pairs of floating point values ;; complex data type

store a fixed number of decimal digits, with the implied decimal point at a fixed position in the value ;; decimal

decimal types are stored very much like character strings, using binary codes for the decimal digits. ;; binary coded decimal(BCD)

often represents switches ;; boolean

one in which the values consist of sequences of characters ;; character string type

a reference to a substring of a given string ;; substring reference

are what substring references are called ;; slices

pattern-matching expressions that are some what loosely based on mathematical regular expressions ;; regular expressions

static and set when the string is created ;; static length string

strings that have varying length up to a declared and fixed maximum set, based on variables definition ;; limited dynamic length strings

strings that have a varying length with no maximum length ;; dynamic length strings

one in which all of the possible values, which are named constants, are provided, or enumerated, in the definition ;; enumeration type

collections of named constants that are defined and group collections ;; enumeration constants

a member in an enumeration type ;; enumeration constant

a homogeneous aggregate of data elements in which an individual elements is identified by its position in the aggregate, relative to the first element ;; array

specific elements of an array that are referenced by means of a two-level syntactic mechanism ;; subscripts or indeces

arrays are sometimes called ==finite mappings==

one in which the subscript ranges are statically bound and storage allocation is static(done before runtime) ;; static array

one in which the subscript ranges are statically bound, but the allocation is done at declaration elaboration time during execution ;; fixed stack-dynamic array

similar to a fixed stack-dynamic array, in that the subscript ranges and the storage bindings are both fixed after storage is allocated ;; fixed heap-dynamic array

one in which the binding of the subscript ranges and storage allocation is dynamic and can change any number of times during the array's lifetime ;; heap-dynamic array

a multidimensional array in which all of the rows have the same number of elements and all of the columns have the same number of elements ;; rectangular array

one in which the lengths of the rows need not be the same ;; jagged array

is some substructure of that array ;; slice

the elements of the array that have as their first subscript the lower bound value of the subscript are stored first, followed by the elements of the second value of the first subscript, and so forth ;; row major order

an unordered collection of data elements that are indexed by an equal number of values called keys, basically hashes ;; associative array

an aggregate of data elements in which the individual elements are identified by names and accesses through offsets from the beginning of the structure ;; record

record elements, not referenced in indices(records) ;; fields

to a record field is one in which all intermediate record names, from the largest enclosing record to the specific field, are named in the reference. ;; fully qualified reference

the field is named, but any or all of the enclosing record names can be omitted, as long as the resulting reference is unambiguous in the referencing environment ;; elliptical references