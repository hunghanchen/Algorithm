![image](https://github.com/hunghanchen/Algorithm/blob/master/Java/Code/img/Reverse%20Integer.PNG)
```java
        int ans = 0;
        int reminder = 0;
        while (x != 0) {
            reminder = x % 10;
            x /= 10;
            if (ans > Integer.MAX_VALUE / 10 || (ans == Integer.MAX_VALUE / 10 && reminder > 7)) {
                return 0;
            }
            if (ans < Integer.MIN_VALUE / 10 || (ans == Integer.MIN_VALUE / 10 && reminder > 8)) {
                return 0;
            }
            ans = ans * 10 + reminder;
        }
        return ans;
    }
 
