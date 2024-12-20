## Binary Search :
- for using binary search array must be sorted
- here we assumed the given array is sorted in ascending order
```java
class Main {
    public static void main(String[] args){
        int[] arr = {12,45,67,89,967};
        System.out.println(binarySearch(arr,89));
    }

    static int binarySearch(int[] arr, int num){
        int low = 0;
        int high = arr.length-1;

        while(low<=high){
            int mid = (low+high)/2;
            
            if(arr[mid]==num){
                return mid;
            }else if (num<arr[mid]){
                high = mid-1;
            }else {
                low = mid+1;
            }
        }

        return -1;
    }
}
```

- above we assumed the given array is sorted in ascending order but what if it was in descending order.
```java
// this is the generalized approch in which we consider both ascending and descending situation
class Main {
    public static void main(String[] args){
        int[] arr = {76,69,56,44,34,23,13};
        int res = binarySearch(arr, 69);
        System.out.println("idx: "+res);
    }

    static int binarySearch(int[] arr, int num){
        int low = 0;
        int high = arr.length-1;

        if(arr[low]<arr[high]){
            while(low<=high){
                int mid = (low+high)/2;
            
                if(arr[mid]==num){
                    return mid;
                }else if (num<arr[mid]){
                    high = mid-1;
                }else {
                    low = mid+1;
                }
            }
        }else{
            while(low<=high){
                int mid = (low+high)/2;

                if(arr[mid]==num){
                    return mid;
                }else if(num<arr[mid]){
                    low = mid+1;
                }else {
                    high = mid-1;
                }
            }
        }

        return -1;
    }
}
```

- best case time complexity : **O(1)**
- worst case time complexity : **O(log n)**

![alt text](image.png)
