### Task 8kyu:
You will be given an array a and a value x. All you need to do is check whether the provided array contains the value.
Array can contain numbers or strings. X can be either.
Return true if the array contains the value, false if not.

[Task link](https://www.codewars.com/kata/57cc975ed542d3148f00015b)

#### Solution:
```
public class Solution {

    public static boolean check(Object[] array, Object value) {
        for (int i = 0; i < array.length; i++) {
            if (array[i].equals(value)) return true;
        }
        return false;
    }

}
```

#### Fav solution:
```
import java.util.Arrays;

public class Solution {

    public static boolean check(Object[] a, Object x) {
        return Arrays.asList(a).contains(x);
    }

}
```

#### Comment:
They connected the library and used the function. I took note for the future.

### Task 6kyu:
If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in. Additionally, if the number is negative, return 0 (for languages that do have them).
Note: If the number is a multiple of both 3 and 5, only count it once.

[Task link](https://www.codewars.com/kata/514b92a657cdc65150000006/train/java)

#### Solution:
```
  public int solution(int number) {
   int sum=0;
    if (number <= 0) {
      return 0;
    }
    for (int i=1; i < number; i++){
      if (i%3==0 || i%5==0){
        sum+=i;
      }
    }
    return sum;
  }
```

#### Fav solution:
```
import java.util.stream.*;

public class Solution {

  public int solution(int number) {
    return IntStream.range(3, number).filter(n -> n % 3 == 0 || n % 5 == 0).sum();
  }
}
```

#### Comment:
Very interesting but not clear. It takes up less space, the operating time coincides with my decision.
