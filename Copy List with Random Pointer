#include <bits/stdc++.h>

/*************************************************************

    Following is the LinkedListNode class structure

    template <typename T>   
    class LinkedListNode
    {
        public:
        T data;
        LinkedListNode<T> *next;
        LinkedListNode<T> *random;
        LinkedListNode(T data)
        {
            this->data = data;
            this->next = NULL;
        }
    };

*************************************************************/

LinkedListNode<int> *cloneRandomList(LinkedListNode<int> *head)
{
    // Write your code here.
    unordered_map<LinkedListNode<int>*, LinkedListNode<int>*> map;
    LinkedListNode<int> *temp = head;

    while(temp != NULL){
        map[temp] = new LinkedListNode<int>(temp->data);
        temp = temp->next;
    }

    temp = head;
    while(temp != NULL){
        map[temp]->next = map[temp->next];
        map[temp]->random = map[temp->random];
        temp = temp->next;
    }

    return map[head];
    

}  
