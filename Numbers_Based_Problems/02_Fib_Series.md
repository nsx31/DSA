```java
class Main {
    public static void main(String[] args){
        printFibSeries(9);
    }

    static void printFibSeries(int numOfTerms){
        int a = 0;
        int b = 1;
        
        while(numOfTerms >= 0){
            System.out.println(a);
            int sum = a+b;
            a=b;
            b=sum;

            numOfTerms--;
        }
    }
}
```

