# BigBST
A C program to search big numerical CSV files using a multidimensional AVL tree
Each column becomes a searchable AVL tree.

## Example usage

Generate a bst from a csv:
```C
bst_t* bst = parseFile(filepath);
```

Define a search:
```C
// Used for binary search on each column
resultsFilter_t bounds[] = {
  {x_lo, x_hi},
  {y_lo, y_hi},
  {z_lo, z_hi},
};

...

// Filters can be added to futher filter which data appear in results
int filterfunc(float* d, results_t* res) {
  return 1
}

...
// Search results appear in a dynamic array
results_t* results = res_search(bst, bounds, filterfunc);
```
