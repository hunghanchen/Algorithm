```java
public static int reverse(int x) {
        int ans = 0;
        while (x != 0) {            
            if (x > Integer.MAX_VALUE) return 0;
            if (x < Integer.MIN_VALUE) return 0;
            int render = x % 10;
            x /= 10;
            ans = ans * 10 + render;
        }
        return ans;
    


    }
   ```
