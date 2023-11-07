## [Merge All Overlapping SubIntervals](https://leetcode.com/problems/merge-intervals/)

``` cpp
vector<vector<int>> mergeOverlappingIntervals(vector<vector<int>> &arr){
	int n = arr.size();
	vector<vector<int>> res;

	for(int i=0; i<n; i++)
	{
		if(res.empty() || arr[i][0]>res.back()[1])
		res.push_back(arr[i]);

		else
		res.back()[1] = max(res.back()[1], arr[i][1]);
	}
	return res;
}
```
- TC: O(NlogN) + O(N)
- SC: O(N)
