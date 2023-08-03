## [Zero Matrix](https://www.codingninjas.com/codestudio/problems/zero-matrix_1171153?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
``` cpp
#include <bits/stdc++.h> 
vector<vector<int>> zeroMatrix(vector<vector<int>> &matrix, int n, int m) {
	bool row0 = false;
	bool col0 = false;
	for(int i=0;i<m;i++)
	{
		if(matrix[0][i]==0)
		row0 = true;
	}
	for(int i=0; i<n; i++)
	{
		if(matrix[i][0] == 0)
		col0 = true;
	}
	for(int i=1;i<n;i++)
	{
		for(int j=1; j<m;j++)
		{
			if(matrix[i][j]== 0) 
			{
				matrix[0][j] = matrix[i][0] = 0;
			}
		}
	}
	for(int i=n-1; i>=1; i--)
	{
		for(int j=m-1; j>=1; j--)
		{
			if(matrix[i][0] == 0 || matrix[0][j] == 0)
			matrix[i][j] = 0;
		}
	}
	if(row0)
	{
		for(int i=0; i<m; i++)
		matrix[0][i] = 0;
	}
	if(col0)
	{
		for(int i=0;i<n; i++)
		matrix[i][0] = 0;
	}
	return matrix;
}
```
