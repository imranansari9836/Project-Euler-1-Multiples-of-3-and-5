# Project-Euler-1-Multiples-of-3-and-5
If we list all the natural numbers below  that are multiples of  or , we get  and . The sum of these multiples is .

Find the sum of all the multiples of  or  below .

Input Format

First line contains  that denotes the number of test cases. This is followed by  lines, each containing an integer, .

Constraints

Output Format

For each test case, print an integer that denotes the sum of all the multiples of  or  below .

Sample Input 0

2
10
100
Sample Output 0

23
2318

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int t = in.nextInt();
        for(int a0 = 0; a0 < t; a0++){
            int n = in.nextInt();
            long x3 = (n-1)/3;
            long x5 = (n-1)/5;
            long x15 = (n-1)/15;          

            long sum1 = 3*x3*(x3+1); 
            long sum2 = 5*x5*(x5+1);
            long sum3 = 15*x15*(x15+1);

            long sum = (sum1+sum2-sum3)/2;
    System.out.println(sum);
        }
    }
}
