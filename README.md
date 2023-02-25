int search(int numbers[], int low, int high, int value) {
    // Base case: low index is greater than high index, meaning the value is not found
    if (low > high) {
        return -1;
    }
    
    // Find the middle index
    int mid = (low + high) / 2;
    
    // If the middle element is the value, return its index
    if (numbers[mid] == value) {
        return mid;
    }
    
    // If the middle element is greater than the value, search the left half of the array
    else if (numbers[mid] > value) {
        return search(numbers, low, mid - 1, value);
    }
    
    // If the middle element is less than the value, search the right half of the array
    else {
        return search(numbers, mid + 1, high, value);
    }
}
