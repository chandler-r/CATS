# CATS

This problem set is from [CS 61 at UC Berkley](https://cs61a.org/proj/cats/)!
CATS (CS61A Autocorrected Typing Software) is inspired by [typeracer](https://www.typeracer.com); you will be implementing the backend for a typing game.

## Objectives

- Review recursion
- Review / learn higher order functions
- Learn how to unit test

## Logistics

You will turn in **only** `cats.py`; you do not need to edit or turn in any other file.

This problem set consists of 7 parts, each of which is a function that you will write in `cats.py`.

Do **not** modify any other function. Do not change any function signatures (names, argument order, or number of arguments).

## Task

Follow the instructions [at this website](https://cs61a.org/proj/cats/) **through Phase 2**. You will not be doing Phase 3! In addition, I have also provided hints below and will do demos in class!

## Phase 1: Typing

### Problem 1
- Before writing any code, be sure to unlock the unit tests by running `python3 ok --local -q 01 -u`
- Once you have unlocked the tests and written your function, you can check the correctness of your code with `python3 ok --local -q 01`
- `choose` is a higher order function that takes a function as a parameter. `filter`, another higher order function, will be very useful!

### Problem 2
- Remember to unlock and use the unit tests! Replace the `01` with `02` (and so on for the later problems).
- `about` is a higher order function that returns a function. Below is a (trivial) example of what the syntax looks like.

  ```py
  def about(y):
    def foo(x):
      return x + y # Notice that we can use y inside foo
    return foo

  about(2)(3) # What will this return?
  about(5)(3) # What about this?
  ```

- First write a function that takes a `paragraph` (string) and `topic` (list of strings), and returns a boolean indicating whether the paragraph contains any of the words in topic. Then, think about how to convert this into the format that `about` requires.

### Problem 3
- Be careful with your list indexes :)
- Double check the edge cases!
- `break` might come in handy as you loop through the lists.

### Problem 4
- This is relatively straightforward! Make sure you have the math correct.

The typeracing game should work at this point!

## Phase 2: Autocorrect

### Problem 5
- Try creating a list of tuples, where each tuple contains the word and the distance returned by `diff_function` for that word.
- List comprehension might come in handy!
- `sorted` is a very nice function for sorting lists.

### Problem 6
- Start with the base cases!
- The actual letter being substituted isn't as important as whether or not a substitution is happening.

### Problem 7
- This is the most difficult problem on this problem set! Don't worry if it takes a while.
- The overall structure is very similar to #6!
