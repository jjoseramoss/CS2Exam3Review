# Search and Complexity: Review
What are the restrictions (if any) for using these?
*How many steps does it take in the worst case to give an answer if I 
provide you with a list of 1,000 numbers? 2,000?
*Is one always better than the other? We mentioned in class that one 
of these can be much much faster than the other – does this mean it is 
the superior choice in all situations? Be prepared to explain your 
reasoning. <br>
a. Sequential  <br>
    
    There are no restrictions on this type of list; it works on both sorted and unsorted lists. It's simple and can be applied to any dataset. Worst case, you need to check all n elements.


b. Binary Search <br>

    This search requires for the list to be sorted beforehand. Sorting itself can add extra computational overhead if the list isn't already sorted (O(n log n) for sorting). Worst  case O(log n), where n is the number of elements

     - For 1000 numbers log_2 1000 = 10 steps
     - For 2000 numbers log_2 2000 = 11 steps

Sequential search is more suitable for datasets that are small, unsorted, or frequently changing. On the other hand, for large datasets that require frequent searches, sorting the data once allows Binary Search to provide much faster results.

Example of Sequential Search:
```
    bool seqSearch(string target, string arr[], int start, int end) {
    for(int i = start; i <= end; i++){
        if(arr[i] == target){
            return true;
        }
    }
    return false;
}

```

Example of Binary Search:
    
    Binary Search
    The values in my array are in order! least to greatest
    1. keep track of start and end index
    2. start is the beginning (index 0), end is end(index size-1)
    3. check if start is before end
        YES - we have numbers to search
        NO - there are no numbers to search(return false)
    4. find middle index
    5. check if middle value is target
        CASE 1: middle val is < than target
            val has to be to the right of middle val
                (index has to be greater than middle)
            UPDATE - start = middle + 1(goes one past middle)
        CASE 2: middle val is > than target
            val has to be to the left of middle val
                (index has to be less than middle)
            UPDATE - end = middle - 1 (one before middle)
        CASE 3: middle val is == target
            return true, we found it
        GO BACK TO STEP 4 - updating MIDDLE

```
bool binSearch(float target, float arr[], int n) {
    int start = 0;
    int end = n;
    
    while(start<end){
        int mid = start+(end - start)/2;
        if(arr[mid] == target){
            return true;
        }
        else if(arr[mid] < target){
            start = mid+1;
        }
        else{
            end = mid-1;
        }

    }
    
    
    return false;	
}


```
mid = start + (end - start) / 2  <br>
end(beginning) = n or n-1
