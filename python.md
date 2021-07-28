# Style Guide for Python Code

## Naming conven­tions

1.  Never use l, O, or I single letter names as these can be mistaken for 1 and 0, depending on typeface
2.  O = 2 # This may look like you're trying to reassign 2 to zero


    | Type  | Example |
    | ------------- | ------------- |
    |Function  |function, my_fun­ction|
    |Vari­able  |x, var, my_var­iable|
    |Class     |Model, MyClass|
    |Method    |class_­method, method|
    |Cons­tant  |CONSTANT, MY_CON­STANT, MY_LON­G_C­ONSTANT|
    |Module     |module.py, my_mod­ule.py|
    |Pack­age    |package, mypackage|


## Maximum Line Length and Line Breaking
1.  PEP 8 suggests lines should be limited to 79 characters. This is because it allows you to have multiple files open next to one another, while also avoiding line wrapping.

- Python will assume line continuation if code is contained within parentheses, brackets, or braces:
    ```
    def function(arg_one, arg_two,arg_three, arg_four):
        return arg_one
    ```

- If it is impossible to use implied continuation, then you can use backslashes to break lines instead:
    ```
    from mypkg import example1, \
        example2, example3
    ```

    #### #Recommended
    ```
    total = (first_variable
             + second_variable
             - third_variable)
    ```
    #### #Not Recommended
    ```
    total = (first_variable +
             second_variable -
             third_variable)
    ```

##  Identation

1.  Use 4 consec­utive spaces to indicate indent­ation.
2.  Prefer spaces over tabs.

## Comments

1.  Limit the line length of comments and docstrings to 72 charac­ters.
2.  Use complete sentences, starting with a capital letter.
3.  Make sure to update comments if you change your code.

## Block Comments

1.  Indent block comments to the same level as the code they describe.
2.  Start each line with a # followed by a single space.
3.  Separate paragraphs by a line containing a single #.

## Inline Comments

1. Use inline comments sparingly.
2. Write inline comments on the same line as the statement they refer to.
3. Separate inline comments by two or more spaces from the statement.
4. Start inline comments with a # and a single space, like block comments.
5. Don’t use them to explain the obvious.

## When to Avoid Adding Whitespace
1. The most important place to avoid adding whitespace is at the end of a line. This is known as trailing whitespace
2. Immedi­ately inside parent­heses, brackets, or braces.
3. Before a comma, semicolon, or colon.
4. Before the open parent­hesis that starts the argument list of a function call.
5. Before the open bracket that starts an index or slice.
6. Between a trailing comma and a closing parent­hesis.
7. To align assignment operators.
8. immedi­ately inside brackets, as well as before commas and colons.

## Progra­mming Recomm­end­ations

1. Don’t compare boolean values to True or False using the equiva­lence operator.
2. Use the fact that empty sequences are falsy in if statem­ents.
3. Use is not rather than not ... is in if statem­ents.
4. Don’t use if x: when you mean if x is not None.

## Code Layout
1. Surround top-level functions and classes with two blank lines
2. Surround method defini­tions inside classes with a single blank line.
3. Use blank lines sparingly inside functions to show clear steps.

## Indent­ation Following Line Breaks
1. There are two styles of indent­ation you can use.
2. The first of these is to align the indented block with the opening delimiter.
3. An altern­ative style of indent­ation following a line break is a hanging indent. This is a typogr­aphical term meaning that every line but the first in a paragraph or statement is indented.

## Indent­ation Following Line Breaks 2
```
    def function(arg_one, arg_two,
                arg_three, arg_four):
        return arg_one


    x = 5
    if (x > 3 and
        x < 10):
        print(x)

    x = 5
    if (x > 3 and
        x < 10):
        # Both conditions satisfied
        print(x)

    x = 5
    if (x > 3 and
            x < 10):
        print(x)

```

#### hanging indent

```
    var = function(
        arg_one, arg_two,
        arg_three, arg_four)
```

## Where to Put the Closing Brace
PEP 8 provides two options for the position of the closing brace in implied line continuations:

1. Line up the closing brace with the first non-whitespace character of the previous line:
```
    list_of_numbers = [
        1, 2, 3,
        4, 5, 6,
        7, 8, 9
        ]
```

2. Line up the closing brace with the first character of the line that starts the construct:
```
    list_of_numbers = [
        1, 2, 3,
        4, 5, 6,
        7, 8, 9
    ]
```

## Docume­ntation Strings
1. Surround docstrings with three double quotes on either side, as in "­"­"This is a docstr­ing­"­"­".
2. Write them for all public modules, functions, classes, and methods.
3. Put the "­"­" that ends a multiline docstring on a line by itself.
4. For one-line docstr­ings, keep the "­"­" on the same line.

## Whitespace Around Binary Operators
### Surround the following binary operators with a single space on either side:
- Assignment operators (=, +=, -=, and so forth)
- Compar­isons (==, !=, >, <. >=, <=) and (is, is not, in, not in)
- Booleans (and, not, or)
### When = is used to assign a default value to a function argument, do not surround it with spaces:
- `def functi­on(­def­aul­t_p­ara­met­er=5):`
- `y = x**2 + 5`
- `z = (x+y) * (x-y)`
- `if x>5 and x%2==0:`
###  Treat the colon as the operator with lowest priority
- list[x+1 : x+2]
### In an extended slice, both colons must be surrounded by the same amount of whitespace
- `list[3­:4:5]`
- `list[x+1 : x+2 : x+3]`
### The space is omitted if a slice parameter is omitted
- `list[x+1 : x+2 :]`

## When to Ignore PEP 8
1. If complying with PEP 8 would break compat­ibility with existing software.
2. If code surrou­nding what you’re working on is incons­istent with PEP 8
3. If code needs to remain compatible with older versions of Python.













