
# _Style_

I've made a lot of similar style suggestions during the code reviews. When someone says "Make this code more readable," it sounds like a good thing to do and I'll nod along with them. But practically I'd rather see concrete examples of what they mean, and so I thought I'd document some of the examples we've gone over.

**I believe that code should be written to be as predictable as possible.**

Everything I've suggested works toward that goal. Here are some specific examples of refactoring we did to reduce the code and make it more readable.


Spacing
----

Code is easier to read with spaces added between the lines. My goal is to visually space code into logical parts.

Good inline spacing also improves code. [PEP8](https://www.python.org/dev/peps/pep-0008/#code-lay-out) has a lot to say about this.

I also think that inline spacing should be consistent throughout the code. For example, one of the code snippets below has this line...

```
right = lst[-1-index]
```

...and then later it has this line

```
right = lst[-1 - index]
```

You should maintain the same habits throughout your code, because it will make it more predictable.

Logic
----

All things equal, your code should be have a logical flow to it. If you're parsing an array, start with the left side and move to the right. If you're declaring the three variables, `low` `mid` and `high`, declare them in that order.

For example, one of the code snippets below initalizes the variables like this:

```python
max_value = len(array)
min_value = 0
```

This'll make me sound super fussy, but I think it reads more logically to _first_ declare the `min_value` and _then_ declare the `max_value`.

About 15 years ago I read the annotated version of the first three _Dragonlance_ books. One of the annotations made a point that's stuck with me, and is relevant here. They said that a science fiction writer can create anything, any kind of world. And so they have a responsibility to balance their invented concepts with regular, terrestrial concepts so as to not overload the reader.

We have the same responsibility and far less room for creativity. Have I said it too many times already? You want your code to be as predictable as possible.

> "The problem is that people just want to fix their bugs and move on. [...] As I talked about in '[Applying neuroscience to software development](http://chrismm.com/blog/how-to-use-your-full-brain-when-writing-code/)', when people have to digest your piece of code, their 'mental stack' fills up and it is hard to make progress."
> [Writing Good Code: how to reduce the cognitive load of your code](http://chrismm.com/blog/writing-good-code-reduce-the-cognitive-load/) by Christian Maioli Mackeprang

----

Alright, I've said my piece. Here are some examples.


**Before**

```python
def length(lst):
    '''Return length of lst containing no duplicates'''
    index = 0
    left = lst[index]
    right = lst[-1-index]
    while left < right:
        index = index +1  # Add a space before the 1
        left = lst[index]
        right = lst[-1 - index]  # Remove these spaces
    return index*2  # Space this out
```

**After**

```python
def length(lst):
    '''Return length of lst containing no duplicates'''
    index = 0
    left = lst[index]
    right = lst[-1-index]

    while left < right:
        index = index + 1
        left = lst[index]
        right = lst[-1-index]

    return index * 2
```

----

**Before**

```python
def find(target,listy):
    size = len(listy)
    if size == 0:
        return -1
    mid = size//2  # Space this out
    hi = size-1  # Space this out
    lo = 0
    while target != listy[mid] and lo <= hi:
        if target < listy[mid]:
            hi = mid - 1
            mid = (hi+lo) // 2  # Space out the addition
        if target > listy[mid]:
            lo = mid + 1
            mid = (hi+lo) //2  # Space out the addition
    if target == listy[mid]:
        return mid
    else:
        return -1
```

**After**

```python
def find(target,listy):
    size = len(listy)
    if size == 0:
        return -1

    mid = size // 2
    hi = size - 1
    lo = 0

    while target != listy[mid] and lo <= hi:
        if target < listy[mid]:
            hi = mid - 1
            mid = (hi + lo) // 2

        if target >  listy[mid]:
            lo = mid + 1
            mid = (hi + lo) // 2

    if target == listy[mid]:
        return mid
    else:
        return -1
```

----

**Before**

```python
def binary_search(element, lst):
    max_index = len(lst)
    min_index = 0

    while True:
        pointer = (max_index - min_index)//2 + min_index
        if lst == []:
            return -1
        elif lst[pointer] == x:
            return pointer
        elif abs(max_index - min_index) <= 1: #we've run out of list to check!
            return -1
        elif lst[pointer] > x:
            max_index = pointer
        elif lst[pointer] < x:
            min_index = pointer
```

**After**

```python
def find(x, listy):
    min_index = 0
    max_index = len(listy)

    while min_index < max_index:
        pointer = (min_index + max_index) // 2

        if listy[pointer] == x:
            return pointer

        elif listy[pointer] > x:
            max_index = pointer

        else:
            min_index = pointer

    return -1
```