# multiples
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
Explanation 0

For , if we list all the natural numbers below  that are multiples of  or , we get  and . The sum of these multiples is .

Similarly for , we get .
--------------------------------------------------------------------------------------------------------------
import sys


def t(n):
   
    return n * (n + 1) // 2


def sum_3_5(n):
    
    return 3 * t(n // 3) + 5 * t(n // 5) - 15 * t(n // 15)


if len(sys.argv) > 1:
    for i in sys.argv[1:]:
        print(i, sum_3_5(int(i) - 1))
else:
    nb = int(input().strip())
    for _ in range(nb):
        n = int(input().strip())
        print(sum_3_5(n - 1))
