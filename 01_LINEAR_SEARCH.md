## Linear Search :
It suggests, start searching from the first element till you find the element you are looking for.

```java
class Main {
    public static void main(String[] args){
        int[] arr = {23,3,1,78,34,2,5,32,1};
        int idx = linearSearch(arr, 5);
        System.out.println("idx: "+idx);
    }

    static int linearSearch(int[] arr, int num){
        for(int i=0; i<arr.length; i++){
            if(arr[i]==num){
                return i;
            }
        }
        return -1;
    }
}
```

- Best case time complexity of linear search is : **O(1)**
- And the worst case time complexity of linear search is : **O(n)**

## Number of digits : 
Suppose we are given a number and we are asked to find the number of digits present in that number. for example 93498349 has 8 digits.

```java
class Main {
    public static void main(String[] args){
        System.out.println(calDigit(348498));
    }
    
    static int calDigit(int num){
        if(num<0){
            num=num*-1;
        }

        int digits = (int)Math.log10(num)+1;
        return digits;
    }
}

```