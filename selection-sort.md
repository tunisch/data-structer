# Selection Sort

<img width="278" height="278" alt="image" src="https://github.com/user-attachments/assets/81b2db43-f7f2-4f91-9a33-8452fdb6c02d" />

The algorithm looks through the array again and again, moving the next lowest values to the front, until the array is sorted.

**How it works:**

1. Go through the array to find the lowest value.
2. Move the lowest value to the front of the unsorted part of the array.
3. Go through the array again as many times as there are values in the array.

## Manual Run Through

Before we implement the Selection Sort algorithm in a programming language, let's manually run through a short array only one time, just to get the idea.

**Step 1:** We start with an unsorted array.

> [ 7, 12, 9, 11, 3]

**Step 2:** Go through the arrat, one value at a time. Which value is the lowest? 3, right?

> [ 7, 12, 9, 11, 3]

**Step 3:** Move the lowest value 3 to the front of the array.

> [ 3, 7, 12, 9, 11]

**Step 4:** Look through the rest of the values, starting with 7. 7 is the lowest value, and already at the front of the array, so we don't need to move it.

> [ 3, 7, 12, 9, 11]

**Step 5:** Look through the rest of the array: 12, 9 and 11. 9 is the lowest value.

> [ 3, 7, 12, 9, 11]

**Step 6:** Move 9 to the front.

> [ 3, 7, 9, 12, 11]

**Step 7:** Looking at 12 and 11, 11 is the lowest.

> [ 3, 7, 9, 12, 11]

**Step 8:** Move it to the front.

> [ 3, 7, 9, 11, 12]

Finally, the array is sorted.

### Manual Run Through: What Happened?

We must understand what happened above to fully understand the algorithm, so that we can implement the algorithm in a programming language.

Can you see what happened to the lowest value 3? In step 3, it has been moved to the start of the array, where it belongs, but at that step the rest of the array remains unsorted.

So the Selection Sort algorithm must run through the array again and again, each time the next lowest value is moved in front of the unsorted part of the array, to its correct position. The sorting continues until the highest value 12 is left at the end of the array. This means that we need to run through the array 4 times, to sort the array of 5 values.

And each time the algorithm runs through the array, the remaining unsorted part of the array becomes shorter.

### Selection Sort Time Complexity

Selection Sort sorts an array of n values.

On average, about n/2 elements are compared to find the lowest value in each loop.

And Selection Sort must run the loop to find the lowest value approximately n times.

We get time complexity:

<img width="341" height="90" alt="image" src="https://github.com/user-attachments/assets/eb4476ad-d35b-4eb4-9373-8946e4fe3d61" />

The time complexity for the Selection Sort algorithm can be displayed in a graph like this:

<img width="672" height="324" alt="image" src="https://github.com/user-attachments/assets/beb6c55e-4bc1-449f-9a93-c8b741915c85" />

The red dashed line represents the theoretical time complexity 

O(n2)

Blue crosses appear when you run the simulation. The blue crosses show how many operations are needed to sort an array of a certain size.

