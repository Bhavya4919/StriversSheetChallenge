## [Height of the binary tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)

Level order method
``` cpp
int heightOfBinaryTree(TreeNode<int> *root)
{
	queue<TreeNode<int>*> q;
    q.push(root);
    int height = 0;
    while(!q.empty()) {
        int len = q.size();
        for (int i = 0; i < len; i++) {
          TreeNode<int> *node = q.front();
          q.pop();
          if (node->left != NULL)
            q.push(node->left);
          if (node->right != NULL)
            q.push(node->right);
        }
        height++;
    }
    return height;
}
```

Recurrsive Method
``` cpp
int heightOfBinaryTree(TreeNode<int> *root)
{
    if(root == NULL) return 0;
    int lh = heightOfBinaryTree(root->left);
    int rh = heightOfBinaryTree(root->right);
    return 1+max(lh,rh);	
}
```
