#include <bits/stdc++.h> 
/************************************************************

    Following is the Binary Tree node structure
    
    template <typename T>
    class TreeNode {
        public :
        T data;
        TreeNode<T> *left;
        TreeNode<T> *right;

        TreeNode(T data) {
            this -> data = data;
            left = NULL;
            right = NULL;
        }

        ~TreeNode() {
            if(left)
                delete left;
            if(right)
                delete right;
        }
    };

************************************************************/

class NodeValue {
public:
  int minNode, maxNode, maxSize;

  NodeValue(int min, int max, int size) {
    minNode = min;
    maxNode = max;
    maxSize = size;
  }
};

NodeValue largestBSTSolve(TreeNode<int> *root) {
  if (!root)
    return NodeValue(INT_MAX, INT_MIN, 0);

  auto left = largestBSTSolve(root->left);
  auto right = largestBSTSolve(root->right);

  if (root->data > left.maxNode and root->data < right.minNode) // is a bst
    return NodeValue(min(left.minNode, root->data),
                     max(right.maxNode, root->data),
                     1 + left.maxSize + right.maxSize);

  return NodeValue(INT_MIN, INT_MAX,
                   max(left.maxSize, right.maxSize)); // not bst
}

int largestBST(TreeNode<int> *root) {
    return largestBSTSolve(root).maxSize;
}
