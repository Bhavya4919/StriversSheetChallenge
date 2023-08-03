## [Print Pascal's Trianlge] (https://www.codingninjas.com/codestudio/problems/print-pascal-s-triangle_6917910?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
``` cpp
vector<vector<int>> pascalTriangle(int N) {
    
    vector<vector<int>> v(N);
    for(int i=0; i<N; i++)
    {
        v[i].resize(i+1);
        v[i][0] = v[i][i] = 1;
        for(int j=1; j<i; j++)
        v[i][j] = v[i-1][j] + v[i-1][j-1];
    }
    return v;
}
```
