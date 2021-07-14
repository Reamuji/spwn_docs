# List of Built-in Functions

| name              | arguments                                                  | example                            | description                                                                                |
| ----------------- | ---------------------------------------------------------- | ---------------------------------- | ------------------------------------------------------------------------------------------ |
| print             | any number of values with types that can convert to string | `$.print("Hello world!")`          | Prints value(s) to the console                                                             |
| sin               | a number                                                   | `$.sin(3.14159)`                   | Calculates the _sin_ of an angle in radians                                                |
| cos               | a number                                                   | `$.cos(3.14159)`                   | Calculates the _cos_ of an angle in radians                                                |
| tan               | a number                                                   | `$.tan(3.14159)`                   | Calculates the _tan_ of an angle in radians                                                |
| asin              | a number                                                   | `$.asin(3.14159)`                  | Calculates the _arcsin_ of a number                                                        |
| acos              | a number                                                   | `$.acos(3.14159)`                  | Calculates the _arccos_ of a number                                                        |
| atan              | a number                                                   | `$.atan(3.14159)`                  | Calculates the _arctan_ of a number                                                        |
| floor             | a number                                                   | `$.floor(3.14159) == 3`            | Calculates the _floor_ of a number, AKA the number rounded **down** to the nearest integer |
| ceil              | a number                                                   | `$.ceil(3.14159) == 4`             | Calculates the _ceil_ of a number, AKA the number rounded **up** to the nearest integer   |
| add               | an `@object` or a `@trigger` value                         | `$.add(obj{ 1: 1 })`               | Adds a Geometry Dash object or trigger to the target level                                 |
| append            | an array, and a value to append to the array               | `$.append(names, "joe")`           | Appends a value to the end of an array. You can also use `array.push(value)`               |
| pop               | an array                                                   | `$.pop(names)`                     | Removes a value from the end of an array. You can also use `array.pop()`                   |
| remove_index      | an array, and the index of a value to be removed           | `$.remove_index(names, 2)`         | Removes a specific value from an array. You can also use `array.remove(index)`             |
| readfile          | a file path (string)                                       | `$.readfile("file.txt")`           | Opens a file and returns it as a string                                                    |
| split_str         | a string to be split, and a string delimeter               | `$.split_str("1,2,3", ",")`        | Returns an array from the split string. You can also use `string.split(delimeter)`         |
| substr            | a string to be sliced, a start index, and an end index     | `$.substr("hello there", 1, 5)`    | Returns a specified part of the input string                                               |
| matches           | a value to be checked and a pattern                        | `$.matches([1, 2, 3], [@number])`  | Returns `true` if the value matches the pattern, otherwise it returns `false`              |
| edit_obj          | an object, an object key, and a value                      | `$.edit_obj(object, ROTATION, 180)`| Changes the value of an object key. You can also use `object.set(key, value)`              |
| b64encode        | a string to be encoded                                      | `$.b64encode"hello there")`      | Returns the input string encoded with base64 encoding (useful for text objects)            |
| b64decode        | a string to be decoded                                      | `$.b64decode("aGVsbG8gdGhlcmU=")` | Returns the input string decoded from base64 encoding (useful for text objects)           |
| get_input         | any number of values with types that can convert to string | `$.get_input("Enter a number:")`   | Prompts the user for input and returns the result as a string                              |
| mutability        | one value                                                  | `$.mutability(my_array)`           | Returns whether the given value is mutable or not.                                         |
| \_or\_            | two booleans                                               | `$._or_(true, false)`              | Default implementation of the `\|\|` operator                                              |
| \_and\_           | two booleans                                               | `$._and_(true, true)`              | Default implementation of the `&&` operator                                                |
| \_more_than\_     | two booleans                                               | `$._more_than_(100, 50)`           | Default implementation of the `>` operator                                                 |
| \_less_than\_     | two numbers                                                | `$._less_than_(50, 100)`           | Default implementation of the `<` operator                                                 |
| \_more_or_equal\_ | two numbers                                                | `$._more_or_equal_(100, 100)`      | Default implementation of the `>=` operator                                                |
| \_less_or_equal\_ | two numbers                                                | `$._less_or_equal_(100, 100)`      | Default implementation of the `<=` operator                                                |
| \_divided_by\_    | two numbers                                                | `$._divided_by_(64, 8)`            | Default implementation of the `/` operator                                                 |
| \_times\_         | two numbers                                                | `$._times_(8, 8)`                  | Default implementation of the `*` operator                                                 |
| \_mod\_           | two numbers                                                | `$._mod_(70, 8)`                   | Default implementation of the `%` operator                                                 |
| \_pow\_           | two numbers                                                | `$._pow_(8, 2)`                    | Default implementation of the `^`/`**` operator                                            |
| \_plus\_          | two numbers                                                | `$._plus_(32, 32)`                 | Default implementation of the `+` operator                                                 |
| \_minus\_         | two numbers                                                | `$._minus_(128, 64)`               | Default implementation of the `-` operator                                                 |
| \_equal\_         | two values                                                 | `$._equal_("hello", "hello")`      | Default implementation of the `==` operator                                                |
| \_not_equal\_     | two values                                                 | `$._not_equal_("hello", "bye")`    | Default implementation of the `!=` operator                                                |
| \_assign\_        | a variable and a value                                     | `$._assign_(val, 64)`              | Default implementation of the `=` operator                                                 |
| \_as\_            | a value and a type-indicator                               | `$._as_(1000, @string)`            | Default implementation of the `as` operator                                                |
| \_swap\_          | two values                                                 | `$._swap_(a, b)`                   | Default implementation of the `<=>` operator                                               |
| \_has\_           | two values                                                 | `$._has_([1,2,3], 2)`              | Default implementation of the `has` operator                                               |
| \_add\_           | a variable and a number                                    | `$._add_(val, 10)`                 | Default implementation of the `+=` operator                                                |
| \_subtract\_      | a variable and a number                                    | `$._subtract_(val, 10)`            | Default implementation of the `-=` operator                                                |
| \_exponate\_      | a variable and a number                                    | `$._exponate_(val, 2)`             | Default implementation of the `^=` operator                                                |
| \_modulate\_      | a variable and a number                                    | `$._modulate_(val, 2)`             | Default implementation of the `%=` operator                                                |
| \_multiply\_      | a variable and a number                                    | `$._multiply_(val, 10)`            | Default implementation of the `*=` operator                                                |
| \_divide\_        | a variable and a number                                    | `$._divide_(val, 3)`               | Default implementation of the `/=` operator                                                |
| \_either\_        | two patterns                                               | `$._either_(@number, @counter)`    | Default implementation of the `\|` operator                                                |
| \_range\_         | two numbers                                                | `$._range_(0, 10)`                 | Default implementation of the `..` operator                                                |