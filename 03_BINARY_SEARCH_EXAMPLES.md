## Ceiling value : 
```java
class Main {
    public static void main(String[] args){
        int[] arr = {2,3,5,9,14,16,18};
        int res = bs(arr,1);
        if(res==-1){
            System.out.println("ceiling value doesnot exists");
            return;
        }
        System.out.println("celing value is: "+arr[res]);
    }

    static int bs(int[] arr, int num){
        int low=0;
        int high=arr.length-1;
        int ceilingValue = -1;

        while(low<=high){
            int mid=(low+high)/2;

            if(arr[mid]==num){
                return mid;
            }else if (num<arr[mid]){
                high=mid-1;
                ceilingValue = mid;
            }else{
                low=mid+1;
            }
        }

        return ceilingValue;
    }
}
```

## Floor value : 
```java

class Main {
    public static void main(String[] args){
        int[] arr = {2,3,5,9,14,16,18};
        int res = bs(arr,161);
        if(res==-1){
            System.out.println("ceiling value doesnot exists");
            return;
        }
        System.out.println("celing value is: "+arr[res]);
    }

    static int bs(int[] arr, int num){
        int low=0;
        int high=arr.length-1;
        int floorValue = -1;

        if(num>arr[arr.length-1]){
            return -1;
        }

        while(low<=high){
            int mid=(low+high)/2;

            if(arr[mid]==num){
                return mid;
            }else if (num<arr[mid]){
                high=mid-1;
            }else{
                low=mid+1;
                floorValue=mid;
            }
        }

        return floorValue;
    }
}
```