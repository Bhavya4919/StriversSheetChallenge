## [Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
``` cpp
vector<int> levelOrder(TreeNode<int> * root) {
    vector<int> level;
    queue<TreeNode<int>*> q;
    q.push(root);

    while(!q.empty()) {
        int it = q.size();
        for(int i=0; i<it; i++) {
            TreeNode<int>* node = q.front();
            q.pop();
            if(node->left != NULL) q.push(node->left);
            if(node->right != NULL) q.push(node->right);
            level.push_back(node->data);
        }
    }
    return level;
}
```
