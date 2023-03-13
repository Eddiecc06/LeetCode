# Summary
Binary search algorithm is widely used to search the target number in an array. 
The time complexity of the binary search algorithm is O(log n). The time complexity of best case would be O(1) when the number of middle index is directly matched to the target value. The worst case could be the target is at either extremity of the list or not in the list.

This page shows the templates of binary search method.
Binary search can be used to find :
1. The number **equals to** the target number
2. The first number **isn't smaller than** the target number 
3. Tha last number **is smaller than** the target number
4. The first number **is larger than** the target number 
5. Tha last number **isn't larger than** the target number
6. Others


## 1. The number equals to the target number

### _C++ Template 1_
```cpp
int Binary_Search(vector<int>& nums, int target) {
    int left = 0, right = nums.size();
    while (left < right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] == target) 
          return mid;
        if (nums[mid] < target)
          left = mid + 1;
        else 
          right = mid;
    }
    return -1;
}
```

### _C++ Template 2_
```cpp
int Binary_Search(vector<int>& nums, int target) {
    int left = 0, right = nums.size()-1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] == target)
          return mid;
        if (nums[mid] < target)
          left = mid + 1;
        else
          right = mid - 1;
    }
    return -1;
}
```

## 2. The first number isn't smaller than the target number

### _C++ Template 1_
```cpp
int Binary_Search(vector<int>& nums, int target) {
    int left = 0, right = nums.size();
    while (left < right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] < target)
          left = mid + 1;
        else
          right = mid;
    }
    return right;
}
```

## 3. Tha last number is smaller than the target number

### _C++ Template 1_
```cpp
int Binary_Search(vector<int>& nums, int target) {
    int left = 0, right = nums.size();
    while (left < right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] < target)
          left = mid + 1;
        else
          right = mid;
    }
    return right-1;
}
```

## 4. The first number is larger than the target number

### _C++ Template 1_
```cpp
int Binary_Search(vector<int>& nums, int target) {
    int left = 0, right = nums.size();
    while (left < right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] <= target)
          left = mid + 1;
        else
          right = mid;
    }
    return right;
}
```

## 5. Tha last number isn't larger than the target number

### _C++ Template 1_
```cpp
int Binary_Search(vector<int>& nums, int target) {
    int left = 0, right = nums.size();
    while (left < right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] <= target)
          left = mid + 1;
        else
          right = mid;
    }
    return right-1;
}
```
