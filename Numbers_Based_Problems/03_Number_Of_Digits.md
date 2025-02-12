## Game Plan:
- We will divide the given number by 10 to find the quotient.
- Next, we will will divide the quotient by 10 again to get the next quotient, and we will keep repeating this process until the quotient becomes 0.
- Finally, we will count the number of times we perform the division. The number of divisions is equal to the number of digits in the given number.

```java
class Main {
    public static void main(String[] args){
        System.out.println(numOfDigits(1237910));
    }

    static int numOfDigits(int num){
        // counting the number of time division is performed
        int count=0;

        // dividing num till it becomes zero.
        while(num != 0){
            num=num/10;
            count++;
        }

        return count;
    }
}
```