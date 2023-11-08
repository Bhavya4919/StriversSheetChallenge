## [Preorder Traversal](https://leetcode.com/problems/binary-tree-preorder-traversal/)

``` cpp
void preorder(TreeNode<int>* root, vector<int>&ans){
    if(root == NULL)
    return ;
    ans.push_back(root->data);
    preorder(root->left,ans);
    preorder(root->right,ans);
}
vector<int> preOrder(TreeNode<int> * root){
    vector<int> ans;
    preorder(root,ans);
    return ans;
}

```
