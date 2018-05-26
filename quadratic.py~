#!/usr/bin/python
import sys
import math

#Python script that returns the roots of a quadratic equation
#of the form a*x^2 + b*x + c = 0
#Enter values for a, b, and c in the command line
#e.g. run: >python quadratic.py 1 2 -15
def main():
    try:
        a = int(sys.argv[1])
    except:
        print("error with first argument")
        sys.exit(1)
    try:
        b = int(sys.argv[2])
    except:
        print("error with second argument")
        sys.exit(1)
    try:
        c = int(sys.argv[3])
    except:
        print("error with third argument")
        sys.exit(1)
    x1, x2 = find_roots(a, b, c)
    try: 
        print ("This is x1: %f" %x1)
        print ("This is x2: %f" %x2)
    except TypeError:
        print("Type error with printing complex number")

def find_roots(a,b,c):
    mid = (b**2) - (4*a*c)    
    #Note: I couldn't figure out how to do this with try/except since
    # when I ran -2**(1.0/2) in jupyter notebook, no error appeared
    assert (mid >= 0),"Error: Roots will be imaginary"
    sqrt_mid = mid**(1.0/2)
    try:
        x1 = ((-1 * b) + sqrt_mid) / (2*a)
    except ZeroDivisionError:
        print("Error: function must be quadratic, a=0")
        sys.exit(1)
    x2 = ((-1 * b) - sqrt_mid) / (2*a)
    return x1, x2


if __name__=="__main__":
        main()


