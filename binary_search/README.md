##Binary Search

**Case:**
- Suppose you're searching for a person in the phone book, their names starts with K. You could start at the beginning and keep flipping pages until you get to the Ks.
- But you're more likely to start at a page in the middle, because you know the Ks are going to be near the middle of the phone book.
- Or suppose you are searching for a word in a dictionary, and it starts with O, again you will start near the middle.
- Now suppose you log on to Facebook, when you do facebook ahs to verify that you have an account on their site. So it needs to search for your username in its database. Suppose your name is Karlmageddon. Facebook could start from the As and serch for your name- but it makes more sense for it to begin somwhere in the middle.

This is a search problem - All are called **Binary Search**

### Binary Search
- is an algorithm, its input is a sorted list of elements. If an element you are looking for is in that list, binary search returns the position where its located. Otherwise, binary search returns null.

## example
I am thinking of a number between 1 and 100

| 1 | 2 | 3 | ... | 100 |

You have to try to guess numbers in the fewest tries possible. With every guess, Ill tell you if your guess is too low or too high or correct

suppose you start guessing like this; 1, 2, 3, 4 
1 - too low  | ~~1~~ | 2 | 3 | ... | 100 |
2 - too low | ~~1~~ | ~~2~~ | 3 | ... | 100 |
7 - too low

- This is simple search. With each guess, you're elminating only one number. If my number was 99 it could take you 99 guesses to get there!

### a better way to search
50 - Too low - this means you elminite any number below 50
51 - 100 the middle is 75, next guess should be 75 -Too high this means any number above 75 is elminited
51 - 75  = 63 - Too high - this means numbers above 63 are elimiated
51 - 63 = 57 Yes

- You used 7 steps to reach the final answer

## Conclusion
 - In general for any list of n, binary search will take log2 n steps to run in the worst case, where in simple search will take n steps

 ### Implementing Binary Search

 - binary_search functiion takes a sorted array and an item. If the item in in the array, the function returns the position. 
 - you will keep track of what part of the array you have to search through. At the begining, this is the entire array:

  - low = 0
  - high = len(list) - 1


  each time you check the middle element: