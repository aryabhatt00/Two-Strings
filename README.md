# Two-Strings
https://www.hackerrank.com/challenges/two-strings/problem?h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=dictionaries-hashmaps

Code:
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'twoStrings' function below.
#
# The function is expected to return a STRING.
# The function accepts following parameters:
#  1. STRING s1
#  2. STRING s2
#

def twoStrings(s1, s2):
    # Write your code here
    
    d={}
    m={}
    for i in s1:
        if i not in d:
            d[i]=0
        d[i]+=1
    for i in s2:
        if i not in m:
            m[i]=0
        m[i]+=1
    c=0
    for i in m.keys():
        if i in d.keys():
            c=1
            break
    if(c==1):
        return("YES")
    else:
        return("NO")
            

            

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    q = int(input().strip())

    for q_itr in range(q):
        s1 = input()

        s2 = input()

        result = twoStrings(s1, s2)

        fptr.write(result + '\n')

    fptr.close()
