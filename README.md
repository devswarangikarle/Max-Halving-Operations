# Max-Halving-Operations

In a math challenge, Mia is presented with N integers written on a board. She can perform a special operation only if all the integers are even. The operation allows her to pick any integer, say x, and replace it with x/2. Mia wants to see how many times she can perform this operation before at least one of the numbers becomes odd. What’s the maximum number of operations Mia can carry out?

import java.io.*; // for handling input/output
import java.util.*; // contains Collections framework

// don't change the name of this class
// you can add inner classes if needed
class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        int res = 0;
        for (int i = 0; i < n; i++) {
            int num = arr[i];
            if (num % 2 != 0) {
                System.out.println(0);
                return;
            }
            while ((num / 2) % 2 == 0) {
                res++;
                num /= 2;
            }
        }
        System.out.println(res);
    }
}
