  
# **@array**: 
 
## Macros:

## **\_partition**:

> **Printed:** 
>```spwn
>(self, low: @number, high: @number, comp: @macro = (a, b) { /* code omitted */ }) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Private function needed for .sort()_
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`low`** | @number | | |
>| 2 | **`high`** | @number | | |
>| 3 | `comp` | @macro | `(a, b) { /* code omitted */ }` | |
>

## **all**:

> **Printed:** 
>```spwn
>(self, map: @macro = (a) { /* code omitted */ }) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Determines whether all the members of an array satisfy the specified callback._
>### Example: 
>```spwn
> arr = [true, true, true]
>$.assert(arr.all())
>arr2 = [1, 2, 3, 1, 4, 7]
>$.assert(arr2.all(el => el > 0)) // checks if the array contains only positive elements
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `map` | @macro | `(a) { /* code omitted */ }` | |
>

## **any**:

> **Printed:** 
>```spwn
>(self, map: @macro = (a) { /* code omitted */ }) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Determines whether the specified callback function returns true for any element of an array._
>### Example: 
>```spwn
> arr = [false, false, true, false]
>$.assert(arr.any())
>arr2 = [1, 2, 3, 1, 4, -1, 7]
>$.assert(arr2.any(el => el < 0)) // checks if the array contains any negative elements
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `map` | @macro | `(a) { /* code omitted */ }` | |
>

## **clear**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Clears the array._
>### Example: 
>```spwn
> let arr = [1, 2, 3]
>arr.clear()
>$.assert(arr.is_empty())
>```
>

## **contains**:

> **Printed:** 
>```spwn
>(self, el) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _See if array contains an element._
>### Example: 
>```spwn
> fruit = ['apple', 'banana', 'mango']
>$.assert(arr.contains('banana'))
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`el`** |any | | |
>

## **enumerate**:

> **Printed:** 
>```spwn
>(self, dict: @bool = false) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns an array of index-element pairs_
>### Example: 
>```spwn
> arr = ["a","b","c"]
>    for i in arr.enumerate() {
>        $.print(i[0], ": ", i[1])
>    }
>    /* output:
>    0: 'a'
>    1: 'b'
>    2: 'c'
>    */
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `dict` | @bool | `false` |Return the pair as a dictionary |
>

## **filter**:

> **Printed:** 
>```spwn
>(self, cb: @macro) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns the elements of an array that meet the condition specified in the callback function._
>### Example: 
>```spwn
> arr = [1, 2, 3, 4, 5]
>$.assert(arr.filter(el => el > 3) == [4, 5])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`cb`** | @macro | | |
>

## **flatten**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Flattens any sub-arrays into one big array._
>### Example: 
>```spwn
> arr = [1, 2, [3, 4], 5, [6, 7, [8]]]
>$.assert(arr.flatten() == [1, 2, 3, 4, 5, 6, 7, 8])
>```
>

## **index**:

> **Printed:** 
>```spwn
>(self, el, from: @number = 0) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Gets the index of an element (if it doesn't exist, `null` is returned)_
>### Example: 
>```spwn
> fruit = ['apple', 'banana', 'mango']
>$.assert(fruit.index('apple') == 0)
>$.assert(fruit.index('carrot') == null)
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`el`** |any | | |
>| 2 | `from` | @number | `0` |Index to start the search from |
>

## **index\_all**:

> **Printed:** 
>```spwn
>(self, el) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns an array of all occurences of an element_
>### Example: 
>```spwn
> arr = [1,-5,2,4,2,6]
>$.assert(arr.index_all(2) == [2,4])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`el`** |any | | |
>

## **index\_last**:

> **Printed:** 
>```spwn
>(self, el, until: @number = 0) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Gets the index of the last occurence of an element (if it doesn't exist, `null` is returned)_
>### Example: 
>```spwn
> arr = [1,-5,2,4,2,6]
>$.assert(arr.index_last(2) == 4)
>$.assert(arr.index_last(-3) == null)
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`el`** |any | | |
>| 2 | `until` | @number | `0` |Index to end the search at |
>

## **is\_empty**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns true if the array has a length of 0, false otherwise._
>### Example: 
>```spwn
> arr = []
>arr2 = [1, 2, 3]
>$.assert(arr.is_empty())
>$.assert(!arr2.is_empty())
>```
>

## **map**:

> **Printed:** 
>```spwn
>(self, cb: @macro) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Calls a defined callback function on each element of an array, and returns an array that contains the results._
>### Example: 
>```spwn
> arr = [1, 2, 3, 4, 5]
>$.assert(arr.map(el => el * 2) == [2, 4, 6, 8, 10])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`cb`** | @macro | | |
>

## **max**:

> **Printed:** 
>```spwn
>(self, key: @macro = (el) { /* code omitted */ }) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Gets the highest number in the array._
>### Example: 
>```spwn
> arr = [3, 1, 4, 1]
>$.assert(arr.max() == 4)
>
>arr = ['abc', 'b', 'abdc']
>$.assert(arr.max(key = (el: @string) => el.length) == 'abdc')
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `key` | @macro | `(el) { /* code omitted */ }` | |
>

## **min**:

> **Printed:** 
>```spwn
>(self, key: @macro = (el) { /* code omitted */ }) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Gets the lowest number in the array._
>### Example: 
>```spwn
> arr = [3, 1, 4, 1]
>$.assert(arr.min() == 1)
>
>arr = ['abc', 'b', 'abdc']
>$.assert(arr.max(key = (el: @string) => el.length) == 'b')
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `key` | @macro | `(el) { /* code omitted */ }` | |
>

## **pop**:

> **Printed:** 
>```spwn
>(self, index: @number = -1) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Removes a specific index from the array and returns it._
>### Example: 
>```spwn
> let arr = [1, 2, 3, 4]
>arr.pop()
>$.assert(arr == [1, 2, 3])
>arr.pop(1)
>$.assert(arr == [1, 3])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `index` | @number | `-1` | |
>

## **push**:

> **Printed:** 
>```spwn
>(self, value) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Pushes a value to the end of the array._
>### Example: 
>```spwn
> let arr = [1, 2, 3]
>arr.push(4)
>$.assert(arr == [1, 2, 3, 4])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`value`** |any | | |
>

## **reduce**:

> **Printed:** 
>```spwn
>(self, cb: @macro) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Calls the specified callback function for all the elements in an array. The return value of the callback function is the accumulated result, and is provided as an argument in the next call to the callback function._
>### Example: 
>```spwn
> arr = [1, 2, 3, 4, 5]
>sum = arr.reduce((acum, el) => acum + el)
>$.assert(sum == 15)
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`cb`** | @macro | | |
>

## **remove**:

> **Printed:** 
>```spwn
>(self, index: @number) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns array with all elements that match value removed_
>### Example: 
>```spwn
> let arr = [1, 2, 3, 4, 5]
>arr.remove(3)
>$.assert(arr == [1, 2, 4, 5])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`index`** | @number | | |
>

## **reverse**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Reverses the array._
>### Example: 
>```spwn
> let arr = [1, 2, 3]
>$.assert(arr.reverse() == [3, 2, 1])
>```
>

## **shift**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Removes the first index from the array and returns it._
>### Example: 
>```spwn
> let arr = [5, 1, 5, 3, 2]
>$.assert(arr.shift() == 5)
>$.assert(arr == [1, 5, 3, 2])
>```
>

## **sort**:

> **Printed:** 
>```spwn
>(self, begin: @number = 0, end: @number = -1, comp: @macro = (a, b) { /* code omitted */ }) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Sorts array in-place_
>### Example: 
>```spwn
> arr = [5, 1, 5, 3, 2]
>arr.sort()
>$.assert(arr == [1, 2, 3, 5, 5])
>
>arr = [5, 1, 5, 3, 2]
>arr.sort(begin = 2, end = 4)
>$.assert(arr == [5, 1, 2, 3, 5])
>
>arr = [5, 1, 5, 3, 2]
>arr.sort(comp = (a, b) => a > b)
>$.assert(arr == [5, 5, 3, 2, 1])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `begin` | @number | `0` | |
>| 2 | `end` | @number | `-1` | |
>| 3 | `comp` | @macro | `(a, b) { /* code omitted */ }` | |
>

## **sorted**:

> **Printed:** 
>```spwn
>(self, begin: @number = 0, end: @number = -1, comp: @macro = (a, b) { /* code omitted */ }) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Returns a sorted verison of the array_
>### Example: 
>```spwn
> arr = [5, 1, 5, 3, 2]
>$.assert(arr.sorted() == [1, 2, 3, 5, 5])
>$.assert(arr.sorted(begin = 2, end = 4) == [5, 1, 2, 3, 5])
>$.assert(arr.sorted(comp = (a, b) => a >= b) == [5, 5, 3, 2, 1])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | `begin` | @number | `0` | |
>| 2 | `end` | @number | `-1` | |
>| 3 | `comp` | @macro | `(a, b) { /* code omitted */ }` | |
>

## **sum**:

> **Printed:** 
>```spwn
>(self) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Gets the sum of the value in the array._
>### Example: 
>```spwn
> arr = [1, 2, 3, 4, 5]
>$.assert(arr.sum() == 15)
>```
>

## **unshift**:

> **Printed:** 
>```spwn
>(self, value) { /* code omitted */ }
>``` 
>**Type:** `@macro` 
>## Description: 
> _Pushes a value to the start of the array and returns it._
>### Example: 
>```spwn
> let arr = [1, 5, 3, 2]
>$.assert(arr.unshift(5) == 5)
>$.assert(arr == [5, 1, 5, 3, 2])
>```
>## Arguments:
>
>| # | name | type | default value | description |
>| - | ---- | ---- | ------------- | ----------- |
>| 1 | **`value`** |any | | |
>
