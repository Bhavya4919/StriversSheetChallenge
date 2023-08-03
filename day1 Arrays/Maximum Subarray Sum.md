## [Maximum Subarray Sum](https://bit.ly/3HZltTa)
``` cpp
#include <bits/stdc++.h> 
long long maxSubarraySum(int nums[], int n)
{
    long long sum = 0, max = nums[0];
    for(int i=0;i<n;i++)
    {
            sum += nums[i];
            if(sum>max) max = sum;
            if (sum<0)sum=0;
    }
    if(max<0)
    return 0;
    return max;
    
}
```
