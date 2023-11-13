## [Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)

``` cpp
int height(TreeNode<int>* root, int& diameter) {
    if(root == NULL) return 0;
    int lh = height(root->left, diameter);
    int rh = height(root->right, diameter);
    diameter = max(diameter, lh+rh);
    return 1+max(lh,rh);
}
int diameterOfBinaryTree(TreeNode<int> *root){
	int diameter = 0;
    int x = height(root, diameter);
    return diameter;
}
```
