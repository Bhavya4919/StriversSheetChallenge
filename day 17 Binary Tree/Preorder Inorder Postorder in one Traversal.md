## [Preorder Inorder Postorder in one Traversal](https://bit.ly/3rlXpTX)
``` cpp
vector<vector<int>> getTreeTraversal(TreeNode *root){
    vector<vector<int>> res;
    vector<int> pre, ino, post;
    stack < pair < TreeNode * , int >> st;
    st.push({root, 1});

    if(root == NULL) return res;
    while(!st.empty()) {
        auto it = st.top();
        st.pop();

        if(it.second == 1) {
            pre.push_back(it.first->data);
            it.second++;
            st.push(it);
            if(it.first->left != NULL)
                st.push({it.first->left, 1});
        }

        else if(it.second == 2) {
            ino.push_back(it.first->data);
            it.second++;
            st.push(it);
            if(it.first->right != NULL)
                st.push({it.first->right, 1});
        }

        else
            post.push_back(it.first->data);
    }
    res.push_back(ino);
    res.push_back(pre);
    res.push_back(post);
    return res;
}
```
