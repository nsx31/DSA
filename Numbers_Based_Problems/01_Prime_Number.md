```java
class Main {
    public static void main(String[] args){
        System.out.println(isNumberPrime(1));
    }

    static boolean isNumberPrime(int num){
        // numbers less than 2 are not prime numbers
        if(num < 2){
            return false;
        }

        // numbers which are divisible by any other number (except 1 and itself ) are not prime numbers.
        /*
            Trick: Instead of looping from 2 to the "num - 1", 
            we loop from 2 to square root of "num".
            If a number is not prime, we will find a factor 
            within this range itself, making the approach more efficient.
        */

        int sqrt = (int)Math.sqrt(num);

        for(int i=2; i<=sqrt; i++){
            if(num%i == 0){
                return false;
            }
        }

        return true;
    }
}
```