#include <bits/stdc++.h> 
/*
    ----------------- Binary Tree node class for reference -----------------

    template <typename T>
    class BinaryTreeNode {
        public : 
            T data;
            BinaryTreeNode<T> *left;
            BinaryTreeNode<T> *right;
            BinaryTreeNode<T> *next;

            BinaryTreeNode(T data) {
                this -> data = data;
                left = NULL;
                right = NULL;
                next = NULL;
            }
    };
*/

void connectNodes(BinaryTreeNode<int> *root) {
  if (!root)
    return;

  queue<BinaryTreeNode<int> *> q;
  q.push(root);

  while (!q.empty()) {
    int n = q.size();
    while (n--) {
      auto p = q.front();
      q.pop();

      p->next = n ? q.front() : NULL;
      if (p->left)
        q.push(p->left);
      if (p->right)
        q.push(p->right);
    }
  }
}
