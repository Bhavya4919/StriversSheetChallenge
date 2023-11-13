## [Maximum Sum Path of a Binary Tree](https://leetcode.com/problems/binary-tree-maximum-path-sum/)

``` cpp
int findMaxPathSum(BinaryTreeNode<int> *root, int& maxi) {
    if(root == NULL) return 0;
    int leftmax = max(0, findMaxPathSum(root->left, maxi));
    int rightmax = max(0, findMaxPathSum(root->right, maxi));
    maxi = max(maxi, root->data + leftmax + rightmax);
    return root->data + max(leftmax , rightmax);
}
int maxPathSum(BinaryTreeNode<int> *root)
{
    int maxi = INT_MIN;
    findMaxPathSum(root, maxi);
    return maxi; 
}
```
