## [Sort 0 1 2](https://bit.ly/3tlM60B)
``` cpp
class Solution {
    public void sortColors(int[] a) 
    {
        int low = 0;
        int high = a.length-1;
        int mid = 0;
        int temp;
        while(mid<=high)
        {
            switch(a[mid])
            {
                case 0:{
                    temp = a[mid];
                    a[mid] = a[low];
                    a[low] = temp;
                    low++;
                    mid++;
                    break;
                }
                case 1:{
                    mid++;
                    break;
                }
                case 2:{
                    temp = a[high];
                    a[high] = a[mid];
                    a[mid] = temp;
                    high--;
                    break;
                }
            }
        }
    }
}
```
