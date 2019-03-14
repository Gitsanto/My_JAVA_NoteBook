# My_JAVA_NoteBook


# Programming language terms(derived from [stackflow](https://stackoverflow.com/questions/18202818/classes-vs-functions))
## function
    - purpose: process data, manipulate data, create result sets.
    - when to use: always code a function if you want to do this: “y=f(x)”

## struct/dict/json/etc (instead of class)
    - purpose: store attr./param., maintain attr./param., reuse attr./param., use attr./param. later.
    - when to use: if you deal with a set of attributes/params (preferably not mutable)
    different languages same thing: struct (C/C++), JSON (js), dict (python), etc.
    always prefer simple struct/dict/json/etc over complicated classes (keep it simple!)

## class (if it is a new data type)
    - a simple perspective: is a struct (C), dict (python), json (js), etc. with methods attached.
    The method should only make sense in combination with the data/param stored in the class.
    - advice: never code complex stuff inside class methods (call an external function instead)
    - warning: do not misuse classes as fake namespace for functions! (this happens very often!)
    other use cases: if you want to do a lot of operator overloading then use classes (e.g. your own matrix/vector multiplication class)
    - ask yourself: is it really a new “data type”? (Yes => class | No => can you avoid using a class)

## array/vector/list (to store a lot of data)
    - purpose: store a lot of homogeneous data of the same data type, e.g. time series
    - advice#1: just use what your programming language already have. do not reinvent it
    - advice#2: if you really want your “class mysupercooldatacontainer”, then overload an existing array/vector/list/etc class (e.g. “class mycontainer : public std::vector…”)

## enum (enum class)
    - Enum are lists of constants.
    - Purpose: When you need a predefined list of values.
    - advice#1: use enum plus switch-case instead of overcomplicated OOP design patterns
    - advice#2: use finite state machines
