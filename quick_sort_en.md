# For a given array: `11 1 30 2 51 6 29 7 67 15 118 4 89 23`, the process of Quick Sort.

    Quick Sort is a divide-and-conquer sorting algorithm that divides an array into two parts by selecting a datum element, where all elements in one part are smaller than the datum and all elements in the other part are larger than the datum. Then, quickly sort the two parts separately.

## 1. Quick Sort visualization

### 1.1 Choosing a Baseline:

    Select the first element (11) as the baseline.

### 1.2 Partition:

    Divide the array into two parts, one part where all elements are smaller than the datum, and the other part where all elements are larger than the datum. For example, a partitioned array might be: 1 2 6 7 11 30 51 29 67 15 118 4 89 23.

## 2. First iteration

Datum Element: `11`

Partitioned array: `1 2 6 7 11 30 51 29 67 15 118 4 89 23`
In this example, let`s assume that the partitioning process is as follows:

Element on the left that is smaller than the datum: `1 2 6 7`

Element larger than datum on the right: `30 51 29 67 15 118 4 89 23`

## 3. Second iteration

Quick sort the elements on the left that are smaller than the datum:

Datum Element: `1`

Partitioned array: `1`

Since there is only one element on the left, no further partitioning is required.

Quickly sort the elements on the right that are larger than the datum:

Datum element: `30`
Partitioned array: `29 67 15 118 4 89 23`

## 4. Third iteration

Further quicksort of elements on the right that are larger than the datum:

Datum element: `29`

Partitioned array: `29`

Since there is only one element on the right, no further partitioning is required.

Quick sort the remaining elements:

Datum element: `67`

Partitioned array: `15 118 4 89 23`

Continue to partitioning

Datum element: `15`

Partitioned array: `15`

Since there is only one element on the right, no further partitioning is required.

Quick sort the remaining elements:

Datum Element: `118`
Partitioned array: `4 89 23`

## 5. Final sorting

Datum element: `4`

Partitioned array: `4`

Since there is only one element on the right, no further partitioning is required.

Quick sort the remaining elements:

Datum element: `89`

Partitioned array: `23`

Since there is only one element on the right, no further partitioning is required.

outcome
After the above steps, we get the sorted array: `1 2 6 7 11 15 23 29 30 44 51 67 89 118`

**Please note that this process is based on hypothetical partitioning results, and the actual partitioning process may vary depending on the choice of baseline element and partitioning strategy.**

## 6. Comparison table

### 6.1 Best Case:

    If we are very lucky enough to choose a benchmark element that happens to divide the array in half, then the time complexity of Quick Sort will be O(n log n). For example, if our array is 1 2 6 7 11 30 51 29 67 15 118 4 89 23 and we have selected 11 as the baseline, Quick Sort will run optimally.

### 6.2 Worst Case Scenario:

    If we are very unfortunate enough to choose a benchmark element that happens to divide the array into one element and the remaining n-1 elements, then the time complexity of Quick Sort will be O(n^2). For example, if our array is 1 2 6 7 11 30 51 29 67 15 118 4 89 23 and we have chosen 1 as the benchmark, Quick Sort will run in the worst case scenario because all the elements are smaller than the benchmark.

Average case: In the average case, the time complexity of Quick Sort is O(n log n). This is because, regardless of which element we choose as a baseline, Quick Sort will divide the array in half, and on average, the size of the partition will be close to n/2.
