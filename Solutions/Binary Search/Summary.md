# Readme
This page shows the templates of binary search method.
Binary search can be used to find :
1. The number **equals to** the target number
2. The first number **isn't smaller than** the target number (lower_bound)
3. Tha last number **is smaller than** the target number
4. The first number **is larger than** the target number (upper_bound)
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
        else if (nums[mid] < target)
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
        else if (nums[mid] < target)
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
