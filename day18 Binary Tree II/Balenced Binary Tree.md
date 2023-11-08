## [Balenced Binary Tree](https://leetcode.com/problems/balanced-binary-tree/)

``` cpp
int heightofBT (TreeNode<int>* root) {
    if(root == NULL) return 0;
    int lh = heightofBT(root->left);
    if(lh == -1)return -1;
    int rh = heightofBT(root->right);
    if(rh == -1)return -1;
    if(abs(lh-rh)>1) return -1;
    return 1+max(lh,rh);
}
bool isBalancedBT(TreeNode<int>* root) {
    return (heightofBT(root) != -1);
}
```
