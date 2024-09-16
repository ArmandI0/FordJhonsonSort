#  Ford–Johnson algorithm : 

Ford-Johnson Sort is an efficient hybrid sorting algorithm that combines principles of merge sort and insertion sort. Designed to optimize performance, this algorithm leverages the strengths of both sorting methods: the divide-and-conquer approach of merge sort and the simplicity of insertion sort for small datasets.

## Generic Example of Ford–Johnson algorithm

[View Generic Example Diagram](https://armandi0.github.io/FordJhonsonSort/FordJhonsonSort.drawio.html)

## My implementation of Ford–Johnson algorithm

[View My Implementation Diagram](https://armandi0.github.io/FordJhonsonSort/CPP-09.drawio.html)

### Explanation of the Recursive Function

Note : The pseudo-code below is an example that follows my logic and the way I implemented the project.

```c
function recursionSort(pairList):
    // Step 1: Create a container for new pairs
    newTab = createEmptyContainer()

    // Step 2: Combine adjacent pairs
    if size(pairList) <= 1:
        return pairList
    for each pair in pairList:
        if there is a next adjacent pair:
            create a new pair from the current and next pair
            add this new pair to newTab
            skip to the pair after the next one
        else:
            add the remaining element of the current pair to the last new pair in newTab

    // Step 3: Sort the new pairs
    for each pair in newTab:
        sort the pair

    // Step 4: Recursively sort the new pairs
    output = recursionSort(newTab)



    sortedList = createEmptyContainer()

    // Step 5: Insert the min
    add the minimum element of the last pair in output to sortedList

    // Step 6: Insert remaining elements, handling cases where the list has an odd number of elements
    if there are remaining elements:
        find the correct position in sortedList
        insert the remaining element

    // Step 7: Insert all remaining elements using the Jacobsthal sequence   
    while insertion is needed:
        calculate the position using Jacobsthal sequence
        insert elements at the calculated positions in sortedList
        update jacobIndex

    // Step 8: Return the sorted result
    return sortedList
```

#### Ressources : 

https://en.wikipedia.org/wiki/Merge-insertion_sort
