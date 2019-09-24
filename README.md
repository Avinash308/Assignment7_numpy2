# Assignment7_numpy2
# Finding Moving average

# Problem Statement
# Write a function to find moving average in an array over a window:
# Test it over [3, 5, 7, 2, 8, 10, 11, 65, 72, 81, 99, 100, 150] and window of 3.

import numpy as np
def moving_average(a, n=3) :
    asum = np.cumsum(a, dtype=float)
    asum[n:] = asum[n:] - asum[:-n] 
    print("Adds starting 3 elemets here : ",asum[n:])
    return asum[n - 1:]/n
a=[3, 5, 7, 2, 8, 10, 11, 65, 72, 81, 99, 100, 150]
a1=np.array(a)
print(np.array(moving_average(a1,n=3)).round(1))


