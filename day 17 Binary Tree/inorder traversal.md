## [Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/)

``` cpp
void inorder(TreeNode* root, vector<int>&ans) {
    if(root == NULL)
    return;
    inorder(root->left, ans);
    ans.push_back(root->data);
    inorder(root->right, ans);
}
vector<int> getInOrderTraversal(TreeNode *root)
{
    vector<int> res;
    inorder(root, res);
    return res;
}
```
