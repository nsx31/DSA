## Bubble sort :
- Adjacent elements are swapped with each other.
- After first step the greatest element present inside the list placed at the end of the list.
```java
import java.util.Arrays;

class Dsa {
    public static void main(String[] args){
        int[] arr = {5,2,4,10,1,6};
        int[]res = bubbleSort(arr);
        System.out.println("Sorted array: "+Arrays.toString(res));
    }

    static int[] bubbleSort(int[] arr){
        for(int i=0; i<arr.length-1; i++){
            boolean isSwapped = false;
            for(int j=0; j<arr.length-1-i; j++){
                if(arr[j]>arr[j+1]){
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                    isSwapped = true;
                }
            }

            if(!isSwapped){
                break;
            }
        }

        return arr;
    }
}
```